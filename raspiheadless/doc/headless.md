# Installation headless

SD Karte mit Rasberry lite (Buster) flashen

leere Datei im Bootverzeichnis anlegen
```
touch /Volumes/boot/ssh
```
wpa_supplicant datei anlegen
```
echo "country=DE
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
    ssid=\"<SSID\"
    psk=\"<Passwort>\"
}" > /Volumes/boot/wpa_supplicant.conf
```

Karte einstecken und Raspi booten