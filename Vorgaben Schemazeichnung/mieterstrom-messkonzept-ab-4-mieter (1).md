# Mieterstrom-Messkonzept ab 4 Mieter

Beispiel: 7 Wohnungen – alte Küferei. Zentraler Wandlerschrank für Leistungen > 50A / 30kVA.

## Grundprinzip Zählkonzept

- Ein Zähler an der Übergabe zum Netzbetreiber (Z1).
- Ein Zähler an **jedem Erzeuger** (z. B. PV/Speicher).
- Ein Zähler an **jedem Verbraucher** – jede Wohnung und **jede Wallbox einzeln** (kein Sammelzähler).
- Alle Zähler erhalten eine fortlaufende Nummer (Z1, Z2, Z3, …).
- Bilanzpflicht: Summe aller Zählerwerte (Bezug/Erzeugung als Plus, Verbrauch als Minus) muss am Ende **0** ergeben.

## Legende / Farbkodierung

| Kategorie | Farbe |
|---|---|
| Ladeinfrastruktur (LIS) / sVe | rot |
| Mieter / Verbraucher | blau |
| PV-Erzeugung & Speicher | orange |
| Zwei-Richtungs-Zähler (eHZ direktmessend) | grün |
| Zentraler Wandlerschrank (Messung > 50A / 30kVA) | gold/gelb |
| Netzbetreiber / VNB | grau |

## Anlagenübersicht

Kundenanlage: **alte Küferei, Blumberg – 7 Wohnungen**

## Energiefluss (Hauptpfad)

1. Öffentliches Stromnetz (VNB)
2. Netzanschluss 400V AC
3. Hausanschlusskasten (HAK)
4. Eigentumsgrenze
5. **Zentraler Wandlerschrank** (Messung > 50A / 30kVA): **Z1 – Wandlerzähler** (Zwei-Richtungs-Messung), Stromwandler (CT) + Sicherungen, Schnittstelle zu VNB — AC-Einspeisung zurück zum HAK
6. Hauptverteilung / Sammelschiene, Kupferschienen (unbegrenzt > 50A)

## PV-System & Batterie (Großbelegung)

- PV-Generator: ca. 23 kWp
- Hybrid-Wechselrichter: Solis / Deye 15K
- DC 48V ↔ Batteriespeicher: Deye SE-G5.1 Pro (x2)
- Energiemanagementsystem (EMS) — Steuerung via SG Ready / Modbus, inkl. Lademodul-Anbindung

## Zählerschrank: Mieterstrom-Kaskade (eHZ direktmessend)

| Zähler | Mieter | Wohnung |
|---|---|---|
| Z2 | Mieter 1 | Wohnung 1 |
| Z3 | Mieter 2 | Wohnung 2 |
| Z4 | Mieter 3 | Wohnung 3 |
| Z5 | Mieter 4 | Wohnung 4 |
| Z6 | Mieter 5 | Wohnung 5 |
| Z7 | Mieter 6 | Wohnung 6 |
| Z8 | Mieter 7 | Wohnung 7 |

## Allgemeinstrom & Ladeinfrastruktur

- **Z_Allg – Allgemeinstrom** (Zwei-Richtungs-Zähler eHZ) → Allgemeinstrom (Flurlicht, Aufzug, etc.)
- Z_Allg → Heizung/WP → Wärmepumpe sVe (IDM AERO ALM 8-18)
- Jede Wallbox erhält einen eigenen, fortlaufend nummerierten Zähler (kein Sammelzähler) – z. B. Z_LIS1, Z_LIS2, … je nach Anzahl Wallboxen

---
*Automatisch aus `mieterstrom-messkonzept-ab-4-mieter (1).png` transkribiert. Quelle: Originalbild im selben Ordner.*
