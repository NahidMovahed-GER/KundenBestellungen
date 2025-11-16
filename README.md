
# Kundenbestellungen – Relationale Datenbank in Microsoft Access

### Mini-Projekt / Arbeitsprobe im Bereich Datenbankentwicklung & Reporting

Eine kompakte Beispiel-Datenbank zur Verwaltung von Kunden, Produkten und Bestellungen.  
Mit SQL-Abfragen und einem Report zur **Umsatzanalyse pro Kunde**.

---

##  Projektziele

- Daten strukturiert modellieren (**Referentielle Integrität**)
- Geschäftslogik korrekt abbilden
- Benutzerfreundliche Datenerfassung über Formulare
- Aussagekräftiges Reporting für das Management erstellen

> Entwickelt mit **Microsoft Access 2016** (kompatibel ab Version 2013)

---

##  Datenmodell

### Tabellen

| Tabelle | Inhalt |
|--------|--------|
| **Kunde** | Stammdaten der Kunden |
| **Produkt** | Produkte inkl. Preis |
| **Bestellung** | Menge & Bestelldatum je Kunde/Produkt |

### Beziehungen

- Kunde → Bestellung: **1 : n**
- Produkt → Bestellung: **1 : n**
- **Referentielle Integrität aktiviert**  
  (keine verwaisten Datensätze möglich)

📎 Beziehungsdiagramm:  
➡️ `docs/relationships.png`

---

##  Abfragen (Queries)

| Name | Funktion |
|------|----------|
| `Abf_BestellungenMitDetails` | Join aus Bestellung + Kunde + Produkt |
| `Abf_BestellungenProKunde` | **Parameterabfrage** nach Kundenname |
| `Abf_TopKunden` | Umsatz je Kunde, absteigend sortiert |
| *(optional)* `Abf_ProduktUmsatz` | Umsatzanalyse pro Produkt |

**Formel Umsatz je Bestellung:**  
> Menge × Produktpreis

---

##  Formulare & Reporting

✔ Formular zur Eingabe von **Kunden**  
✔ Formular zur Eingabe von **Bestellungen**  
✔ Fixer **Report „Top Kunden“**

Mit Datums-/Seitenangabe und Gesamtsumme aller Umsätze.

📎 Beispielreport:  
➡️ [docs/report_topkunden.pdf](docs/report_topkunden.pdf)

---

##  Nutzung

1. Datei **KundenBestellungen.accdb** in Microsoft Access öffnen
2. Daten über die bereitgestellten Formulare eingeben
3. Auswertungen starten:
   - `Abf_BestellungenProKunde` → Bestellungen eines bestimmten Kunden anzeigen
   - `Abf_TopKunden` → Umsatzanalyse je Kunde als Report

---

##  Umgesetzte Inhalte (Technik & Analyse)

- Relationale Datenmodellierung & Integritätssicherung
- Primär-/Fremdschlüssel + Validierung
- SQL-Joins, Parameter & Aggregationen
- Formulare zur Benutzerinteraktion
- Reporting mit Seiten- und Datumsangabe
- Strukturierte Projektdokumentation

> Zeigt Fähigkeiten Richtung **Datenbankentwicklung, Reporting & Business-Analyse**

---

##  Tools & Technologien

- Microsoft Access
- SQL (Aggregation & Parameterabfragen)
- Access Reports (Reporting-Design)
- Datenbankmodellierung

---

## Struktur

Projektverzeichnis
```
/
├─ KundenBestellungen.accdb
├─ README.md
└─ docs/
├─ relationships.png
├─ form_bestellung.png
└─ report_topkunden.pdf
```