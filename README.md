🌟 VStar Analyzer
Präzise Serien-Photometrie und Lichtkurven-Analyse leicht gemacht.
Der VStar Analyzer ist eine leistungsstarke Python-Applikation, die es Astrofotografen und Citizen Scientists ermöglicht, Helligkeitsschwankungen von veränderlichen Sternen, Exoplaneten-Transits oder Asteroiden-Okkultationen aus einer Bildserie herauszumessen.
Mit Fokus auf wissenschaftliche Standards (wie die automatische heliozentrische Zeitkorrektur HJD) und eine intuitive Benutzeroberfläche, schlägt der VStar Analyzer die Brücke zwischen einfacher Bedienung und den strengen Vorgaben astronomischer Fachgruppen (wie der BAV - Bundesdeutsche Arbeitsgemeinschaft für Veränderliche Sterne).


✨ Hauptfunktionen
🧩 Automatisches Plate Solving & Stern-Identifikation: Löst dein Referenzbild lokal per ASTAP (oder via Astrometry.net Cloud). Danach reicht ein Klick auf einen Stern, und das Programm identifiziert ihn per SIMBAD-Datenbank.
🔭 Discovery-Modus: Erkennt dank Anbindung an den VSX (Variable Star Index) automatisch alle bekannten Veränderlichen in deinem Bildfeld!
🎯 Smartes Auto-Tracking: Verfolgt deinen Ziel- und Vergleichsstern über Hunderte von FITS-Bildern hinweg – auch bei leichtem Teleskop-Drift. Mit dem Review-Modus kannst du Tracking-Fehler manuell korrigieren.
📈 Echtzeit-Lichtkurve & Statistik: Berechnet "on the fly" die instrumentelle Magnitude (
Δ
Δ
 mag), Amplitude, Maxima/Minima und bestimmt per Lomb-Scargle-Periodogramm die dominante Periode der Helligkeitsschwankung.
🕒 Wissenschaftliche Zeitkorrektur: Rechnet JD-Zeitstempel aus den FITS-Headern automatisch in HJD (Heliozentrisches Julianisches Datum) um (Lichtlaufzeitkorrektur).
💾 Profi-Exporte (CSV & BAV): Speichert Messreihen als .csv oder exportiert sie strikt formatiert für die BAV (Format C). Zusätzlich können druckfertige Lichtkurvenblätter (.png) inkl. aller Metadaten generiert werden.
📥 Installation & Download
Für Anwender (Fertige App)
Die einfachste Methode:
Navigiere rechts zu den [Releases].
Lade dir die neueste VStarAnalyzer_vX.X.zip herunter.
Entpacke die Datei an einen beliebigen Ort.
Starte die VStarAnalyzer.exe.
Für Entwickler (Python Quellcode)
Wenn du den Quellcode lesen, anpassen oder ausführen möchtest:
Klone das Repository:
code
Bash
git clone https://github.com/SteffSarek/VStar.git
Installiere die Abhängigkeiten (ein Virtual Environment wird empfohlen):
code
Bash
pip install customtkinter pillow numpy matplotlib opencv-python astropy astroquery photutils
Starte das Programm:
code
Bash
python main.py
⚙️ Vorbereitungen & Tipps für die Photometrie
ASTAP installieren: Für ein zügiges Plate Solving wird dringend die lokale Installation von ASTAP inkl. einer Sternendatenbank (z. B. H18) empfohlen. Den Pfad zur astap.exe kannst du in den Einstellungen des Programms hinterlegen.
Daten-Qualität: Füttere das Programm am besten mit kalibrierten FITS-Bildern (Darks, Flats), um den Hintergrundrauschen-Einfluss (SNR) zu minimieren.
Tracking & Radien: Die Größen für Apertur und Annulus (Hintergrund-Ring) lassen sich in den Einstellungen an dein Kamera-Setup (Pixelscale) anpassen.
📝 Lizenz & Credits
Dieses Projekt steht unter der GNU General Public License v3.0.
Entwickelt von Stefan Raphael (2025-2026).
Astrometrie, Photometrie und Datenbank-Abfragen werden bereitgestellt durch die großartigen Open-Source Projekte Astropy, Astroquery und Photutils.