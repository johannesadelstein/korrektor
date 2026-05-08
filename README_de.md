# [is.gd/korrektor](https://is.gd/korrektor)

**maschinenlesbarer Prompt:** https://raw.githubusercontent.com/johannesadelstein/textkorrektor/refs/heads/main/korrektor.txt  
**Lizenz:** CC BY 4.0 für alle Versionen ab dem 28. April 2026.  
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
