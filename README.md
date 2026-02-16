# stimme-releases

Stimme release binaries — voice-to-text with a global hotkey.

## Installation

### Check your platform

```bash
uname -m
```

| Output     | Platform              | Binary                 |
|------------|-----------------------|------------------------|
| `x86_64` (Linux) | Linux x86_64   | `stimme-linux-x86_64`  |
| `arm64`    | macOS Apple Silicon   | `stimme-macos-aarch64` |

### Linux

```bash
curl -fsSL -o stimme https://github.com/masater/stimme-releases/releases/latest/download/stimme-linux-x86_64
chmod +x stimme
./stimme --install
```

### macOS (Apple Silicon)

```bash
curl -fsSL -o stimme https://github.com/masater/stimme-releases/releases/latest/download/stimme-macos-aarch64
chmod +x stimme
xattr -d com.apple.quarantine stimme
./stimme --install
```

After install, grant permissions in **System Settings > Privacy & Security**:

1. **Accessibility** — add your terminal app (e.g. Terminal.app)
2. **Input Monitoring** — add your terminal app
3. **Microphone** — will prompt automatically on first use

Then quit and reopen Terminal, and run:

```bash
~/.local/bin/stimme
```

> **Note:** On Mac laptops, press **Fn + F9** to trigger the hotkey,
> or enable "Use F1, F2, etc. keys as standard function keys" in
> System Settings > Keyboard.

### Update

```bash
stimme --update
```

### Uninstall

**Linux:**
```bash
stimme --uninstall
```

**macOS:**
```bash
pkill stimme
rm ~/.local/bin/stimme
rm ~/Library/LaunchAgents/com.stimme.plist
rm -rf ~/Library/Application\ Support/stimme
```

## Redistribution and Usage

Stimme is proprietary software. All rights reserved. Binaries are
provided for personal use only. Redistribution is not permitted.

## Disclaimer

THIS SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS
BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN
ACTION OF CONTRACT, TORT, OR OTHERWISE, ARISING FROM, OUT OF, OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR DOWNLOAD THEREOF. USE AT
YOUR OWN RISK.
