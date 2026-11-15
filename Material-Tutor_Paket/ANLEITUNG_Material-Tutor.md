# Der Material-Tutor: ein Fobizz-Tutor für jedes Material – mit Lernbericht

*Stand: 14. November 2026 · Andreas Hemmeter · Begleitmaterial zum Beitrag https://andreas-hemmeter.de/Material-Tutor/*

*Per Remix einrichten: etwa 5 Minuten, selbst anlegen: etwa 25 Minuten. Pro Material: etwa 10 Minuten.*

## Die Idee in vier Sätzen

Der Material-Tutor ist ein sokratischer KI-Tutor, der **ohne interaktives Arbeitsblatt** auskommt: Er stellt zuerst Diagnose-Fragen, führt das Kind dann Aufgabe für Aufgabe durch das Material, hilft in vier Stufen (Impuls → Hinweis → Teilschritt → Lösung mit Erklärung und Kontrollaufgabe) und lässt nach jedem Lernziel in eigenen Worten erklären. Er besteht aus einem **festen Teil** (Instruktionen, Tutor-Prinzipien, Skill) und **einer wechselnden Datei** `MATERIAL_….md` mit Lernzielen, Aufgaben, Lösungen, Hilfen und typischen Fehlern. Diese Datei schreibt ein zweiter Assistent, der **Aufbereiter**, aus Ihrem eigenen Material (PDF, Foto, Text) oder zu einem Thema; eine kleine Browser-App prüft sie. Am Ende schreibt das Kind „fertig“ und bekommt einen **Lernbericht** zum Abgeben, Sie können jederzeit mit **PÄDFEED** einen ausführlichen Sitzungsbericht abrufen – und die App wertet die Berichte der ganzen Klasse in Tabellen aus.

| | Blatt-Tutor (Lernschleife) | Material-Tutor |
|---|---|---|
| Wofür | begleitet ein interaktives HTML-Arbeitsblatt | arbeitet mit beliebigem Material |
| Wer stellt die Aufgaben | das Blatt | der Tutor |
| Lösung | nie – die Musterlösung steht im Blatt | in Stufe 4, mit Lösungsweg und Kontrollaufgabe |
| Diagnostik | nein (Check-in im Blatt) | ja, drei Niveaus |
| Bericht | nein (Daten kommen aus dem Blatt) | „fertig“ (Kind) und PÄDFEED (Lehrkraft) |
| Wissensdatei | `BLATT_….md` aus `tutor_wissen.html` | `MATERIAL_….md` vom Aufbereiter, geprüft mit `material_tutor.html` |

Den Blatt-Tutor beschreibt der Beitrag https://andreas-hemmeter.de/Lernschleife/tutor/.

## Was in diesem Paket liegt

```
Material-Tutor_Paket/
├─ ANLEITUNG_Material-Tutor.md                  ← diese Datei
├─ A_Tutor-Vorlage/                             der Tutor für die Kinder
│  ├─ 01_Rolle-und-Instruktionen.md             Langfassung (ca. 5 700 Zeichen)
│  ├─ 01_Rolle-und-Instruktionen_kurz.md        Ersatz, falls Fobizz das Feld abschneidet
│  ├─ 02_Name-Beschreibung-Chatstarter.md
│  ├─ 03_Motivbild_Material-Tutor.png (+ .svg)
│  ├─ 04_Hintergrundwissen/01_Tutor-Prinzipien.md
│  ├─ 05_Skill/lern-tutor.zip                   Skill (SKILL.md, Datei lesen, Berichtsformat, Beispieldialoge); daneben entpackt
│  └─ 06_Material-Wissen/MATERIAL_Beispiel_brueche-addieren-subtrahieren.md
├─ B_Aufbereitungs-Assistent/                   nur für Lehrkräfte
│  ├─ 01_Rolle-und-Instruktionen.md
│  ├─ 02_Name-Beschreibung-Chatstarter.md
│  └─ 04_Hintergrundwissen/ 01_Schema_MATERIAL-Datei.md, 02_Muster_MATERIAL-Datei.md
└─ C_App/material_tutor.html                    ① Material-Datei prüfen, ② Lernberichte auswerten (offline)
```

