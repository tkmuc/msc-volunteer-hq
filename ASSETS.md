# Bildassets und Quellen

## Porträts

Quelle ist ausschließlich die vom Nutzer bereitgestellte Datei `Helles UX-Review-Board_ Ansprechpartner-4.png` (1448 × 1086 px). Die SVG-Bildfenster in `portrait()` zeigen die vorhandenen fotografischen Bildbereiche; die Gesichter wurden nicht neu gezeichnet oder neu generiert.

- Anna: x 556, y 444, Breite 124, Höhe 178.
- Max: x 540, y 694, Breite 86, Höhe 78.
- Julia: x 541, y 784, Breite 85, Höhe 78.

Lokales Original: `assets/people-reference.png`. Verlustfreie WebP-Fassung für die App: `assets/people-reference.webp`.

## Frauenkirche

[Historischer Aufriss der Frauenkirche, Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Frauenkirche_M%C3%BCnchen_Aufrisse_vor_1900.jpg). Urheber unbekannt, vor 1900; auf der Dateiseite als gemeinfrei ausgewiesen. Upload und Helligkeitsangleichung: Ulamm. Die App zeigt die westliche Frontansicht mit zwei Türmen; die Papierfläche wird nur in der Darstellung durch Graustufen, Kontrast und Blendmodus zurückgenommen.

Datei: `assets/frauenkirche-historical.jpg`.

## Hotelrecherche und Grenzen

