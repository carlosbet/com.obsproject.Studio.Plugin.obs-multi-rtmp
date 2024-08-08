# com.obsproject.Studio.Plugin.obs-multi-rtmp

For newer versions of OBS Studio (30.2), manually installed plugins (copy-paste into the config folder) are not supported in Flatpak.

I made this simple repo to shed some light after seeing a Twitch streamer asking for help and after participating in some comments on the issue:

https://github.com/sorayuki/obs-multi-rtmp/issues/436

Please, consider donating to the original project creator (SoraYuki) if this is helpful to you. We all like to see our work appreciated.

https://github.com/sorayuki/obs-multi-rtmp/?tab=readme-ov-file#donate

THANKS ❤️❤️


### Install flatpak-builder (for Debian-based systems):

```
sudo apt install flatpak-builder
```

### Compile into local OSTree flatpak repo:

```
flatpak-builder --install-deps-from=flathub --repo=./localRepo --force-clean build-dir com.obsproject.Studio.Plugin.obs-multi-rtmp.yaml
```

### Install:

```
flatpak --user --runtime install ./localRepo com.obsproject.Studio.Plugin.obs-multi-rtmp
```

### Create a portable flatpak file (Only if you want it for something):

```
flatpak build-bundle --runtime ./localRepo obs-multi-rtmp.flatpak com.obsproject.Studio.Plugin.obs-multi-rtmp stable
```

### Enjoy:

```
flatpak run com.obsproject.studio
```

#### References:

https://github.com/sorayuki/obs-multi-rtmp

https://github.com/flathub/com.obsproject.Studio/wiki/Plugins

https://docs.flatpak.org/en/latest/flatpak-builder-command-reference.html#
