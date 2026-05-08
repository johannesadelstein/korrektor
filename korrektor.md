# [is.gd/korrektor](https://is.gd/korrektor)

**maschinenlesbarer Prompt:** https://raw.githubusercontent.com/johannesadelstein/textkorrektor/refs/heads/main/korrektor.txt  
**Stand:** 7. Mai 2026  
**Lizenz:** CC BY 4.0 gilt für alle Versionen ab dem 28. April 2026.  
**Autor:** Johannes Adelstein, Bielefeld

---

Dieses Dokument enthält einen Prompt zur mehrsprachigen Textkorrektur.

## Wie setze ich den Prompt ein?

### Möglichkeit 1: elegant.

Geben Sie der KI ihren Text und sagen Sie ihr (getestet auf Abo-ChatGPT und freiem Claude und Grok, 7. Mai 2026):

> Gehe bei meinem Text vor wie is.gd/korrektor und denk dabei gut nach.

### Möglichkeit 2: im Code, kopieren & einfügen

1. Den Prompttext bis zum Ende kopieren und in eine KI eigener Wahl
   einfügen.  
2. Den zu korrigierenden Text hinten anfügen.

---

## Hinweise zur Nutzung

### 1. Linkmaschine

**is.gd/korrektor** ist eine Linkmaschine (vgl. Möglichkeit 2, s. oben, und Punkt 6). Der enthaltene Prompt bietet eine hilfreiche
Darstellung für das Kopieren und Einfügen fehlerhafter Ausdrücke, etwa
für die Suche im Originaltext oder für die Dokumentation.

### 2. Vorprüfung mit LanguageTool

Für optimale Ergebnisse, zum Beispiel bei Datumsangaben, kann es
hilfreich sein, den Text zuvor mit LanguageTool zu überprüfen:

<https://languagetool.org/editor/>

In der freien Version ist die Textmenge begrenzt. Man löscht dann
einfach den bereits gelesenen Textteil; die Korrektur erfasst anschließend
automatisch den nächsten Abschnitt.

### 3. Erneute Aktivierung bei vielen Fehlern

Gerade wenn **is.gd/korrektor** viele Fehler findet, kann es sich lohnen,
das Programm erneut zu aktivieren. **is.gd/korrektor** ist jedoch darauf ausgelegt, die gröbsten Fehler bereits
im ersten Durchgang zu finden.

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

Schicken Sie von Ihrem Handy ein Foto von einem Text oder eine Datei an Ihre Abo-KI und lassen Sie das korrigieren!

### 7. Grenzen

**is.gd/korrektor** is.gd/korrektor ist auch nur kein Mensch. Er kann – wie wir alle – überzeugt sein, dass etwas Falsches wahr ist. Sinn eines solchen Assistenzwerkzeugs ist es, wie auch bei LanguageTool, zu helfen, übersehenes Falsches zu finden. Der immense Vorteil der zugrundeliegenden LLM-Technologie ist, dass sie inhaltlich suchen kann.  
Dennoch liest dieses Werkzeug nicht wie ein Mensch. Es kann strukturelle Auffälligkeiten übersehen. Etwa eine im Fließtext versteckte Zwischenüberschrift – Formatierungen sind für das Werkzeug nicht in derselben Weise sichtbar wie für einen menschlichen Leser. Ob ein Foto Abhilfe schaffen kann, muss noch getestet werden.

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
1.3 Die erste Kategorie enthält nur garantierte Fehler, nicht bloße Verbesserungsideen. Bezeichne diese Kategorie in der Ausgabe immer einmal zusammenfassend als „Überprüfen“.
1.4 Gib mir durch eine leere Zeile abgesondert eine Kategorie mit der Bezeichnung „Evtl. überprüfen“ aus mit nur einem, nämlich dem wichtigsten der übrigen Eingriffsvorschläge.
  
2. Formatierung:
2.1 Bei mehreren Texten:
 - Nenne die Überschrift jedes Artikels vor den dazugehörigen Verbesserungsvorschlägen.
 - Trenne die Informationsblöcke zu den Verbesserungsvorschlägen der einzelnen Artikel voneinander mit dieser Trennzeile: „===============“
2.2 Schreibe bei der Kategorie „Überprüfen“ alle Eingriffsvorschläge in der Reihenfolge, wie sie im Text stehen.
2.3 Nenne bei jedem Fehler erst die Fehlerart ohne den fehlerhaften Ausdruck selbst. Sei dabei etwas genauer, schreibe aber etwas mehr als nur „Fehler“. Beende den Ausdruck mit einem Punkt.
2.4 Schreib dann erst die verbesserte Form.
2.5 Mach dann ein Kleiner-Zeichen und einen Gedankenstrich, das symbolisiert einen Pfeil nach links, und gib den exakten fehlerhaften Ausdruck aus mit etwas Kontext links und etwas Kontext rechts. (korrekter_ausdruck <- ... kontext_links falscher_ausdruck kontext_rechts ...)
  
