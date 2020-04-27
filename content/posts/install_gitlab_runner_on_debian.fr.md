+++
draft = true
date = 2020-04-19T10:00:17+02:00
title = "Installation GitLab Runner sur Debian"
tags = [ "debian", "gitlab", "runner", "buster" ]
categories = [ "gitlab" ]
+++

## Installation GitLab Runner sur Debian

* Ajout du repository officiel GitLab

```bash
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh | sudo bash
```

* Installation de la dernière version de GitLab Runner

```bash
sudo apt-get install gitlab-runner
```
* [Enregistrer le Runner](https://docs.gitlab.com/runner/register/index.html)

## Erreurs sur Debian 10 Buster

Runner executor de type shell

```bash
 Running with gitlab-runner 12.9.0 (4c96e5ad)
   on xxx
Preparing the "shell" executor
00:00
 Using Shell executor...
Preparing environment
00:00
 Running on xxx..
Uploading artifacts for failed job
00:00
 bash: line 98: cd: /home/gitlab-runner/builds/ugz-uvsS/0/bauguste/docker-multiarch-builder: No such file or directory
 ERROR: Job failed: exit status 1
 ```

Pour résoudre cette erreur il faut supprimer le fichier `.bash_logout` de l'utilisateur **gitlab-runner**

```bash 
rm /home/gitlab-runner/.bash_logout 
```

## Références

* [https://docs.gitlab.com/runner/install/linux-repository.html](https://docs.gitlab.com/runner/install/linux-repository.html)
