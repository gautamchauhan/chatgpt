# ChatGPT Desktop

A lightweight desktop application for Linux that wraps the ChatGPT web interface (chatgpt.com) and provides a native application experience.

![ChatGPT Desktop](https://img.shields.io/badge/version-1.0.0-blue)
![Platform](https://img.shields.io/badge/platform-Linux-orange)
![License](https://img.shields.io/badge/license-MIT-green)

## Features

- ✅ Native desktop application wrapper for ChatGPT
- ✅ Full website functionality preserved
- ✅ Window state persistence (size, position, zoom)
- ✅ Session management (stay logged in)
- ✅ Keyboard shortcuts
- ✅ Application menu with common actions
- ✅ Zoom controls
- ✅ External links open in default browser
- ✅ Multiple package formats (.deb, AppImage)

## Installation

### Ubuntu/Debian (.deb package)

```bash
# Download the .deb package from releases
sudo dpkg -i chatgpt-desktop_1.0.0_amd64.deb

# If there are dependency issues, run:
sudo apt-get install -f
```

### AppImage (Universal)

```bash
# Download the AppImage from releases
chmod +x ChatGPT-Desktop-1.0.0.AppImage
./ChatGPT-Desktop-1.0.0.AppImage
```

## Usage

### Launching the Application

- From application menu: Search for "ChatGPT Desktop"
- From terminal: `chatgpt-desktop` (if installed via .deb)
- From AppImage: Run the AppImage file

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Q` | Quit application |
| `Ctrl+R` | Reload page |
| `Ctrl+M` | Minimize window |
| `Ctrl+Plus` | Zoom in |
| `Ctrl+Minus` | Zoom out |
| `Ctrl+0` | Reset zoom |
| `F11` | Toggle fullscreen |
| `Ctrl+Shift+I` | Toggle Developer Tools |

### Menu Bar

- **File**: Minimize, Quit
- **Edit**: Undo, Redo, Cut, Copy, Paste, Select All
- **View**: Reload, Zoom controls, Fullscreen, Developer Tools
- **Help**: About, GitHub Repository

## Building from Source

### Prerequisites

- Node.js >= 18.x
- npm >= 8.x
- Git

### Steps

```bash
# Clone the repository
git clone https://github.com/gautamchauhan/chatgpt.git
cd chatgpt

# Install dependencies
npm install

# Run in development mode
npm start

# Build packages
npm run build              # Build all packages
npm run build:deb          # Build .deb only
npm run build:appimage     # Build AppImage only
```

The built packages will be in the `dist/` directory.

## System Requirements

- **OS**: Ubuntu 25.10 (or compatible Linux distribution)
- **Architecture**: x64, ARM64
- **RAM**: 4GB minimum, 8GB recommended
- **Disk Space**: 500MB

## Technical Details

### Technology Stack

- **Electron**: Cross-platform desktop application framework
- **electron-store**: Settings and state persistence
- **electron-builder**: Package builder

### Project Structure

```
chatgpt/
├── src/
│   ├── main/           # Main process (Electron)
│   │   └── main.js
│   └── preload/        # Preload scripts
│       └── preload.js
├── assets/
│   └── icons/          # Application icons
├── build/
│   └── icons/          # Build-time icons
├── dist/               # Built packages
├── package.json
├── electron-builder.yml
└── README.md
```

## Troubleshooting

### Application won't start

1. Check if all dependencies are installed:
   ```bash
   sudo apt-get install libgtk-3-0 libnotify4 libnss3 libxss1
   ```

2. Try running from terminal to see error messages:
   ```bash
   chatgpt-desktop
   ```

### Can't log in to ChatGPT

- Clear application data and restart:
  ```bash
  rm -rf ~/.config/chatgpt-desktop
  ```

### High memory usage

- Close unnecessary tabs in other browsers
- Restart the application
- Check system resources with `htop`

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This is an unofficial desktop wrapper for ChatGPT. It is not affiliated with, maintained, authorized, endorsed or sponsored by OpenAI. All product names, logos, and brands are property of their respective owners.

## Acknowledgments

- [Electron](https://www.electronjs.org/) - Framework for building desktop applications
- [OpenAI](https://openai.com/) - For creating ChatGPT
- [electron-builder](https://www.electron.build/) - For building distributable packages

## Support

- **Issues**: [GitHub Issues](https://github.com/gautamchauhan/chatgpt/issues)
- **Discussions**: [GitHub Discussions](https://github.com/gautamchauhan/chatgpt/discussions)

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes.

---

Made with ❤️ by [Gautam Chauhan](https://github.com/gautamchauhan)
