# Splunk

## Lernziel

* Analyse strukturierter Logfiles eines Online Shops mit Hilfe von Splunk

## Voraussetzungen schaffen

* lokale Docker Installation
* Splunk Trial installiert
* Splunk "Buttercup Games" Shop Logs importiert

### Docker Installation

* Windows: https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe
* MacOS: https://download.docker.com/mac/stable/Docker.dmg

### Splunk Trial installieren

```
$ docker run --rm -d -p 8000:8000 -e "SPLUNK_START_ARGS=--accept-license" -e "SPLUNK_PASSWORD=bootcamp" --name splunk splunk/splunk:latest
```

* Testen mit

```
$ docker ps
CONTAINER ID        IMAGE                  COMMAND                  CREATED              STATUS                        PORTS                                                                           NAMES
9396350d7309        splunk/splunk:latest   "/sbin/entrypoint.sh…"   About a minute ago   Up About a minute (healthy)   8065/tcp, 8088-8089/tcp, 8191/tcp, 9887/tcp, 0.0.0.0:8000->8000/tcp, 9997/tcp   splunk
```

* [Browser Öffnen](http://localhost:8000/en-GB/account/login)
* Login mit _admin_/_bootcamp_

### "Buttercup Games" Shop Logs importieren

* Demo Daten herunterladen http://docs.splunk.com/images/Tutorial/tutorialdata.zip
* Demo Daten mal auspacken und ansehen (z.B `www1/access.log` oder `www1/secure.log`)
* weiter in der Doku https://docs.splunk.com/Documentation/Splunk/7.3.2/SearchTutorial/GetthetutorialdataintoSplunk

# Prometheus

Installation und Test des `prometheus-node-exporter` (Exporter for machine metrics)

```
$ sudo apt-get install -y prometheus-node-exporter curl
$ prometheus-node-exporter &
$ curl -s localhost:9100/metrics
```

