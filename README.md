# Système d'Alerte Edge et Actionnement Industriel Automatisé

Prototype embarqué de sécurité industrielle et d'arrêt d'urgence basé sur microcontrôleur Arduino Uno. Le système assure la surveillance continue de la température ambiante et applique une logique stricte de coupure d'actionneur avec verrouillage matériel de sécurité (Safety Latch).

---

## ⚙️ Caractéristiques Techniques
- **Plateforme matérielle** : Arduino Uno (ATmega328P).
- **Capteur d'acquisition** : DHT22 (température et humidité numérique haute précision).
- **Actionnement de sécurité** : Module Relais électromécanique commandant la charge/moteur.
- **Signalisation & Alarmes** : 
  - Alerte sonore via Buzzer piézoélectrique.
  - Alerte visuelle via LED rouge dédiée.
- **Interface opérateur** : Bouton-poussoir de réarmement manuel (Reset) avec résistance de rappel interne (Pull-up).

---

## 🔒 Logique de Sécurité Industrielle
1. **Surveillance continue** : Mesure cyclique des grandeurs physiques.
2. **Déclenchement d'urgence ($T \ge 50^\circ\text{C}$)** :
   - Désactivation immédiate du relais pour couper l'alimentation de l'actionneur.
   - Activation simultanée de la LED d'alarme et de l'avertisseur sonore.
3. **Verrouillage de sécurité (Safety Latch)** :
   - Même si la température redescend en dessous de $50^\circ\text{C}$, le système refuse le redémarrage automatique pour éviter les redémarrages intempestifs.
4. **Réarmement manuel obligatoire** :
   - L'opérateur doit intervenir physiquement en appuyant sur le bouton de réarmement une fois le défaut thermique éliminé.

---

## 🔗 Simulation Interactive en Direct (Wokwi)
Testez le comportement du banc et déclenchez l'alerte thermique directement en ligne :  
👉 **[Lancer la simulation interactive sur Wokwi](https://wokwi.com/projects/480035997133632513)**

---

## 👨‍💻 Auteur
**Ahmed El Ayachi**  
*Ingénieur en Informatique Industrielle et Systèmes Embarqués*
