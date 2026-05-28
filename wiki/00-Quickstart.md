# Quickstart

← [Home](Home)

Erster Emote ingame in 5 Minuten. Keine Theorie — wenn du verstehen willst **warum**, siehe [Kapitel 1](01-Grundlagen).

---

## 1. Tools

- [Blockbench](https://www.blockbench.net/) installieren
- In Blockbench: **File → Plugins → GeckoLib Models & Animations → Install**

## 2. Template öffnen

[nrc_default_emote_model.bbmodel](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc_default_emote_model.bbmodel) herunterladen → Doppelklick.

*(Erst nach GeckoLib-Install öffnen.)*

## 3. Animation bauen

1. Oben rechts: **Animate** Mode
2. Links auf **+** → Name z.B. `meinerstemote` → **Confirm**
3. Bone im Outliner anklicken (z.B. `armorRightArm`)
4. Playhead in der Timeline verschieben → Bone drehen/verschieben → Keyframe entsteht automatisch
5. 2–3 Keyframes reichen. **Leertaste** für Preview.

## 4. Exportieren

**File → Export → Export GeckoLib Animations** → speichern als `meinerstemote.animation.json`.

## 5. Ingame einbauen

**Einmalig:** [nrc-cosmetics.zip](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc-cosmetics.zip) entpacken, Ordner `nrc-cosmetics/` nach `<MC-Ordner>/NoRiskClient/designer/` kopieren.

**Deine Animation** nach:
```
NoRiskClient/designer/nrc-cosmetics/assets/noriskclient-cosmetics/emotes/
```

**`.norisk.json`** daneben anlegen in:
```
NoRiskClient/designer/nrc-cosmetics/assets/noriskclient-cosmetics/shop/emotes/meinerstemote.norisk.json
```

```json
{
  "id": "ERSETZEMICH-AAAA-BBBB-CCCC-DDDDDDDDDDDD",
  "price": 0,
  "rarity": "COMMON",
  "name": "Mein erster Emote",
  "creator": "dein name",
  "emoteFile": "meinerstemote.animation.json",
  "dateAdded": "2026-01-01",
  "category": "FUNNY",
  "overflow": { "overflowInShop": true },
  "isExclusive": false
}
```

`id` ersetzen mit eigener UUID → [Generator](https://www.uuidgenerator.net/).

**Minecraft starten, dann Chat:**
```
/nrc designer source toggle
/nrc emote play meinerstemote
```

Fertig.

---

## Geht nicht?

| Problem | Lösung |
|---------|--------|
| Command `designer source` existiert nicht | Keine Designer-Permission → [Discord-Ticket](https://discord.com/channels/774271756549619722) |
| Emote zeigt nicht | UUID in JSON ersetzt? `emoteFile` passt zum Dateinamen? |
| Crash beim Template öffnen | GeckoLib nicht installiert — Blockbench neu starten |

---

**Mehr lernen:** [Model](03-Model) · [Texture](04-Texture) · [Particle](08-Particle) · [Sound](09-Sound) · [Cosmetics](11-Test-Setup) · oder komplett ab [Kapitel 1](01-Grundlagen).
