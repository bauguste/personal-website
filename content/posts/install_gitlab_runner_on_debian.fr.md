+++ 
draft = true
date = 2020-04-19T10:00:17+02:00
title = "Installation GitLab Runner sur Debian"
description = ""
slug = "install_gitlab_runner_on_debian" 
tags = [ "debian", "gitlab", "runner" ]
categories = [ "gitlab" ]
+++
## Installation GitLab Runner sur Debian
1. Ajout du repository officiel GitLab
```bash
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh | sudo bash
```
2. Installation de la dernière version de GitLab Runner
```bash
sudo apt-get install gitlab-runner
```
3. [Enregistrer le Runner](https://docs.gitlab.com/runner/register/index.html)

## Références
* [https://docs.gitlab.com/runner/install/linux-repository.html](https://docs.gitlab.com/runner/install/linux-repository.html)
