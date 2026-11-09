# Paket für den beruflichen Claude-Account

Stand: 09.11.2026. Quellen der Recherche: Notion (Cortex Kern, Verfassung, Workstation Tieto, Public Sector Kontext, Voice Principles, Meeting „AI at Tieto“ vom 06.11.2026), die privaten Skills `sprache-der-macht` und `ci-olaf` sowie gesendete Mails aus Okt./Nov. 2026. Craft wurde nicht verwendet.

## Inhalt

| Datei | Zweck |
| --- | --- |
| `systemprompt-beruflich.md` | Text für die persönlichen Präferenzen oder eine Projektanweisung (Lang- und Kurzfassung) |
| `skills/tieto-arbeitskontext/` | Rolle, Markt, Portfolio, Partner, Vergabe, MEDDICC, Dokument-Vorlagen, Austauschweg |
| `skills/sprache-der-macht/` | Export deines Nöllke-Skills, auf berufliche Kommunikation zugeschnitten |
| `skills/mail-stil-beruflich/` | Dein Mail-Stil, abgeleitet aus echten Mails, mit acht neutralisierten Beispielen |
| `zip/*.zip` | Upload-fertige Skill-Archive |

## Was bewusst fehlt

Politik und CDU, Buchprojekte und Pseudonyme, Side Business, Familie, Finanzen, Gesundheit, Notion- und Drive-IDs. Das gehört nicht in einen Account, den dein Arbeitgeber verwaltet. Das Side Business ist zusätzlich genehmigungspflichtig (§7 Arbeitsvertrag), dort wäre es doppelt ungünstig.

## Import

1. **Prüfen, ob eigene Skills erlaubt sind.** In Team- und Enterprise-Organisationen kann der Admin Skills oder „Code Execution and file creation“ abschalten. Ohne diese Funktion lassen sich Skills nicht hochladen. Dann siehe „Fallback“.
2. **Systemprompt:** Einstellungen › Profil › persönliche Präferenzen. Langfassung aus `systemprompt-beruflich.md` einfügen.
3. **Skills:** Einstellungen › Capabilities (bzw. Skills) › „Upload skill“. Je ZIP aus `zip/` einzeln hochladen und aktivieren.
4. **Test:** Neuer Chat, „Schreib eine Absage an einen Recruiter, Englisch“ und „Prüf diese Opportunity mit MEDDICC: …“. Antwort muss ohne Gedankenstriche, mit deinem Gruß und ohne Einleitung kommen.

## Fallback, falls keine Skills erlaubt sind

Ein Projekt „Tieto Public Sector“ anlegen. Projektanweisung = Langfassung des Systemprompts. Die drei `SKILL.md` und die Referenzdateien als Projektwissen hochladen. Wirkt fast gleich, nur ohne automatisches Auslösen außerhalb des Projekts.

## Informationsaustausch ohne Konnektoren

Laut Meeting vom 06.11.2026 erlaubt die Tieto-Richtlinie keine Konnektoren, aber das Hochladen von Einzeldateien. Daraus folgt dieser Weg:

**Privat nach beruflich (unkritisch, wenn nicht vertraulich):** Im privaten Setup mit dem Prompt „Erstelle ein Kontext-Update für den beruflichen Account nach der Vorlage, nur Tieto-Themen, nichts Privates“ eine Datei `kontext-update-JJJJ-MM-TT.md` erzeugen, prüfen, in den beruflichen Chat oder ins Projektwissen hochladen. Vorlage: `skills/tieto-arbeitskontext/references/kontext-update-vorlage.md`.

**Beruflich nach privat (kritisch):** Hier liegt das eigentliche Risiko. Dein Cortex-Gedächtnis, deine Meeting-Notizen in Notion und das Morning Briefing beruflich ziehen heute schon Tieto-Inhalte in private Tools. Die alte Regel „KI-Nutzung nur auf privaten Geräten“ stammt aus der Zeit vor dem Tieto-Claude-Zugang. Sobald Tieto einen offiziellen Account stellt, wird sich die Frage stellen, warum Tieto-Wissen weiter in privatem Notion und privatem Claude landet. Meine Empfehlung: einmal schriftlich bei Thomas Schenk oder der IT klären, welche Tieto-Inhalte (Meeting-Notizen, Kontaktlisten, Pipeline) privat verarbeitet werden dürfen, bevor du den Austausch in diese Richtung ausbaust. Bis dahin vom beruflichen Account nur nicht vertrauliche Übergaben zurückholen.

Eine technische Brücke (gemeinsamer Ordner, Mail an dich selbst, Skript) würde ich nicht bauen. Sie wäre genau die Verbindung, die die Richtlinie ausschließt, nur ohne Kontrolle.

## Pflege

Master bleibt Notion (Cortex). Ändern sich Rolle, Portfolio oder Organisation, den Skill `tieto-arbeitskontext` neu erzeugen und als ZIP ersetzen, statt ihn im Account per Hand zu flicken. Fakten mit Datum im Skill: PPF-Verkauf (27.10.2026), Lead Offerings (Juli 2026).
