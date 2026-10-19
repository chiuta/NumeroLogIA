# NumeroLogIA

[English](README.md) · [Română](README.ro.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [Español](README.es.md) · [Português](README.pt.md) · **Deutsch** · [Magyar](README.hu.md)

**Version:** 1.2.0 · **Zuletzt aktualisiert:** 2026-10-19

Oberflächensprachen: **Română, English, Français, Italiano, Español, Português (PT), Català, Deutsch, Magyar**

Pythagoreische und chaldäische Numerologie mit Zyklenanalyse, Kompatibilität und einem optionalen KI-Orakel, das auf deinem lokalen Modell läuft.

**Online-App:** https://chiuta.github.io/NumeroLogIA/

![Screenshot](screenshot.png)

## Was es ist

NumeroLogIA berechnet ein numerologisches „Porträt“ aus dem vollständigen Geburtsnamen, dem Geburtsdatum und optional der Geburtszeit. Die Anwendung nutzt die pythagoreische Numerologie (mit chaldäischer Option), behält die Meisterzahlen 11/22/33 bei und kennzeichnet die karmischen Schulden 13/14/16/19; die Berechnungen werden Schritt für Schritt angezeigt. Die Anwendung stellt ausdrücklich klar, dass die Numerologie ein traditionelles symbolisches System ist, das zur persönlichen Reflexion und kulturellen Erkundung angeboten wird, keine Wissenschaft.

## Funktionen

- Oberfläche in 9 Sprachen: Englisch, Rumänisch, Italienisch, Spanisch, Französisch, Portugiesisch, Katalanisch, Deutsch, Ungarisch.
- Systemumschalter **Pythagoras / Chaldäisch**; helles/dunkles Thema (Schaltfläche ◐); **⎙** zum Drucken / Speichern als PDF.
- Tabs: **Profil**, **Zyklen**, **Geburtsraster**, **Namensrechner**, **Kompatibilität**, **Universal & Referenz**, **BaZi**, **Biorhythmus**, **KI**, **Gespeichert**.
- Schaltflächen im Profil: **Porträt enthüllen**, **Porträt speichern**, **Teilbaren Link kopieren**, **Beispiel**, **PDF-Bericht**.
- Rechner für den Zahlenwert beliebiger Namen oder Wörter, Buchstabe für Buchstabe aufgeschlüsselt (Vokale und Konsonanten), in beiden Systemen, und Vergleich zweier Namen (Künstlernamen, Namen nach der Heirat, Pseudonyme).
- Kompatibilität zwischen zwei Personen (Lebensweg, Ausdruck, Seelenwunsch).
- Die universellen Zahlen des Tages und eine vollständige Referenz der Zahlen.
- **Gespeicherte Porträts** im Browser, mit **JSON-Export / -Import** (Sicherung; beim Import werden Name, Datum und Uhrzeit validiert, Duplikate entfernt, höchstens 50 Einträge, Datei unter 1 MB).
- **Zusammenfassung kopieren** (Profil): die Hauptzahlen als einfacher Text, mit dem Hinweis, dass die Numerologie keine wissenschaftliche Validierung hat; ein ungültig eingegebenes Datum erzeugt nun eine Meldung.
- **KI-Orakel** (optional): Porträtsynthese, Orientierung für heute, Kompatibilitätsdeutung und freie Fragen, gesendet an ein Sprachmodell unter einer Adresse, die du selbst festlegst (Standard: lokales Ollama). Es kann installierte Modelle auflisten und Modelle über Ollama herunterladen.

## Bedienungsanleitung

1. Wähle die Sprache aus der Sprachliste und das System (Pythagoras oder Chaldäisch).
2. Gib unter „Profil“ den vollständigen Geburtsnamen (Diakritika werden normalisiert), das Geburtsdatum und, wenn du möchtest, die Uhrzeit ein; drücke **Porträt enthüllen** (Enter in den Feldern bewirkt dasselbe). **Beispiel** füllt Demonstrationsdaten ein.
3. Gehe die Tabs Zyklen, Geburtsraster, BaZi und Biorhythmus für den Rest der Analyse durch.
4. Für ein beliebiges Wort nutze „Namensrechner“; für zwei Personen „Kompatibilität“.
5. **Porträt speichern** legt es im Tab „Gespeichert“ ab; **Teilbaren Link kopieren** legt Name, Datum, Uhrzeit, Sprache und System in den Link.
6. **PDF-Bericht** oder **⎙** öffnen den Druckdialog des Browsers, von dem aus du ein PDF speichern kannst.
7. Für den KI-Tab: Installiere Ollama (oder einen anderen OpenAI-kompatiblen Server), starte ein Modell, öffne „Einstellungen“, prüfe die Adresse (Standard `http://localhost:11434/v1`) und das Modell, drücke Speichern / Testen und wähle dann eine Aktion. Wird die Seite von einer Website ausgeliefert, weist die Anwendung darauf hin, Ollama mit `OLLAMA_ORIGINS=*` zu starten, um die Verbindung aus dem Browser zu erlauben.

## Hinweis

Informations-/Unterhaltungsinhalt ohne wissenschaftliche Validierung: Numerologie, BaZi, Astrologie und Biorhythmus sind traditionelle oder populäre symbolische Systeme, keine Wissenschaften, und bieten weder Vorhersagen noch medizinische, finanzielle oder rechtliche Beratung. Die Anwendung zeigt in der Fußzeile einen „Ehrlichen Hinweis“; von KI erzeugte Texte können falsch oder erfunden sein.

## Datenschutz und Netzwerk

- **Lokaler Speicher (localStorage):** `numerologie_saved_v1` (die gespeicherten Porträts), Schlüssel `num_pref_*` (Sprache, System, Thema) und `num_ai_*` (die Adresse, das Modell und, falls du ihn eingibst, der API-Schlüssel des KI-Orakels: Standardmäßig wird er nur in `sessionStorage` gehalten (bis zum Schließen des Tabs) und gelangt unverschlüsselt in `localStorage` nur, wenn du „Schlüssel zwischen Sitzungen merken“ ankreuzt; die Anwendung zeigt jetzt in allen 7 Sprachen einen sichtbaren Hinweis unter dem Feld „API-Schlüssel“ in den KI-Einstellungen).
- **Netzwerk:** Die numerologischen Berechnungen stellen keine Anfragen. Die einzigen möglichen Anfragen stammen aus dem KI-Tab, nur wenn du eine KI-Aktion (oder das Auflisten/Herunterladen von Modellen) auslöst, an die von dir konfigurierte Adresse, standardmäßig `http://localhost:11434` (Ollama auf deinem eigenen Rechner). Legst du eine entfernte Adresse fest, gelangen deine Namen, Daten und Fragen an diesen Server. Die Anwendung enthält keine Schlüssel, Analytics oder Telemetrie und lädt keine Drittressourcen; eine CSP-Richtlinie (`default-src 'none'`, `connect-src http: https:`) beschränkt die Seite bei jedem anderen Laden.
- Der teilbare Link enthält im Teil nach `#` den eingegebenen Namen und das Datum (der Hash wird bei jeder Berechnung aktualisiert, erscheint also auch in der Adressleiste/im Verlauf des Browsers, wird aber an keinen Server gesendet); die Bestätigungsmeldung beim Kopieren sagt nun ausdrücklich, dass der Link Namen und Geburtsdatum enthält; teile ihn bewusst.

## Lokale Ausführung / offline

Lade `index.html` herunter und öffne sie in einem Browser; die Numerologie funktioniert ohne Internet. Das KI-Orakel benötigt einen lokalen Modellserver (z. B. Ollama) oder eine Adresse deiner Wahl.

## Verlauf / Changelog

### 1.1.0 — 2026-10-14
- Datensicherung und Datenkennzeichnung (fff-kit).

### 12. Oktober 2026 (v1.0.0)
- 1.0.0 — 2026-10-12: Version und Datum der letzten Aktualisierung werden in der App angezeigt

### 11. Oktober 2026 (zweiter Eintrag)
- Sicherheit: Der API-Schlüssel des KI-Orakels wird standardmäßig nur für die Sitzung gehalten; die Speicherung in `localStorage` ist eine ausdrückliche Option („Schlüssel zwischen Sitzungen merken“, 7 Sprachen), und beim Speichern wird ein alter Schlüssel aus `localStorage` in die Sitzung verschoben, wenn die Option nicht angekreuzt ist. Im Browser getestet.

### 11. Oktober 2026
- Barrierefreiheit: Inhalt in <main> eingefasst, dekoratives Canvas vor Screenreadern verborgen, Labels mit Feldern verknüpft (axe: 0 Verstöße).
- Die „heutigen“ Daten (universelle Zahlen, BaZi) werden dynamisch aus dem aktuellen Datum berechnet; es gibt keine veralteten festen Daten. Die Inline-Attribute `on*` (22) wurden durch einen delegierten Dispatcher ersetzt (`data-click` / `data-change` / `data-input` / `data-keydown`, Whitelist von Funktionen, JSON-Argumente), und die CSP verwendet einen Hash für das Skript, ohne `'unsafe-inline'` für Skripte (bei Stilen bleibt es; `connect-src http: https:` bleibt für die konfigurierbare Adresse des KI-Modells).
- Neu: JSON-Export/-Import der gespeicherten Porträts, „Zusammenfassung kopieren“, Meldung bei ungültigem Datum (in den 7 Sprachen). Screenshot aktualisiert.

## Lizenz

MIT — siehe Datei `LICENSE`. © 2026 Alexandru-Ionuț Chiuță (Alexio). Eventuell in der Datei enthaltene Drittbibliotheken behalten ihre eigenen Lizenzen.

Lizenz: MIT (siehe Datei LICENSE). Kontakt: alexio@trom.tf

Dieselbe Erklärung erscheint im HTML-Kopf und in der Fußzeile der Anwendung (RO + EN). Der Lizenztext befindet sich in der Datei LICENSE.

## Audit

Audit: 2026-10-10 — mit Playwright und axe-core geprüft (alle Tabs, beide Themen); im Code geprüft: ein einziger `fetch` (KI-Tab, bei Aktion, an die konfigurierte Adresse); der Name aus dem Link `#n=` und aus den Feldern, getestet mit `<img onerror>`, wird nicht ausgeführt (escaped). Korrigiert: fehlende Labels an den Datums-/Uhrzeitfeldern, Kontrast im hellen Thema, zugänglicher Name am Biorhythmus-Regler.

## Autor

Alexio — Alexandru-Ionuț Chiuță. Kontakt: alexio@trom.tf

## Englische Zusammenfassung

NumeroLogIA ist ein Numerologie-Werkzeug in einer einzigen Datei (pythagoreisches und chaldäisches System, Meisterzahlen, Zyklen, Geburtsraster, Namensrechner, Kompatibilität, BaZi, Biorhythmus) in 9 Sprachen, mit in localStorage gespeicherten Porträts. Ein optionaler KI-Tab kommuniziert nur mit einem von dir konfigurierten Endpunkt (Standard: lokales Ollama unter localhost:11434); bei einem entfernten Endpunkt würden deine Eingaben dorthin gesendet. Keine Telemetrie und keine Drittressourcen. Lizenz: MIT (siehe Datei LICENSE) (Kontakt: alexio@trom.tf).

Runde 3 (2026-10-11): ausdrückliche Lizenzerklärung (zuvor nicht deklariert) hinzugefügt (Kopfzeile, Fußzeile, README); CSP hinzugefügt; das esoterische Thema und die Speicherung des API-Schlüssels bleiben Entscheidungen des Autors.
