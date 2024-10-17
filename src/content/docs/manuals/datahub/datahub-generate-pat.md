---
title: Generate a Personal Access Token (PAT)
authors:
  - dominik-brilhaus
license: '[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)'
lastUpdated: 2023-07-07
sidebar:
  badge:
    text: Beginners
    variant: note
---


## About this guide

This guide shows you how to generate a Personal Access Token (PAT). The PAT can be used to authenticate your local machine to communicate with your DataHUB account. 

:::note
You need to do this only once per machine (unless you specify an expiration date)
:::

1. Sign in to the [DataHUB](https://git.nfdi4plants.org/)
2. Go to the [Access Tokens](https://git.nfdi4plants.org/-/profile/personal_access_tokens) settings
3. Fill all required information:
   - Token name: e.g. the name of the machine to be linked ("Office PC") (1)
   - Expiration date (optional) (2)
   - Select a scope: e.g. `api` (3)
4. Click "Create personal access token" (4)

![](@images/datahub/datahub-access-token01.drawio.png)

5. `Your new personal access token` appears on top. Copy (1) it somewhere **safe** for later use.

![](@images/datahub/datahub-access-token02.drawio.png)