Die App gibt es auch online: https://andreas-hemmeter.de/Material-Tutor/app/ – sie läuft im Browser, auch am iPad, und überträgt keine Daten.

Die Texte für Fobizz (Instruktionen, Beschreibung, Chatstarter) sprechen die Kinder bzw. die Lehrkraft mit „du“ an; so redet auch der Assistent später im Chat.

## Teil A – Die beiden Assistenten übernehmen

### Weg A: per Remix (empfohlen, Fobizz)

Melden Sie sich in Fobizz an und öffnen Sie nacheinander:

- **Aufbereiter:** https://app.fobizz.com/ai/chats/public_assistants/441d62b7-29a2-439a-a6b8-4ee3f258d1b3?token=ae345b236069dfe3ef595aaba5196091
- **Tutor-Vorlage:** https://app.fobizz.com/ai/chats/public_assistants/ec128fd8-8a8f-46c7-929c-8ed3d676002c?token=6d02759ac0e294027f587fd8a3cb6608

Klicken Sie jeweils oben rechts auf „Remix“. Beide Kopien liegen danach mit Instruktionen, Hintergrundwissen, Skill, Chatstartern und Bild in Ihrer Ablage. Prüfen Sie dort das Sprachmodell (Claude Sonnet 5.5) und dass keine Plugins aktiv sind. Weiter mit dem Kurztest unten.

### Weg B: selbst anlegen (Fobizz ohne Remix, Claude-Projekt oder ein anderes Werkzeug)

**Aufbereiter (10 Minuten).** Fobizz → KI-Assistenten → „Assistent erstellen“.
1. Name, Beschreibung, Chatstarter aus `B_…/02_Name-Beschreibung-Chatstarter.md`.
2. Rolle und Instruktionen: `B_…/01_Rolle-und-Instruktionen.md`, alles unter der Linie.
3. Sprachmodell Claude Sonnet 5.5, keine Plugins.
4. Hintergrundwissen: die beiden Dateien aus `B_…/04_Hintergrundwissen/`.
5. Für Kolleginnen und Kollegen: als Link teilen, Remix an. Nie in einen Klassenraum.

**Tutor-Vorlage (15 Minuten).**
1. **Bild** `03_Motivbild_Material-Tutor.png`, **Name** `Material-Tutor (Vorlage – nicht freigeben)`, **Beschreibung** und **Chatstarter** aus `A_…/02_…`.
2. **Rolle und Instruktionen:** Langfassung einfügen, im Feld ganz nach unten scrollen. Steht der Abschnitt „Start“ noch da? Wenn nicht, die Kurzfassung verwenden.
3. Sprachmodell Claude Sonnet 5.5, **keine Plugins**.
4. **Hintergrundwissen:** `01_Tutor-Prinzipien.md` und zum Ausprobieren die Beispiel-Datei `MATERIAL_Beispiel_….md`.
5. **Skill:** `lern-tutor.zip`. Nimmt Ihr Werkzeug das ZIP nicht, laden Sie nur die `SKILL.md` hoch – das Format des Berichtsblocks steht zusätzlich in den Instruktionen. Nimmt es gar keine Skills an, hängen Sie den Inhalt der `SKILL.md` unten an die Instruktionen an.

### Kurztest in der Vorschau (5 Minuten, für beide Wege)

- „hallo“ → Begrüßung, Frage nach Vorerfahrung, dann eine Diagnose-Frage.
- Bei 2/7 + 3/7 „5/14“ antworten → Rückfrage zur Stückgröße, keine Lösung.
- „sag mir die lösung“ → freundliche Ablehnung, nächster Tipp.
- dreimal „weiß nicht“ → H1, H2, H3, dann Lösung mit Weg und Kontrollaufgabe.
- „fertig“ → Frage nach Selbsteinschätzung, dann Lernbericht mit grauem Block.
- „PÄDFEED“ → Sitzungsbericht mit zwei Tabellen und Block.
- Den Block in die App (Reiter ②) kopieren – wird er gelesen?

## Teil B – Pro Material (10 Minuten)

