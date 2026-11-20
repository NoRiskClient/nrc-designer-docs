# Quickstart

← [Home](Home)

Erster Emote ingame in 5 Minuten. Keine Theorie — wenn du verstehen willst **warum**, siehe [Kapitel 1](01-Grundlagen).

> 💡 Für den Quickstart brauchst du **keine** Designer-Rechte. Jeder kann über den **Test-Ordner** testen.

---

## 1. Tools

- [Blockbench](https://www.blockbench.net/) (Desktop-Version) installieren
- In Blockbench: **File → Plugins → Load Plugin from URL** → diesen Link einfügen:

```
https://raw.githubusercontent.com/NoRiskClient/nrc-blockbench-plugins/master/plugins/nrc_cosmetics/nrc_cosmetics.js
```

Details: [1. Grundlagen](01-Grundlagen#nrc-plugin-installieren)

## 2. Neues Emote

1. **File → New → NoRisk Client Emote**
2. **Blank Emote** wählen (oder eine Vorlage)
3. Namen eingeben, z.B. `meinerstemote` → das Rig mit Spieler-Skelett ist sofort da

## 3. Animation bauen

1. Oben rechts in den **Animate**-Modus wechseln — die Animation `meinerstemote` ist schon angelegt
2. Bone im Outliner anklicken (z.B. `bipedRightArm`)
3. Playhead in der Timeline verschieben → Bone drehen/verschieben → Keyframe entsteht automatisch
4. 2–3 Keyframes reichen. **Leertaste** für Preview.

## 4. Exportieren

**File → Export → Export NoRisk Client Emote** → Ordner wählen → **Confirm**.

Das Plugin legt einen Ordner `meinerstemote/` mit `meinerstemote.animation.json` an.

## 5. Ingame abspielen

**Minecraft mit NoRiskClient starten, dann Chat:**

```
/nrc test folder
```

Öffnet den Test-Ordner. Zieh deinen `meinerstemote/`-Ordner (oder nur die `.animation.json`) hinein. Der Client lädt ihn automatisch.

```
/nrc test emote meinerstemote
```

Fertig. Nochmal den gleichen Command → Emote stoppt.

> 👀 Was im Test-Ordner liegt, siehst **nur du**.

---

## Geht nicht?

| Problem | Lösung |
|---------|--------|
| `File → New` zeigt kein *NoRisk Client Emote* | Plugin nicht geladen — [Installation](01-Grundlagen#nrc-plugin-installieren) wiederholen, Blockbench neu starten |
| `/nrc test emote` findet das Emote nicht | `/nrc test` eingeben — zeigt alles, was erkannt wurde, und warum etwas übersprungen wurde |
| Datei wird übersprungen | Name darf nur `a-z`, `0-9`, `.`, `_`, `-` enthalten — keine Großbuchstaben, keine Leerzeichen |
| Änderung kommt nicht an | `/nrc test reload` |

---

**Mehr lernen:** [Model](03-Model) · [Texture](04-Texture) · [Particle](08-Particle) · [Sound](09-Sound) · [Cosmetics](11-Test-Setup) · oder komplett ab [Kapitel 1](01-Grundlagen).
