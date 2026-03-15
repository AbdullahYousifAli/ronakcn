<p align="center">
  <img src="https://ronakcn.softisn.com/logo.svg" width="120" alt="RonakCN Logo" />
</p>

<h1 align="center">RonakCN</h1>

<p align="center">
  <strong>ڕۆناک — Light for Flutter UI</strong>
</p>

<p align="center">
  Beautiful, copy-paste Flutter components inspired by ShadCN/ui.<br/>
  Drop-in widgets with a CLI registry — no package install needed.
</p>

<p align="center">
  <a href="https://ronakcn.softisn.com">Documentation</a> ·
  <a href="https://ronakcn.softisn.com/components">Components</a> ·
  <a href="https://github.com/AbdullahYousifAli/ronakcn/issues">Report Bug</a> ·
  <a href="https://github.com/AbdullahYousifAli/ronakcn/issues">Request Component</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-3.x-02569B?logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Dart-3.x-0175C2?logo=dart&logoColor=white" alt="Dart" />
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License" />
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome" />
  <img src="https://img.shields.io/github/stars/AbdullahYousifAli/ronakcn?style=social" alt="Stars" />
</p>

---

## What is RonakCN?

**RonakCN** (ڕۆناک — Kurdish for "light/bright") is a collection of beautiful, accessible Flutter components that you **copy and paste** into your project. Inspired by [shadcn/ui](https://ui.shadcn.com/) for React.

**This is NOT a package you install.** Instead, you use the CLI to add individual component source files directly into your codebase. You own the code. You customize it however you want.

### Why RonakCN?

- 🎨 **Not a package** — Components live in YOUR project. No dependency lock-in.
- 📋 **Copy & Paste** — Use the CLI or manually copy. The code is yours.
- 🌗 **Dark mode** — Every component supports light and dark themes out of the box.
- 🔄 **RTL-first** — Built-in support for Arabic, Kurdish, Persian, and Hebrew.
- 📱 **Cross-platform** — Works on Android, iOS, Web, macOS, Windows, and Linux.
- 🎯 **Accessible** — Keyboard navigation and screen reader support.
- ⚡ **No bloat** — Only add what you need. No unused code in your bundle.

---

## Quick Start

### 1. Install the CLI

```bash
dart pub global activate ronakcn
```

### 2. Initialize in your Flutter project

```bash
ronakcn init
```

This creates a `ronakcn.json` config file and sets up the theme:

```
lib/
  components/
    ui/          ← Components go here
  theme/
    ronak_theme.dart
    ronak_colors.dart
```

### 3. Add components

```bash
ronakcn add button
ronakcn add card
ronakcn add dialog
```

### 4. Use them in your app

```dart
import 'package:your_app/components/ui/button.dart';
import 'package:your_app/theme/ronak_theme.dart';

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return RonakApp(
      theme: RonakTheme.light(),
      darkTheme: RonakTheme.dark(),
      child: Scaffold(
        body: Center(
          child: RonakButton(
            onPressed: () {},
            variant: ButtonVariant.primary,
            child: Text('Get Started'),
          ),
        ),
      ),
    );
  }
}
```

---

## Components

> 🚧 **Work in Progress** — We're building components one by one with care and quality.

### Available Now

| Component | Description | Status |
|-----------|-------------|--------|
| Theme | Design token system with light/dark mode | 🟢 Ready |
| Button | Clickable button with 6 variants | 🟡 Building |
| Badge | Status indicator with variants | 🟡 Building |
| Card | Content container with header/footer | 🟡 Building |

### Coming Soon

| Component | Description | Status |
|-----------|-------------|--------|
| Input | Text field with labels and validation | ⬜ Planned |
| Avatar | User image with fallback | ⬜ Planned |
| Switch | Toggle on/off | ⬜ Planned |
| Checkbox | Check/uncheck with indeterminate | ⬜ Planned |
| Dialog | Modal dialog with backdrop | ⬜ Planned |
| Dropdown | Menu with items and sub-menus | ⬜ Planned |
| Tabs | Tabbed content panels | ⬜ Planned |
| Toast | Notification popup | ⬜ Planned |
| Select | Single-select dropdown | ⬜ Planned |
| Accordion | Expandable sections | ⬜ Planned |
| Separator | Visual divider | ⬜ Planned |
| Skeleton | Loading placeholder | ⬜ Planned |
| Progress | Progress bar/ring | ⬜ Planned |
| Tooltip | Hover information popup | ⬜ Planned |
| Sheet | Bottom sheet / side sheet | ⬜ Planned |
| Data Table | Sortable, filterable table | ⬜ Planned |
| Calendar | Date display widget | ⬜ Planned |
| Date Picker | Date selection | ⬜ Planned |
| Command | Command palette / search | ⬜ Planned |
| Form | Form with validation | ⬜ Planned |

---

## Theming

RonakCN uses a token-based design system. Customize everything:

```dart
final myTheme = RonakTheme(
  colors: RonakColors(
    background: Color(0xFFFFFFFF),
    foreground: Color(0xFF0F172A),
    primary: Color(0xFF0F172A),
    primaryForeground: Color(0xFFF8FAFC),
    secondary: Color(0xFFF1F5F9),
    muted: Color(0xFFF1F5F9),
    accent: Color(0xFFF1F5F9),
    destructive: Color(0xFFEF4444),
    border: Color(0xFFE2E8F0),
    ring: Color(0xFF0F172A),
  ),
  radius: RonakRadius.md,  // none, sm, md, lg, xl, full
  spacing: RonakSpacing.default,
);
```

### Pre-built Themes

```bash
ronakcn init --theme default    # Clean and minimal
ronakcn init --theme slate      # Cool gray tones
ronakcn init --theme rose       # Warm rose accents
ronakcn init --theme emerald    # Nature-inspired greens
```

---

## CLI Reference

| Command | Description |
|---------|-------------|
| `ronakcn init` | Initialize RonakCN in your Flutter project |
| `ronakcn add <component>` | Add a component to your project |
| `ronakcn add --all` | Add all available components |
| `ronakcn list` | List all available components |
| `ronakcn update <component>` | Update a component to latest version |
| `ronakcn diff` | Show changes since last update |
| `ronakcn theme` | Regenerate theme files |

---

## How It Works

RonakCN is built on a **registry model**, similar to shadcn/ui:

```
┌─────────────┐     ┌──────────────┐     ┌─────────────────┐
│  ronakcn.dev │────▶│  Registry    │────▶│  Your Project   │
│  (website)   │     │  (JSON API)  │     │                 │
└─────────────┘     └──────────────┘     │  lib/           │
                           │              │  ├── components/ │
                    ┌──────┴──────┐       │  │   └── ui/     │
                    │  CLI Tool   │──────▶│  │       ├── button.dart
                    │  ronakcn    │       │  │       ├── card.dart
                    └─────────────┘       │  │       └── ...  │
                                          │  └── theme/      │
                                          │      └── ronak_theme.dart
                                          └─────────────────┘
```

1. The **registry** is a JSON file that maps component names to their source files
2. The **CLI** reads the registry, resolves dependencies, and downloads files
3. **Components** are placed directly in your project — you own the code
4. The **theme** is a set of design tokens that all components reference

---

## RTL Support

Every component is built with RTL (right-to-left) support. Perfect for Arabic, Kurdish, Persian, and Hebrew apps:

```dart
RonakApp(
  theme: RonakTheme.light(),
  textDirection: TextDirection.rtl,  // Enable RTL
  child: MyApp(),
);
```

All padding, margins, icons, and layouts automatically flip for RTL.

---

## What Makes RonakCN Different?

| Feature | RonakCN | shadcn_flutter | shadcn_ui |
|---------|---------|----------------|-----------|
| Installation | Copy-paste via CLI | pub.dev package | pub.dev package |
| Code ownership | You own it | Dependency | Dependency |
| Customization | Edit source directly | Theme overrides | Theme overrides |
| RTL support | First-class | Basic | Basic |
| CLI tool | ✅ | ❌ | ❌ |
| Registry model | ✅ | ❌ | ❌ |
| Tree-shaking | Natural (only what you add) | Framework handles it | Framework handles it |

---

## Project Structure

When you add components, your project looks like this:

```
your_flutter_app/
├── lib/
│   ├── components/
│   │   └── ui/
│   │       ├── button.dart
│   │       ├── card.dart
│   │       ├── badge.dart
│   │       └── ... (only what you added)
│   ├── theme/
│   │   ├── ronak_theme.dart
│   │   ├── ronak_colors.dart
│   │   ├── ronak_typography.dart
│   │   └── ronak_radius.dart
│   └── main.dart
├── ronakcn.json          ← CLI config
└── pubspec.yaml
```

---

## Contributing

We love contributions! RonakCN is built by the community, for the community.

- 🐛 [Report a bug](https://github.com/AbdullahYousifAli/ronakcn/issues)
- 💡 [Request a component](https://github.com/AbdullahYousifAli/ronakcn/issues)
- 🔧 [Submit a PR](https://github.com/AbdullahYousifAli/ronakcn/pulls)

See our [Contributing Guide](CONTRIBUTING.md) for details.

---

## Roadmap

- [x] Project setup and branding
- [ ] Theme system (design tokens, light/dark mode)
- [ ] Core components (Button, Card, Badge)
- [ ] CLI tool (init, add, list)
- [ ] Registry API
- [ ] Documentation website
- [ ] 10 core components for v1.0
- [ ] Theme playground (interactive customizer)
- [ ] VS Code extension
- [ ] Figma design kit

---

## The Name

**Ronak** (ڕۆناک) means **"light"** or **"bright"** in Kurdish (Sorani).

ShadCN comes from **"shadow"** — so RonakCN is its complement: **light**.

Built with ❤️ from Kurdistan.

---

## License

MIT License — see [LICENSE](LICENSE) for details.

Free to use in personal and commercial projects.

---

<p align="center">
  <strong>RonakCN — ڕۆناک — Bringing light to Flutter UI.</strong>
</p>
