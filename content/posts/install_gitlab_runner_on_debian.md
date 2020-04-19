+++ 
draft = false
date = 2020-04-19T10:00:17+02:00
title = "Install GitLab Runner on Debian"
description = ""
slug = "install_gitlab_runner_on_debian" 
tags = [ "debian", "gitlab", "runner" ]
categories = [ "gitlab" ]
+++

## Install GitLab Runner on Debian

*  Add GitLab’s official repository:

{{< highlight shell >}}
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh | sudo bash
{{< /highlight >}}

* Install the latest version of GitLab Runner

{{< highlight shell >}}
sudo apt-get install gitlab-runner
{{< /highlight >}}

* [Register the Runner](https://docs.gitlab.com/runner/register/index.html)

## References

* [https://docs.gitlab.com/runner/install/linux-repository.html](https://docs.gitlab.com/runner/install/linux-repository.html)
