--- 
date: 2020-04-19T10:00:17+02:00
title: "Install GitLab Runner on Debian"
tags: [ "debian", "gitlab", "runner", "buster" ]
categories: [ "gitlab" ]
---

## Install GitLab Runner on Debian

*  Add GitLab’s official repository:

```bash
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh | sudo bash
```

* Install the latest version of GitLab Runner

```bash
sudo apt-get install gitlab-runner
```

* [Register the Runner](https://docs.gitlab.com/runner/register/index.html)

## Errors on Debian 10 Buster

Runner executor in shell mode

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

To solve this error, delete the `.bash_logout` file for the **gitlab-runner** user

```bash 
rm /home/gitlab-runner/.bash_logout 
```

## References

* [https://docs.gitlab.com/runner/install/linux-repository.html](https://docs.gitlab.com/runner/install/linux-repository.html)
