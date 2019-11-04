# Lernziel

* Analyse strukturierter Logfiles anhand eines Online Shops

# Voraussetzungen schaffen

* lokale Docker Installation
* Splunk Trial installiert
* Splunk "Buttercup Games" Shop Logs importiert

## Docker Installation

* https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe
* https://download.docker.com/mac/stable/Docker.dmg

## Splunk Trial installiert

```
$ docker run --rm -d -p 8000:8000 -e "SPLUNK_START_ARGS=--accept-license" -e "SPLUNK_PASSWORD=password" --name splunk splunk/splunk:latest
```

## "Buttercup Games" Shop Logs importieren

* Daten importieren http://docs.splunk.com/images/Tutorial/tutorialdata.zip
* weiter in der Doku https://docs.splunk.com/Documentation/Splunk/8.0.0/SearchTutorial/GetthetutorialdataintoSplunk


