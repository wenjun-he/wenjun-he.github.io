---
layout: post
title: Daily Issues Trouble Shooting
date: 2021-08-26 
tags: markdown    
---

## Daily Issues
### git push facing *LibreSSL SSL_connect:SSL_ERROR_SYSCALL in connection to github.com:443*
>* It will probably caused by the VPN, therefore try to close the VPN and try again

### error: RPC failed; HTTP 413 curl 22 The requested URL returned error: 413 Request Entity Too Large; fatal: The remote end hung up unexpectedly
>* set the http into git like the following : git remote set-url origin git@github.com:GitUserName/GitRepoName.git