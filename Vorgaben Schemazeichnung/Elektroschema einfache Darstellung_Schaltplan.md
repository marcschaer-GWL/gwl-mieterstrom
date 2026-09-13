# Elektroschema – einfache Darstellung (Schaltplan)

## Projektinformationen (Titelblock)

| Feld | Wert |
|---|---|
| Unternehmen | GWL Design |
| Projektname | Pütz |
| Erstellt von | Marc Schaer |
| Projektadresse | Hermann-Reebstein-Straße 4, 78234 Engen |
| Systeminformation | Nennleistung DC/AC: 19,32 kWp / 30,0 kW; Netzanschluss: Dreiphasig |
| Referenz | gwl-51 |
| Dokumenttyp | Schaltplan |
| Ausgabedatum | 24.08.2026 |
| Blatt | 1/1 |

## Legende

| Symbol | Bedeutung |
|---|---|
| m × n Module (Rechteck mit Pfeil) | m Strings mit n Modulen |
| Rechteck mit Pfeil (Variante) | (weiterer String-Typ) |
| Dreieck-Symbol "B ~3∼" | Wechselrichter: Deye – SUN-15K-SG05LP3-EU-SM2, 15KW |
| Batterie-Symbol | Batterie: Deye – SE-G5.1 Pro |
| Blaues Rechteck | Hausanschluss |
| Pfeil | Netzanschluss |
| Kreis mit X | Verbrauch |
| Kreis mit Symbol | Wärmepumpe |
| Rechteck "Energiemanagement" | PLEXLOG – PL Commercial (PL100) |
| kWh-Symbol (bidirektionaler Pfeil) | Energiezähler (Zwei-Richtungs) |
| kWh-Symbol (unidirektionaler Pfeil) | Energiezähler (einseitig) |

## Anlagenstruktur

### PV-Strings & Batterie – Gruppe 1
- String "1 × 1" und String "1 × 1" → Wechselrichter Nr. 1 (B ~3∼)
- Batterie (4×-Symbol) → Wechselrichter Nr. 1

### PV-Strings – Gruppe 2
- String "3 × 2" und String "3 × 3" → Wechselrichter Nr. 2 (B ~3∼)

### Hauptstrang (nach den Wechselrichtern)

1. Beide Wechselrichter → **Energiezähler (bidirektional, kWh)**
2. → **Übergabe EMS** (Energiezähler, kWh)
3. → **Messstellenbetreiber** (Energiezähler, kWh)
4. → **HAK** (Hausanschlusskasten, min. 80A)
5. → Netzanschluss

### Abzweige ab dem ersten Energiezähler (nach den Wechselrichtern)

- **Allgemeinstrom**: Energiezähler (kWh) → Energiemanagement (PLEXLOG PL100)
- **Wärmepumpe**: Energiezähler (kWh) → Wärmepumpe
- **Mieter**: Energiezähler (kWh) → Verbrauch XXX kWh

---
*Automatisch aus `Elektroschema einfache Darstellung_Schaltplan.pdf` transkribiert (PDF ohne Textebene → als Bild gerendert und ausgewertet).*