- [Offizielle Konferenzbroschüre Bayerischer Hof, 2025](https://www.bayerischerhof.de/media/Hotel_Bayerischer_Hof/Downloads/Veranstaltungen/HBH_Konferenzbroschuere_DE_2025.pdf): gedruckte Grundrisse des Festsaal-Ensembles und Innenraumansichten.
- [Offizieller Orientierungsplan zur Umbauphase, 2025](https://www.bayerischerhof.de/media/Hotel_Bayerischer_Hof/Eine_Welt_fuer_sich/Aktuelles/HBH_Orientierungsplan_Umbau2025__V2.pdf): Eingangsfoyer und Anordnung im Erdgeschoss. Temporäre Zutrittsmarkierungen werden nicht als heutige Situation übernommen.
- [falk’s Bar, offizielle Hotelbeschreibung](https://www.bayerischerhof.de/de/tagen-feiern/raeumlichkeiten/festsaal-ensemble/falks-bar.html).
- [MSC-Website als zusätzliche Gestaltungsreferenz](https://securityconference.org/).

Die öffentliche Raumfolge ist die Grundlage der 3D-Interpretation. Möbel, Detailgeometrie und vereinfachtes Foyer sind gestalterische Interpretation. Es wurden keine internen MSC-Pläne verwendet. Volunteer Desk, Sekretariat, Personalzuordnung, Besetzungszeiten sowie alle D-Raumkennungen sind fiktiv. Die zwei Obergeschosse und Venue B sind vollständig frei gestaltete Demonstrationsmodelle.

## Generierte Assets

Erstellt mit dem eingebauten Bildgenerierungswerkzeug. PNG-Originale bleiben erhalten; die App lädt komprimierte WebP-Fassungen mit Transparenz. Es wurden keine CLI- oder externen KI-APIs eingebaut.

### Erdgeschoss Bayerischer Hof

App-Datei: `assets/venue-hof-ground.webp`, Original: `assets/venue-hof-ground.png`.

Finaler Prompt:

> Use case: sketch-to-render. Image 1 is the edit target: the official hotel brochure page with ground-floor plan at the TOP and mezzanine plan at the BOTTOM. Transform ONLY THE TOP GROUND-FLOOR PLAN into a single beautiful architectural 3D cutaway model for a mobile venue explorer. Image 2 is a supporting official orientation plan: use it ONLY to understand the main entrance and lobby in front of the room ensemble. Image 3 contains supporting interior photos, use those ONLY for refined warm stone, ivory stucco, galleries and brass/wood material cues. Preserve the actual plan topology, do not invent an unrelated hotel. Precise layout left to right: very large ballroom (Festsaal) on the LEFT, with a stage and twin curved staircases at its left end, then Cocktail Lounge immediately to its right, then a large open Atrium in the center-right, and a narrow Fireplace Lounge/Kamin Lounge at the far RIGHT. Falk's Bar is a separate long rectangular room DIRECTLY BEHIND the Atrium toward the BACK of the model, as in the plan; give it ornate mirrored ivory walls, subtle lilac-blue bar lighting, a bar counter and a few stools. In FRONT of the whole ensemble show a simplified continuous entrance/lobby/foyer strip, with the main entrance near the front-LEFT below the ballroom, stairs and a small concierge/reception-style counter as schematic architectural furniture. The lobby should connect visually to the Atrium. Keep all main rooms clearly distinguishable, physically connected by visible openings; genuine thick walls, volumetric columns, doors, furniture, realistic soft shadows. Model must be seen from elevated front three-quarter perspective while maintaining ballroom visibly LEFT and bar at BACK-RIGHT. Show ONE floor only, as a premium miniature architectural model, low cutaway front walls and taller rear walls. Ivory and warm stone materials, subtle muted navy furniture, light oak, realistic ambient occlusion, delicate dimensional details. No people, no text, no numbers, no labels, no logos, no pins, no arrows, no PDF page, no UI, no dimensions. Landscape composition with the entire building footprint fully visible and generous transparent margins. Honest simplified visualization, not a claim of exact measured construction.

Die drei Eingabebilder waren lokal gerenderte Seiten der oben verlinkten Hotel-PDFs; sie werden nicht als Fotos oder Pläne in der App weiterveröffentlicht.

### Freie Etagenmodelle

App-Dateien: `assets/venue-hof.webp` und `assets/venue-b.webp`; entsprechende PNG-Originale liegen daneben.

Gemeinsamer Prompt, jeweils gefolgt vom untenstehenden Zusatz:

> Use case: stylized-concept. Asset type: production 3D illustration sprite sheet for a mobile venue explorer. Portrait canvas with exactly THREE fully isolated isometric dollhouse floor plates in equal horizontal thirds, all same elevated three-quarter perspective. Each floor is FULLY CONTAINED within its own third with clear transparent separation. Every plate fills about 92 percent of canvas width, same scale. Exquisite realistic miniature architectural rendering: thick white cutaway walls, visible doors and corridors, glass partitions, pale blue-gray floors, light oak, navy seating, indoor plants, real depth and fine soft ambient-occlusion shadows. No flat vector art. No people, text, letters, numbers, labels, icons, markers, frame, arrows or UI. Transparent background outside the three physical floor models.

Hotel-Demo-Zusatz:

> Subject: an imaginary Munich conference hotel, not an actual plan of a real hotel. Consistent rectangular footprint. TOP THIRD: second floor volunteer lounge, sofa groups, coffee bar, round tables, plants, quiet area. MIDDLE THIRD: first floor, team briefing room with meeting tables, team-coordination office, central stairwell and corridor. BOTTOM THIRD: ground floor with a beautiful hotel lobby, curved volunteer reception desk, small secretariat office beside the entrance, doors, stairs and a waiting area. Exact presentation: one independent, beautifully detailed model per third of the canvas, no connections between plates.

Venue-B-Zusatz:

> Subject: a fictional modern conference annex with an L-shaped footprint, distinct from a rectangular hotel. TOP THIRD: second floor, coffee kitchen, welcoming sofas and a quiet room. MIDDLE THIRD: first floor, check-in/meeting room and a material storage room with shelves, boxes and tables. BOTTOM THIRD: ground floor reception with support desk, administrative office/secretariat, glass entrance and stairwell. Architectural materials are carefully rendered, not flat. One isolated floor model in each third of the portrait canvas.

Die erzeugten Modelle bleiben als vollständige Ansichten erhalten. Sie werden nicht an den gedachten Drittelgrenzen abgeschnitten.

### Elefant

App-Datei: `assets/elephant-engraving.webp`, Original: `assets/elephant-engraving.png`. Referenz war der Feedback-Screenshot des Nutzers.

Finaler Prompt:

> Use case: background-extraction. Image 1 is the edit target: a mobile feedback UX reference. Extract and carefully reconstruct ONLY the fine, realistic engraved elephant head visible faintly at the upper right of the phone screen. Deliver a standalone centered head-and-trunk illustration: broad ears, detailed wrinkled skin, realistic eyes, subtle tusks and long trunk, thin slate blue-gray engraving/pencil lines for an elegant background watermark. Reconstruct parts covered by interface text. Remove ALL text, phone frame, buttons, navigation, callouts, annotations, numbers and other objects. Preserve the sophisticated realistic engraved style of the reference. No cartoon, simple icon or geometric outline. Full normal line opacity, because the application will adjust opacity. Transparent background with generous clear margins.
