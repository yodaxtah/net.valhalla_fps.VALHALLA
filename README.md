# VALHALLA Flatpak package

To install this package for VALHALLA, open a terminal and execute the following commands:

```
git clone https://github.com/yodaxtah/net.valhalla_fps.VALHALLA.git
cd net.valhalla_fps.VALHALLA
```

Next, follow the following standard flatpak workflow to install the package locally using `flatpak`.

1. install the **FLATPAK** build tools 
   ```
   flatpak install -y flathub org.flatpak.Builder
   ```

1. add the flatpak repo (slightly different to the command for flatpak setup)
   ```
   flatpak remote-add --if-not-exists --user flathub https://dl.flathub.org/repo/flathub.flatpakrepo
   ```

1. run the build tool on the manifest
   ```
   flatpak run --command=flathub-build org.flatpak.Builder --install net.valhalla_fps.VALHALLA.yaml
   ```

1. test the package **IN THE TERMINAL** to see potential issues
   ```
   flatpak run net.valhalla_fps.VALHALLA
   ```

See https://docs.flathub.org/docs/for-app-authors/submission for more up-to-date information.
