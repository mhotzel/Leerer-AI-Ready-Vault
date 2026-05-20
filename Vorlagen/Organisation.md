# {{title}}

Datum:: {{date:YYYY-MM-DD}}
Uhrzeit:: {{time}}

Tags: #Organisation #Geschäftspartner

---

# Kontaktdaten

- Anschrift:: 
- Webseite:: 
- E-Mail:: 
# Kerndaten

- Link zu neuem Dokument pro Jahr

# Kerngeschäft

# Ansprechpartner / Kontakte


# Protokolle / Meetings

```dataview
TABLE WITHOUT ID datum AS Datum, file.link AS File
FROM #Protokoll and -"Vorlagen" AND [[{{title}}]]
SORT datum ASC
```
# Baustellen / Pain Points

# Projekte

- Jahr / Thema
- 
```dataview
LIST
FROM [[{{title}}]] AND #Projekt AND -"Vorlagen"
```
