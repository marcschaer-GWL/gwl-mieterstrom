# MESSSTELLENSCHEMA – MFH 78176

Einseitiges Messstellenschema für Mieterstrommodell mit Smart Meter (EMS) vor Hauptverteilung – PV-Anlage mit optionalem DC-seitigem Speicher.

- **Objekt:** MFH 78176
- **Projekt-Nr.:** –
- **Stand:** 22.08.2026
- **Kennzahl:** 15 abrechnungsrelevante Messpunkte

## Legende

| Symbol | Bedeutung |
|---|---|
| Linie blau, durchgezogen | AC – Energiefluss |
| Linie grün, durchgezogen | DC – Energiefluss |
| Linie gestrichelt | Kommunikation / Messdaten (Modbus / CLS) |
| kWh-Symbol | Zähler MID / eichrechtskonform (abrechnungsrelevant) |
| SM-Symbol | Smart Meter (führt EMS aus) (nicht abrechnungsrelevant) |

## Messpunkte gesamt

- 2 zentrale Zähler
- 11 Mieterverbrauchszähler
- 2 Eigentümerverbrauchszähler
- **= 15 abrechnungsrelevante Messpunkte**

## Option Speicher (DC-seitig)

Batteriespeicher DC-seitig am Hybridwechselrichter (PV-gekoppelt) – heute optional, später integrierbar.

## Energiefluss (Hauptpfad)

1. Öffentliches Netz
2. Hausanschlusskasten (HAK)
3. **Z1 – Summenzähler Netz**: Bezug / Einspeisung (HAK nach TAB), Bilanzgrenze zum Netz
4. **SM – Smart Meter (EMS)**: Messung und Steuerung
5. Hauptverteilung (HV)
6. Verteilung an Mieter (11 Zähler) und Eigentümer (2 Zähler)

## PV-Anlage (DC)

PV-Module → Hybridwechselrichter (DC/AC) → AC-Einspeisung in Smart Meter (SM).
Batteriespeicher (optional, DC) – gestrichelt/kommunikativ an Hybridwechselrichter angebunden.

## Smart Meter (EMS) – Funktionen

- Erfassung aller relevanten Messwerte
- Energiemanagement & Optimierung
- Steuerung Wärmepumpe (SG Ready / Modbus)
- Lastmanagement / Peak Shaving
- PV-Überschussnutzung
- optionale Speichersteuerung
- Schnittstelle zu metergrid (CLS/SMGW)

## Wärmepumpe (Heizung / Warmwasser)

Anbindung an Smart Meter (EMS) zur Steuerung und Verbrauchserfassung (keine separate Messstelle erforderlich).

## Mieter – 11 Zähler

### 7 Wohnungen
| Zähler | Zuordnung |
|---|---|
| Z3 | Wohnung 1 |
| Z4 | Wohnung 2 |
| Z5 | Wohnung 3 |
| Z6 | Wohnung 4 |
| Z7 | Wohnung 5 |
| Z8 | Wohnung 6 |
| Z9 | Wohnung 7 |

### Weitere Mieter
| Zähler | Zuordnung | Details |
|---|---|---|
| Z10 | Garage 1 | inkl. Licht, Steckdose und ggf. Wallbox |
| Z11 | Garage 2 | inkl. Licht, Steckdose und ggf. Wallbox |
| Z12 | Stellplätze Hausseite | 1 Leerplatz Vorbereitung Wallbox (Reserve) |
| Z13 | Hobbyraum | zur Vermietung |

**Hinweis Garagen / Stellplätze:** Wallboxen werden hinter dem jeweiligen Zähler angeschlossen. Bei Bedarf kann jede Wallbox zusätzlich einen MID-Unterzähler erhalten, falls der Verbrauch separat abgerechnet werden soll.

## Eigentümer – 2 Zähler

| Zähler | Zuordnung | Details |
|---|---|---|
| Z14 | Wärmepumpe (Heizung/Warmwasser) | inkl. Umwälzpumpen, Regelung, WW-Bereitung |
| Z15 | Allgemeinstrom | Treppenhaus, Keller, Außenlicht, Technik, Netzwerk, Briefkastenanlage, sonstige Gemeinschaftsverbraucher |

## Schnittstellen / Kommunikation

Anbindung Smart Meter (EMS):
- Messdatenübertragung (CLS/SMGW) zu metergrid
- Steuerbefehle (z.B. WP, Speicher, Wallboxen)
- Datenbereitstellung für Abrechnung & Monitoring

### metergrid / Messstellenbetreiber
- Bereitstellung & Betrieb der Messinfrastruktur (SMGW)
- Messdatenverarbeitung
- Abrechnung Mieterstrommodell
- Marktkommunikation

### Netzbetreiber
- Netzanschluss
- Z1 – Summenzähler (Bezug / Einspeisung)
- Einspeisung PV

## Wichtige Hinweise

- Alle Zähler sind MID / eichrechtskonform auszuführen.
- Unterverteilungen je Einheit mit entsprechendem Überspannungsschutz und RCD.
- Für zukünftige Wallboxen und Leerrohre, Lastmanagement und Reserveplatz in Unterverteilung vorzusehen.
- Messkonzept entspricht Anforderungen für Mieterstrommodell / GGV.
- Smart Meter (EMS) ist zentrale Instanz für Messung, Steuerung und Optimierung.

## Zählerübersicht (Gesamtliste)

### Zentrale Zähler
| Zähler | Bezeichnung |
|---|---|
| Z1 | Summenzähler Netz |
| Z2 | PV-Erzeugungszähler |

### Mieterzähler (11)
| Zähler | Bezeichnung |
|---|---|
| Z3–Z9 | Wohnungen 1–7 |
| Z10 | Garage 1 |
| Z11 | Garage 2 |
| Z12 | Stellplätze Hausseite (Reserve Wallbox) |
| Z13 | Hobbyraum |

### Eigentümerzähler (2)
| Zähler | Bezeichnung |
|---|---|
| Z14 | Wärmepumpe |
| Z15 | Allgemeinstrom |

## Zusammenfassung Messpunkte

| Kategorie | Anzahl |
|---|---|
| Summenzähler Netz (Z1) | 1 |
| PV-Erzeugungszähler (Z2) | 1 |
| Mieterzähler | 11 |
| Eigentümerzähler | 2 |
| **Gesamt** | **15** |

> Hinweis: Z2 (PV-Erzeugungszähler) ist in der Zähler-Übersichtstabelle und Zusammenfassung des Originals aufgeführt, im gezeichneten Hauptflussdiagramm jedoch nicht als separat beschrifteter Block sichtbar (vermutlich im/am Smart Meter integriert erfasst).

---
*Automatisch aus `260822_Messstellenschema_Entwurf.png` transkribiert. Quelle: Originalbild im selben Ordner.*
