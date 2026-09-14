---
name: niederspannungsnetz-schema-vorgaben
description: Verbindliche Vorgabe für den Aufbau von Niederspannungsnetz-/Zähler-Fließschemen im Mieterstrom-Projekt (Konfigurator-Diagramm und ähnliche Darstellungen).
scope: Nur dieses Projekt (Mieterstrom) — kein projektübergreifendes @-Import in 99.Software/CLAUDE.md.
---

# Vorgabe: Niederspannungsnetz-Fließschema (Mieterstrom)

Grundlage: Auswertung der eigenen Referenzunterlagen in diesem Ordner (`Elektroschema einfache
Darstellung_Schaltplan`, `mieterstrom-messkonzept-bis-4-mieter`, `mieterstrom-messkonzept-ab-4-mieter`,
`260822_Messstellenschema_Entwurf`) plus Klärung mit Marc am 2026-09-14. Gilt für das interaktive
Schema auf `mieterstrom-erklaerung.html` und für vergleichbare zukünftige Darstellungen in diesem
Projekt.

## Grundprinzip Zählkonzept

- Ein Zähler an der Übergabe zum Netzbetreiber (Messstellenbetreiber-Zähler) — **kein** GWL-Z-Tag,
  da er nicht GWL/dem Eigentümer gehört.
- Die GWL-eigene, fortlaufende Nummerierung (Z01, Z02, …) beginnt direkt beim Hauptzähler/
  Wandlerschrank.
- Ein Zähler an **jedem Erzeuger** (PV/Speicher-Kette wird über den Hauptzähler mitgemessen, kein
  separater Erzeugungszähler in der Kundenseiten-Darstellung).
- Ein Zähler an **jedem Verbraucher-Zweig**: Allgemeinstrom, Wärmepumpe, jede Wohnung einzeln, jede
  Wallbox einzeln.
- **Kein Sammelzähler** — auch dann nicht, wenn mehrere Verbraucher (z. B. Garage + Wallbox) real am
  selben Zähler hängen könnten. Für dieses Projekt gilt bewusst die einfachere, konsistentere Regel:
  jede Kategorie bekommt immer ihren eigenen Zähler (siehe Entscheidungen unten).
- Bilanzprinzip (aus den Referenzschemen): Summe aller Zählerwerte (Bezug/Erzeugung positiv,
  Verbrauch negativ) ergibt am Ende 0. Für die Kundenseite nicht rechnerisch relevant, aber als
  fachlicher Hintergrund für Texte/Erklärungen nützlich.

## Hauptpfad (Energiefluss)

1. Öffentliches Netz
2. Netzanschluss (400V AC, i. d. R. dreiphasig)
3. Hausanschlusskasten (HAK) — Eigentumsgrenze direkt danach
4. Übergabezähler (Messstellenbetreiber, zweirichtig, kein GWL-Z-Tag)
5. Hauptzähler (≤ 50A/44A) **oder** zentraler Wandlerschrank (> 50A/30kVA) — Z01
6. Hauptverteilung / Sammelschiene

## PV-Seite

PV-Module → (Hybrid-)Wechselrichter → optional DC-seitiger Batteriespeicher → speist in den
Hauptpfad vor der Hauptverteilung ein. Kein separater Erzeugungszähler in der
Kundenseiten-Darstellung (vereinfacht gegenüber den technischen Referenzschemen, die teils einen
PV-Erzeugungszähler führen).

## EMS / PlexLog

Sitzt konzeptionell an der Übergabe, misst alle Zähler passiv mit (Strichpunktlinie zu jedem
GWL-Zähler, siehe Frontend-Vorgaben.md "Layout & Linien" für die Linienführung: rechtwinklig, nie
durch andere Felder). Funktionen laut Referenzschema: Messdatenerfassung, Steuerung Wärmepumpe
(SG Ready/Modbus), Lastmanagement/Peak Shaving, PV-Überschussnutzung, Schnittstelle zum
Messstellenbetreiber (z. B. metergrid).

## Abzweig-Kategorien ab der Hauptverteilung

