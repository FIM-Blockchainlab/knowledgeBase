# Angular

## Auto compile not working
Von Zeit zu Zeit funktioniert das automatische Kompilieren von Angular funktioniert nicht mehr. Hier helfen folgende zwei Shell befehle.

```
sudo sysctl fs.inotify.max_user_watches=524288
sudo sysctl -p --system
```
