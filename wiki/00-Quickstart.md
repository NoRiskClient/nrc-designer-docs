# 🚀 Quickstart — Dein erster Emote in 5 Minuten

← [Home](Home) · *Für absolute Anfänger*

---

Du willst **jetzt sofort einen Emote bauen und ingame sehen**? Dann mach genau diese 5 Schritte. Keine Theorie, keine Erklärung — einfach machen.

> 📚 Wenn du verstehen willst **warum** du etwas tust → [Vollständige Doku ab Kapitel 1](01-Grundlagen).

---

## ✅ Schritt 1 — Tools installieren

1. **[Blockbench](https://www.blockbench.net/)** herunterladen + installieren *(Desktop-Version)*
2. Blockbench öffnen → **File → Plugins** → **GeckoLib Models & Animations** suchen → **Install** klicken

✅ **Fertig.**

---

## ✅ Schritt 2 — Template runterladen + öffnen

**[⬇ nrc_default_emote_model.bbmodel](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc_default_emote_model.bbmodel)**

Doppelklick auf die Datei → öffnet sich automatisch in Blockbench.

> ⚠️ Erst öffnen **nachdem** du GeckoLib installiert hast.

---

## ✅ Schritt 3 — Animation bauen

1. Oben rechts auf **„Animate"** klicken *(Mode-Switcher)*
2. Links auf **➕** klicken → Animation **„meinerstemote"** nennen → **Confirm**
3. Im Outliner einen **Bone** anklicken (z.B. `armorRightArm`)
4. In der Timeline unten Position des **Playheads** ändern → Bone drehen/verschieben → **Keyframe** wird automatisch gesetzt
5. Wiederhole bis du eine Bewegung hast die dir gefällt
6. **Leertaste** → Preview abspielen

> 🎯 Hauptsache **2-3 Keyframes** auf einem Bone. Mehr brauchst du jetzt nicht.

---

## ✅ Schritt 4 — Exportieren

1. Oben Menü: **File → Export → Export GeckoLib Animations**
2. Speichern unter: **`meinerstemote.animation.json`**
3. Merk dir den Ordner.

---

## ✅ Schritt 5 — Ingame einbauen + abspielen

### 5a. Designer-Ordner einrichten (nur einmal!)

**[⬇ nrc-cosmetics.zip](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc-cosmetics.zip)** runterladen + entpacken.

Den Ordner `nrc-cosmetics/` kopieren nach:
```
<dein Minecraft Ordner>/NoRiskClient/designer/
```

### 5b. Deine Animation einsortieren

Kopiere `meinerstemote.animation.json` nach:
```
NoRiskClient/designer/nrc-cosmetics/assets/noriskclient-cosmetics/emotes/
```

### 5c. Eine `.norisk.json` daneben legen

Im Ordner `NoRiskClient/designer/nrc-cosmetics/assets/noriskclient-cosmetics/shop/emotes/` eine neue Datei **`meinerstemote.norisk.json`** anlegen mit diesem Inhalt:

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

> 🔧 **`id`** ersetzen mit einer eigenen UUID → [hier eine generieren](https://www.uuidgenerator.net/)

### 5d. Ingame aktivieren

Minecraft starten → NRC öffnen → Chat öffnen → diese 2 Commands:

```
/nrc designer source toggle
/nrc emote play meinerstemote
```

🎉 **Deinen Emote tanzt!**

---

## 😱 Es funktioniert nicht?

| Problem | Lösung |
|---------|--------|
| Command **„designer source"** existiert nicht | Du hast keine Designer-Permissions → Ticket im [Discord](https://discord.com/channels/774271756549619722) |
| Emote zeigt nicht | UUID in JSON noch nicht ersetzt? Doppelklick auf Datei prüfen |
| Crash beim Öffnen vom Template | GeckoLib war noch nicht installiert → Blockbench neu starten |
| Animation läuft nicht | Animation-Name in `.norisk.json` muss zur Datei passen (`emoteFile`) |

---

## 📖 Jetzt mehr lernen

Du hast dein erstes Emote? Geil! Jetzt:

- **Cubes & Modelle** hinzufügen → [3. Model](03-Model)
- **Texturen** drauf → [4. Texture](04-Texture)
- **Particle** ✨ → [8. Particle](08-Particle)
- **Sound** 🔊 → [9. Sound](09-Sound)
- **Cosmetics** statt Emotes → [11. Test-Setup](11-Test-Setup)

→ Komplette Doku ab **[1. Grundlagen](01-Grundlagen)**

---

← [Home](Home)
