# Storyboard: Einführung in pyMeSys

**Zielgruppe:** Anwender / Maschinenbauer im Labor
**Tonalität:** Erklärend, beruhigend, vorteilsorientiert (Nutzen vor Technik)

---

## Slide 1: Titel
**Titel:** pyMeSys – Die Zukunft unserer Messtechnik
**Untertitel:** Flexibel. Robust. Datengetrieben.
**Bild:** Screenshot der GUI oder WKK Logo
**Speaker Notes:** 
Willkommen. Heute geht es nicht um Code, sondern um unser Werkzeug für die tägliche Arbeit im Labor: pyMeSys. Was es ist, warum wir es haben und wie es uns das Leben leichter macht.

---

## Slide 2: Was ist das ganze? (Der Überblick)
**Inhalt:**
*   **Historie:** 
    *   Früher: NiMeSys, BeMeSys, diverse LabVIEW-VIs.
    *   Problem: Wildwuchs, schwer wartbar, Datenchaos.
*   **Heute: pyMeSys**
    *   Eine einheitliche Software für (fast) alle Prüfstände.
    *   Verbindet die Welten: Beckhoff Hardware (Steuerung) + Python (Daten & UI).
**Kernaussage:** pyMeSys ist das "Betriebssystem" für unsere Versuche.

---

## Slide 3: Wofür brauchen wir das? (Der Nutzen)
**Inhalt:**
*   **1. Einheitlichkeit:** Egal ob Zeitstandversuch oder Ermüdungstest – die Oberfläche und Bedienung bleiben vertraut.
*   **2. Datenqualität:** Automatische Speicherung in TDMS. Wichtig: Metadaten sind direkt dabei (Material, Prüfer, Parameter). Das ist die Basis für unsere KI-Auswertungen.
*   **3. Unabhängigkeit:** Wir sind nicht mehr an teure LabVIEW-Lizenzen oder starre Programme gebunden.
**Kernaussage:** Weniger Zeit mit "Software-Kampf" verbringen, mehr Zeit für echte Versuche.

---

## Slide 4: "Warum so kompliziert?" (Die Config-Frage)
**Frage:** "Früher habe ich eine .exe geklickt und es lief. Jetzt muss ich Configs laden?"
**Antwort:** 
*   Die "Komplexität" ist eigentlich **Superkraft**.
*   Früher war die Software fest verdrahtet mit der Maschine. Wollte man einen neuen Sensor, musste man programmieren.
*   **Heute:** Die Software ist ein leeres Blatt. Die **Konfiguration (YAML)** sagt ihr, was sie ist.
*   **Vorteil:** Wir können einen Prüfstand morgens für Zugversuche und nachmittags für Bauteiltests nutzen, nur durch Laden einer anderen Datei.
**Analogie:** Ein Smartphone ist "komplizierter" als ein altes Festnetztelefon, aber es kann Taschenrechner, Kamera und Telefon sein – je nachdem welche "App" (Config) wir starten.

---

## Slide 5: Was ist das für ein System? (Architektur Light)
**Visuell:** Schaubild
[Python GUI (Das Gehirn)] <---> [Beckhoff SPS (Die Muskeln)] <---> [Prüfstand (Die Realität)]

**Erklärung:**
*   **Der Muskel (Beckhoff):** Läuft in Echtzeit. Garantiert Sicherheit. Schaltet ab, wenn etwas schief geht. Robust und industriell.
*   **Das Gehirn (pyMeSys/Python):** Zeigt die Kurven, speichert die riesigen Datenmengen, lässt sich schön bedienen.
*   Die Trennung sorgt dafür, dass die Anlage sicher ist, auch wenn der PC mal hängen sollte (was wir nicht hoffen!).

---

## Slide 6: Wie sieht das für den Anwender aus?
**Inhalt:**
*   Starten -> Config wählen -> Messen.
*   Live-Grafiken ohne Ruckeln.
*   Einbindung neuer Technik (z.B. Thermokameras) ist nahtlos integriert.
*   Kein manuelles Exportieren von CSV-Dateien mehr nötig – alles liegt sauber auf dem Server.

---

## Slide 7: Zusammenfassung & Fragen
**Takeaway:**
*   pyMeSys macht unsere Versuche vergleichbar und zukunftssicher.
*   Die "Hürde" der Konfiguration gibt uns die Freiheit, schnell auf neue Anforderungen zu reagieren.
**Call to Action:** Probiert es aus, gebt Feedback. Das System lebt von euren Anforderungen.

**Offene Runde:** Eure Fragen?
