# NRC Designer Doc

> by **Tinus aka. p2pe** ❤️

Komplette Doku zum Erstellen eigener **Emotes** & **Cosmetics** für **NoRiskClient** — von Blockbench-Setup über GeckoLib-Export bis zum Ingame-Test.

## 📖 → [Zum Wiki](https://github.com/NoRiskClient/nrc-designer-docs/wiki)

Alle Inhalte (12 Kapitel, Screenshots, Beispiel-GIFs) liegen im Wiki dieses Repos.

## 📥 Downloads

Die Designer-Assets werden bei jedem Update **automatisch** als Release veröffentlicht (rolling `latest`-Tag):

| Datei | Direkt-Download |
|-------|-----------------|
| **Blockbench-Template** | [⬇ nrc_default_emote_model.bbmodel](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc_default_emote_model.bbmodel) |
| **Designer-Ordner (zum Testen)** | [⬇ nrc-cosmetics.zip](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc-cosmetics.zip) |

🔖 Alle Versionen: https://github.com/NoRiskClient/nrc-designer-docs/releases

## Repo-Struktur

```
.
├── README.md
├── designer/
│   └── nrc-cosmetics/          ← Source-Ordner, wird vom Workflow gezippt
├── assets/
│   └── nrc_default_emote_model.bbmodel
├── wiki/                       ← Wiki-Pages (Home, _Sidebar, Kapitel 01-12, images)
│                                  wird automatisch ins .wiki.git gespiegelt
└── .github/workflows/
    ├── release.yml             ← zippt designer/ + bbmodel → Release "latest"
    └── sync-wiki.yml           ← pusht wiki/ → <repo>.wiki.git
```

> 💡 **Ein Branch, ein Remote.** Alle Änderungen (Doku ODER Assets) gehen auf `main` in diesem Repo. Die zwei Workflows kümmern sich um Release + Wiki-Sync.

### Quick-Links

| Kapitel | |
|---|---|
| 1 | [Grundlagen](https://github.com/NoRiskClient/nrc-designer-docs/wiki/01-Grundlagen) |
| 2 | [Aufbau](https://github.com/NoRiskClient/nrc-designer-docs/wiki/02-Aufbau) |
| 3 | [Model](https://github.com/NoRiskClient/nrc-designer-docs/wiki/03-Model) |
| 4 | [Texture](https://github.com/NoRiskClient/nrc-designer-docs/wiki/04-Texture) |
| 5 | [Animation](https://github.com/NoRiskClient/nrc-designer-docs/wiki/05-Animation) |
| 6 | [Keyframes](https://github.com/NoRiskClient/nrc-designer-docs/wiki/06-Keyframes) |
| 7 | [Molang](https://github.com/NoRiskClient/nrc-designer-docs/wiki/07-Molang) |
| 8 | [Particle](https://github.com/NoRiskClient/nrc-designer-docs/wiki/08-Particle) |
| 9 | [Sound](https://github.com/NoRiskClient/nrc-designer-docs/wiki/09-Sound) |
| 10 | [Export](https://github.com/NoRiskClient/nrc-designer-docs/wiki/10-Export) |
| 11 | [Test-Setup](https://github.com/NoRiskClient/nrc-designer-docs/wiki/11-Test-Setup) |
| 12 | [Ingame-Test](https://github.com/NoRiskClient/nrc-designer-docs/wiki/12-Ingame-Test) |

## Fragen?

Discord-Ticket im [NoRisk Server](https://discord.com/channels/774271756549619722) erstellen — wir erklären alles wichtige.
