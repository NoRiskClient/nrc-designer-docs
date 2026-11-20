# 15. Blockbench-Plugin

← [Referenz](14-Referenz) · **15 / 15** · [🏠 Home](Home)

---

Alles rund um unser Plugin **NoRisk Client Cosmetics** auf einen Blick. Die Kapitel 1–12 erklären die einzelnen Schritte, hier findest du alle Funktionen gesammelt.

> ℹ️ Stand: Plugin-Version **1.14.0**, ab Blockbench **4.11**.

## Installation

**File → Plugins → Load Plugin from URL** → diesen Link einfügen:

```
https://raw.githubusercontent.com/NoRiskClient/nrc-blockbench-plugins/master/plugins/nrc_cosmetics/nrc_cosmetics.js
```

Berechtigungen (Dateisystem, Netzwerk) erlauben. Ausführlich mit Screenshots: [1. Grundlagen](01-Grundlagen#nrc-plugin-installieren).

> 💡 Hast du noch das **GeckoLib-Plugin** von früher? Kannst du installiert lassen, wird aber nicht mehr gebraucht.

---

## Wo finde ich was?

| Menü | Eintrag | Wofür |
|------|---------|-------|
| **File → New** | NoRisk Client Emote / Cosmetic | Neues Projekt mit Spieler-Rig → [1. Grundlagen](01-Grundlagen#neues-projekt) |
| **File** | Rename NoRisk Client Emote / Cosmetic | Projekt, Animation und alle Sound-IDs auf einmal umbenennen |
| **File → Import** | Import NoRisk Client Emote / Cosmetic | Fertigen Ordner öffnen → [Import](#import) |
| **File → Import** | Import NoRisk Client Emote Animation | Nur eine `.animation.json` aufs Rig laden |
| **File → Export** | Export NoRisk Client Emote / Cosmetic | Alles in einen Ordner exportieren → [10. Export](10-Export) |
| **Edit** | Protect Player Rig | Rig-Cubes gegen Verschieben sperren |
| **Animation** | Edit NoRisk Client Emote Settings | Emote-Einstellungen → [14. Referenz](14-Referenz#extra-einstellungen-in-der-animationjson-emotes) |
| **Tools** | Create Outline | Umriss um ausgewählte Cubes → [unten](#create-outline) |
| **Tools** | Molang Guide | Alle Molang-Funktionen mit Live-Beispiel → [7. Molang](07-Molang) |
| **Rechtsklick in die Vorschau** | Set Preview Skin, Toggle Skin Preview, Toggle Skin Second Layer, Toggle Slim Arms | Skin-Vorschau → [1. Grundlagen](01-Grundlagen#vorschau-mit-deinem-skin) |
| **Animate-Modus, rechts** | Panel *Emote Effects* | Particles & Sounds → [8. Particle](08-Particle), [9. Sound](09-Sound) |
| **Keyframe-Panel** | Easing | Easing für Emote-Keyframes → [6. Keyframes](06-Keyframes#easing-nur-mit-dem-nrc-plugin) |

---

## Neues Emote oder Cosmetic

- Das Projekt startet mit dem Spieler-Rig (`bipedRig`, `bipedHead`, `bipedBody`, Arme und Beine) und allen `armor`-Knochen inklusive `armorRightArmSlim` / `armorLeftArmSlim`.
- **Emotes:** Vorlage wählen oder **Blank Emote**, dann Namen vergeben. Die Vorlagen kommen aus dem aktuellen [Designer-Ordner](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc-cosmetics.zip).
- **Cosmetics:** startet direkt mit der Animation `nrc.idle` (Loop).
- Die Cubes des Rigs sind nur zur Orientierung — exportiert werden **nur deine eigenen** Cubes.

## Create Outline

**Tools → Create Outline** legt um die ausgewählten Cubes eine leicht größere, „umgedrehte“ Hülle. Ingame sieht das aus wie ein farbiger Rand — praktisch für den Cartoon-Look.

- **Thickness:** Dicke des Rands (Standard `0.25`)
- **Colour:** Farbe des Rands

Das Plugin malt die Farbe in einen **freien, komplett durchsichtigen Pixel** deiner Textur. Ist keiner mehr frei, mach die Textur größer oder einen Pixel frei.

## Import

**File → Import → Import NoRisk Client Emote / Cosmetic** öffnet einen fertigen Ordner (`.geo.json`, `.png`, `.animation.json`, `.norisk.json`, Particles, Sounds) wieder in Blockbench — praktisch, um alte Emotes oder Cosmetics weiterzubearbeiten oder aus der Zeit vor dem Plugin zu übernehmen.

- Die `.norisk.json` wird gemerkt: beim nächsten Export bleiben `id` und alle Felder erhalten, die das Plugin nicht kennt.
- Particles und Sounds landen direkt im Panel *Emote Effects*.

Mit **Import NoRisk Client Emote Animation** holst du nur eine einzelne `.animation.json` aufs Rig.

---

## Bekannte Einschränkungen

| Einschränkung | Was du tun musst |
|---------------|------------------|
| Die exportierte `.norisk.json` für **Emotes** enthält kein `emoteFile` und keine `category` | Beide Felder von Hand ergänzen (siehe [11. Test-Setup](11-Test-Setup#emotes-1)), sonst erscheint das Emote nicht richtig im Shop. Für den **Test-Ordner** brauchst du sie nicht. |
| Typ **`BUDDY`** fehlt in der Auswahl | Exportieren und `type` von Hand auf `"BUDDY"` ändern |
| `UNOBTAINABLE` fehlt bei der Rarity | Von Hand eintragen |
| Keine Eingabe für `features`, `animationSettings`, `multiTexture`, `variant`, `color` … | Von Hand eintragen → [Referenz](14-Referenz) |
| Bei Cosmetics wird nur `nrc.idle` angelegt | Weitere Animationen (`nrc.walking` …) selbst anlegen → [5. Animation](05-Animation) |
| Keine Vorlage für interaktive Emotes (Multi-Emotes) | Rig duplizieren und `multiEmote` von Hand setzen → [Referenz](14-Referenz#interaktive-emotes) |
| Zwei Animationen mit gleichem Namen | Nur die letzte wird exportiert — das Plugin warnt dich |
| WebApp statt Desktop | Textur, Sounds und Ordner werden nicht geschrieben — Desktop-Version nehmen |

---

← [Referenz](14-Referenz) · **15 / 15** · [🏠 Home](Home)
