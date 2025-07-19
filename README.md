# 0xNiri

Personal dotfiles for the [Niri](https://github.com/YaLTeR/niri) Wayland compositor.

> 🎨 Theme: [Catppuccin Mocha](https://github.com/catppuccin)

## ✨ Features

- Waybar auto-hide script.
- Consistent **Catppuccin Mocha** theme across all apps.
- Full desktop-like experience on a minimal **Niri** setup.

## 🧰 Tools & Utilities

| Category | Application |
| - | - |
| Compositor | [`niri`](https://github.com/YaLTeR/niri) |
| Bar | [`waybar`](https://github.com/Alexays/Waybar) |
| Terminal | [`kitty`](https://github.com/kovidgoyal/kitty) |
| Notification | [`swaync`](https://github.com/ErikReider/SwayNotificationCenter) |
| Wallpaper Manager | [`swaybg`](https://github.com/swaywm/swaybg) / [`swww`](https://github.com/LGFae/swww) |
| Clipboard Manager | [`cliphist`](https://github.com/sentriz/cliphist) |
| Launcher | [`fuzzel`](https://codeberg.org/dnkl/fuzzel) |
| Power Menu | [`wlogout`](https://github.com/ArtsyMacaw/wlogout) |
| Screen Locker | [`gtklock`](https://github.com/jovanlanik/gtklock) |
| On-Screen Display | [`avizo`](https://github.com/heyjuvi/avizo) |
| File Manager | [`nautilus`](https://gitlab.gnome.org/GNOME/nautilus) / [`yazi`](https://github.com/sxyazi/yazi) |
| Shell | [`fish`](https://github.com/fish-shell/fish-shell) |
| Display Manager | [`ly`](https://github.com/fairyglade/ly)

## 📦 Installation

> [!WARNING]
> The install script is WIP.

> [!NOTE]
> This setup is intended for Arch-based distributions.

### Clone the repo
```bash
git clone https://github.com/rickinshah/niri-dotfiles ~/.dotfiles
cd ~/.dotfiles
```

### Run the install script
```bash
chmod +x install.sh
./install.sh
```

This will:

- Install all required packages from `packages.txt`.
- Set up ~/.config with symlinks.
- Create necessary folders and permissions.
- Set up systemd user services for Niri session.

## 🔧 Startup Applications

Startup applications are managed using `systemd` — as recommended in [official Niri documentation](https://github.com/YaLTeR/niri/wiki/Example-systemd-Setup)

Custom unit files are stored in: `~/.config/systemd/user`

> [!NOTE]
> Some systemd services and custom keybindings rely on scripts stored in `~/.local/bin`. Make sure it's present in your `$PATH`.

Enable services with:
```bash
systemctl --user add-wants niri.service <service>.service
```

For example:
```bash
systemctl --user add-wants niri.service waybar.service
systemctl --user add-wants niri.service avizo.service
```

## 📚 Credits

- [Wallpapers](https://github.com/orangci/walls-catppuccin-mocha)
