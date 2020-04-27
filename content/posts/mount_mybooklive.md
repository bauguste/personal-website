---
title: "How to mount mybooklive ?"
date: 2020-04-27T19:00:41+02:00
tags: [ "mybooklive" ]
categories: [ "mybooklive" ]
---

## How to mount mybooklive ?

* Example to mount the Public folder

```bash
sudo mount -t cifs -o rw,guest,vers=1.0 //${IP}/Public /media/mybooklive/Public   

```