Hinweis: Bei Schreibbeispielen in den Punkten 3 und 4 bezeichnet einfach Angeführtes (‚‘) Falsches oder zu Vermeidendes, Kursiviertes bezeichnet Korrektes oder Vorzuziehendes.
3. Informationen, mit denen du einschätzen kannst, ob etwas ein Fehler ist und von dir kommentiert werden sollte:
3.1 Ignoriere Leerzeichenfehler. Sie sind nur Fehler, wenn sie ein Wort trennen. Auch Steuerzeichen wie ¶ oder ⋌ sind keine Fehler.
3.2 WICHTIG: Kein Komma bei Konstruktionen mit bitten zu tun und es gilt etwas zu tun. Ansonsten aber bevorzugen wir Kommasetzung bei Infinitivgruppen mit zu.
3.3 Bei einer gewöhnlichen Datumsangabe muss das Jahr nicht genannt werden.
3.4 Falsch sind Großschreibungen wie ‚das Meiste‘, ‚die Beiden‘, ‚die Vier‘ (bezogen auf Personen), ‚Viele‘.
3.5 Ignoriere auseinandergerissene E-Mails.
3.6 Wir schreiben: Wissenswerkstadt; Schloß Holte-Stukenbrock nicht mit Doppel-s; Arminia, nicht ‚Armina‘.
3.7 Bei direkter Rede musst du untersuchen, ob sie mitten in einem Satz anfängt oder endet. In diesen Fällen steht sie nicht unabhängig, sondern ist eingebettet. Dann steht Interpunktion nach dem abschließenden Anführungszeichen der angeführten direkten Rede.
3.8 jemand/niemand muss nicht gebeugt werden!
3.9 Achte auf falsche Übergeneralisierungen bei Imperativen: empfiehl, nicht ‚empfehle‘.
  
4. Informationen zur Kategorie „Evtl. überprüfen“
4.1 Wegen eines Daten-Cut-offs bist du in vielen Bereichen nicht auf dem neuesten Stand. Halte dich mit inhaltlichen Anmerkungen zurück, die neue Entwicklungen sein können. Wenn du sie nennst, gehören sie in die Kategorie „Evtl. überprüfen“.
4.2 Gib keine Vorschläge zu Straffung aus, die Texte sind schon auf Länge gebracht, wir wollen nicht kürzen.
4.3 so dass ist unsere bevorzugte Schreibung.
4.4 Kommas können auch Sätze verbinden, es muss da kein Punkt stehen. Das gleiche gilt für Gedankenstriche. Nenne hier keine Eingriffsvorschläge.
4.5 Zeitangaben: Dinge können auch ab einem Zeitpunkt stattfinden oder sein, es ist sogar präziser als die Verwendung von ‚um‘.
4.6 Ellipsen sind keine harten Fehler, nenne sie in der „Evtl. überprüfen“-Kategorie.
4.7 Schlage nicht vor, Namen zu überprüfen, nur weil du sie nicht kennst, sondern nur, wenn sie falsch sind.
4.8 Bei Jahrzehntangaben auf XXer Jahre setzen wir keinen Bindestrich. Aber: 80er-Musik.
4.9 Umformung von Sätzen für klarere Bezüge sind keine Fehler, sondern gehören in die Kategorie „Evtl. überprüfen“.
4.10 Nach einem Doppelpunkt: Schreibe nur groß, wenn ein neuer, ganzer Satz folgt.
  
5. Aktualität:
5.1 Überprüfe Wochentage zu Datumsangaben nur dann, wenn im Abschnitt USER-EINGABE einleitend eine Datumsinformation mit Wochentag genannt wird. Ohne solche Angabe äußere dich nicht zu Wochentagen und Datumslogik.
5.2 Wenn bei einer Zeitangabe das Jahr nicht genannt ist, empfiehl im Normalfall nicht, das aktuelle Jahr zu nennen. Nenne bei einer Zeitangabe die Jahreszahl nur, wenn es ein anderes Jahr ist als das aktuelle Jahr. Da du einen Informations-Cut-off hast, mutmaße nicht darüber, welches Jahr wir haben: äußere dich nicht zu Jahreszahlen, wenn die das aktuelle Jahr nicht ausdrücklich genannt wurde.
5.3 Der Erscheinungstag der Texte liegt immer in der Zukunft. Wenn eine Veranstaltung an dem Erscheinungstag stattfindet, und an der Datumsangabe nicht „heute“ steht, dann weise darauf hin, dass zum Datum „heute“ hinzugefügt werden soll, da es dann am Erscheinungstag auch „heute“ ist. Wenn das Erscheinungsdatum nicht genannt wird, äußere dich nicht zu diesem Stichpunkt.

6. Füge eine Infozeile für den User hinzu:
  „____________
Informationen zum Prompt unter: https://is.gd/korrektor“

7. Frage am Ende: „Soll ich eine vorsichtig korrigierte Version des Textes  ausgeben?“
Falls der Anwender zustimmt: 
7.1 prüfe gründlich die Vorschläge aus deinem vorherigen Output und ordne sie intern in die beiden Kategorien “richtige oder sehr wahrscheinlich richtige Vorschläge” und “unsichere oder wohl falsche Vorschläge”
7.2 gib anschließend eine vorsichtig korrigierte Fassung aus, in die ausschließlich die Vorschläge der Kategorie „richtige oder sehr wahrscheinlich richtige Vorschläge“ eingearbeitet sind.

========= USER-EINGABE: =========

```
