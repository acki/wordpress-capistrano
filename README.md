# Wordpress Capistrano Deploy

Einfaches Deployment für Wordpress Seiten.

## Voraussetzungen
1. Production- und Staging-Server müssen über ssh zugänglich sein
2. git muss unter allen Umgebungen installiert sein
2. wp-cli muss sowohl lokal als auch remote installiert sein (http://wp-cli.org/#install)

## Setup
Damit das Capistrano deployment läuft, müssen ein paar Vorbereitungen getroffen werden.
Sowohl lokal, als auch auf den Staging oder Production Servern:

### Lokal
1. Capistrano muss installiert sein: `bundler install`
2. local-config.SAMPLE.php muss in local-config.php umbenannt werden und es müssen die Zugangsdaten für die lokale Datenbank eingetragen sein
3. Die config.SAMPLE.rb im Ordner config muss in config.rb umbenannt werden und für jede Stage müssen die entsprechend Datenbankzugangsdaten eingetragen werden
4. Im Ordner config/deploy müssen für jede benutzte Stage die entsprechende Datei umbenannt und angepasst werden

## Todo
* Wordpress Multisite Deployment
* Sync von Upload-Ordnern
* Möglichkeit Wordpress als Submodule einzubinden