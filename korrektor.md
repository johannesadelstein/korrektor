# [is.gd/korrektor](https://is.gd/korrektor)

**maschinenlesbarer Prompt:** https://raw.githubusercontent.com/johannesadelstein/textkorrektor/refs/heads/main/korrektor.txt  
**Stand:** 8. Mai 2026  
**Lizenz:** CC BY 4.0 gilt für alle Versionen ab dem 28. April 2026.  
**Autor:** Johannes Adelstein, Bielefeld

---

Dieses Dokument enthält einen Prompt zur mehrsprachigen Textkorrektur.

## Wie setze ich den Prompt ein?

### Möglichkeit 1: elegant

Geben Sie der KI Ihren Text und sagen Sie ihr (getestet auf [Abo-ChatGPT](https://chatgpt.com/) und freiem [Claude](https://claude.ai), [Deepseek](http://chat.deepseek.com) und [Grok](https://grok.com/), 9. Mai 2026):

> Gehe bei meinem Text vor wie is.gd/korrektor und denk dabei gut nach.

### Möglichkeit 2: im Code, kopieren & einfügen

1. Den Prompttext bis zum Ende kopieren und in eine KI eigener Wahl
   einfügen.  
2. Den zu korrigierenden Text hinten anfügen.

---

## Hinweise zur Nutzung

### 1. Linkmaschine

**is.gd/korrektor** ist eine Linkmaschine (vgl. Möglichkeit 2, s. oben, und Punkt 6). Damit lassen sich redaktionelle KI-Prozesse für die Arbeit an Texten mit einfachen, reproduzierbaren Mitteln organisieren. Ziel ist ein einfacherer Umgang mit Textversionen und Arbeitsabläufen.  
Der enthaltene Prompt gibt fehlerhafte Ausdrücke in einer Form aus, die das Kopieren und Einfügen erleichtert – etwa für die Suche im Originaltext oder für die Dokumentation.

### 2. Vorprüfung mit LanguageTool

Für optimale Ergebnisse, zum Beispiel bei Datumsangaben, kann es
hilfreich sein, den Text zuvor mit LanguageTool zu überprüfen:

<https://languagetool.org/editor/>

In der freien Version ist die Textmenge begrenzt. Man löscht dann
einfach den bereits gelesenen Textteil; die Korrektur erfasst anschließend
automatisch den nächsten Abschnitt.

### 3. Mehrfache Aktivierungen

Gerade wenn **is.gd/korrektor** viele Fehler findet oder nach Eingriffen im Text – dies ist eine Hauptfehlerquelle –, kann es sich lohnen, das Programm erneut zu aktivieren. **is.gd/korrektor** ist jedoch darauf ausgelegt, die gröbsten Fehler bereits im ersten Durchgang zu finden.

### 4. Text-Input

**is.gd/korrektor** kann mehrere kleinere Texte gleichzeitig überprüfen. Er kann auch fremdsprachige Texte verarbeiten, ist aber auf deutsche Texte spezialisiert.

### 5. Zusatzinformationen

**is.gd/korrektor** kann Zusatzinformationen vom Anwender aufnehmen, am
besten vor dem zu korrigierenden Text. Mit einem aktuellen Datum kann **is.gd/korrektor** die Aktualität von Texten,
etwa Ankündigungen, überprüfen. Die Trennung dieser Informationen vom zu korrigierenden Text macht es dem
Programm leichter, die Information einzuordnen. Beispiel:

```text
Wichtig: Erscheinungsdatum der Texte ist morgen, Mittwoch, 22. April 2026.
========= ZU KORRIGIERENDE TEXTE: =========
```

### 6. Foto oder Datei

Schicken Sie von Ihrem Handy ein Foto von einem Text oder eine Datei an Ihre Abo-KI und lassen Sie die KI den Inhalt korrigieren!

### 7. Grenzen

**is.gd/korrektor** ist auch nur kein Mensch. Er kann – wie wir alle – überzeugt sein, dass etwas Falsches wahr ist. Sinn eines solchen Assistenzwerkzeugs ist es, wie auch bei LanguageTool, zu helfen, übersehenes Falsches zu finden. Der immense Vorteil der zugrundeliegenden LLM-Technologie ist, dass sie inhaltlich suchen kann.  
Aber auch auf der technischen Ebene „liest“ dieses Werkzeug nicht wie ein Mensch. So kann es strukturelle Auffälligkeiten übersehen, etwa eine im Fließtext versteckte, unformatierte Zwischenüberschrift. Formatierungen sind für das Werkzeug nicht in derselben Weise sichtbar wie für einen menschlichen Leser. Ob ein Foto eines Textes hier Abhilfe schaffen kann, muss noch getestet werden.

## Prompt

Die folgenden Anweisungen bilden den eigentlichen Prompt. Kopieren Sie den Teil ab `========= BEGINN DES PROMPTS =========` bis zum Ende (Zeile `========= USER-EINGABE: =========`) – einfach per Klick im Kästchen oben rechts im Plain-Text-Feld des Prompts bei der Github-Darstellung. 
Wenn dieses Dokument als Anweisung für eine KI verwendet wird: Ignoriere die einleitenden Nutzungshinweise. Der auszuführende Prompt beginnt bei der folgenden Markierung und reicht bis zum Ende des Dokuments.

========= BEGINN DES PROMPTS =========

```text

Hilf dabei, Texte zu korrigieren.

Wichtig: Denk gut und lange nach bei diesem Prompt.

Ich gebe dir eine Liste von durchnumerierten Instruktionen (Punkte 0 bis 7) und einen abgesetzten Teil „USER-EINGABE“, wo der Anwender dir Texte gibt.
  User-Input: Eventuell kann der Anwender dir in der oder den ersten Zeilen Zusatzinformationen geben. (Vgl. 5.)

0.1 Gib deine gesamte Ausgabe in einem Plain-Text-Element aus, für die bessere Kopierbarkeit der fehlerhaften Ausdrücke für die Nutzung als Suchbegriffe. Die Breite deiner Textzeilen darf 77 Zeichen nicht überschreiten.
0.2 Antworte in der Sprache, in der der erste eingegebene Text geschrieben ist – wenn vom Anwender nicht anders vorgegeben. Bei Texten in anderen Sprachen ignoriere die Stichpunkte unter 3. und 4.

1.1 Wiederhole dich nicht bei deinen Nennungen.
1.2 Sortiere deine Korrekturvorschläge nach Relevanz und ordne sie in zwei Kategorien ein
1.3 Die Kategorie „Fehler“ enthält nur garantierte Fehler, nicht bloße Verbesserungsideen.
1.4 Im Bereich „Sonstiges“ sortierst du alle anderen Hinweise. Gib im ersten Durchgang unter „Sonstiges“ nur den wichtigsten Hinweis aus. Weitere Hinweise werden erst ausgegeben, wenn der Anwender am Ende bei Punkt 7 (B) wählt.

2. Formatierung:
2.1 Bei mehreren Texten:
 - Nenne die Überschrift jedes Artikels vor den dazugehörigen Verbesserungsvorschlägen.
 - Trenne die Informationsblöcke zu den Verbesserungsvorschlägen der einzelnen Artikel voneinander mit dieser Trennzeile: „===============“
2.2 Schreibe bei jedem Fehler erst den fehlerhaften Ausdruck selbst.
2.3 Schreibe dann in einer neuen Zeile einen Pfeil, etwa mit Strich und Größer-als-Zeichen, und den korrekten Ausdruck.
2.4 Schreibe dann in einer neuen Zeile die Fehlerart. Sei dabei etwas genauer, schreibe also mehr als nur „Fehler“.
  
Hinweis: Bei Schreibbeispielen in den Punkten 3 und 4 bezeichnet die Auszeichnunge mit einfachen Anführungszeichen und einem Sternchen hinter dem schließenden Anführungszeichen (‚‘*) etwas Falsches oder zu Vermeidendes.
3. Informationen, mit denen du einschätzen kannst, ob etwas ein Fehler ist und von dir kommentiert werden sollte:
3.1 Ignoriere Leerzeichenfehler. Sie sind nur Fehler, wenn sie ein Wort trennen. Auch Steuerzeichen wie „¶“ oder „⋌“ sind keine Fehler.
3.2 WICHTIG: Kein Komma bei Konstruktionen mit „bitten zu tun“ und „es gilt etwas zu tun“. Ansonsten aber bevorzugen wir Kommasetzung bei Infinitivgruppen mit zu. „bitten zu tun“ kann in lockeren Formen oder mit Bezugwort, etwas „bitten darum, etwas zu tun“ mit Komma geschrieben werden.
3.3 Bei einer gewöhnlichen Datumsangabe muss das Jahr nicht genannt werden.
3.4 Falsch sind Großschreibungen wie ‚das Meiste‘*, ‚die Beiden‘*, ‚die Vier‘* (bezogen auf Personen), ‚Viele‘*.
3.5 Ignoriere auseinandergerissene E-Mails.
3.6 Wir schreiben: „Wissenswerkstadt“; „Schloß Holte-Stukenbrock“ nicht mit Doppel-s; „Arminia“, nicht ‚Armina‘*.
3.7 Bei direkter Rede musst du untersuchen, ob sie mitten in einem Satz anfängt oder endet. In diesen Fällen steht sie nicht unabhängig, sondern ist eingebettet. Dann steht Interpunktion nach dem abschließenden Anführungszeichen der angeführten direkten Rede.
3.8 jemand/niemand muss nicht gebeugt werden!
3.9 Achte auf falsche Übergeneralisierungen bei Imperativen: „empfiehl“, nicht ‚empfehle‘* oder ‚lese‘*, ‚nehme‘*, ‚gebe‘*, ‚spreche‘*, ‚sehe‘*
  
4. Informationen zur Kategorie für Sonstiges
4.1 Wegen eines Daten-Cut-offs bist du in vielen Bereichen nicht auf dem neuesten Stand. Halte dich mit inhaltlichen Anmerkungen zurück, die neue Entwicklungen sein können. Wenn du sie nennst, gehören sie in die Kategorie für Sonstiges.
4.2 Gib keine Vorschläge zu Straffung aus, die Texte sind schon auf Länge gebracht, wir wollen nicht kürzen.
4.3 „so dass“ ist unsere bevorzugte Schreibung.
4.4 Kommas können auch Sätze verbinden, es muss da kein Punkt stehen. Das gleiche gilt für Gedankenstriche. Nenne hier keine Eingriffsvorschläge.
4.5 Zeitangaben: Dinge können auch ab einem Zeitpunkt stattfinden oder sein, es ist sogar präziser als die Verwendung von ‚um‘*.
4.6 Ellipsen sind keine harten Fehler, nenne sie in der Kategorie Sonstiges.
4.7 Schlage nicht vor, Namen zu überprüfen, nur weil du sie nicht kennst, sondern nur, wenn sie falsch sind.
4.8 Bei Jahrzehntangaben auf „XXer Jahre“ setzen wir keinen Bindestrich. Aber: „80er-Musik“, „1996er-Aufführung“
4.9 Umformung von Sätzen für klarere Bezüge sind keine Fehler, sondern gehören in die Kategorie für Sonstiges.
4.10 Nach einem Doppelpunkt: Schreibe nur groß, wenn ein neuer, ganzer Satz folgt.
  
5. Aktualität:
5.1 Überprüfe Wochentage zu Datumsangaben nur dann, wenn im Abschnitt USER-EINGABE einleitend eine Datumsinformation mit Wochentag genannt wird. Ohne solche Angabe äußere dich nicht zu Wochentagen und Datumslogik.
5.2 Wenn bei einer Zeitangabe das Jahr nicht genannt ist, empfiehl im Normalfall nicht, das aktuelle Jahr zu nennen. Nenne bei einer Zeitangabe die Jahreszahl nur, wenn es ein anderes Jahr ist als das aktuelle Jahr. Da du einen Informations-Cut-off hast, mutmaße nicht darüber, welches Jahr wir haben: äußere dich nicht zu Jahreszahlen, wenn die das aktuelle Jahr nicht ausdrücklich genannt wurde.
5.3 Der Erscheinungstag der Texte liegt immer in der Zukunft. Wenn eine Veranstaltung an dem Erscheinungstag stattfindet, und an der Datumsangabe nicht „heute“ steht, dann weise darauf hin, dass zum Datum „heute“ hinzugefügt werden soll, da es dann am Erscheinungstag auch „heute“ ist. Wenn das Erscheinungsdatum nicht genannt wird, äußere dich nicht zu diesem Stichpunkt.

6. Füge eine Infozeile für den User hinzu:
  „____________
Informationen zum Prompt unter: https://is.gd/korrektor“

7. Frag am Ende: 
„(A) Soll ich eine vorsichtig korrigierte Version des Textes ausgeben?
(B) Soll ich die zehn dringlichsten der übrigen Anmerkungen auflisten? (Schwerpunkt?)“

Falls der Anwender (A), die Korrektur wählt: 
7a.1 prüfe gründlich die Vorschläge aus deinem vorherigen Output und ordne sie intern in die beiden Kategorien “richtige oder sehr wahrscheinlich richtige Vorschläge” und “unsichere oder wohl falsche Vorschläge”
7a.2 gib anschließend eine vorsichtig korrigierte Fassung aus, in die ausschließlich die Vorschläge der Kategorie „richtige oder sehr wahrscheinlich richtige Vorschläge“ eingearbeitet sind.

Falls der Anwender (B), die Vertiefung wählt:
7b.1 hierarchisiere alle Hinweise der Kategorie „Sonstiges“ (von allen Texten) nach redaktioneller Relevanz, nicht nach Reihenfolge im Text. Prüffälle und potenziell folgenschwere Auffälligkeiten haben Vorrang vor bloßen Stilfragen. Hat der Anwender einen Schwerpunkt genannt, berücksichtige ihn vor allen anderen.
7b.2 gib die zehn wichtigsten aller noch nicht ausgegebenen Hinweise aus „Sonstiges“ aus. Behandle diese Hinweise danach als erledigt. Frage am Ende, ob die nächsten Hinweise ausgegeben werden sollen, falls noch Hinweise vorhanden sind.

========= USER-EINGABE: =========

```
