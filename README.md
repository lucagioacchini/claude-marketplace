# Claude Marketplace

A personal plugin marketplace.

[![Claude](https://img.shields.io/badge/Claude-D97757?logo=claude&logoColor=fff)](#)
[![ChatGPT](https://custom-icon-badges.demolab.com/badge/ChatGPT-74aa9c?logo=openai&logoColor=white)](#)

## Installation

### Claude

**Via CLI (Claude Code):** add the marketplace, then install the plugin:

```
/plugin marketplace add lucagioacchini/claude-marketplace
/plugin install culture-compass@personal-marketplace
```

**Via UI (Claude Desktop):**

1. Open the plugins section (**Customize** → **Plugins**).
2. Choose to add a marketplace and enter the GitHub repository `lucagioacchini/claude-marketplace`.
3. Select **Culture Compass** from the marketplace and click **Install**.

### ChatGPT

ChatGPT has no marketplace support, so plugins are installed manually:

1. Zip the plugin folder, e.g. `plugins/culture-compass`:
   ```bash
   cd plugins && zip -r culture-compass.zip culture-compass
   ```
2. Upload the resulting `.zip` file in ChatGPT.

## Plugins

| Plugin | Description |
|---|---|
| [Culture Compass](plugins/culture-compass/README.md) | Companion for going deeper into culture: spoiler-free context before experiencing a work, and itineraries to explore places. |

### Culture Compass skills

| Skill | Description |
|---|---|
| [Opera Context Briefing](plugins/culture-compass/skills/opera-context-briefing/README.md) | Spoiler-free background on a film, book, or series before you experience it. |
| [Travel Map](plugins/culture-compass/skills/travel-map/README.md) | Realistic tourist itineraries with tour-guide-style explanations, a Google Maps route link, and optional local food recommendations. |