# Prompt-Seite nach Vorlage erstellen

> Wandelt Stichpunkte oder eine Rohfassung in eine fertige Prompt-Library-Seite um, die exakt der verbindlichen Markdown-Vorlage folgt.

| | |
|---|---|
| **Kategorie** | Prompt Library, Dokumentation |
| **Getestet mit** | Dieser Seite |
| **Sprache** | Deutsch |
| **Version** | 1.0 |
| **Zuletzt getestet** | 25.10.2026 |

---

## Zweck

Der Prompt erzeugt aus meinen Angaben eine vollständige Seite für die Prompt Library. Er liest dafür die Vorlage über einen Permalink auf GitHub und hält sich an deren Struktur, sodass alle Einträge einheitlich aussehen.

**Gut geeignet für:**
- Neue Prompts schnell und einheitlich dokumentieren
- Rohfassungen oder Stichpunkte in eine saubere Seite überführen

**Weniger geeignet für:**
- Modelle ohne Internetzugriff, sofern der Inhalt der Vorlage nicht manuell eingefügt wird

---

## Prompt

Zum Kopieren auf das Kopiersymbol rechts oben im Codeblock klicken. Die Platzhalter in `{{doppelten geschweiften Klammern}}` vor dem Einsetzen ersetzen.

````text
Du bist Redakteur meiner persönlichen Prompt Library und dokumentierst neue Prompts als fertige Markdown-Seiten.

Verbindliche Vorlage:
Rufe die Vorlage unter diesem Permalink ab und lies sie vollständig:
https://github.com/pichler/PromptLibrary/blob/b39886824d90afa036d1d01bdfa9836d51a21e5f/Vorlagen/Vorlage.md
Wenn du den Link nicht öffnen kannst, sage es mir und bitte mich, den Inhalt der Vorlage einzufügen. Rekonstruiere die Struktur nicht aus dem Gedächtnis.

Aufgabe:
Erstelle aus meinen Angaben eine vollständige Prompt-Seite, die der Vorlage exakt folgt.

Meine Angaben:
- Titel bzw. Thema: {{Titel}}
- Zweck des Prompts: {{Zweck}}
- Kategorie: {{Kategorie}}
- Getestet mit: {{Modelle}}
- Datum für den Änderungsverlauf: {{TT.MM.JJJJ}}
- Rohfassung des Prompts oder Stichpunkte dazu: {{Rohfassung}}

Regeln:
1. Übernimm Überschriften, Reihenfolge, Tabellen und Trennlinien der Vorlage unverändert und ersetze nur die Platzhaltertexte.
2. Setze den Prompt in einen Codeblock (```text) und kennzeichne alle Variablen als {{Platzhalter}}.
3. Die Variablen-Tabelle enthält genau die Platzhalter, die im Prompt vorkommen, mit Bedeutung und Beispiel.
4. Erfinde keine Testergebnisse. Fülle das Beispiel nur mit Inhalten, die ich geliefert habe, oder kennzeichne es klar als Vorschlag.
5. Setze die Version auf 1.0 und trage mein Datum in den Änderungsverlauf ein.
6. Lass den Abschnitt "Direkt starten" weg, außer ich verlange ihn.
7. Wenn wichtige Angaben fehlen, stelle vor dem Schreiben gesammelt höchstens drei Rückfragen.

Ausgabe:
Gib ausschließlich die fertige Markdown-Seite in einem einzigen Codeblock mit vier Backticks aus, damit innere Codeblöcke erhalten bleiben. Schlage danach in einer Zeile einen Dateinamen vor (Kleinbuchstaben, Bindestriche, Endung .md).
````

---

## Variablen

| Platzhalter | Bedeutung | Beispiel |
|---|---|---|
| `{{Titel}}` | Titel oder Thema des neuen Prompts | LinkedIn-Post aus Stichpunkten |
| `{{Zweck}}` | Wofür der neue Prompt gedacht ist | Aus Projektnotizen einen Post für LinkedIn schreiben |
| `{{Kategorie}}` | Einordnung in der Library | LinkedIn |
| `{{Modelle}}` | Modelle, mit denen der neue Prompt getestet wurde | Claude, ChatGPT |
| `{{TT.MM.JJJJ}}` | Datum für den Änderungsverlauf | 25.10.2026 |
| `{{Rohfassung}}` | Entwurf oder Stichpunkte zum neuen Prompt | Rolle, Aufgabe, Tonalität und Länge in Stichpunkten |

---

## Beispiel

**Eingabe (Vorschlag, nicht getestet):**

```text
- Titel bzw. Thema: LinkedIn-Post aus Stichpunkten
- Zweck des Prompts: Aus Projektnotizen einen sachlichen, persönlichen Post schreiben
- Kategorie: LinkedIn
- Getestet mit: Claude
- Datum für den Änderungsverlauf: 25.10.2026
- Rohfassung des Prompts oder Stichpunkte dazu: Rolle Texter, Zielgruppe Fachleute, maximal 1.200 Zeichen, Fließtext
```

**Ergebnis (Auszug):**

> Noch kein Ergebnis dokumentiert. Nach dem ersten Test hier einen kurzen Auszug ergänzen.

---

## Tipps und Varianten

- **Tipp:** Kann das Modell den Link nicht öffnen, den Inhalt der Vorlage direkt unter den Link einfügen.
- **Variante A:** Statt des Permalinks den Raw-Link verwenden (`.../raw/<Commit>/Vorlagen/Vorlage.md`). Er liefert reinen Text ohne GitHub-Oberfläche und funktioniert bei manchen Modellen besser.
- **Variante B:** In den Angaben "Direkt starten" verlangen, wenn die Seite Links zum Öffnen im Modell enthalten soll.
- **Hinweis:** Ändert sich die Vorlage, den Permalink im Prompt auf den neuen Commit aktualisieren und die Version erhöhen.

---

## Änderungsverlauf

| Version | Datum | Änderung |
|---|---|---|
| 1.0 | 25.10.2026 | Erste Version |
