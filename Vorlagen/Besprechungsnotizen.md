# {{title}}

- Datum:: {{date:YYYY-MM-DD}}
- Uhrzeit:: {{time}}
- Kunde:: 
- Projekt:: 

Tags: #Meeting #Protokoll

---
# Teilnehmer


# Agenda


# Ergebnis


# Aufgaben

```dataview
TABLE WITHOUT ID Enddatum, file.link AS File
FROM #Task and -"Vorlagen" AND [[{{title}}]]
SORT Enddatum ASC
```

