# Launch it as a floating always-on-top window (no chrome UI)
chromium-browser --app=file:///home/gerard/myr-monitor.html \
  --window-size=1200,700 \
  --window-position=100,100 \
  --no-default-browser-check \
  --disable-infobars

For a proper autostart on login (not a daemon — it's a GUI app):

bashmkdir -p ~/.config/autostart
nano ~/.config/autostart/myr-monitor.desktop

[Desktop Entry]
Type=Application
Name=MYR Monitor
Exec=chromium-browser --app=file:///home/gerard/myr-monitor.html --window-size=1200,700
X-GNOME-Autostart-enabled=true
