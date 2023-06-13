---
marp: true
theme: dataplant_marp-theme
paginate: true
headingDivider:
- 1
- 2
license: '[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)'
footer: '<a href="https://nfdi4plants.org"> <img id="footer-img1" src="../../../../img/_logos/DataPLANT/DataPLANT_logo_square_bg_transparent.svg"></a> <a href="https://ceplas.eu"> <img id="footer-img2" src="../../../../img/_logos/CEPLAS/CEPLAS_Icon.jpeg"></a><a href="https://creativecommons.org/licenses/by/4.0/"><img id="footer-img3" src="../../../../img/_logos/CreativeCommons/by.svg"></a>'
style: 'footer {height: 30px;padding: 10px;bottom: 00px;} #footer-img1 {height: 30px; padding-left: 0px;} #footer-img2 {height: 30px; padding-left: 20px;opacity: 0.5;}  #footer-img3 {height: 20px;padding-left: 20px; opacity: 0.5;}'
title: Start-Your-ARC Workshop Series - Session 02
author: 
    - Dominik Brilhaus
    - Cristina Martins Rodrigues
author_orcid: 
    - https://orcid.org/0000-0001-9021-3197
    - https://orcid.org/0000-0002-4849-1537
author_github: 
    - brilator
    - CMR248
---

# Start Your ARC Workshop Series

<!-- Title slide to class -->

<!-- _color: white -->
<!-- _paginate: false -->
<!-- _footer: "" -->

![bg fit](../custom/img/background_title_ceplas.drawio.svg)

Session 02 - Build your ARC
May 31st, 2023

<br>

Dominik Brilhaus - CEPLAS Data Science

# Goals

- Create your first ARC
- Add data to your ARC
- Share the ARC

# Legend

💻 = Locally (on your machine)

🌐 = Remote (in the DataHUB)  

Info in `<brackets>` are placeholders - please replace with proper info


# Part 0: Check-in


<!-- ## Open the online notepad

> link removed from online presentation


## Screen-sharing during the workshop

> link removed from online presentation

:bulb: Any windows volunteer? -->

## Installation

Open a terminal and one after the other execute

```bash
git --version
```

```bash
git-lfs --version
```

```bash
arc --version
```

:bulb: If you see a warning at any of these, let me know.

## Config

```bash
git config --global --get-regexp user
```

:bulb: If this does not display your user name and email, you need to [configure git](https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ArcCommanderManual/git_config.html).


## Have a simple text editor ready

- Windows Notepad
- MacOS TextEdit

Recommended text editors with code highlighting:

- Visual Studio Code <https://code.visualstudio.com/>
- BBEdit <https://www.barebones.com/products/bbedit/>
- Sublime <https://www.sublimetext.com/>

## Create a fresh folder for your ARCs

For this workshop, create a new folder somewhere on your machine where you want to store ARCs, e.g. on the desktop:

- `C:\Users\<username>\Desktop\workshop-arcs` (windows)
- `~/Desktop/workshop-arcs` (mac)

## Download the demo data

```bash
git clone "https://demo-user:1_eznikmzxzARAbUxxnF@git.nfdi4plants.org/teaching/demo-arc_level0.git"
```


# Part 1: Hands-on with demo data


# Your fresh ARC folder

1. 💻 Create a new folder, which you want to initialize as an ARC.
2. 💻 Open the command line inside the folder or navigate via command line to that folder.

For example:
```bash
mkdir -p ~/Desktop/workshop-arcs/arc-demo
cd ~/Desktop/workshop-arcs/arc-demo
```

## Initiate the ARC folder structure

```bash
arc init
```

## Create an investigation

```bash
arc i create -i TalinumPhotosynthesis
```

## Add a study

```bash
arc s add -s talinum_drought
```
  
## Add assays

```bash
arc a add -s talinum_drought -a rnaseq
arc a add -s talinum_drought -a metabolomics
```

# Upload your local ARC to the DataHUB

```bash
arc sync -r https://git.nfdi4plants.org/<username>/arc-demo
```

## Sort the demo data into the ARC

Identify "raw dataset(s)" and "protocols" and move them to the proper subfolders in the ARC.

![bg right w:500](../../../../img/demo_data_screenshot.png)

## Sync your ARC to the DataHUB

To save the changes, sync the ARC to the DataHUB including a message.

```bash
arc sync -m "sorted the demo data"
```


## Invite a collaborator 🌐

---

1. Click on **Project Information** in the left navigation panel

![fit w:1050](../../../../img/datahub_members_seq2.png)

---

2. Click on **Members**

![fit w:1050](../../../../img/datahub_members_seq3.png)

---

3. Click on **Invite members**

![fit w:1050](../../../../img/datahub_members_seq4.png)

---

4. Search for potential collaborators

![fit w:1050](../../../../img/datahub_members_seq5.png)

---

5. Select a role 

![fit w:1050](../../../../img/datahub_members_seq6.png)

<!-- Source to slide(s) -->
<!-- ../../bricks/datahub_invite-collaborators.md -->


## Choosing the proper role

<u>Guest</u>
Have the least rights. This is recommended for people you ask for consultancy.

<u>Developers</u> 
The choice for most people you want to invite to your ARC. Developers have read and write access, but cannot maintain the project on the DataHUB, e.g. inviting others.

<u>Maintainers</u> 
Gives the person the same rights as you have (except of removing you from your own project). This is recommended for inviting PIs or group leaders allowing them to add their group members for data upload or analysis to the project as well.

*A detailed list of all permissions for the individual roles can be found [here](https://docs.gitlab.com/ee/user/permissions.html)*

<!-- Source to slide(s) -->
<!-- ../../bricks/datahub_choose-collaborator-role.md -->