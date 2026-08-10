# Pflegelog – Ausflugsfinder Todtmoos

Nachvollziehbare Pflegehistorie der Seite. **Jeder Monats-Pflegelauf** (nach der
Pflege-Checkliste in der [README](README.md#pflege-checkliste-monatlich-ca-3060-minuten))
bekommt hier einen Eintrag: Datum, Katalogversion, `check-links`-Ergebnis und die
abgearbeiteten Reviews bzw. Befunde. Katalog-Erweiterungen sind unten als Wachstums-
Zeitleiste festgehalten.

> Hinweis zur Datierung: In der Aufbauphase trug die `catalog_version` das Label
> `2026-07-27.x`, obwohl die tatsächlichen Arbeitstage der 8./9. August 2026 waren.
> Am 2026-08-09 wurde die Datierung angeglichen (siehe Pflegelauf unten): Version
> `2026-08-09.2`, alle betroffenen `source_checked_on` auf das reale Datum, alle
> `next_review_on` intervallerhaltend nachgezogen. Künftige Läufe versionieren
> direkt mit dem realen Datum.

---

## Pflegeläufe (neueste zuerst)

### 2026-08-10 · Preisrunde über die 21 unbelegten Ziele · Katalog `2026-08-10.1`
Ziel des Laufs: für jedes Ziel mit `cost_status: unknown` eine offizielle Preisseite
finden. Ergebnis: **8 von 21 belegt, 13 bleiben bewusst gelb.**

**Neu belegt (7× `known`, 1× `free`):**

| Ziel | Preis | Beleg |
|---|---|---|
| Erdmannshöhle Hasel | 7,00 € Erw. / 5,00 € Kind / 22,00 € Familie | Gemeinde Hasel |
| Besuchsbergwerk Teufelsgrund | 8,00 € / 5,50 € / 25,00 € Familie | Betreiberseite |
| Heimatmuseum Resenhof Bernau | 6,00 € / 2,00 € Kind | Museumsseite |
| Steinwasen-Park Oberried | 29,00 € / 25,00 € Kind | Ticketseite |
| Hasenhorn Coaster Todtnau | 7,00 € nur Coaster, 15,00 € mit Bergbahn | Preisseite |
| Kandertalbahn | 18,00 € hin und zurück, **Kind 1,00 €** | Zweckverband |
| Cassiopeia Therme Badenweiler | 16,00 € für 2 Std., 24,00 € Tageskarte | Staatsbad |
| Stadtmuseum Wehr | **kostenlos** | Förderkreis, wörtlich |

- **Stadtmuseum Wehr** wechselte damit von gelb auf grün, weil der Förderkreis den
  freien Eintritt wörtlich ausschreibt – das ist der einzige Ampelwechsel nach grün,
  der nicht auf einer Zahl beruht.
- **Kandertalbahn**: Der Erwachsenenpreis von 18,00 € sieht teuer aus, begleitete
  Kinder zahlen aber 1,00 € je Richtung. Für Gruppen mit Kindern ist das eines der
  günstigsten Ziele überhaupt – deshalb steht das ausdrücklich im Kostenvermerk.
- **Hasenhorn Coaster**: eingetragen ist der günstigste Weg (7,00 €, Aufstieg zu Fuß),
  nicht der bequeme (15,00 € mit Bergbahn). Beides steht im Vermerk.

**13 bleiben gelb – mit Begründung statt Leerstelle.** Jeder dieser Einträge hat jetzt
einen datierten Vermerk, warum kein Preis dasteht, und wo er zu erfragen ist:
- *Betreiber nennt online keine Preise*: Hoffnungsstollen, Minigolf Todtmoos,
  Hotzenwald-Alpaka, Schloss Bonndorf, Klettgau-Museum Tiengen, Segerhof Wembach,
  Schlossberg Hornberg, Loipen Todtmoos.
- *Preis bewusst nicht fest*: Skigebiet Feldberg – dynamische Tagespreise, nur im
  Shop tagesaktuell; fest steht nur die Jahreskarte (480,00 €).
- *Technisch nicht auslesbar*: Schwarzwaldzoo Waldkirch (Preisliste nur als Bild),
  Vogtsbauernhof Gutach (Preistabelle wird per Skript nachgeladen, war weder im
  Seitentext noch im Browser sichtbar). Beim Vogtsbauernhof nennen Drittportale
  13,00 € – **bewusst nicht als belegt eingetragen**, nach der Lehre aus dem
  Wiedener-Eck-Fehler: keine Quelle als offiziell führen, die nicht selbst gelesen wurde.
- *Geparkt*: Radon Revital Bad Menzenschwand, geschlossen, Wiedervorlage 2026-11-08.
- **Teilbefund Wintersportplatz Todtmoos:** Die Gemeinde belegt „Schlittenfahrt am
  Rodelhang ist kostenlos", nennt für die Lifte aber nur „Preise auf Anfrage". Der
  Eintrag bleibt gelb, weist den Rodelhang jetzt aber als planbar kostenfreien Teil aus.

**Bilanz der 100 Ziele:** 50 kostenlos, 37 mit belegtem Preis, 13 offen
(vorher 49 / 30 / 21). Quellen: 129 eindeutige URLs.

**Linkcheck (130 URLs, 122 erreichbar):**
- **Echter Fehler gefunden und behoben:** Vita Classica Bad Krozingen – die
  hinterlegte URL enthielt ein „Ö" im Pfad und lief auf 404. Der Betreiber nutzt
  `Oeffnungszeiten` in ASCII-Schreibweise; korrigiert und gegengeprüft.
- Die übrigen 7 sind die bekannten Bot-Sperren (hochschwarzwald.de, basel.com),
  die im echten Browser einwandfrei laden. Keine fälligen Reviews.

---

### 2026-08-10 · Mobil-Nachbesserung: Ergebnisse kommen zuerst
Nachmessung nach dem Bedienelement-Lauf vom Vortag brachte zwei echte Ärgernisse ans Licht:

- **Man sah auf dem Handy kein einziges Ziel, ohne zu scrollen.** Gemessen bei 375 ×
  812 px lag die erste Karte bei **1247 px**. Aufteilung: Filterpanel 694 px,
  Ampel-Erklärung 359 px, Neuigkeiten 158 px, dazu Kopf und Hero.
- **Das Sortierfeld hatte 13,6 px Schriftgröße.** Unter 16 px zoomt iOS beim Antippen
  in die Seite hinein und kommt nicht von selbst zurück.

**Behoben:**
- Filterpanel startet unter 880 px eingeklappt, hinter einem 48 px hohen Knopf.
  Der Knopf zeigt einen Zähler, wenn Filter gesetzt sind – ein zugeklappter,
  unbemerkt aktiver Filter wäre die schlechtere Falle als der lange Scrollweg.
- Neuigkeiten und Ampel-Erklärung rutschen unter 880 px per `order` unter die
  Ergebnisse. Beide bleiben erhalten, stehen aber nicht mehr im Weg.
- Alle Eingabe- und Auswahlfelder auf 16 px, damit iOS nicht hineinzoomt.
- Der Touch-Medienblock stand zu früh im Stylesheet und wurde von den allgemeinen
  Chip- und Feldregeln überschrieben; er steht jetzt am Ende.

**Nachgemessen:** erste Karte bei **692 px** statt 1247 px, eine Karte ohne Scrollen
sichtbar, kein Überlauf, keine Konsolenfehler. Umschalter, Zähler und Zurücksetzen
geprüft: Voreinstellung „Regentag" → Zähler 1, 33 Treffer; Zurücksetzen → Zähler aus,
100 Treffer. Auf dem Desktop unverändert: Knopf versteckt, Filter klebend, normale
Reihenfolge. Der Zustandswechsel schaltet nur bei echtem Wechsel zwischen schmal und
breit um – auf dem Handy löst schon die eingeblendete Tastatur ein Resize aus, das
darf den Filter nicht unter den Fingern zuklappen.

---

### 2026-08-09 · Mobil-Audit: Bedienelemente fingerfreundlich
- **Layout war bereits mobiltauglich:** `viewport`-Meta korrekt, bei 375 px kein
  horizontaler Überlauf, Raster fällt auf eine Spalte, das Filterpanel wird unter
  880 px `static` (kein Eigen-Scroll, kein Klebe-Effekt), Überschrift skaliert per `clamp`.
- **Befund:** die Bedienelemente waren zu klein für den Daumen. Der Entfernungs-
  Schieberegler maß nur 16 px Höhe, Kategorie-Chips 31 px, Voreinstellungen 33 px,
  Kästchen und Auswahlfeld unter 40 px. Empfohlenes Mindestmaß für Touch: 44 px.
- **Behoben** über einen Medienblock `(pointer: coarse), (max-width: 880px)`:
  Schieberegler 44 px (Griff 26 px), Chips und Voreinstellungen 40 px, Kästchenzeilen
  44 px, Sortierauswahl 44 px, Zurücksetzen 46 px, Themenknopf 44 px.
- **Nachgemessen:** 375 px und 768 px, jeweils kein Überlauf, kein Bedienelement mehr
  unter 40 px, keine Konsolenfehler. Auf dem Tablet zwei Karten pro Reihe.
- Reine Darstellungsänderung, Katalog unberührt.

### 2026-08-09 · Letzter Beleg nachgezogen – 100/100 amtlich
- **Wiedener Eck** war das einzige Ziel ohne amtliche Einzelquelle. Jetzt belegt durch die
  Attraktionsseite **Info-Pavillon am Wiedener Eck** und die Tourenseite „Vom Wiedener Eck auf
  den Feldberg" (beide Schwarzwald Tourismus, erreichbar geprüft).
- Der Eintrag wurde dabei inhaltlich aufgewertet: Passhöhe 1035 m, **Westweg-Portal** (hier endet
  die 10. und beginnt die 11. Etappe des Westwegs Pforzheim–Basel), Wanderparkplatz, Einstieg
  links vom Hotel; Touren zum Feldberg (rund 17 km, 6 Std, anspruchsvoll), zum Belchen und zum
  Rollspitz (1236 m).
- **Ergebnis: Jedes der 100 Ziele hat jetzt mindestens einen amtlichen Verweis.**
  127 Quellenbelege insgesamt.

### 2026-08-09 · Verweis-Audit über alle 100 Ziele
- **Anlass:** Vollprüfung, ob die Quellenverweise sauber sind – Erreichbarkeit **und** Struktur.
- **Struktur (fehlerfrei):** 100 Ziele, alle mit mindestens einer Quelle; keine leeren URLs,
  alle Links `https`, keine doppelten `seed_key` oder Titel. Vier URLs belegen jeweils zwei
  verwandte Ziele (Gemeinde-Übersichtsseiten) – geprüft und in Ordnung.
- **`check-links`:** 114 von 122 URLs erreichbar. Sieben Meldungen sind der bekannte Bot-Block
  (HTTP 403 von `hochschwarzwald.de` und `basel.com`) – die Seiten laden für Besucher.
- **Ein echter Fehler – aus dem eigenen letzten Lauf:** Die in der zweiten Qualitätsrunde
  eingetragene Pfarrei-URL `se-todtmoos-bernau.de` ist **per DNS nicht auflösbar**. Ersetzt durch
  die offizielle Gemeindeseite `todtmoos.de/p/wallfahrtsort-todtmoos` (Öffnungszeiten dort
  bestätigt). **Wichtige Folge:** Die Gemeinde sagt nichts zur Barrierefreiheit – die zuvor
  gesetzte Angabe `step_free: true` stammte allein aus der toten Quelle und wurde
  **zurückgenommen**. Lieber keine Angabe als eine unbelegte.
- **Schwachstellen behoben:** Einträge ganz ohne amtliche Quelle 3 → 1.
  - **Todtmooser Wasserfall** (Kernziel!) hatte nur eine abgeleitete Quelle → zwei amtliche
    Belege ergänzt (Schwarzwald Tourismus, Gemeinde Todtmoos) und die Beschreibung präzisiert
    (Steg mit Geländern, Brücke, Sitzbänke; im Winter Vereisungsgefahr).
  - **Ihringen** – `ihringen-touristik.de` ist die offizielle Tourismusseite der Gemeinde,
    Status entsprechend korrigiert.
  - **Wiedener Eck** bleibt als einziges Ziel ohne amtliche Einzelquelle (nur Regions-Übersicht) –
    dokumentiert, Beleg bei Gelegenheit nachziehen.
- **Ergebnis:** 126 Quellenbelege, davon 120 amtlich.

### 2026-08-09 · Zweite Qualitätsrunde: Öffnungszeiten amtlich belegt
- **Anlass:** 9 Einträge trugen einen abgeleiteten Sonntagsstatus (`derived`) – Öffnung oder
  Zugänglichkeit war nur plausibel, nicht belegt.
- **Fünf amtlich nachbelegt:**
  - **Wallfahrtskirche Todtmoos** – die Seelsorgeeinheit belegt täglich 8–19 Uhr (Sommer) bzw.
    8–17 Uhr (Winter) und **Barrierefreiheit**; Quelle von `derived` auf `official`, Sonntag auf
    `confirmed`, `step_free` auf true. → **grün**
  - **Colmar** – Quelle auf das offizielle Office de Tourisme umgestellt; Altstadt und Petite
    Venise jederzeit zugänglich. → **grün**
  - **Römische Badruine Badenweiler** – Staatliche Schlösser und Gärten BW: täglich 10–18 Uhr
    (ab 1.11. bis 17 Uhr), Erwachsene 3 €, ermäßigt 1,50 €, Familien 7,50 €. → **grün**
  - **Krunkelbachhütte Bernau** – Betreiber belegt täglich 10:30–18 Uhr, **kein Ruhetag**
    (Küche 11–17 Uhr). → **grün**
  - **Vita Classica Bad Krozingen** – täglich 8:30–22 Uhr belegt, Tageskarte 21,90 € plus 3 €
    Wochenendaufpreis (sonntags also rund 24,90 €). → **rot**, weil weit über Standardbudget –
    aber jetzt belastbar statt unbekannt.
- **Bewusst nicht hochgestuft:** Pfarrkirche Rickenbach – keine veröffentlichten Öffnungszeiten
  auffindbar; bleibt `derived` mit präzisiertem Hinweis. Ebenso Radon Revital Bad (Betreiber-
  wechsel, Prüfung im November), Schlossberg Hornberg und Naturzentrum Kaiserstuhl
  (sonntags in der Regel geschlossen – das ist ein echter Prüfgrund).
- **Ergebnis:** abgeleiteter Sonntagsstatus 9 → **4**, unbelegte Preise 23 → **21**,
  Quellenbelege 124. Ampel von 57/31/12 auf **60 Passt / 27 Vorher prüfen / 13 Passt nicht**.

### 2026-08-09 · Qualitätsrunde: Preise nachbelegt
- **Anlass:** 38 Einträge standen auf „Vorher prüfen". Analyse der Ursachen: 30× unbelegter
  Preis, 20× saisonale Öffnung, 9× abgeleiteter Sonntagsstatus, 7× abgeleitete Quelle.
- **Fokus:** Nur bei **9 Einträgen** konnte ein Preisbeleg überhaupt etwas ändern (die übrigen
  bleiben zu Recht gelb – eine saisonale Öffnung ist ein echter Prüfgrund, den kein Preis heilt).
- **Sieben Preise offiziell nachbelegt:** Heimethüs Todtmoos 4 €, Hans-Thoma-Kunstmuseum
  Bernau 5 €, Skimuseum Hinterzarten 5 €, Kloster Museum St. Märgen 6 €, Burg Rötteln 4 €
  (alle → **grün**), Rothaus-Brauereiführung 15 € und Museum Tinguely CHF 18 (→ **rot**, weil
  über dem Standardbudget von 10 €).
- **Bewusst nicht belegt:** Cassiopeia Therme Badenweiler – die Drittquellen widersprechen sich
  (14,50 € vs. 15,50 €) und eine offizielle Preisseite war nicht auffindbar. Bleibt „Kosten
  unklar", die Spanne steht jetzt als Hinweis im Eintrag.
- **Ergebnis:** unbelegte Preise 30 → 23. Ampel von 52/38/10 auf **57 Passt / 31 Vorher prüfen /
  12 Passt nicht**. Die zwei neuen „Passt nicht" sind ein Qualitätsgewinn, kein Rückschritt:
  ein belegter zu hoher Preis ist ehrlicher als ein unbekannter – und bei höherem Budget
  werden beide grün.

### 2026-08-09 · DIE 100 IST VOLL
- **Ausbau:** 70 → **100 Ziele** (Version `2026-08-09.8`), 132 Quellenbelege. Damit deckt die
  Bibliothek den Südschwarzwald, den Hochrhein und das Dreiländereck bis rund 95 km ab.
- **Neu in diesem Lauf (30):** Colmar, Breisach (Stephansmünster), Klosteranlage St. Peter,
  Kloster Museum St. Märgen, Augusta Raurica, Schlossbergturm Freiburg, Höchenschwand,
  Bergwerk Teufelsgrund, Fondation Beyeler, Augustinermuseum Freiburg, Schwarzwaldzoo
  Waldkirch, Kandertalbahn, Riesenbühlturm Schluchsee, Klettgau-Museum Tiengen, Vita Classica
  Bad Krozingen, Schlossberg Hornberg, Belchen-Seilbahn, Bergwerk Finstergrund, Klösterle
  Schönau, Segerhof Wembach, Energieerlebnispark Buchenbrändle, Hasenhornturm, Todtnauberg/
  Stübenwasen, Schönau im Wiesental, Stadtrundgang Wehr mit Sagenpfad, Museum Tinguely,
  Naturzentrum Kaiserstuhl, Stadtmuseum Wehr, Ihringen, Wiedener Eck.
- **`check-links`:** 105 von 114 URLs erreichbar.
  - **Burg Rötteln** – `/oeffnungszeiten.htm` 404 → auf die Startseite umgestellt und dabei die
    Zeiten präzisiert (Unterburg frei, Oberburg täglich 10–18 Uhr, letzter Einlass 17:30).
  - **Staufen** – `breisgau-burgen.de` 404 → durch Schwarzwald-Tourismus und Tourismus BW ersetzt.
  - Sieben weitere Meldungen sind HTTP 403 von `hochschwarzwald.de` und `basel.com` – Bot-Block,
    keine toten Links (alle Seiten wurden bei der Recherche gelesen).
- **Verteilung:** 9 Todtmoos / 29 Nahbereich / 48 Tagesausflug / 14 Fernziel.
  Ampel 51 Passt / 39 Vorher prüfen / 10 Passt nicht.
- **Hero:** Meilenstein-Zeile „💯 100 Ziele seit 09.08.2026" ergänzt.

### 2026-08-09 · Ausbau auf 70 Ziele + Umbenennung
- **Ausbau:** 50 → **70 Ziele** (Version `2026-08-09.5`), 102 Quellenbelege. Der Radius reicht
  jetzt bis rund 95 km: Triberger Wasserfälle, Europa-Park Rust, Basel (Altstadt/Münster, Zolli),
  Vitra Campus Weil, Ravennaschlucht, Schauinslandbahn + Museums-Bergwerk, Erdmannshöhle Hasel,
  Burg Rötteln, Badeparadies Titisee, Kaiserstuhl, Mundenhof, Rheinfall Schaffhausen,
  Skimuseum Hinterzarten, Staufen, Kloster St. Trudpert, Feldsee, Badenweiler (Römerbadruine
  und Cassiopeia Therme).
- **Umbenennung:** Der Katalog deckt nun den ganzen Südschwarzwald bis ins Dreiländereck ab.
  Titel, Logo und Hero heißen deshalb **„Ausflugsfinder Südschwarzwald – Basis Todtmoos"**;
  die Entfernungen bleiben ab Todtmoos gemessen.
- **Stufen angepasst:** Nahbereich bis 20 km (vorher 15), Tagesausflug bis 60 km (vorher 45),
  darüber Fernziel – sonst wären Basel, Freiburg und Rust alle in einem Topf gelandet.
  Verteilung jetzt: 9 Todtmoos / 23 Nahbereich / 33 Tagesausflug / 5 Fernziel.
- **Nicht aufgenommen:** Deutsches Uhrenmuseum Furtwangen – wegen Generalsanierung **bis 2027
  geschlossen** (analog zum Museum am Dom bei der Schwesterseite).
- **Grenzhinweise:** Bei den Schweizer Zielen (Basel, Zolli, Rheinfall) stehen Ausweis- und
  Franken-Hinweise in der Checkliste; Preise sind als CHF gekennzeichnet.
- Ampel danach: 38 Passt / 25 Vorher prüfen / 7 Passt nicht (die „no" sind hochpreisige Ziele
  wie Europa-Park und Thermen über dem Standardbudget – budgetabhängig, kein Fehler).

### 2026-08-09 · Großer Ausbau auf 50 Ziele + Link-Check
- **Ausbau:** 32 → **50 Ziele** (Version `2026-08-09.4`), 81 Quellenbelege. Der Radius wurde
  bewusst ausgeschöpft (bis rund 95 km), damit die Bibliothek über den Nahbereich hinaus trägt:
  Titisee, Wutachschlucht, Steinwasen-Park, Sauschwänzlebahn, Skigebiet Feldberg, Freiburger
  Altstadt, Waldshut, Laufenburg, Grafenhausen (Hüsli, Schwarzwaldhaus der Sinne, Rothaus),
  Schloss Bonndorf, Vogtsbauernhof Gutach, Albsteig, Windbergwasserfall, Hotzenpfad und
  Pfarrkirche Rickenbach, Krunkelbachhütte Bernau.
- **`check-links`:** 60 von 63 URLs erreichbar.
  - **Schloss Bonndorf** – `bonndorf.de`-Unterseite liefert 404 (Seite umgezogen) → durch die
    offizielle Landes-Tourismusquelle ersetzt; bei der Gelegenheit die Narrenstuben-Zeiten
    präzisiert (So 14–17 Uhr) und der Unterschied zwischen Fasnachtsmuseum und den
    Wechselausstellungen des Kulturzentrums im Eintrag klargestellt.
  - **Titisee** und **Wutachschlucht** – HTTP 403 von `hochschwarzwald.de`: Bot-Block, kein toter
    Link (beide Seiten wurden bei der Recherche erfolgreich gelesen). Keine Änderung nötig.
- **Verteilung nach Stufen:** 9 in Todtmoos, 16 Nahbereich, 23 Tagesausflug, 2 Fernziel.
  Ampel 30 Passt / 18 Vorher prüfen / 2 Passt nicht.
- **Commit:** siehe Repo-Historie zum Katalog `2026-08-09.4`.

### 2026-08-09 · Datierung angeglichen
- **Anlass:** Die `catalog_version` und die Prüfdaten trugen noch das Aufbau-Label
  `2026-07-27`, obwohl real am 8./9. August gearbeitet wurde – Label und Wirklichkeit
  gingen auseinander.
- **Umgestellt:** Version auf `2026-08-09.2`; **28 Einträge** von `source_checked_on:
  2026-07-27` auf `2026-08-09`, **34 Quelldaten** ebenso; alle zugehörigen
  `next_review_on` **intervallerhaltend** um 13 Tage nachgezogen (90/180-Tage-Regel bleibt
  exakt gewahrt). Die ortsunabhängigen Vorlagen behalten ihr eigenes Datum (2026-07-14/20).
- **Zwei Ausreißer nachjustiert:** Der bewusst gesetzte Radon-Klärungstermin war
  mitverschoben worden → zurück auf **2026-11-08**; Belchen lag 13 Tage unter dem
  180-Tage-Intervall → auf **2027-02-05** angeglichen.
- **Ergebnis:** keine Datumsreste von `2026-07-27`, keine Intervall-Ausreißer,
  kein überfälliger Eintrag. README-Standzeile auf 2026-08-09 / 32 Ziele korrigiert.

### 2026-08 · Erster Monats-Pflegelauf
- **Stand vor dem Lauf:** 28 Ziele, Katalog `2026-07-27.6`.
- **`check-links`:** 32 von 35 URLs erreichbar. Drei Funde – alle behoben:
  - **Radon Revital Bad Menzenschwand** – TLS-Handshake-Fehler beim Link-Check. Recherche
    ergab einen echten Statuswechsel: Stadtratsbeschluss vom 23.09.2025 = dauerhafte
    Schließung zum Jahresende 2025 (zu ab 01.11.2025); nach Käuferwechsel ist eine
    Wiedereröffnung im Mai 2026 gemeldet (früher täglich 10–21 Uhr, Tageskarte 15 €).
    Eine amtliche Bestätigung des aktuellen Betriebs für August 2026 war nicht auffindbar
    (Betreiberseite TLS-blockiert, Stadt-Revitalbad-Seite 404, Preis-PDF nur Bild).
    → Nicht zurückgestellt (Wiedereröffnung gemeldet), aber bewusst auf „Vorher prüfen"
    gehalten: `sunday_status: derived`, Preis nur als Hinweis, Schließungs-/Wiedereröffnungs-
    geschichte im Kartentext, offizielle Stadt-Quelle (Schließungsbeschluss) ergänzt,
    tote `radonrevitalbad.de`-Quelle durch eine DMO-Quelle ersetzt. Nächste Prüfung 2026-11-08.
  - **Wintersportplatz Todtmoos** – tote `schwarzwald-tourismus.info`-URL (404) durch die
    funktionierende Wintersportgebiet-Seite ersetzt.
  - **Kurgarten St. Blasien** – tote `heilbaeder-bw.de`-URL (404) entfernt; Stadt-St.-Blasien-
    Quelle bleibt.
- **README:** Pflege-Checkliste und alle Pfade/URLs von der Schwesterseite Sonntagsfinder
  auf Todtmoos umgestellt (`todtmoos-offline.html`, `Todtmoos-Public`, Live-URL, `repoIssues`,
  Datenbasis).
- **Nach anschließenden Katalog-Erweiterungen** (auf 32 Ziele) erneuter Link-Check:
  **40 von 40 URLs erreichbar, keine toten Links, keine fälligen Reviews.**
- **Commits:** `445162b` (Pflegelauf + README), `70c66b5` (Radon-Status geklärt),
  `8f7b6be` (Erweiterung auf 32 Ziele, Link-Recheck 40/40).
- **Offene Wiedervorlagen:** Radon Revital Bad (2026-11-08), diverse Preis-/Saison-Einträge
  (2026-10-25 / 2026-11-08).

---

## Katalog-Aufbau (Wachstum)

| Datum | Version | Ziele | Commit | Neu / Anlass |
|---|---|---:|---|---|
| 2026-08-08 | `2026-07-27.1` | 6 | `91d4ad0` | Erstkatalog – Sonntagsfinder-Engine auf Todtmoos umgebrandet |
| 2026-08-08 | `2026-07-27.2` | 11 | `e524888` | Kurpark, Lebküchlerweg, Menzenschwander + Todtnauer Wasserfall, Schluchsee |
| 2026-08-08 | `2026-07-27.3` | 15 | `f225beb` | Holzbrücke Bad Säckingen, Radon Revital Bad, Feldberg-Gipfel, Minigolf |
| 2026-08-08 | `2026-07-27.4` | 19 | `97de412` | Bernau-Museen (Hans-Thoma, Resenhof), Aqualon Therme, Wintersportplatz; Meldeweg auf GitHub-Issues |
| 2026-08-08 | `2026-07-27.5` | 24 | `a8f316d` | Wildgehege St. Blasien, Hochkopfturm, Rabenschlucht, Bergsee, Domsteig |
| 2026-08-09 | `2026-07-27.6` | 28 | `767293f` | Wehraschlucht, Kurgarten St. Blasien, Hotzenwald-Alpaka, Loipen/Winterwandern |
| 2026-08-09 | `2026-07-27.9` | 32 | `8f7b6be` | Hochrheinmuseum + Wild Kids Bad Säckingen, Kreismuseum St. Blasien, Belchen |

Öffentlich live seit dem ersten Deploy auf **https://tschenso.github.io/todtmoos/**
(Repo `github.com/Tschenso/todtmoos`, GitHub Pages von `main` / `/root`; jeder Push auf
`main` aktualisiert die Live-Seite automatisch).
