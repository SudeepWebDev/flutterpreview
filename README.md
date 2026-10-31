# Flutter Widget Preview Plugin for Antigravity

[![Antigravity Plugin](https://img.shields.io/badge/Antigravity-Plugin-4285F4)](https://antigravity.google)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)

An interactive **Widget Studio & Preview Canvas** sidecar plugin for Google Antigravity. Renders isolated Flutter widgets and screens with live interactive property controls without having to launch a full mobile emulator or desktop application.

---

## ✨ Features

- ⚡ **Instant Headless Render**: Uses Flutter's test canvas engine (`--no-pub` + `--update-goldens`) to render sharp, pixel-perfect widget snapshots in seconds.
- 🎨 **Font & Glyph Emulation**: Pre-loads Material Icons, Cupertino Icons, and automatically detects Google Fonts and project custom fonts from AST and `pubspec.yaml`, eliminating solid Ahem test blocks.
- 🖼️ **Local Asset & Network Resilience**: Transparently reads disk `assets/` and intercepts image network calls so components never fail due to missing HTTP or asset bundle bounds.
- 🎛️ **Storybook Control Sidebar**:
  - Dynamically extracts constructor parameters (Strings, booleans, colors, enums, numbers, callbacks, domain models).
  - Smart heuristic seeding (e.g. populates realistic names, titles, prices, avatar URLs).
  - Collapsible sidebar (`☰`) and draggable horizontal resizer.
- 📱 **Multi-Device & Responsive Preview**: Switch between mobile and tablet viewports, dark/light themes, and custom text scales.
- 🔄 **Real-Time Project Path Switcher**: Change between Flutter repositories seamlessly from the top toolbar.

---

## 🚀 Installation & Usage

### Installing via Antigravity Plugin Manager
```bash
agy plugin install flutter-widget-preview
```

### Manual Installation
Clone or copy this repository into your local Antigravity plugin directory:
- **Windows**: `%USERPROFILE%\.gemini\config\plugins\flutter-widget-preview`
- **macOS / Linux**: `~/.gemini/config/plugins/flutter-widget-preview`

Then validate and enable the plugin:
```bash
agy plugin validate ~/.gemini/config/plugins/flutter-widget-preview
agy plugin enable flutter-widget-preview
```

---

## 🛠 Project Structure

```
flutter-widget-preview/
├── plugin.json                    # Plugin manifest and capability declarations
├── README.md                      # Documentation & usage guide
├── LICENSE                        # Apache 2.0 License
├── sidecars/
│   └── flutter-preview/
│       ├── sidecar.json           # Aux pane sidecar configuration
│       ├── package.json           # Node environment dependencies
│       ├── server.mjs             # AST scanner, test snapshot runner & HTTP API
│       └── studio.html            # Webview UI (Sidebar, Canvas, Shimmer)
└── skills/
    └── flutter-preview/
        └── SKILL.md               # AI agent instructions for widget preview workflows
```

---

## 📄 License
Licensed under the [Apache License, Version 2.0](LICENSE).
