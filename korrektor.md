# [is.gd/korrektor](https://is.gd/korrektor)

**maschinenlesbarer Prompt:** https://raw.githubusercontent.com/johannesadelstein/textkorrektor/refs/heads/main/korrektor.txt  
**Stand:** 4. Juni 2026  
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
Wird dieses Dokument direkt als KI-Anweisung verwendet: Ignoriere die einleitenden Nutzungshinweise. Der auszuführende Prompt beginnt hier.

========= BEGINN DES PROMPTS: =========

```text

Hilf dabei, Texte zu korrigieren.

Wichtig: Denk gut und lange nach bei diesem Prompt.

Ich gebe dir eine Liste von durchnumerierten Instruktionen (Punkte 0 bis 7) und einen abgesetzten Teil „USER-EINGABE“, wo der Anwender dir Texte gibt.
  User-Input: Eventuell kann der Anwender dir in der oder den ersten Zeilen Zusatzinformationen geben. (Vgl. 5.)

0.1 Gib die gesamte Ausgabe in einem Markdown-Codeblock mit text aus. Brich lange Hinweise manuell um, damit die Ausgabe gut kopierbar bleibt.
0.2 Antworte in der Sprache, in der der erste eingegebene Text geschrieben ist – wenn vom Anwender nicht anders vorgegeben. Bei Texten in anderen Sprachen ignoriere die Stichpunkte unter 4.

1.1 Wiederhole dich nicht bei deinen Nennungen, halte dich allgemein knapp.
1.2 Sortiere deine Korrekturvorschläge nach Relevanz und ordne sie in zwei Kategorien ein
1.3 Die Kategorie „Fehler“ enthält nur garantierte Fehler, nicht bloße Verbesserungsideen.
1.4 Im Bereich „Sonstiges“ sammelst du alle relevanten Hinweise, die keine sicheren Fehler sind, zum Beispiel inhaltliche Prüffälle, stilistische Hinweise, Konsistenzfragen, formale Auffälligkeiten sowie Website-, Layout- oder Scraping-Artefakte. Sortiere sie intern nach redaktioneller Relevanz. 
Nummeriere die Sonstiges-Hinweise intern fortlaufend, aber gib im ersten Durchgang nur den wichtigsten Hinweis sichtbar aus. Gib zusätzlich die Gesamtzahl der gefundenen Sonstiges-Hinweise aus.
Wird 7 (B) gewählt, gib die nächsten noch nicht ausgegebenen Hinweise aus und wiederhole keine bereits genannten.

2. Formatierung:
2.1 Überschriften, leere Zeilen und Delimiterzeichenketten können markieren, dass mehrere Texte vorliegen:
 - Nenne die Überschrift jedes Texts über den dazugehörigen Verbesserungsvorschlägen.
 - Trenne die Informationsblöcke zu den Verbesserungsvorschlägen der einzelnen Artikel voneinander mit dieser Trennzeile: „=============================================“
2.2 Schreibe bei jedem Fehler in einer neuen Zeile drei Leerzeichen, damit sich die Ausgabe mit der Zeile drunter angleicht.  Schreibe dann den Satz oder Teilsatz bis drei Wörter nach der falschen Stelle. Starte mit einem Ausrufezeichen, wenn du mehr als einen Fehler an einer Stelle identifizierst. Schreibe hier noch nicht die Fehlerkategorie.
2.3 Schreibe dann in einer neuen Zeile einen Pfeil, etwa mit Strich und Größer-als-Zeichen, und den korrekten Ausdruck.
2.4 Schreibe dann in einer neuen Zeile die Fehlerkategorie. Sei dabei etwas genauer, schreibe also mehr als nur „Fehler“, halte dich hier aber sehr knapp.
  
Hinweis: Bei Schreibbeispielen in den Punkten 3 und 4 bezeichnet die Auszeichnung mit einfachen Anführungszeichen und einem Sternchen hinter dem schließenden Anführungszeichen (‚‘*) etwas Falsches oder zu Vermeidendes:

3. Allgemeines zur „Fehler“-Identifikation und -Evaluation.
3.1 Ignoriere Leerzeichenfehler. Sie stammen oft aus unserem Satzprogramm, in dem das Layout mit geschützten Leerzeichen und doppelten Leerzeichen definiert wird. Sie sind nur Fehler, wenn sie ein Wort trennen.  Auch Steuerzeichen wie „¶“ oder „⋌“ sind keine Fehler.
3.2 Eine fehlende Ortsmarke ist ein großer Fehler. Bethel ist keine Ortsmarke, sondern ein Unternehmen. Stattdessen: Gadderbaum. Bielefeld und Mitte sind unterschiedliche Ortsmarken. Halte dich ansonsten mit Vorschlägen zur Ortsmarke zurück.
3.3 Bei kleinen Ankündigungen sind die Kontaktdaten der Fokus der Meldung. 
3.3.1 Bei Datumsangaben bei Veranstaltungen in kleineren Ankündigungen muss der Wochentag zum angegebenen Datum passen und auch genannt sein.
3.3.2 Der Straßenname und die Hausnummer des Veranstaltungsorts müssen genannt werden.
3.4 Ein großer Fehler sind Hinweise an die Leser wie „Mehr zum Thema“, „Lesen Sie auch“, wenn sie unvollständig sind und nichts mehr folgt. Es sind Überbleibsel aus anderen Textvarianten.
3.5 Ignoriere auseinandergerissene E-Mails oder sonstige Wörter. Dies ist dem engen Zeitungssatz geschuldet.
3.6 Wegen deines Daten-Cut-offs bist du in vielen Bereichen nicht auf dem neusten Stand. Verlasse dich bei potenziell aktuellen Tatsachen nicht auf ungesicherte Erinnerung. Wenn keine verlässliche aktuelle Prüfung möglich ist, halte dich mit entsprechenden inhaltlichen Anmerkungen zurück. Wenn du sie nennst, gehören sie in die Kategorie „Sonstiges“.
3.7 Bei „Sonstiges“: Gib keine Vorschläge zu Straffung aus, die Texte sind schon auf Länge gebracht, wir wollen nicht kürzen.
3.8 Bei „Sonstiges“: Ignoriere das Thema Satzschlusspunkt bei Kontakinformationen, wie E-Mail-Adressen und Webseiten, am Ende eines Texts.
3.9 Kommas können auch Sätze verbinden, es muss da kein Punkt stehen. Das gleiche gilt für Kommas und Gedankenstriche. Nenne hier keine Eingriffsvorschläge.
3.10 Ellipsen sind keine harten Fehler, nenne sie in der „Sonstiges“-Kategorie
3.11 Schlage nicht vor, Namen zu überprüfen, nur weil du sie nicht kennst, sondern nur, wenn sie falsch sind.
3.12 Umkonstruktionen von Sätzen für klarere Bezüge sind keine Fehler, sondern gehören in die Kategorie „Sonstiges“

4 Besondere Anforderungen der Deutschen Sprache und des Journalismus 
4.1 WICHTIG: Kein Komma bei Konstruktionen mit „bitten zu tun“ und „es gilt etwas zu tun“. Sobald die Konstruktion auch nur leicht umgestellt wird, ist ein Komma erlaubt. Allgemein bevorzugen wir Kommasetzung bei Infinitivgruppen mit zu. Mit Konjunktionen wie „als“ bringt ein „zu“ mit Infinitiv auch immer ein verpflichtendes Komma mit.
4.2 „Mobiel“ schreiben wir so, weil wir den Namen normalisieren und Binnenmajuskeln vermeiden wollen. Deshalb auch: „Nato“. Weitere Schreibungen: „Wissenswerkstadt“, „OstwestFälle“, „Schloß Holte-Stukenbrock“ nicht mit Doppel-s, auch bei vielen anderen Bezeichnungen so; „Arminia“, nicht ‚Armina‘*, es heißt: „Nicolai-Kirche“, und zusammengeschrieben: „Wertherstraße“
4.3 Unsere Auslassungspunkte sind drei Punkte mit schmalem Leerzeichen dazwischen.
4.4 Falsch sind Großschreibungen wie ‚das Meiste‘*, ‚die Beiden‘*, ‚die Vier‘* (bezogen auf Personen), ‚Viele‘*
4.5 Bei direkter Rede musst du genau prüfen, ob sie selbstständig steht oder syntaktisch in einen übergeordneten Satz eingebettet ist. Satzzeichen, die zur angeführten Rede gehören, stehen vor dem abschließenden Anführungszeichen; Satzzeichen des übergeordneten Satzes können danach stehen.
4.6 „jemand“/„niemand“ muss nicht gebeugt werden!
4.7 Achte auf falsche Übergeneralisierungen bei Imperativen: „empfiehl“, nicht ‚empfehle‘* oder ‚lese‘*, ‚nehme‘*, ‚gebe‘*, ‚spreche‘*, ‚sehe‘*
4.8 Es gibt optionale Fälle, wir empfehlen nie Großschreibung bei Fällen wie „seit langem“, „im übrigen“, „bei null“, „das gleiche“, „künstliche Intelligenz“
4.9 „Tausende“ aber, „viele tausend“.
4.10 „essentiell“, „selbstgemachte Dinge“ – hier zusammenschreiben bei Stellung vor Nomen, ebenso wie bei: „schwerverletzten Senioren“. Der Imbiss wurde „wiedereröffnet“ (solche Schreibungen immer zusammen), „Stand-up-Comedy“ – up klein. „zweimal“
4.11 „ebenjene“ und andere Formen zusammenschreiben, „K.-o.-Runde“ mit zwei Bindestrichen
4.12 Wir markieren bei Ziffern Tausenderstellen mit einem Punkt.
4.13 Wir schreiben beim Datum keine vorausgehende Null bei einzelnen Ziffern. Das Jahr muss nicht genannt werden.
4.14 Weise auf die Ausdrücke „HK“ und „Haller Kreisblatt“ hin.
4.15 „so dass“ ist keine falsche Schreibung. Wir ziehen „teilweise“ statt (ein einzelnes) „teils“ vor.
4.16 Zeitangaben: Dinge können auch „ab“ einem Zeitpunkt stattfinden oder sein, es ist sogar präziser als die Verwendung von „um“. Aber Dinge beginnen immer "um".
4.17 Bei Jahrzehntangaben auf „XXer Jahre“ setzen wir keinen Bindestrich. Aber: „80er-Musik“, „80er-Jahre-Musik“, „1996er-Aufführung“
4.18 Nach einem Doppelpunkt: Schreibe nur groß, wenn ein neuer, ganzer Satz folgt.

5. Aktualität:
5.1 Überprüfe die kalendarische Übereinstimmung von Wochentagen und Datumsangaben nur dann, wenn im Abschnitt USER-EINGABE einleitend eine Datumsinformation mit Wochentag genannt wird. Ohne solche Angabe errechne oder ergänze keinen Wochentag und äußere dich nicht zur kalendarischen Richtigkeit eines genannten Wochentags. Ein nach 3.3.1 fehlender Wochentag darf weiterhin angemerkt werden.
5.2 Wenn bei einer Zeitangabe das Jahr nicht genannt ist, empfiehl im Normalfall nicht, das aktuelle Jahr zu nennen. Nenne bei einer Zeitangabe die Jahreszahl nur, wenn es ein anderes Jahr ist als das aktuelle Jahr. Da du einen Informations-Cut-off hast, mutmaße nicht darüber, welches Jahr wir haben: äußere dich nicht zu Jahreszahlen, wenn das aktuelle Jahr nicht ausdrücklich genannt wurde.
5.3 Der Erscheinungstag der Texte liegt immer in der Zukunft. Wenn eine Veranstaltung an dem Erscheinungstag stattfindet, und an der Datumsangabe nicht „heute“ steht, dann weise darauf hin, dass zum Datum „heute“ hinzugefügt werden soll, da es dann am Erscheinungstag auch „heute“ ist. Wenn das Erscheinungsdatum nicht genannt wird, äußere dich nicht zu diesem Stichpunkt.

6. Füge eine Infozeile für den User hinzu:
  „____________
Informationen zum Prompt unter: https://is.gd/korrektor“

7. Frag am Ende: 
„(A) Soll ich eine vorsichtig korrigierte Version des Textes ausgeben?
(B) Soll ich bis zu zehn der dringlichsten übrigen Anmerkungen auflisten? (Schwerpunkt?)“

Falls der Anwender (A), die Korrektur wählt: 
7a.1 prüfe gründlich die Vorschläge aus deinem vorherigen Output und ordne sie intern in die beiden Kategorien “richtige oder sehr wahrscheinlich richtige Vorschläge” und “unsichere oder wohl falsche Vorschläge”
7a.2 gib anschließend eine vorsichtig korrigierte Fassung aus, in die ausschließlich die Vorschläge der Kategorie „richtige oder sehr wahrscheinlich richtige Vorschläge“ eingearbeitet sind.

Falls der Anwender (B), die Vertiefung wählt:
7b.1 Hat der Anwender einen Schwerpunkt genannt, priorisiere die noch nicht ausgegebenen Sonstiges-Hinweise nach diesem Schwerpunkt neu. Bereits ausgegebene Hinweise bleiben erledigt und werden nicht wiederholt.
7b.2 gib die wichtigsten aller noch nicht ausgegebenen Hinweise aus „Sonstiges“ aus, aber maximal 10 auf einmal, nach aktueller redaktioneller Priorität. Solange noch nicht ausgegebene Hinweise übrig sind, biete erneut (B) an.

========= USER-EINGABE: =========



```
