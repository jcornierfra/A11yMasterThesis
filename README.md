# Comment implémenter les pratiques inclusives dans le Continuous Delivery Pipeline ?

Microsoft Skills Evolution Program, CentraleSupélec, Promotion 2018-2019

## Introduction

Ce Mémoire clôture ma formation "Expert en ingénierie numérique (MS)" – [RNCP code 15274](https://www.francecompetences.fr/recherche/rncp/15274/), niv. 1 Fr, 7 EU, délivrée en 2018-2019 par L'Ecole CentraleSupélec.

Le sujet porte sur la prise en compte des situations de handicap dans le cadre de la transformation numérique des Entreprises, avec un focus particulier sur la partie technique pour l'implémentation de tests d'accessibilités dans un modèle DevOps d'intégration et de déploiement continu.

Pour cette étude, un prototype a été réalisé comme "proof of concept" afin de démontrer la faisabilité technique. Ce dépôt contient les informations permettant de reproduire ce prototype.

### Résumé du Mémoire

La prise en compte de la diversité et en particulier des personnes en situation de handicap est devenu une priorité sociale et politique. Cela se traduit par le renforcement des lois s’appuyant sur des référentiels d’accessibilité numérique très complets.

Au même moment la transformation digitale oblige les entreprises à multiplier les solutions numériques et à adopter des stratégies de livraison continue de mises à jour. Comment l’entreprise peut-elle satisfaire aux exigences d’accessibilité dans ce contexte ?

Nous dresserons un état de l’art de l’accessibilité. Puis nous étudierons en théorie et en pratique comment intégrer l’accessibilité dès la conception d’une solution et comment s’assurer que la chaîne DevOps dans un modèle agile dispose des moyens permettant de garantir cette accessibilité tout au long du cycle de vie du produit.

## Prototype

Pour la plateforme de démonstration, le prototype a été développé en deux versions :
* Application Web "classique" dans Azure (Web App)
* Application en Container Docker Linux stocké dans Azure Container Registry

Pipeline DevOps pour la version classique | Pipeline DevOps pour la version Docker
-|-
![Web App Classique](https://github.com/jcornierfra/A11yMasterThesis/blob/master/Screenshots/WebAppClassic.png "Web App Classique") | ![Web App Docker](https://github.com/jcornierfra/A11yMasterThesis/blob/master/Screenshots/WebAppDocker.png "Web App Docker")

## Pré-requis

Les prérequis concernent la construction du prototype :

* Souscription Azure
  * Azure DevOps
* Microsoft Visual Studio

## Fabriqué avec

Les programmes/logiciels/ressources utilisés pour rédiger ce Mémoire et construire le Prototype :

### Mémoire
* [Microsoft 365](https://www.microsoft.com/fr-fr/microsoft-365) - Texte et présentation
* [Zotero](https://www.zotero.org/) - Gestion des références avec intégration dans Word et les Navigateurs Web (facultatif pour la lecture du document)

### Prototype
* [Visual Studio](https://visualstudio.microsoft.com/fr/) - EDI utilisé pour l'application test du prototype
* [Microsoft Azure](https://azure.microsoft.com/fr-fr/) - Cloud Microsoft utilisé pour le pipeline DevOps et pour héberger l'application de test
* [GitHub](https://github.com/) - Dépôt utilisé pour la source logicielle du prototype, Chaque modification entraîne une exécution des tâches du pipeline DevOps
* [Docker Desktop](https://www.docker.com/products/docker-desktop) - Pour la version en container du prototype (Cf. Configuration du prototype.docx)
* Machine virtuelle (Windows) de test d'accessibilité pour le pipeline
  * [Firefox](https://www.mozilla.org/fr/firefox/new/) - Navigateur utilisé par le dispositif de test d'accessibilité
  * [Gecko driver](https://github.com/mozilla/geckodriver/) - API HTTP permettant d'interagir automatiquement avec Firefox pour les tests d'accessibilité
  * [node.js](https://nodejs.org/en/) - Environnement Javascript utilisé par l'API axe-core implémentée par le module DevOps de test d'accessibilité
  * [A11yVMAgent](https://marketplace.visualstudio.com/items?itemName=DrewLewis.Accessibility) - Module de test d'accessibilité intégré au pipeline "Release" d'Azure DevOps
    * [API axe-core](https://github.com/dequelabs/axe-core) - API du moteur de test Open Source Deque Axe implémenté dans l'Agent DevOps

### Dépôt
* [Visual Studio Code](https://code.visualstudio.com/docs/languages/markdown) - VS Code et les extensions markdown pour la création de ce README.md

## Mots clés
Accessibilité, accessibility, A11y, WCAG, RGAA

## Versions

Version disponible :

- **Dernière version :** 1.1 Avril 2019

## Auteur

Mémoire rédigé par :

* **Jérôme Cornier** _alias_ [@jcornierfra](https://github.com/jcornierfra/)

## License

Ce projet est sous licence ``AGPL - GNU Affero General Public License v3.0`` - voir le fichier [LICENSE.md](LICENSE.md) pour plus d'informations.
