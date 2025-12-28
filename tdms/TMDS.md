---
theme: white
---

### Warum TDMS-Files für die Datenspeicherung?


---
### Wie haben wir es früher gemacht? (ASCII)

ASCII Files ohne besondere Endung - meistens .dat oder .dtv

#### ✅ Vorteile

- Einfach zu öffnen (z.B. mit Excel, Notepad)
- Universell verständlich - Menschenlesbar

---
### Wie haben wir es früher gemacht? (ASCII)
#### ❌ Nachteile

- **Performance:**
	- Text-Parsing (z.B. von „3.14159“) ist langsam.  
	- Binärzahlen sind CPU-freundlicher.
- **Dateigröße:**  
	- `-1.23456E-07` braucht 12 Bytes, ein binärer `float` nur 4.
	- Ca. um Faktor 3 größer bei schlechterer Auflösung
- **Fehlende Metadaten:**  
	- Einheiten, Abtastrate, Sensor-ID etc. sind meist in separaten Dateien oder Dateinamen „versteckt“ (z.B. `Test_A_Sensor_3_Kanal_X_50kHz.csv`).  
	- Daten sind **nicht selbstbeschreibend**.
---
### 💩 WORST CASE Szenario
Da in LabVIEW die Programmierung von ASCII Header aufwendig ist:

Eine Datei ganz OHNE Spaltenbeschriftungen - zwar existieren noch Header als xls Files - aber sind das wirklich die richtigen???

Data Lost

Danke 2010er Lars!

---

![[screenshot-shityfile.png]]

---

## 🚀 Wie kamen wir zu TDMS?
Bei den VHCF-Anlagen benutzen wir von Anfang an TDMS Files - um die großen Datenmengen bewältigen zu können.

Da wir dort gute Erfahrungen gemacht haben und LabVIEW das TDMS-Format mitlieferte wurde das (ca. 2015) zum Quasi-Standard

---
## 🧩 Was ist TDMS?

TDMS (Technical Data Management Streaming) ist ein von National Instruments entwickeltes Binärformat, das speziell für Messdaten optimiert ist.

- **Hierarchische Struktur:**
    
    - **Root (Datei):** Enthält globale Informationen (z.B. Prüflings-ID, Datum, Autor).
    - **Groups (Gruppen):** Bündeln logisch zusammengehörige Kanäle (z.B. "Motor 1", "Umweltdaten").
    - **Channels (Kanäle):** Die eigentlichen Rohdaten-Arrays (z.B. "Temperatur", "Drehzahl", "Spannung").



---

### ✌️ Vorteile von TDMS

- **Integrierte Metadaten (Properties)**
    - JEDE Ebene (Root, Group, Channel) kann beliebig viele Metadaten (Attribute/Eigenschaften) speichern.
    - Beispiel: Ein Kanal "Temperatur" speichert seine Einheit ("°C") und Skalierungsfaktoren direkt bei sich.
- **Streaming-Optimierung**
    - Das Format ist dafür ausgelegt, Daten "live" während der Messung schnell anzuhängen (hoher Datendurchsatz).
- **Performance & Effizienz**
    - Als Binärformat extrem schnell zu lesen und zu schreiben.
    - Deutlich geringerer Speicherbedarf als ASCII.


---
### 😱 Risiko: Ein proprietäres Format?

- **Proprietäres Format von NI.**
- **Vendor-Lock-in-Risiko:**  
    → Ursprünglich stark an NI-Software (LabVIEW, DIAdem) gebunden.  
    → Was, wenn man die Software wechselt oder Daten extern analysieren will?

---
### 😎 Lösung zur manuellen Weiterverarbeitung

- TDMS File können über ein Add-In von NI in Excel importiert werden.
- OriginLab unterstützt das imporieren der Files von "Haus aus"

---
### 🤓 Python Lösung 

Das "proprietäre" Risiko ist heute weitgehend gemindert.
- **NI hat das Format dokumentiert:** Die Spezifikation ist öffentlich zugänglich.
- **Open-Source-Bibliotheken (Die Lösung!)**
    - **Python:** `nptdms` ist eine exzellente, stabile Bibliothek zum Lesen und Schreiben von TDMS-Dateien.
- **Fazit:** Daten sind nicht mehr "gefangen". Eine Analyse in Python oder MATLAB ist problemlos möglich.


---

### Hands on 
Files öffnenen in Excel und Origin