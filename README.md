# Analyse der CO₂-Emissionen in Deutschland (1990–2024)

## Ziel
Ziel dieses Projekts ist die Analyse der langfristigen Entwicklung der CO₂-Emissionen in Deutschland sowie der Beitrag einzelner Wirtschaftssektoren.  
Der Fokus liegt auf der Beantwortung zentraler Leitfragen zur Emissionsentwicklung, sektoralen Unterschieden und strukturellen Veränderungen.

---

## Datenquelle
Die Analyse basiert auf öffentlich zugänglichen Emissionsdaten des **Umweltbundesamtes (UBA)**.

- Datensatz: *Emissionsübersichten nach Sektoren gemäß Bundes-Klimaschutzgesetz (KSG)*
- Zeitraum: **1990–2024**
- Format: Excel (Originaldaten), CSV (aufbereitet)

---

## Methodik

1. **Datenaufbereitung**
   - Import der Rohdaten aus einer Excel-Datei
   - Entfernung von Meta- und Summenspalten
   - Umwandlung der Jahreswerte in ein Long-Format (`pandas.melt`)
   - Export der bereinigten Daten als CSV

2. **Datenmodellierung**
   - Trennung von Gesamtwerten (mit und ohne LULUCF)
   - Fokus auf aggregierte Hauptsektoren gemäß KSG
   - Ausschluss von detaillierten CRF-Unterkategorien zur besseren Vergleichbarkeit

3. **Analyse & Visualisierung**
   - Zeitreihenanalyse der nationalen CO₂-Emissionen (ohne LULUCF)
   - Vergleich der Emissionen nach Hauptsektoren
   - Identifikation langfristiger Trends und möglicher Trendbrüche

---

## Zentrale Fragestellungen

- Wie haben sich die CO₂-Emissionen in Deutschland seit 1990 entwickelt?
- Welche Wirtschaftssektoren sind die größten Emittenten?
- Lassen sich Trendbrüche (z. B. Pandemie, Energiekrise) erkennen?
- Welche Sektoren zeigen deutliche Fortschritte bei der Emissionsreduktion?

---

## Ergebnisse (Kurzfassung)

- Die CO₂-Emissionen in Deutschland sind seit 1990 insgesamt deutlich gesunken.
- Besonders starke Reduktionen sind ab den späten 2010er-Jahren sichtbar.
- Die **Energiewirtschaft** ist der größte Emittent, zeigt jedoch zugleich die stärksten absoluten Emissionsrückgänge.
- Der **Verkehrssektor** weist über Jahrzehnte hinweg kaum strukturelle Reduktionen auf.
- Im Jahr **2020** ist ein deutlicher Emissionsrückgang im Zusammenhang mit der COVID-19-Pandemie erkennbar.
- Weitere Rückgänge ab **2022** stehen im Kontext der Energiekrise und des veränderten Energiemixes.

---

## Fazit

Die Analyse zeigt, dass strukturelle Veränderungen – insbesondere in der Energiewirtschaft – einen erheblichen Einfluss auf die nationale Emissionsentwicklung haben.  
Während in einzelnen Sektoren deutliche Fortschritte erzielt wurden, bestehen insbesondere im Verkehrssektor weiterhin erhebliche Herausforderungen.

---

## Projektstruktur

```
co2-analyse-deutschland/
│
├── daten/
│   ├── original/
│   │   └── Emissionsübersichten_KSG-Sektoren_1990–2024.xlsx
│   └── aufbereitet/
│       └── co2_emissionen_deutschland.csv
│
├── notebooks/
│   ├── 01_datenaufbereitung.ipynb
│   └── 02_analyse_und_visualisierung.ipynb
│
├── visualisierungen/
|   ├── co2_emissionen_hauptsektoren
│   └── co2_trend_deutschland.png
│
└── README.md
```

---

## Hinweise
Dieses Projekt dient als Demonstration grundlegender Data-Analysis-Kompetenzen, einschließlich Datenaufbereitung, explorativer Analyse und verständlicher Ergebnisdarstellung.