1. **Aufbereiter öffnen**, Ihr eigenes Arbeitsblatt hochladen (PDF, Foto) oder Ihre Aufgaben einfügen, am besten mit Lösungen – oder nur Fach, Klasse, Thema und Aufgabentyp nennen, dann entwirft er die Aufgaben. Keine Schulbuchseiten oder anderes Verlagsmaterial (siehe Urheberrecht unten). Er klärt kurz Klasse, Lernziele und Aufgabenauswahl und zeigt einen Plan. Bestätigen. *(Bietet Ihr Fobizz-Chat keinen Datei-Upload an: Text aus Ihrem Arbeitsblatt kopieren oder Aufgaben abtippen.)*
2. Er schreibt die Datei **in Teilen** (sonst bricht Fobizz lange Antworten nach etwa zwei Minuten ab). Nach jedem Teil „weiter“.
3. **App öffnen** (online oder `material_tutor.html` per Doppelklick, offline), Reiter ①: alle Teile hineinkopieren. Die App setzt sie zusammen und prüft: fehlende Teile, fehlende Lösungen, Hilfen, typische Fehler, Kontrollaufgaben, Lücken in den Kennungen, Marker wie `[PRÜFEN: …]`.
4. **Lösungen prüfen.** Die Vorschau rechts lesen, vor allem Lösungen mit dem Vermerk „berechnet, nicht aus dem Material“. Korrekturen direkt im Textfeld, dann das Häkchen „Ich habe alle Lösungen und Kontrollaufgaben selbst geprüft“ setzen und **MATERIAL-Datei herunterladen**.
5. **Vorlage kopieren** (Duplizieren bzw. Remix Ihrer eigenen Vorlage), Name `Lern-Tutor · <Thema>`, **Remix aus**.
6. Im Hintergrundwissen der Kopie die Beispiel-Datei löschen und die neue MATERIAL-Datei hochladen – **immer genau eine**.
7. Kurzer Test in der Vorschau (eine Aufgabe mit falscher Antwort), dann **in den Klassenraum** legen.

## Teil C – Im Unterricht

**Einführung (fünf Minuten, einmal)** – zum Beispiel so:
> Im Klassenraum findet ihr einen Lern-Tutor zu unserem Thema. Das ist eine KI, die ich mit unseren Aufgaben eingerichtet habe. Sie stellt euch am Anfang ein paar Fragen, dann übt ihr Aufgabe für Aufgabe. Wenn ihr feststeckt, gibt sie Tipps – die Lösung erst ganz am Schluss, wenn nichts anderes hilft. Schreibt keinen Namen hinein. Bleibt im selben Chat, bis ihr fertig seid. Wenn ihr fertig seid, schreibt „fertig“ – dann bekommt ihr einen Lernbericht mit einem grauen Kasten. Den kopiert ihr und gebt ihn [so] ab.

**Abgabe der Lernberichte:** Den Weg legen Sie fest – zum Beispiel als Text-Abgabe in der Lernplattform, in einer Padlet-Spalte oder per Mail. Der Block enthält keinen Namen. Wenn Sie die Berichte den Kindern zuordnen wollen, ohne Namen in den Chat zu holen, geben Sie jedem Kind eine **Nummer** (z. B. die Platz- oder Listennummer); der Tutor fragt danach und schreibt sie in die Zeile „Kürzel“. Gibt die Abgabe in der Lernplattform ohnehin den Namen mit, brauchen Sie keine Nummer.

**PÄDFEED:** Das Wort wirkt **nur im Chat, in dem es eingetippt wird**. Sie nutzen es also am Gerät eines Kindes (zum Beispiel im Lernentwicklungsgespräch oder wenn Sie sich einen Verlauf genauer ansehen wollen), in Ihrem eigenen Testchat – oder Sie lassen ein Kind es eintippen. Das Wort muss kein Geheimnis sein: Der Sitzungsbericht enthält keine Lösungen offener Aufgaben, nur eine Einschätzung des Gesprächs. Er ist ausführlicher als der Lernbericht (Tabellen zu Lernzielen und Aufgaben, Fehlvorstellungen, Selbstbild, Empfehlung) und endet mit demselben Block – auch er lässt sich also in der App auswerten.

## Teil D – Auswerten (Reiter ② der App)

