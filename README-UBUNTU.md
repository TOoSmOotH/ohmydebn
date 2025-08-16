# Ubuntu Support for OhMyDebn

OhMyDebn now includes experimental support for Ubuntu with Cinnamon desktop environment.

## Usage

To install OhMyDebn on Ubuntu, you MUST use the `--ubuntu` flag:

```bash
# Download and run the installer with Ubuntu flag
curl -O https://raw.githubusercontent.com/dougburks/ohmydebn/refs/heads/main/install.sh
bash install.sh --ubuntu
```

You can combine it with other flags:

```bash
bash install.sh --ubuntu --no-uninstall
```

**Important**: Without the `--ubuntu` flag, the script will exit with an error message saying it's only for Debian 13.

## Configuration

OhMyDebn automatically creates a configuration file at `~/.config/ohmydebn/ohmydebn.conf` on first run. You can edit this file to customize the installation:

```bash
# Whether to replace the desktop background
REPLACE_BACKGROUND=true

# Whether to install themes
INSTALL_THEMES=true

# Whether to remove unnecessary packages
REMOVE_PACKAGES=true

# Whether to install Nerd Fonts
INSTALL_FONTS=true
```

## Differences from Debian

When running in Ubuntu mode, OhMyDebn makes the following adjustments:

1. **Package Names**: Uses Ubuntu-specific package names (e.g., `chromium-browser` instead of `chromium`)
2. **Themes**: Installs Nordic theme (blue-grey aesthetic) and Papirus icons instead of Mint themes
3. **Repository Configuration**: Skips Debian repository configuration
4. **OS Check**: Verifies Ubuntu instead of Debian 13

## Tested On

- Ubuntu 22.04 LTS with Cinnamon
- Ubuntu 24.04 LTS with Cinnamon

## Known Limitations

- Some features may work differently on Ubuntu compared to Debian
- Mint themes are not available on Ubuntu (uses Nordic theme instead for a cohesive blue-grey look)
- Package availability may vary between Ubuntu versions

## Troubleshooting

If you encounter issues:

1. Check that you have Cinnamon desktop environment installed
2. Ensure you're running the script with the `--ubuntu` flag
3. Review the configuration file at `~/.config/ohmydebn/ohmydebn.conf`
4. Check package names if installation fails (some packages might have different names in Ubuntu)