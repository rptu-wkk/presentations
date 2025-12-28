## 📄 Folie 1: Titel und Agenda

# 🚀 Technologiewechsel in der Messtechnik
### Der Umstieg: National Instruments (NI) zu Beckhoff

* **Überblick:** Warum dieser Hardware-Wechsel?
* **Fokus 1:** Einsatzgebiet & Robustheit
* **Fokus 2:** Flexibilität & Kosten
* **Fokus 3:** Software-Strategie
* **Fazit:** Der Sweet Spot für NI und Beckhoff

---

## 🗺️ Folie 2: Einsatzgebiet und Kernkompetenzen

### 1. Einsatzgebiet: Labor vs. Industrie

| Merkmal | National Instruments (NI) | Beckhoff |
| :--- | :--- | :--- |
| **Typische Umgebung** | **"Sauberes" Labor** | **"Raue/Dreckige" Industrieumgebung** |
| **Primäre Rate** | High-Speed-Erfassung | Prozess-Erfassung |
| **Max. Rate** | Bis zu **1 MS/s** | Bis max. **10 kS/s** |
| **Ergebnis** | NI ist für unsere meisten Prozesse **überdimensioniert**. | Beckhoff ist optimal für die **Prozess-Welt** konzipiert. |

---

## 💪 Folie 3: Warum Beckhoff in der Industrie robuster ist

### 2. Robustheit und Störfestigkeit

Beckhoff ist technisch besser für industrielle Umgebungen gerüstet: 

* **Dezentraler Aufbau:**
    * **Modulare, dezentrale** Klemmen-Architektur.
    * Führt zu **kürzeren Kabellängen** vom Sensor zur Klemme.
    * **Vorteil:** Reduziert die Anfälligkeit für Rauschen und EMV-Störungen deutlich.
* **Analoge Eingänge:**
    * Analoge Eingänge besitzen einen **niedrigeren Innenwiderstand**.
    * **Vorteil:** Bessere Stabilität und Unempfindlichkeit gegenüber Umgebungseinflüssen.

---

## 💰 Folie 4: Flexibilität und Kosten

### 3. Skalierbarkeit und Wirtschaftlichkeit

| Kriterium | National Instruments (NI) | Beckhoff |
| :--- | :--- | :--- |
| **Flexibilität** | Eher **vorher projektiert und starr** in der Konfiguration. | **Flexibel durch modularen Aufbau.** |
| **Erweiterung** | Weniger dynamisch erweiterbar. | Über **EtherCAT** jederzeit einfach und modular erweiterbar. |
| **Kosten** | Tendenziell **überteuert**. | **Wirtschaftlicher** in der Anschaffung. |

---

## 🐍 Folie 5: Der Wegfall des NI-Vorteils

### 4. Software-Strategie und LabVIEW-Bindung

Der entscheidende strategische Wechsel:

* **Alte Situation (NI):**
    * NI-Hardware war **optimal an LabVIEW** angebunden.
    * Dies war der größte Vorteil.
* **Neue Situation:**
    * Durch den strategischen Umstieg auf **Python** als primäre Steuerungssoftware ist dieser Vorteil **komplett weggefallen**.
    * Die Bindung an ein teures, proprietäres System ist nicht mehr erforderlich.

---

## 🧩 Folie 6: Software-Integration und Steuerung

### 5. Steuerungsschicht und Flexibilität

| Merkmal | National Instruments (NI) | Beckhoff |
| :--- | :--- | :--- |
| **Software-Layer** | Proprietärer **DAQmx-Layer** notwendig. | Muss in **TwinCAT/XAE** (oder eigener Python-Anbindung) "nachgebaut" werden. |
| **Funktionalität** | Messung und Steuerung getrennt. | Höhere Flexibilität. **Regler und Steuerungslogik** können direkt im **XAE-Umfeld** integriert werden. |
| **Zusatznutzen** | - | **Made in Germany** – Stärkung regionaler Partner und guter Support ("Support your local dealer"). |

---

## 📈 Folie 7: Fazit – Wann NI noch Sinn macht

### Zusammenfassung und Ausblick

**Der Umstieg auf Beckhoff ist die strategisch und wirtschaftlich sinnvollste Lösung für unsere Standard-Prozessmesstechnik.**

**Ausnahmen – Wann NI weiterhin sinnvoll ist:**

* **Extrem hohe Abtastraten:** Bei Anforderungen **über 10 kS/s** (bis 1 MS/s).
* **Spezialanwendungen:** Zum Beispiel die **Ultraschall-Analyse** (typische Abtastrate von $\approx 20\,\text{kHz}$).

> **Fokus:** Beckhoff für die **robuste, flexible, kosteneffiziente Prozess- und Steuerungstechnik**.