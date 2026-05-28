# NRC Designer Doc

> **by Tinus aka. p2pe**

Willkommen im offiziellen Designer-Wiki für **NoRiskClient**. Diese Dokumentation führt dich Schritt für Schritt durch den kompletten Workflow zum Erstellen eigener **Emotes** und **Cosmetics** für NRC — vom ersten Modell in Blockbench bis zum Ingame-Test deiner fertigen Datei.

Wenn ihr offene Fragen habt oder allgemein was wissen wollt, könnt ihr auch gerne jederzeit ein Ticket erstellen und wir versuchen dann euch alles wichtige zu erklären. ❤️

---

## Komplett neu hier?

→ **[Quickstart](00-Quickstart)** — erster Emote ingame in 5 Minuten, ohne Theorie. Danach kannst du mit den Kapiteln unten tiefer einsteigen.

---

## Voraussetzungen

Bevor du loslegst, brauchst du folgende Tools:

| Tool | Pflicht | Zweck |
|------|---------|-------|
| [Blockbench](https://www.blockbench.net/) | ✅ | 3D-Modeling, Texturen, Animationen |
| [GeckoLib Plugin](https://github.com/bernie-g/geckolib/wiki/Molang) | ✅ | Export-Format für NRC Cosmetics & Emotes |
| [Snowstorm](https://snowstorm.app/) | optional | Particle-Effekte |
| [Audacity](https://www.audacityteam.org/) | optional | Sound-Bearbeitung (Mono `.ogg`) |

---

## Roter Faden — so liest du dieses Wiki

Die Kapitel bauen aufeinander auf. Wenn du das erste Mal hier bist, arbeite sie **in Reihenfolge** von oben nach unten ab. Jede Seite endet mit einem **Nächstes Kapitel →** Link, sodass du dich nahtlos durch den ganzen Workflow klicken kannst.

### Workflow-Übersicht

```
Grundlagen → Aufbau → Model → Texture → Animation → Keyframes → Molang
                                                                    ↓
                            Ingame-Test ← Test-Setup ← Export ← Sound ← Particle
```

### 📥 Quick-Download

| Datei | Download |
|-------|----------|
| **Designer-Ordner zum Testen** | [⬇ nrc-cosmetics.zip](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc-cosmetics.zip) |
| **Blockbench-Template** | [⬇ nrc_default_emote_model.bbmodel](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc_default_emote_model.bbmodel) |

Beide Files werden **automatisch** aus dem [Source-Repo](https://github.com/NoRiskClient/nrc-designer-docs) gebaut — bei jeder Änderung gibt's ein neues Release. Alle Versionen: [Releases](https://github.com/NoRiskClient/nrc-designer-docs/releases).

### Kapitel

1. **[Grundlagen](01-Grundlagen)** — Blockbench, GeckoLib & NRC Default Template installieren
2. **[Aufbau](02-Aufbau)** — Das 7-Knochen-System verstehen
3. **[Model](03-Model)** — Cubes & UVs richtig setzen
4. **[Texture](04-Texture)** — Style-Guide (16x / 32x)
5. **[Animation](05-Animation)** — Animation erstellen, Loop-Modi, Timeline
6. **[Keyframes](06-Keyframes)** — Linear vs. Smooth, Bones bewegen
7. **[Molang](07-Molang)** — Funktionen für Idle-Loops & Endzustände
8. **[Particle](08-Particle)** — Snowstorm-Particle einbinden
9. **[Sound](09-Sound)** — Mono-OGGs mit Audacity vorbereiten
10. **[Export](10-Export)** — GeckoLib-Export für Emotes & Cosmetics
11. **[Test-Setup](11-Test-Setup)** — `.norisk.json` schreiben & Files einsortieren
12. **[Ingame-Test](12-Ingame-Test)** — Designer-Commands & Live-Preview

---

→ Starte hier: **[1. Grundlagen](01-Grundlagen)**
