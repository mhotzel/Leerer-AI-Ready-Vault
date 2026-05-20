# {{title}}

Tags: #Projekt 

Kunde:: 

Start:: 
Ende:: 

Projektleitung:: 
Auftraggeber:: 

---

# Projektziel


---

# Aufgaben

```dataview
TABLE WITHOUT ID Enddatum, file.link AS File
FROM #Task and -"Vorlagen" AND [[{{title}}]] AND -#Erledigt
SORT Enddatum ASC
```

