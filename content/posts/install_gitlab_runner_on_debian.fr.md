+++ 
draft = false
date = 2020-04-19T10:00:17+02:00
title = "Installation GitLab Runner sur Debian"
description = ""
slug = "install_gitlab_runner_on_debian" 
tags = [ "debian", "gitlab", "runner" ]
categories = [ "gitlab" ]
+++

## Installation GitLab Runner sur Debian

* Ajout du repository officiel GitLab

{{< highlight shell >}}
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh | sudo bash
{{< /highlight >}}

* Installation de la dernière version de GitLab Runner

{{< highlight shell >}}
sudo apt-get install gitlab-runner
{{< /highlight >}}

* [Enregistrer le Runner](https://docs.gitlab.com/runner/register/index.html)

## Références

* [https://docs.gitlab.com/runner/install/linux-repository.html](https://docs.gitlab.com/runner/install/linux-repository.html)
