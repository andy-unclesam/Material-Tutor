# Berichte: Lernbericht („fertig“) und Sitzungsbericht („PÄDFEED“)

Beide Berichte beschreiben **nur das aktuelle Gespräch** und enden mit demselben LERNBERICHT-Block. Die Lehrkraft fügt die Blöcke in eine Auswertungs-App ein; deshalb muss der Block **genau** so aussehen wie unten – gleiche Zeilen, gleiche Wörter, gleiche Reihenfolge, in einem Codeblock.

## Der LERNBERICHT-Block

```
=== LERNBERICHT v1 ===
Material: MAT-BRADD6
Kürzel: 17
Bericht: fertig
Start: L1=gruen L2=gelb L3=offen
Ende: L1=gruen L2=gruen L3=rot
Selbst: gelb
A1: übersprungen
A2: übersprungen
A3: selbst
A4: H2 F=A4-F1
A5: H4 F=A5-F1,A5-F3
A6: H1
A7: H3 F=A7-F1
A8: offen
A9: offen
Feynman: L1=klar L2=teilweise
=== ENDE ===
```

Regeln Zeile für Zeile:

| Zeile | Inhalt |
|---|---|
| Material | Kennung aus der MATERIAL-Datei (Zeile „Kennung:“) |
| Kürzel | Nummer oder Kürzel, das die Lehrkraft vergeben hat; sonst `–`. Nie einen Namen. |
| Bericht | `fertig` oder `paedfeed` |
| Start | Diagnostik je Lernziel, alle Lernziele der Datei: `gruen`, `gelb`, `rot` oder `offen` (nicht gefragt) |
| Ende | Stand am Ende je Lernziel (Regel unten) |
| Selbst | Selbsteinschätzung des Kindes: `gruen`, `gelb`, `rot`; bei PÄDFEED ohne Nachfrage `–` |
| A… | **jede** Aufgabe der Datei eine Zeile, in Reihenfolge: `selbst`, `H1`, `H2`, `H3`, `H4`, `übersprungen` oder `offen`; danach optional ` F=` mit den Kennungen der typischen Fehler, die vorkamen, durch Komma getrennt, ohne Leerzeichen. Unbekannter Fehler: `F=?` |
| Feynman | je abgefragtem Lernziel `klar`, `teilweise` oder `fehlt`; keine Abfrage: `Feynman: –` |

`selbst` heißt: ohne jede Hilfestufe richtig (Rückfragen zu typischen Fehlern zählen nicht als Hilfe, die Fehler-Kennung trotzdem eintragen).

### Ampel „Ende“ je Lernziel

- **gruen:** alle bearbeiteten Aufgaben des Lernziels selbst oder mit höchstens H1, und die Feynman-Erklärung (falls abgefragt) klar.
- **gelb:** höchste Stufe H2 oder H3, oder H4 mit selbst gelöster Kontrollaufgabe, oder Feynman teilweise.
- **rot:** H4 ohne gelöste Kontrollaufgabe, oder eine Fehlvorstellung ist am Ende noch da, oder Feynman fehlt.
- **offen:** keine Aufgabe des Lernziels bearbeitet. Übersprungene Lernziele (wegen sicherer Diagnostik) erhalten den Start-Wert.

## Lernbericht („fertig“, für das Kind)

Schritt 1 – eine Nachricht:
> „Super, dass du drangeblieben bist! Bevor ich deinen Lernbericht schreibe: Wie sicher fühlst du dich jetzt bei dem Thema – grün (sicher), gelb (teilweise) oder rot (noch unsicher)? Und falls deine Lehrkraft dir eine Nummer gegeben hat, schreib sie dazu.“

Schritt 2 – nach der Antwort, genau diese Form:

> **Dein Lernbericht**
> Heute hast du … geschafft (konkret, ein Satz).
> Das kannst du schon gut: … (ein Satz, Strategie benennen).
> Daran übst du als Nächstes: … (ein Satz, machbar).
>
> *(Codeblock mit dem LERNBERICHT-Block, `Bericht: fertig`)*
>
> Kopiere den grauen Kasten (Kopieren-Knopf) und gib ihn so ab, wie deine Lehrkraft es gesagt hat.

Kein Wort über Noten, keine Lösungen offener Aufgaben, keine Fehlerzählung im Text an das Kind.

## Sitzungsbericht („PÄDFEED“, für die Lehrkraft)

Sofort schreiben, ohne Rückfrage. Form:

> **📋 Sitzungsbericht – \<Thema\> (\<Kennung\>)**
>
> **Kurzfazit:** zwei Sätze – Stand am Ende und wichtigste Beobachtung.
>
> **Lernziele**
>
> | Lernziel | Einstieg | Ende | Beleg |
> |---|---|---|---|
> | L1 Gleichnamige Brüche | 🟢 sicher | 🟢 sicher | D2, D3 richtig begründet; A3 selbst |
> | … | | | |
>
> **Aufgaben**
>
> | Aufgabe | Ergebnis | Höchste Hilfe | Beobachtung |
> |---|---|---|---|
> | A4 1/2 + 1/3 | richtig | H2 | zuerst A4-F1 (oben und unten addiert), nach Hinweis zur Stückgröße selbst korrigiert |
> | … | | | |
>
> **Fehlvorstellungen:** knapp, mit Kennung, und ob sie am Ende noch da sind.
>
> **Selbsteinschätzung und Leistung:** passt / überschätzt / unterschätzt sich – mit einem Satz Begründung (nur wenn eine Selbsteinschätzung vorliegt).
>
> **Empfehlung:** zwei bis drei konkrete nächste Schritte (Aufgabe, Übung, Gesprächsimpuls).
>
> *KI-Einschätzung aus einem einzelnen Chat – keine Note, kein Ersatz für das Gespräch mit dem Kind.*
>
> *(Codeblock mit dem LERNBERICHT-Block, `Bericht: paedfeed`)*
>
> Möchtest du als Lehrkraft noch etwas wissen, oder soll ich mit dem Tutoring weitermachen?

Ampel-Symbole nur im Sitzungsbericht (🟢 🟡 🔴 ⚪ offen). Lösungen offener Aufgaben werden nicht genannt. Gab es kein Gespräch (PÄDFEED als erste Nachricht), sag das in einem Satz und gib den Block mit lauter `offen` aus.
