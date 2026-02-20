# stimme-releases

Stimme release binaries — voice-to-text with a global hotkey.

## Installation

### Check your platform

```bash
uname -m
```

| Output     | Platform              | Asset                          |
|------------|-----------------------|--------------------------------|
| `x86_64` (Linux) | Linux x86_64   | `stimme-linux-x86_64`          |
| `arm64`    | macOS Apple Silicon   | `Stimme-macos-aarch64.zip`     |

### Linux

```bash
curl -fsSL -o stimme https://github.com/masater/stimme-releases/releases/latest/download/stimme-linux-x86_64
chmod +x stimme
./stimme --install
```

### macOS (Apple Silicon)

```bash
curl -fsSL -o Stimme.zip https://github.com/masater/stimme-releases/releases/latest/download/Stimme-macos-aarch64.zip
unzip Stimme.zip -d ~/Applications/
xattr -dr com.apple.quarantine ~/Applications/Stimme.app
~/Applications/Stimme.app/Contents/MacOS/stimme --install
```

The installer opens a graphical setup wizard. After setup, grant
permissions in **System Settings > Privacy & Security**:

1. **Accessibility** — add **Stimme** (not Terminal)
2. **Input Monitoring** — add **Stimme**
3. **Microphone** — will prompt automatically on first use

Stimme starts automatically on login via LaunchAgent.

To run manually:

```bash
~/Applications/Stimme.app/Contents/MacOS/stimme
```

> **Tip:** Add the binary to your PATH so you can just type `stimme`:
> ```bash
> echo 'export PATH="$HOME/Applications/Stimme.app/Contents/MacOS:$PATH"' >> ~/.zshrc
> source ~/.zshrc
> ```

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
stimme --uninstall
```

Or manually:
```bash
pkill stimme
rm -rf ~/Applications/Stimme.app
rm ~/Library/LaunchAgents/com.stimme.daemon.plist
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
