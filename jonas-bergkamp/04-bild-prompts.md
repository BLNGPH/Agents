> 🧭 **PROJEKTBRIEF** · *Bild-Prompts und Konsistenzregeln*
> Stand 22.08.2026 · Baut auf dem Portrait-Prompt der Notion-Autorenseite auf

# 🖼️ Das Gesicht von Jonas

> *Ein Masterprompt, sechs Ableitungen und die Technik, mit der das Gesicht über Monate gleich bleibt. Der Notion-Prompt war der Rohentwurf, hier ist die produktionsreife Fassung.*

## ❓ Warum der alte Prompt überarbeitet werden musste

Der Prompt auf der Notion-Autorenseite liefert ein brauchbares Bild, hat aber drei Lücken. Er beschreibt keine Kameraeinstellung, deshalb wird der Bildausschnitt bei jedem Durchlauf anders. Er nennt kein Seitenverhältnis, deshalb passt das Ergebnis nicht in einen quadratischen Profilrahmen. Und er hat keine Negativliste, deshalb rutschen Hochglanzhaut und Model-Ästhetik durch, obwohl die Beschreibung genau das ausschließen will.

Der zweite Prompt aus dem Buchprojekt ("Modell C", Mann Ende dreißig mit Brille im Café) ist damit überholt. Brille und Alter widersprechen der Autorenseite. Nicht mehr verwenden.

---

## ⭐ Masterprompt: Das Autorenportrait

Dieser Prompt erzeugt das Bild, das auf Amazon, LinkedIn, im Buch und überall sonst steht. Er wird einmal benutzt, das Ergebnis wird gespeichert, und alle weiteren Bilder werden davon abgeleitet.

```
Photorealistic editorial author portrait of a 36-year-old Norwegian man.
Narrow oval face with defined but soft cheekbones, a straight narrow nose,
calm alert blue-gray eyes, dark blond eyebrows that are thick but tidy.
Short dark blond hair, fine and slightly wavy, worn in a natural side part
with a little movement, not styled stiff. Neatly trimmed three-day stubble.
Fair skin with a cool Nordic undertone, visible natural skin texture,
faint fine lines around the eyes, no retouching.

He wears a charcoal fine-knit sweater over a plain dark shirt. Muted
palette only: charcoal, navy, warm grey.

Head and shoulders, three-quarter angle with the face turned slightly
toward the camera, eyes looking directly into the lens. Calm, approachable
expression with the faintest hint of a smile, thoughtful rather than
cheerful.

Soft natural window light from the front left, gentle falloff on the right
cheek, no hard shadows, no rim light. Clean bright neutral background in
warm grey, softly out of focus.

Shot on 85mm lens at f2.0, sharp focus on the eyes, shallow but not
extreme depth of field. Documentary editorial photography, quiet and
understated, like a portrait for a book jacket.
```

**Negativliste, immer mitgeben:**

```
glossy skin, airbrushed, beauty retouching, male model, fashion editorial,
perfect symmetry, studio strobe, hard rim light, teeth showing, wide grin,
glasses, beard longer than stubble, tattoos, jewelry, logos, busy
background, office cliché, bookshelf backdrop, blue tech lighting, neon,
circuit boards, robot imagery, text, watermark, extra fingers, plastic
texture, oversaturated, HDR
```

**Einstellungen:**

| Zweck | Seitenverhältnis |
| --- | --- |
| 📇 Profilbild alle Kanäle | 1:1 |
| 📖 Buchklappe, Presse | 4:5 |
| 💼 LinkedIn und Website | 3:2 |

> 💡 **Praxisnotiz:** Generiere acht bis zwölf Varianten und nimm dir Zeit bei der Auswahl. Dieses eine Gesicht trägt jahrelang alle Bücher. Nimm nicht das schönste Ergebnis, sondern das unauffälligste. Ein Gesicht, das zu perfekt ist, wird sofort als generiert gelesen und beschädigt genau die Glaubwürdigkeit, die das Bild herstellen soll.

---

## 🔒 Konsistenz: das eigentliche Problem

Ein einzelnes Bild ist einfach. Zwanzig Bilder derselben Person über zwölf Monate sind das Problem. Drei Techniken, aufsteigend nach Aufwand:

| 🧰 Technik | Wie | Wann |
| --- | --- | --- |
| 🎲 **Seed festhalten** | Seed-Nummer des gewählten Bildes notieren und bei jeder neuen Generierung wieder eingeben | Minimalaufwand, hält nur bei kleinen Änderungen |
| 🖼️ **Referenzbild** | Das Masterbild als Bildreferenz mitgeben, Stärke etwa 0.5 bis 0.7 | Standardweg, funktioniert für alle Ableitungen unten |
| 🧬 **Eigenes Modell trainieren** | Aus zwölf konsistenten Bildern ein LoRA trainieren | Erst wenn es dauerhaft läuft und Bilder wöchentlich gebraucht werden |

