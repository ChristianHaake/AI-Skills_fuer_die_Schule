# Automatisierung und Regelwerk

Dieses Hintergrunddokument beschreibt die Pflege der Sammlung „AI-Skills für die Schule". Es richtet sich an Mitwirkende und gehört nicht zum regulären Leseweg.

---

## Redaktionelle Regel

Empfohlen werden nur Tools, Skills und Ressourcen, die aus praktischer Nutzung im schulischen Kontext sinnvoll erscheinen und deren Empfehlung kurz begründet werden kann. Die Sammlung ist **kuratiert**, keine vollständige Marktübersicht und kein objektives Ranking.

Besonderer Fokus liegt auf:

- **Datenschutz & lokale Verarbeitung** (DSGVO-konform, keine Cloud-Zwang)
- **Freie Lizenzen** (Open Source, CC BY-SA, CC BY-NC-SA, AGPL, GPL)
- **Deutschsprachigkeit** & Curriculum-Bezug (deutsche Lehrpläne)
- **Sofortige Einsatzbarkeit** (keine komplexen Setup-Hürden)

---

## Format einer Empfehlung

```md
### Toolname / Skillname

- **Zweck:** Wofür das Tool/Skill gedacht ist und welches konkrete Problem es im Unterricht löst.
- **Warum hier:** Warum du es empfiehlst – mit der wichtigsten Stärke oder Einschränkung (z.B. Lizenz, Datenschutz, Curriculum-Bezug).
- **Lizenz:** Lizenzbezeichnung (z.B. CC BY-SA 4.0, AGPL-3.0, GPL-3.0)
- **Quelle:** Link zur offiziellen Quelle / Download / Repository
```

**Pflichtfelder:** Zweck, Warum hier, Lizenz, Quelle. Fehlt eines, wird der Eintrag nicht aufgenommen.

---

## Technische Statusprüfung

Statusdaten werden künftig automatisiert geprüft. Erfasst werden nur überprüfbare Fakten:

- Erreichbarkeit der offiziellen Projektseite / Download-Links
- Letzte veröffentlichte Version oder letzter Release
- Aktivität eines offiziellen Repositories (Commits, Issues, Releases)
- Lizenz (Maschinenlesbar via SPDX / REUSE / LICENSE-Datei)
- Plattform-Support (macOS, iPadOS, Browser, Linux, Windows)
- Preis- / Tarifangaben, soweit öffentlich verfügbar

**Die technische Prüfung beurteilt nicht, ob ein Tool weiterhin empfehlenswert ist — das bleibt eine redaktionelle Entscheidung.**

---

## Synchronisation & Quellen

### Quellen-Strategie

- **Primärquellen:** Offizielle Repositories (GitHub, GitLab, Codeberg), Projektwebseiten, OER-Portale
- **Sekundärquellen:** Nur wenn Primärquelle nicht auffindbar, mit Verweis auf Primärquelle
- **Keine:** Aggregatoren ohne eigene Kuratierung, reine Linklisten

### Lizenz-Prüfung

- Bevorzugt: **Freie Lizenzen** (OSI/FSF-anerkannt, Creative Commons mit SA/ND-Klausel nur bei guter Begründung)
- NICHT aufgenommen: Proprietär ohne Free-Tier, Lizenzen mit kommerziellen Nutzungseinschränkungen ohne Schul-Ausnahme
- Lizenz **MUSS** im Eintrag angegeben sein (SPDX-Kurzform oder Vollname)

---

## Kategorien-Systematik

Die Kategorien sind **nicht starr** — ein Tool kann in mehreren Kategorien auftauchen, wenn es thematisch passt. Die Einordnung folgt dem **primären Einsatzzweck im Unterricht**.

Aktuelle Kategorien (Stand Initial-Setup):

1. **KI-Skills & Claude Skills** — KI-gestützte Skills für Unterrichtsplanung & Materialerstellung
2. **Lernplattformen & Assistenten** — Plattformen für KI im Unterricht (AIS.chat, etc.)
3. **Unterrichts-Tools (lokal/datenschutzfreundlich)** — Webtools & Apps ohne Cloud-Zwang
4. **OER-Fundgruben** — Sammlungen freier Lernmaterialien
5. **Lern- und Reflexionshilfen** — Feedbackbögen, Reflexionsbögen, Beobachtungstools
6. **KI-Kompetenz & Curriculum** — Medientheorie, KI-Ethik, direkte Lehrplan-Bezüge

Neue Kategorien werden im Team (Issues) besprochen, bevor sie aufgenommen werden.

---

## Automatisierung (Geplant)

Folgende Automatisierungen sind angedacht, aber noch nicht implementiert:

1. **Link-Checker (wöchentlich):** Prüft alle `Quelle:`-URLs auf Erreichbarkeit (HTTP 200), markiert tote Links in Issues.
2. **Lizenz-Scanner:** Extrahiert SPDX/LICENSE aus verlinkten Repos, vergleicht mit Eintrag.
3. **Release-Watcher:** Überwacht GitHub Releases der verlinkten Repos, meldet neue Versionen.
4. **Sync mit Tool-Collection_MacOS/Linux:** Plattformübergreifende Tools (z.B. browserbasierte Webtools) sollen in allen drei Sammlungen identisch geführt werden.

---

## Beitragsprozess

1. **Issue eröffnen** (Template: `.github/ISSUE_TEMPLATE/tool-empfehlung.md`) mit Tool-Name, Link, Kategorie, Begründung.
2. **Redaktionelle Prüfung** durch Maintainer (Format, Lizenz, Schulbezug).
3. **Aufnahme** via PR in `README.md` (ein Eintrag pro PR, saubere History).
4. **Merge** nach Review — keine direkten Commits auf `main`.

---

## Metadaten-Datei (Optional, zukünftig)

Für tiefere Automatisierung kann jede Empfehlung eine begleitende YAML/JSON-Metadaten-Datei erhalten (z.B. `data/tools/<slug>.yaml`) mit:

```yaml
name: "Toolname"
category: "KI-Skills & Claude Skills"
purpose: "Kurzzweck"
why: "Begründung"
license: "CC BY-SA 4.0"
source_url: "https://..."
repo_url: "https://github.com/..."  # optional
platforms: ["browser", "macos", "linux", "windows", "ipados"]
price: "free"  # oder "freemium", "paid"
last_checked: "2026-09-21"
status: "active"  # active, deprecated, archived
```

Dies ist **optional** und wird erst bei Bedarf eingeführt.

---

## Changelog

| Datum | Änderung |
|:---|:---|
| 2026-09-21 | Initial-Version (adaptiert von Tool-Collection_MacOS) |