ScoreDrop Unity Package

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Unity Version](https://img.shields.io/badge/Unity-2020.3%2B-blue)](https://unity.com)
[![GitHub Release](https://img.shields.io/github/v/release/Guardabarrancos/scoredrop-unity)](https://github.com/Guardabarrancos/scoredrop-unity/releases)

Official Unity integration for [ScoreDrop](https://leaderboard-game.vercel.app) - A simple, modern leaderboard API for indie games.

Features

- **Ready-to-use UI** - Prefab with leaderboard, name editing, and score simulation
- **Automatic player identification** - Each player gets a unique `player_id` stored in PlayerPrefs
- **Live leaderboard** - Paginated display with current player highlighting
- **Name editing** - Players can change their display name
- **Score simulation** - Built-in +10 button for testing (replace with your game logic)
- **Persistent data** - Player name and best score saved locally
- **Multi-platform** - Works on all platforms Unity supports

Installation

Via Unity Package Manager (UPM)
1. Open Unity and go to `Window > Package Manager`
2. Click the `+` button and select "Add package from git URL"
3. Enter: `https://github.com/Guardabarrancoestudio/scoredrop-unity.git`

Manual Installation
1. Download the latest release from [Releases](https://github.com/Guardabarrancos/scoredrop-unity/releases)
2. Import the `.unitypackage` into your project

Quick Start

1. Add the Manager
- Drag the `ScoreDropManager` prefab into your first scene, OR
- Add the `ScoreDropManager` component to any GameObject

2. Configure API Keys
In the Inspector, set your:
- **API Key** (from your leaderboard)
- **Leaderboard ID** (UUID from your leaderboard)

3. Add the UI
- Drag the `ScoreDropCanvas` prefab into your scene
- In the Inspector, assign the references:
  - `Name HUD`: Text that shows player name
  - `Score HUD`: Text that shows current score
  - `Player Name Input`: Input field for editing
  - `Leaderboard Container`: Where scores will appear
  - `Score Entry Prefab`: Your leaderboard entry prefab
  - All buttons (Submit, Refresh, Next, Prev, Edit Name, Add Score)

4. Run the Demo
- Open the `DemoScene` to see a working example
- Test adding scores, editing name, and submitting

🎮 How It Works

Player Flow
1. **First launch**: Player gets default name (e.g., "Player5824")
2. **Add Score (+10)**: Increases local score (simulate gameplay)
3. **Submit**: Sends current score to ScoreDrop API
4. **Edit Name**: Changes display name (saved on next submit)

API Integration
- `player_id` is automatically generated and persisted
- Scores only update if higher than previous best
- Clear feedback messages for each outcome

Documentation

For detailed API documentation, visit [ScoreDrop API Docs](https://leaderboard-game.vercel.app/docs_api.html)

Contributing

Contributions are welcome! Feel free to:
- Report issues
- Suggest features
- Submit pull requests

Contact

- Email: Guardabarrancoestudioapp@gmail.com
- Website: [ScoreDrop](https://leaderboard-game.vercel.app)
- Website: [Guardabarranco](https://voxelplayercontroller.lat/)

License

MIT License - see [LICENSE](LICENSE.txt) file for details

---

**Made with for indie game developers**