**In jeden abgeleiteten Prompt gehört dieser Block wörtlich:**

```
Same man as reference: 36-year-old Norwegian, narrow oval face, blue-gray
eyes, short dark blond hair with a natural side part, trimmed stubble,
fair skin with a cool undertone, calm thoughtful expression. Identical
facial structure. Muted palette: charcoal, navy, forest green, warm grey.
```

---

## 📐 Die sechs Ableitungen

### 1. Instagram-Profilbild, 1:1, enger Ausschnitt

```
[Konsistenzblock]
Tight square crop, head only, chin to just above the hairline. Face fills
the frame. Neutral warm grey background. Soft frontal light. Expression
calm and open. Must stay readable at 40 pixels wide.
```

### 2. LinkedIn und Amazon, 3:2, mehr Raum

```
[Konsistenzblock]
Head and shoulders with generous space above the head and to the right.
Charcoal knit sweater. Bright neutral background, softly blurred. Warm,
professional, understated. Editorial portrait photography.
```

### 3. Bannerbild, 3:1, quer, ohne Gesicht

Für LinkedIn, Facebook und Twitter. Bewusst ohne Portrait, weil ein KI-Gesicht in Bannergröße auffällt und weil dort ohnehin Text liegt.

```
Minimal editorial still life, top down view on a pale oak desk. An open
notebook with handwriting too small to read, a simple black pen, a plain
white coffee cup, a pair of reading glasses folded shut. Soft morning
window light from the left, long gentle shadows. Muted Nordic palette in
warm grey, charcoal and a touch of forest green. Large empty space on the
left third for text. Calm, uncluttered, photorealistic, shallow depth of
field, 3:1 aspect ratio.
```

### 4. Content-Bild: Café

Der Bildtyp aus dem alten "Modell C", jetzt aber als Content-Motiv statt als Portrait.

```
[Konsistenzblock]
The man sits at a window table in a quiet modern cafe, writing in a paper
notebook, seen from a slight distance at three-quarter angle. He is not
looking at the camera. Bright overcast daylight through a large window.
Muted interior in wood and warm grey, other guests blurred beyond
recognition. Natural documentary photography, unposed, calm optimistic
atmosphere, 4:5 aspect ratio.
```

### 5. Content-Bild: Küste

Für Beiträge über Herkunft, Haltung und Pausen. Zahlt auf die nordische Bildmarke ein.

```
[Konsistenzblock]
The man stands on a wooden pier by the water in a dark navy wool coat,
seen from behind at three-quarter angle, looking out over grey water
toward a low coastline. Overcast Nordic daylight, muted greens and greys,
soft cool colors. Wide shot, the figure small in the frame. Quiet,
contemplative, photorealistic, 4:5 aspect ratio.
```

### 6. Content-Bild: Schreibtisch, über die Schulter

Für Prompt-Beiträge, wenn ein Bild von Menschenhand gebraucht wird.

```
[Konsistenzblock]
Over the shoulder view of the man at a plain wooden desk, typing on a
laptop whose screen is not readable. Warm afternoon light from the side.
A notebook and a cup next to the laptop. Shallow depth of field, focus on
the hands and the notebook. Natural, unstaged, no visible logos, no
readable text on screen, 4:5 aspect ratio.
```

---

## 🎨 Bildvorlagen für Prompt-Beiträge

Die Prompt-Karussells brauchen keine Fotos, sondern Textgrafiken. Dafür kein Bildmodell benutzen, sondern eine feste Vorlage bauen und immer wiederverwenden.

| Element | Festlegung |
| --- | --- |
| 🎨 **Hintergrund** | Warmgrau oder Beige, einfarbig, kein Verlauf |
| 🔤 **Prompt-Text** | Groteske, sehr groß, linksbündig, maximal fünf Zeilen |
| 🗂️ **Rahmen** | Der Prompt liegt in einem hellen Kasten mit weichen Ecken, damit er als kopierbar gelesen wird |
| 🧭 **Fuß** | Namenszug klein unten rechts, immer gleiche Position |
| 📏 **Format** | 1080 mal 1350 für Instagram, 1000 mal 1500 für Pinterest |

Wichtig: kein Gesicht auf Prompt-Grafiken. Die Karte soll weitergeschickt werden, und dabei stört ein Portrait.

---

## ⚠️ Zwei Grenzen bei generierten Bildern

**Keine erfundenen Belege.** Keine Bilder, die Ereignisse behaupten, die nicht stattgefunden haben. Kein Jonas auf einer Bühne, kein Jonas bei einer Lesung, kein Jonas mit anderen Menschen im Gespräch. Ein Portrait und Stimmungsbilder sind Illustration, ein erfundenes Vortragsfoto ist eine Behauptung.

**Kein reales Vorbild.** Der Prompt darf keinen existierenden Menschen benennen und das Ergebnis darf niemandem erkennbar ähneln. Bei Ähnlichkeit zu einer echten Person: verwerfen und neu generieren.
