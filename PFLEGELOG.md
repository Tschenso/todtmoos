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
