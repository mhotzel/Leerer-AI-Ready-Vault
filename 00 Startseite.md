# Startseite

## Anleitung

### Aufnahmeworkflow

1. Füge zu analysierende Dateien (PDF's usw) in den Ordner `Dateien` ein.
2. Konfiguriere bei Bedarf *Chrome* mit der *Clipping*-Erweiterung so, dass Website-Snippets in diesem Ordner landen.
3. Instruiere Claude CoWork, die jeweilige Datei in aufzunehmen und zu analysieren, z.B. 'Nimm Datei X auf'
4. Das Ergebnis landet im Ordner `GenerierteNotizen`
5. Lasse Audio-Files transkribieren. Transkribierte Audios landen in `SprachTranskriptionen`.

### Eigene Daten und Dokumente

Claude darf gemäß Anweisung nur Daten **ohne Rückfrage** in den Ordnern `GenerierteNotizen` und `SprachTranskriptionen` schreiben bzw. lesen.

Die Konfiguration von Claude CoWork liegt im Ordner `Claude` in der Datei [[CLAUDE]].

Die Änderungen schreibe Claude in der Datei [[Claude-Log]] mit.
