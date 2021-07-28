# TYPO3 CMS 10 LTS - Typo3 Extbase Extension

![alt text](https://sonarqube.xima.local/api/project_badges/measure?project=Typo3 Extbase Extension&metric=alert_status)
![alt text](https://sonarqube.xima.local/api/project_badges/measure?project=Typo3 Extbase Extension&metric=security_rating)
![alt text](https://sonarqube.xima.local/api/project_badges/measure?project=Typo3 Extbase Extension&metric=reliability_rating)
![alt text](https://sonarqube.xima.local/api/project_badges/measure?project=Typo3 Extbase Extension&metric=coverage)
[SonarCube](https://sonarqube.xima.local/dashboard?id=Typo3 Extbase Extension)

## Inhalt
* [Wozu dient das Projekt?](#intro)
* [Technische Dokumentation](#technical-doc)
* [Installation](#installtion)
* [Deployment](#deployment)
    * [RSYNC](#deployment-rsync)

<a name="intro"></a>
## Wozu dient das Projekt?

Dieses Projekt ist das TYPO3 Basisprojekt für die Webseite [www.typo3-extbase-extension.de ](www.typo3-extbase-extension.de ).

<a name="technical-doc"></a>
## Technische Dokumentation
* Die Technische Dokumentation befindet sich im [Confluence](n).

<a name="installtion"></a>
## Installation

1. Git-Repository klonen:

    ````shell script
    $ git clone https://github.com/JGN5496/typo3-extbase-extension.git
    ````

2. Lokale Entwicklungsumgebung, wie unter [.ddev/README.md](.ddev/README.md) beschrieben, einrichten.

<a name="deployment"></a>
## Deployment

Das Deployment erfolgt mittles [GitLab-CI](https://docs.gitlab.com/ee/ci/) und dem Tool 
[Phing Typo3 Deployer](https://github.com/hirnsturm/phing-typo3-deployer). Die Konfiguration ist in der 
Datei `.gitlab-ci.yml` zu finden.

<a name="deployment-rsync"></a>
#### RSYNC

Die Konfiguration der RSYNC-Excludes erfolgt je Stage in den folgenden Dateien:

```bash
deployment/rsync/
    dev_exclude.txt
    prod_exclude.txt
    stage_exclude.txt
```