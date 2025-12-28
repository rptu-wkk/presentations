

# Git, GitLab, GitHub & DataHub

**Wie wir unsere Daten und Software verwalten – einfach erklärt.**

---

### Was ist Git? (Der Motor)

- **Definition:** Ein System zur Versionsverwaltung von Dateien.
- **Das Problem bisher:** `Datensatz_final_v2_echt_jetzt_fertig.txt`
- **Die Git-Lösung:**
    - Speichert jede Änderung ("Savepoint").
    - Man kann in der Zeit zurückreisen.
    - Mehrere Leute arbeiten gleichzeitig an einer Datei, ohne sich zu überschreiben.
- **Für uns:** Wie ein lückenloses Logbuch oder eine Zeichnungsverwaltung im CAD.
    

> _Sprechernotiz: "Stellt euch Git vor wie eine Zeitmaschine für unsere Arbeit. Statt Dateien ständig unter neuem Namen zu speichern, merkt sich Git jede Änderung. Wir sehen wer, wann, was geändert hat und können jeden Fehler rückgängig machen."_

---

### Git vs. GitLab vs. GitHub (Die Werkstatt vs. Der Showroom)

- **Git:** Das Werkzeug auf deinem Laptop (Lokal).
- **GitLab & GitHub:** Die Online-Plattformen, wo der Code liegt (Server).
- **Der Unterschied:**
    - **GitLab:** Unsere **private Werkstatt**. Sicher, intern, volle Kontrolle.        
    - **GitHub:** Der **öffentliche Marktplatz**. Weltweiter Standard, riesige Community.      

> _Sprechernotiz: "Git ist der Hammer in meiner Hand. GitLab und GitHub sind die Häuser, die wir damit bauen. GitLab ist unser abgesperrtes Firmengelände. GitHub ist die öffentliche Messehalle, wo wir unsere besten Stücke präsentieren."_

---

### Unser interner Standard: GitLab

- **Einsatzgebiet:** Internes Projektmanagement & Datenspeicher.
- **Nutzung 1: "Lab Repositories"**
    - Speicherung von **Anlagen-Konfigurationen**.    
    - Jede Anlage hat ihr eigenes "Repository" (Ablageort).    
    - Änderungen an der Maschineneinstellung sind nachvollziehbar.    

> _Sprechernotiz: "Wir nutzen GitLab als unser internes Archiv. Wenn wir eine Anlagenkonfiguration ändern, landet das hier. So wissen wir immer, wie die Maschine vor drei Wochen eingestellt war."_


---

### Unser Ziel: Ab nach GitHub!

- **Status Quo:** Python-Code zur Datenanalyse liegt versteckt auf GitLab.
    
- **Das Problem:** Niemand draußen sieht unsere Arbeit; keine "Strahlkraft".
    
- **Der Plan:** Umzug des Python-Codes auf **GitHub**.
    
- **Die Vorteile:**
    
    - Sichtbarkeit in der Industrie (GitHub ist Standard).
        
    - Community-Effekt: Andere können Verbesserungen vorschlagen.
        
    - Wir zeigen Kompetenz nach außen.
        

> _Sprechernotiz: "Wir haben super Analyse-Tools in Python geschrieben. Aber die verstauben auf unserem internen Server. Wir wollen die auf GitHub veröffentlichen. Das ist quasi das 'Facebook für Entwickler'. Damit zeigen wir Flagge und erhöhen unsere technische Reichweite massiv."_

---

### Spezialfall: Der DataHub

- **Was ist das?** Unsere zentrale Sammelstelle für Messdaten.
    
- **Technische Basis:** Basiert "unter der Haube" auf **GitLab**.
    
- **Funktion:**
    
    - Archivierung von Rohdaten aus dem Labor.
        
    - Sichert die Original-Messwerte unveränderbar.
        
    - Verbindet die Messung mit der Version der Auswertung.
        

> _Sprechernotiz: "Der DataHub ist unser Tresor für Messergebnisse. Technisch läuft das über GitLab, aber für uns ist es einfach der Ort, wo die Rohdaten sicher liegen und nicht mehr verloren gehen."_