| Kategorie | Eigener Zähler? |
|---|---|
| Allgemeinstrom (Treppenhaus, Keller, Außenlicht, Aufzug, Technik) | Ja, immer |
| Wärmepumpe (Heizung/Warmwasser) | Ja, immer eigener Zähler (Entscheidung 2026-09-14 — Referenzschemen zeigen teils auch "hinter Allgemeinstrom ohne eigenen Zähler", das gilt für dieses Projekt bewusst nicht) |
| Mieter (jede Wohnung) | Ja, immer, eine pro Wohnung |
| Ladeinfrastruktur/Wallbox | Ja, immer eigener Zähler pro Wallbox (Entscheidung 2026-09-14 — Referenzschema MFH 78176 zeigt teils Wallbox hinter Zonen-Zähler gebündelt, das gilt hier bewusst nicht) |
| Eigentümer-Eigennutzung als separate Kategorie (getrennt von "Mieter") | Nein — für diese Kundenseite nicht nötig (Entscheidung 2026-09-14), generischer Begriff "Wohnung" reicht |

Der Heizungsabzweig (Wärmepumpe) sitzt fix auf der Symmetrielinie des Schemas; Allgemeinstrom und
Sonstiges verteilen sich symmetrisch links/rechts davon (siehe Frontend-Vorgaben.md).

## Farbkategorien

Vier Kategorien, je Zähler-/Bauteil-Rolle (nicht AC/DC-Signalfarbe):

| Kategorie | Farbe | Umfasst |
|---|---|---|
| Netz / Messstellenbetreiber | Blau (`#58A6FF`) | Netz, HAK, Übergabezähler |
| Energieerzeuger | Grün (`#2DA44E`) | PV-Module, Wechselrichter, Speicher |
| EMS | Gold (`#E3A008`) | Nur PlexLog |
| GWL-Zähler (MID) | Violett (`#A371F7`, neu) | Hauptzähler/Wandlerschrank, Allgemeinstrom-, Wärmepumpen-, Mieter-, LIS-Zähler |
| Verbraucher/Struktur (neutral) | Grau, wie bisher | Endverbrauchs-Boxen (Wohnung, Wallbox, Allgemeinstrom-Verbrauch, …) |

**Hinweis:** Grün wechselt damit die Bedeutung gegenüber dem ursprünglichen Konfigurator-Stand
(vorher: Grün = MID-Zähler, Gold = Erzeuger+EMS zusammen).

Verbindungslinien bleiben neutral grau (`#8B949E`), unabhängig von der Kategorie der verbundenen
Felder — nur die Feld-Farbe selbst zeigt die Kategorie.

## Linien & Layout

Gilt zusätzlich zu Frontend-Vorgaben.md "Layout & Linien" (Raster, Eck-Radius, nur
senkrecht/waagerecht):

- Kommunikations-/Steuerlinien (PlexLog → Zähler): Strichpunktlinie, dezent (niedrige Deckkraft),
  rechtwinklig geführt über eine freie Trasse, kreuzt keine anderen Feld-Boxen — Kreuzung mit der
  Kupfer-Hauptverteilungsschiene selbst ist akzeptiert (keine "Feld"-Box).
- Boxen, die exakt auf der Symmetrieachse liegen wie ein anderes Strukturelement (z. B.
  Wärmepumpe auf der Mieter/LIS-Schiene): blickdichte Hintergrund-Unterlage statt sichtbarem
  Durchscheinen — die Struktur bleibt durchgängig, wird aber nicht sichtbar überdeckt.

## Umsetzungsstand

Farbschema (Blau/Grün/Gold/Violett wie oben) ist im Konfigurator-Code umgesetzt (Stand 2026-09-14):
CSS-Tokens `--violet`/`--blue` ergänzt, JS-`styleFor`-Kategorien `mid`→violett, `erzeuger`
(neu, PV/Wechselrichter/Speicher)→grün, `ems` (nur noch PlexLog)→gold, Legende um "Netz &
Messstellenbetreiber" und "Energieerzeuger" ergänzt.
