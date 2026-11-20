# NRC Designer Doc

> by **Tinus aka. p2pe** ❤️

Komplette Doku zum Erstellen eigener **Emotes** & **Cosmetics** für **NoRiskClient** — von Blockbench und unserem eigenen Plugin bis zum Ingame-Test.

## 📖 → [Zum Wiki](https://github.com/NoRiskClient/nrc-designer-docs/wiki)

Alle Inhalte (15 Kapitel, Screenshots, Beispiel-GIFs) liegen im Wiki dieses Repos.

## 📥 Downloads

Die Designer-Assets werden bei jedem Update **automatisch** als Release veröffentlicht (rolling `latest`-Tag):

| Datei | Direkt-Download |
|-------|-----------------|
| **Designer-Ordner** (Designer-Rechte, Plugin-Vorlagen) | [⬇ nrc-cosmetics.zip](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc-cosmetics.zip) |
| Altes Blockbench-Template *(nicht mehr nötig)* | [⬇ nrc_default_emote_model.bbmodel](https://github.com/NoRiskClient/nrc-designer-docs/releases/latest/download/nrc_default_emote_model.bbmodel) |

**Blockbench-Plugin:** in Blockbench **File → Plugins → Load Plugin from URL** →
`https://raw.githubusercontent.com/NoRiskClient/nrc-blockbench-plugins/master/plugins/nrc_cosmetics/nrc_cosmetics.js`

> ⚠️ Das Plugin lädt seine Emote-Vorlagen aus `nrc-cosmetics.zip` im `latest`-Release dieses Repos. Repo-Name und Asset-Name nicht ändern.

🔖 Alle Versionen: https://github.com/NoRiskClient/nrc-designer-docs/releases

## Repo-Struktur

```
.
├── README.md
├── designer/
│   └── nrc-cosmetics/          ← Source-Ordner, wird vom Workflow gezippt
├── assets/
│   └── nrc_default_emote_model.bbmodel
├── wiki/                       ← Wiki-Pages (Home, _Sidebar, Kapitel 01-15, images)
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
| 13 | [Cosmetic-Typen](https://github.com/NoRiskClient/nrc-designer-docs/wiki/13-Cosmetic-Typen) |
| 14 | [Referenz](https://github.com/NoRiskClient/nrc-designer-docs/wiki/14-Referenz) |
| 15 | [Blockbench-Plugin](https://github.com/NoRiskClient/nrc-designer-docs/wiki/15-Blockbench-Plugin) |

## Fragen?

Discord-Ticket im [NoRisk Server](https://discord.com/channels/774271756549619722) erstellen — wir erklären alles wichtige.
