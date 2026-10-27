# MSC Volunteer HQ · Konzeptdemo

Eine eigenständige, vertikal aufgebaute Webapp für die Volunteer Experience. Alle Inhalte, Personen, Zeitangaben und Pläne sind fiktive Beispiele. Die App ist keine offizielle MSC-Anwendung.

## Starten

`index.html` direkt im Browser öffnen. Den Ordner `assets` daneben belassen. Es gibt keinen Build-Schritt, keine externen Schriften oder erforderlichen Netzwerkanfragen.

## Gestaltung nach den Referenzen

Die App bleibt auch auf großen Bildschirmen eine zentrierte, höchstens 480 px breite Spalte. Auf Smartphones nutzt sie die verfügbare Breite. Die Bottom-Navigation bleibt am unteren Bildschirmrand erreichbar. Die Ansichten folgen den sechs Referenzen: Briefing mit Einsatzkarte, Venue Explorer mit Etagen und Ortsdetails, Ansprechpartner mit Porträtillustrationen, FAQ mit Themenfiltern, Reisekosten in vier Schritten und Feedback mit drei Beitragsarten.

Die Porträts sind unveränderte Bildausschnitte aus den bereitgestellten Screenshots, verlustfrei als WebP gespeichert. Die Frauenkirche stammt aus einem historischen Architekturaufmaß. Elefant und räumliche Gebäudedarstellungen sind hochwertige generierte Bildassets. Die App enthält keine Präsentationsränder oder künstliche Telefon-Statusleiste.

Das Erdgeschoss des Bayerischen Hofs orientiert sich an der öffentlichen Konferenzbroschüre und einem Hotel-Orientierungsplan von 2025: Festsaal links, Cocktail Lounge, Atrium vor falk’s Bar und Kamin Lounge. Die neue 3D-Skizze ist eine vereinfachte Interpretation, keine maßstäbliche Rekonstruktion und kein aktueller Zugangsplan. Die Obergeschosse und Venue B bleiben frei gestaltete Demoetagen.

Ortskarten enthalten eine Bereichs- oder Raumkennung, eine grobe Lagebeschreibung, konkrete Zuständigkeiten und einen Kontakt. Kennungen mit `D-` sind erfundene Demo-Raumkennungen und keine echten Hotelnummern. Öffentlich dokumentierte Hotelräume sind als Orientierungspunkte ausgewiesen. Quellen und Entstehung der Assets stehen in `ASSETS.md` und unter „Karte → Planquellen und Demo-Hinweise“.

## Teilen / GitHub Pages

Die private Sites-Vorschau ist unter [MSC Volunteer HQ](https://msc-volunteer-hq-concept.fnac.chatgpt.site) veröffentlicht. Sie ist auf das Eigentümerkonto beschränkt und verlangt eine ChatGPT-Anmeldung. Eine öffentliche Freigabe wurde nicht gesetzt.

Für GitHub Pages `index.html`, `.nojekyll` und den Ordner `assets` in ein Repository auf `main` übernehmen. Danach **Settings → Pages → Deploy from a branch → main / root** wählen. Die App verwendet relative Hash-Navigation und benötigt keine Server-Routen. Eine getrennte Sites-Bereitstellung wird unter `sites/msc-volunteer-hq` verwaltet; die Root-Dateien bleiben die editierbare lokale App.

## Demo-Grenzen

Änderungen bleiben im localStorage des jeweiligen Browsers. Es gibt keine Benutzerverwaltung, Geolocation, Wegeführung, Nachrichtenversand, Upload, OCR/KI, Bankdaten oder Synchronisation zwischen Personen. Admin- und Teamwechsel sind Präsentationsfunktionen.

Belegdateien (JPG, PNG, WebP oder PDF bis 8 MB) werden lokal einer Kostenposition zugeordnet. Nur Dateiname, Typ und Größe bleiben gespeichert. Eine Bildvorschau ist im laufenden Browser verfügbar; nach einem Reload muss die Datei für die Vorschau erneut gewählt werden. Die vorausgefüllte Hinfahrt besitzt einen fiktiven Beispielbeleg.

Der Schlüssel `msc-volunteer-hq-demo-v2` speichert den Zustand. Vorhandene Daten der ersten Version werden beim ersten Start übernommen. Unter „Mehr“ lassen sich die Beispieldaten zurücksetzen.

## Wichtige Stellen

- Designvariablen: `:root` am Anfang von `index.html`
- Beispieldaten: `initial()`, `buildings`, `contacts`, `faqs`
- Seiten: `home`, `venue`, `contactsPage`, `faqPage`, `expenses`, `feedback`, `more`, `admin`
- Maximale Appbreite: `--app-width` in `:root`

Die Navigation nutzt Hashes, sodass Browser-Zurück und Aktualisieren funktionieren.

## Prüfung

`node tests/verify.mjs` prüft ohne zusätzliche Pakete die Seitendarstellung und wichtige Zustandsübergänge: Verknüpfungen, Gebäude-/Etagenwechsel, Suchergebnisse, Briefing-Zielgruppen, Kostenrechnung, Datei- und Formularvalidierung, lokales Speichern und Reset. Das ist eine Prüfung der Logik und erzeugten HTML-Struktur, keine visuelle Browserprüfung.

25 Funktions- und Strukturprüfungen bestehen. Die neuen Bildassets wurden visuell einzeln geprüft; ihre Referenzen und die Rauminformationen sind geprüft. Die private Bereitstellung wurde vom Hostingdienst als erfolgreich bestätigt.

Der integrierte Browser blockiert lokale Dateien und den lokalen Previewserver. Die veröffentlichte private Vorschau ist erreichbar, verlangt aber eine persönliche ChatGPT-Anmeldung. Deshalb ist die visuelle Prüfung der vollständigen App bei 320/390 px und auf Desktop noch offen. Anmeldedialoge werden nicht automatisiert. Nach der Anmeldung kann die Prüfung in derselben Vorschau fortgesetzt werden. Flexible Schaltflächen, umbrechende Texte und die auf 480 px begrenzte Navigation sind im CSS festgelegt.
