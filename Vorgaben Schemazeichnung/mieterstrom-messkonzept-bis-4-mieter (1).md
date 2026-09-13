# Mieterstrom-Messkonzept bis 4 Mieter

Direktmessung bis 50A / 44A Dauerleistung.

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
| Zwei-Richtungs-Zähler (eHZ / Dreipunkt) | grün |
| Netzbetreiber / VNB | grau |

## Anlagenübersicht

Kundenanlage: **alte Küferei, Blumberg**

## Energiefluss (Hauptpfad)

1. Öffentliches Stromnetz (VNB)
2. Netzanschluss 400V AC
3. Hausanschlusskasten (HAK)
4. Eigentumsgrenze
5. **Z1 – Hauptzähler** (Zwei-Richtungs-Zähler), Direktmessend eHZ oder Dreipunkt (max. 50A / 44A) — AC-Einspeisung zurück zum HAK
6. Hauptleitungsverteiler / Sammelschiene (max. 50A Belastung)

## PV-System & Batterie

- PV-Generator: 11 kWp
- Hybrid-Wechselrichter: Solis / Deye
- DC 48V ↔ Batteriespeicher: Deye SE-G5.1 Pro
- Energiemanagementsystem (EMS) — Steuerung via SG Ready / Modbus, inkl. Lademodul-Anbindung

## Zählerschrank: Mieterstrom-Kaskade / Direktmessung

| Zähler | Mieter | Wohnung |
|---|---|---|
| Z2 | Mieter 1 | Wohnung 1 (Mieter 1) |
| Z3 | Mieter 2 | Wohnung 2 (Mieter 2) |
| Z4 | Mieter 3 | Wohnung 3 (Mieter 3) |
| Z5 | Mieter 4 | Wohnung 4 (Mieter 4) |

## Allgemeinstrom & Ladeinfrastruktur

- **Z_Allg – Allgemeinstrom** (Zwei-Richtungs-Zähler) → Allgemeinstrom (Flurlicht, Keller, etc.)
- Z_Allg → Heizung/WP → Wärmepumpe sVe (IDM AERO ALM 8-18)
- Jede Wallbox erhält einen eigenen, fortlaufend nummerierten Zähler (kein Sammelzähler) – z. B. Z_LIS1, Z_LIS2, … je nach Anzahl Wallboxen

---
*Automatisch aus `mieterstrom-messkonzept-bis-4-mieter (1).png` transkribiert. Quelle: Originalbild im selben Ordner.*