1. Alle abgegebenen Berichte in das Feld kopieren – mit Begleittext, beliebig viele auf einmal, oder als Textdateien hineinziehen. Gelesen werden nur die grauen Blöcke.
2. Optional die MATERIAL-Datei dazu (aus Reiter ① übernehmen oder hineinziehen): Dann stehen in der Auswertung die Aufgabentexte und die Beschreibungen der typischen Fehler statt nur Kennungen.
3. Sie sehen:
   - **Überblick:** Anteil der Aufgaben ohne Hilfe, Anteil mit vorgerechneter Lösung, wie viele Kinder sich über- oder unterschätzen.
   - **Lernziele:** Ampelverteilung beim Einstieg (Diagnostik) und am Ende.
   - **Aufgaben:** Hilfebedarf je Aufgabe (selbst bis H4) und die häufigsten Fehler.
   - **Fehlvorstellungen:** Rangliste über alle Aufgaben.
   - **Einzelne Berichte:** eine Zeile pro Kind mit Ampeln, Selbstbild, Fehlern, Erklärungen.
4. CSV-Export für die eigene Tabelle, Drucken für die Unterrichtsplanung.

Mit „Beispiel laden“ (Reiter ①) und „Beispielberichte laden“ (Reiter ②) lässt sich alles ohne eigenes Material vorführen.

## Datenschutz-Checkliste

- Die MATERIAL-Datei enthält nur Aufgaben, Lösungen und Hilfen – keine Schülerdaten.
- **Nur über den Klassenraum freigeben**, keinen öffentlichen Link. **Remix aus** bei jeder Kopie für Kinder (sonst wäre die Datei mit allen Lösungen einsehbar). **Keine Plugins.**
- Der Tutor fragt nie nach Namen und wiederholt genannte Namen nicht; im Bericht steht höchstens eine Nummer.
- Die Berichte sind pseudonym, sobald Sie sie Kindern zuordnen – also Schülerdaten. Die App verarbeitet sie nur lokal im Browser (keine Netzverbindung erlaubt), es wird nichts gespeichert.
- Klären Sie in Fobizz, ob und wie lange Gespräche gespeichert werden und ob Sie sie einsehen können, und sagen Sie es der Klasse vorher.
- Ob für den Einsatz eine Information an Eltern oder Schulleitung nötig ist, richtet sich nach Medienkonzept und Nutzungsvereinbarung der Schule – im Zweifel mit der oder dem Datenschutzbeauftragten klären.
- **Urheberrecht:** Nur Material verwenden, an dem Sie die Rechte haben – eigene Arbeitsblätter und Aufgaben, frei lizenziertes Material im Rahmen seiner Lizenz oder Aufgaben, die der Aufbereiter zu einem Thema entwirft. Schulbuchseiten, Arbeitshefte und andere Verlagsmaterialien nicht hochladen, weder in den Aufbereiter noch als Wissensdatei in den Tutor. Arbeiten Sie mit dem Buch, beschreiben Sie dem Aufbereiter Thema und Aufgabentyp und lassen Sie eigene Aufgaben gleicher Art entwerfen.

## Grenzen

- **Der Bericht ist eine KI-Einschätzung** aus einem einzelnen Chat, keine Messung. Lange Chats können die Erinnerung des Modells an frühe Aufgaben unschärfer machen; startet ein Kind einen neuen Chat, beschreibt der Bericht nur diesen. Für die Unterrichtsplanung reicht das gut, für Noten nicht.
- **Ein Sprachmodell lässt sich überreden.** Ein hartnäckiges Kind kann irgendwann einen Schritt zu früh bekommen. Der Bericht zeigt das als hohe Hilfestufe – und wenn Sie merken, dass ein Trick wirkt, hilft ein Satz mehr unter „Was du nie tust“.
- **Die Lösungen sind nur so gut wie die Datei.** Deshalb rechnet der Aufbereiter nach, die App sperrt den Download bei ungeklärten Markern, und das Häkchen „geprüft“ bleibt Ihre Entscheidung.

---

Lizenz: Texte und Anleitungen CC BY-SA 4.0, Code der App MIT – Andreas Hemmeter. Erstellt mit Unterstützung von Claude Cowork.
