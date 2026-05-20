#claude

---

# Session-Anweisungen für Claude

## Benutzer
- Der Benutzer ist Matthias Hotzel. Wiki-Links der Form `[[Matthias Hotzel]]` beziehen sich auf den Benutzer selbst.

## Datenquellen
- Daten zuerst aus dem Vault nutzen, dann auf das Internet zugreifen.
- Bei der Analyse von Dokumenten keine Annahmen treffen, die nicht durch Informationen in den zugrundeliegenden Dokumenten abgedeckt sind – stattdessen immer die Quelldaten verwenden.
- Bei unklaren Anfragen beim Benutzer nachfragen.

## Logging
Alle von Claude vorgenommenen Änderungen in der Log-Datei `/Claude/Claude-Log.md` ([[Claude-Log]]) dokumentieren. Format:

`## (YYYY-MM-DD) <Aktion> | <Titel>`

- `<Aktion>`: z. B. `Erstellt`, `Bearbeitet`, `Gelöscht`, `Zusammengefasst`
- `<Titel>`: Dateiname oder Thema des betroffenen Dokuments

Beispiel: `## (2026-04-02) Erstellt | Zusammenfassung Meeting XY`

## Dateiablage
- **Rohdaten**
	- Rohdaten liegen in den Ordnern `/Dateien` und `Clippings`. Diese Dateien nur lesen, nicht verändern.
- **Erzeugter Code**:
	- Erzeugten Code im Vault-Ordner `/Code` ablegen.
- **Generierte Seiten**:
	- Durch Claude generierte Dokumente im Vault-Ordner `/GenerierteNotizen` ablegen.
	- In der Datei `/GenerierteNotizen/index.md` einen Eintrag für jede neu erstellte Datei anlegen (Format: Wiki-Link).
- **Vorlagen**: Für neue Notizen die Vorlagen aus dem Ordner `/Vorlagen` benutzen.
	- Template-Platzhalter `{{title}}` durch den Dateinamen der erzeugten Datei ersetzen.
	- Template-Platzhalter `{{date:YYYY-MM-DD}}` durch das aktuelle Datum ersetzen (`YYYY` = Jahr vierstellig, `MM` = Monat zweistellig, `DD` = Tag zweistellig).
	- Template-Platzhalter `{{time}}` durch die aktuelle Uhrzeit im Format `HH:mm` ersetzen.
- **Verarbeitung von Transkriptionen**
	- Ich nehme Sprachnachrichten auf und lasse sie in Text umwandeln. Diese lege ich als Datei im Ordner `/SprachTranskriptionen` ab. 
	- Wenn ich dich um die Erstellung von Notizen bzw. die Zusammenfassung von Transkriptionen bitte, nutze bitte als Quelle die in diesem Ordner abgelegten Dateien.
- **Claude-Konfiguration**: Konfigurationsdateien und Prompts liegen im Ordner `/Claude` (außer der Log-Datei). Die Datei `CLAUDE.md` zu Beginn jeder Session einlesen.

## Markdown-Dokumente
- Von Claude erstellte Markdown-Dokumente immer mit dem Hashtag #claude am Anfang des jeweiligen Dokuments versehen.

## Aufnahmeworkflow
- Wenn der Benutzer eine neue Quelle in die Ordner `/Dateien` oder `Clippings` hinzufügt und dich bittet, diese aufzunehmen:
	- Lies das vollständige Dokument.
	- Übersetze es ins Deutsche, wenn die Quelle in einer anderen Sprache ist, ohne den Inhalt zu verändern.
	- Bespreche die wichtigsten Erkenntnisse mit dem Benutzer, bevor du etwas schreibst.
	- Erstelle eine Zusammenfassungsseite im Ordner `/GenerierteNotizen` benannt nach der Quelle mit einem Dateinamen nach dem Schema 'yyyy-MM-dd Thema'. Nutze dazu die Vorlage 'Mediennotiz'. 
	- Erstelle oder aktualisiere Konzeptseiten für jede wichtige Idee oder Entität basierend auf der Vorlage 'Idee'. Lege diese auch im Order 'GenerierteNotizen' ab.
	- Füge Wiki-Links hinzu, die von der Konzeptseite auf die Zusammenfassungsseite verweisen und umgekehrt.
	- Schreibe das Log
