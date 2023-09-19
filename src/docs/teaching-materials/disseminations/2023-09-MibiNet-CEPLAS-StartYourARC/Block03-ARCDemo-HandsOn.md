---
marp: true
theme: marp-theme_dataplant-ceplas-mibinet-ccby
paginate: true
license: '[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)'
title: ARC demo and hands-on
author:
- name: Dominik Brilhaus
  github: https://github.com/brilator
  orcid: https://orcid.org/0000-0001-9021-3197
- name: Sabrina Zander
  orcid: https://orcid.org/0009-0000-4569-6126
---



# Block 3 &ndash; ARC demo and hands-on

<style scoped>section {background: none; background-color: white}</style>
<!-- _paginate: false -->

September 21st, 2023
 

<div style="position: fixed; bottom: 10%; right: 40%;">
  <div class="profile-picture">
    <img src="https://www.biological-data-science.hhu.de/fileadmin/_processed_/8/c/csm_Sabrina_Zander_3c8daca973.jpg" alt="Sabrina Zander" style="position:absolute; height: auto; width: auto; top:65%; left: 0%; transform:translateY(-50%);"> 
  </div>

  <div>

  Sabrina Zander <br> [MibiNet](https://www.sfb1535.hhu.de/projects/research-area-z/z03)
  </div>
</div>

<div style="position: fixed; bottom: 10%; right: 10%;">
  <div class="profile-picture">
    <img src="https://www.ceplas.eu/fileadmin/_processed_/d/c/csm_Brilhaus_Dominik_4fd48a61a2.jpeg" alt="Dominik Brilhaus">
  </div>

  <div>

  Dominik Brilhaus <br> [CEPLAS Data Science](https://www.ceplas.eu/en/research/data-science-and-data-management/)

  </div>

</div>

---

<!-- 

## Tutor prep:

- change `<username>` in `arc sync` steps
- make sure no `demo-arc` exists at given URL or adapt URL in sync steps

- download the folder with unstructured sample data
    ```bash
    git clone "https://demo-user:1_eznikmzxzARAbUxxnF@git.nfdi4plants.org/teaching/demo-arc_level0.git"
    ```

    > no access needed, "read_registry" token is part of command
    > Note: If you want to provide another dataset for download. 
    > 1. Create a new DataHUB project with the data. 
    > 2. Create an access token only for that project with role "maintainer" and scopes "read_repository".
    > 3. Adapt the URL `https://<tokenname>:<token>@git.nfdi4plants.org/<username>/<projectname>.git`

 -->

# First steps towards your ARC

---

## You just received your data

![bg right width:400](./../../../img/demo_data_screenshot.png)

---

## Goal

- Structure,
- Annotate, and
- Share **your experimental data**.

---


<!-- 
## Tools and software

📂 Explorer or Finder on your local computer
<br>
<img align="left" height=35px src='https://raw.githubusercontent.com/nfdi4plants/Branding/master/icons/Swate/Excel/Core/swate_c_40x40.png'/> DataPLANT's Excel-Plugin SWATE
<br>
🌐 DataPLANT's [DataHUB](https://git.nfdi4plants.org/)
<br>
👩‍💻 "Terminal" or "command prompt" on your local computer 
-->

## Structure your data

![width:800](./../../../img/ARC_fillWithData_experimental.png)

---


## Annotate your data

<style scoped>

section p img {
width: 900px;
height: 400px;
object-fit: cover;
object-position: 50% 60%;
/* display: block; */;
}
</style>

![](./../../../img/Swate_metadataTemplates.png)

<!-- 
1. Fill study characteristics (completely manually)

2. Fill assay parameters (by template, copy paste metadata from sheet, link files by picker)

3. Fill assay parameters (by json import, link files by picker) -->

---


## Collaborate and share



![w:650](./../../../img/ARC_DataSharing_Experts02_img1.png)


---

## Sync your ARC to the DataHUB

```bash
arc sync -f -r https://git.nfdi4plants.org/brilator/demo-arc
```

<!-- 
:bulb: The URL decomposed:
- `https://git.nfdi4plants.org/` = DataHUB
- `brilator/` = username @ DataHUB  
- `demo-arc` = name of the ARC @ DataHUB   -->

---


## Invite collaborators to your ARC

https://git.nfdi4plants.org/brilator/demo-arc

<!-- 
## Check your progress at the DataHUB

- Open your ARC at https://git.nfdi4plants.org/brilator/demo-arc/ and click the `commits` link below the project avatar
- Or directly navigate to https://git.nfdi4plants.org/brilator/demo-arc/-/commits/main 

-->

---

## Initiate the ARC folder structure

![bg right:40% w:250](./../../../img/ARCitect-help-Sidebar.drawio.svg)

1. Create a **New ARC** (2)
2. Select a location and name **TalinumPhotosynthesis** 

---

## Your ARC's name

💡 By default, your ARC's name will be used
   - for the ARC folder on your machine
   - to create your ARC in the DataHUB at `https://git.nfdi4plants.org/<YourUserName>/<YourARC>` (see next steps)
   - as the identifier for your investigation

💡 Make sure that no ARC exists at  `https://git.nfdi4plants.org/<YourUserName>/<YourARC>`. Otherwise you will sync to that ARC.

![bg right:30% w:450](ARCitect_TalinumPhotosynthesis.png)

---

## Add a study

by clicking "Add Study" and entering an identifier for your study

Use **talinum_drought** as an identifier

![bg right w:500](ARCitect_TalinumPhotosynthesis_Study.png)

---

## Study panel

In the study panel you can add

- general metadata,
- people, and
- publications

![bg right w:500](ARCitect_TalinumPhotosynthesis_StudyPanel.png)

---


## Add an assay

by clicking "Add Assay" and entering an identifier for your assay

Add two assays with **rnaseq** and **metabolomics** as an identifier
![bg right w:500](ARCitect_TalinumPhotosynthesis_Assay.png)

---

## Link your assay to a study

You can either
- link your new assay to an existing study in your ARC or
- create a new one
  
Link your assays to your **talinum_drought** study


![bg right w:500](ARCitect_TalinumPhotosynthesis_Assay2.png)

---

## Add information about your assay

In the assay panel you can

1. link or unlink the assay to studies, and
2. define the assay's
   - measurement type
   - technology type, and
   - technology platform.

![bg right w:700](./../../../img/arcitect-AssayPanel.png)

---

## Add protocols

You can either
- directly write a **new protocol** within the ARCitect or
- import an existing one from your computer

![w:800](./../../../img/arcitect-ARCPanel-protocol.png)



---

## Add protocols and datasets

In the file tree you can
  - **add a dataset** and 
  - **protocols** associated to that dataset.

:bulb: **Add Dataset** allows to import data from any location on your computer into the ARC.

:warning: Depending on the file size, this may take a while. Test this with a small batch of files first.

![bg right:40% w:400](./../../../img/arcitect-ARCPanel-assay03.png)

---

## Add Demo Data to your ARC


---

## Login to the DataHUB

Click **Login** (1) in the sidebar to login to the DataHUB.

:bulb: This automatically opens your browser at the DataHUB (https://git.nfdi4plants.org) and asks you to login, if you are not already logged in. 

![bg right:40% w:250](./../../../img/ARCitect-help-Sidebar.drawio.svg)

---

## Upload your local ARC to the DataHUB

From the sidebar, navigate to **Versions** (6)

![bg right:40% w:250](./../../../img/ARCitect-help-Sidebar.drawio.svg)

---

## Versions

The versions panel allows you to
- store the local changes to your ARC in form of "commits",
- sync the changes to the DataHUB, and
- check the history of your ARC

![bg right w:650](./../../../img/arcitect-VersionsPanel.png)

---

## Connection to the DataHUB

If you are logged in, the versions panel shows
- your DataHUB's *Full Name* and *eMail*
- the URL of the current ARC in the DataHUB `https://git.nfdi4plants.org/<YourUserName>/<YourARC>`

![bg right w:650](./../../../img/arcitect-VersionsPanel.png)


<!-- *Create and navigate to a new folder* -->
<!-- 
```bash
mkdir ~/Desktop/demo-arc; cd ~/Desktop/demo-arc
``` -->


---

## Invite collaborators

* Unless changed, your ARC is set to private by default. 
* To collaborate, you can invite lab colleagues or project partners to your ARC by following the steps on the subsequent slides. 
* To get started [sign in](https://auth.nfdi4plants.org/realms/dataplant/login-actions/registration?client_id=account&tab_id=4bQkU161waI) to the DataHUB and open the ARC you want to share.

---

1. Click on **Project Information** in the left navigation panel

![fit w:1050](./../../../img/datahub_members_seq2.png)

---

2. Click on **Members**

![fit w:1050](./../../../img/datahub_members_seq3.png)

---

3. Click on **Invite members**

![fit w:1050](./../../../img/datahub_members_seq4.png)

---

4. Search for potential collaborators

![fit w:1050](./../../../img/datahub_members_seq5.png)

---

5. Select a role 

![fit w:1050](./../../../img/datahub_members_seq6.png)

<!-- Source to slide(s) -->
<!-- ../../bricks/datahub_invite-collaborators.md -->


---

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

---

## <div align="center">Congratulations!</div>
<div align="center">You have just shared your ARC with a collaborator.</div>

<style scoped>

section p img {
width: 1000px;
height: 300px;
object-fit: cover;
object-position: 100% 45%;
/* display: block; */;
}
</style>

![](./../../../img/ARC_Sharing_img1.png)

<!-- Source to slide(s) -->
<!-- ../../bricks/datahub_congrats-for-sharing.md -->

---

## Your ARC is ready

<style scoped>

section p br {
   display: block;
   margin-top: 20px;
   content: "";
}
</style>

👩‍💻 Initiated an ARC
<br>
📂 Structured and ...  
<br>
<img align="left" height=35px src='https://raw.githubusercontent.com/nfdi4plants/Branding/master/icons/Swate/Excel/Core/swate_c_40x40.png'/> ... annotated experimental data
<br>
🌐 Shared with collaborators

![bg right width:400](./../../../img/demo_arc_screenshot.png)


<!-- ## Outlook

1. Data analysis: add workflows and runs (scripts + external data)
2. Iterative and reproducible data analysis: add runs (CWL)
3. Publish your ARC and get a DOI -->

<!-- Source to slide(s) -->
<!-- ../../../units/promotion_arc-demo/promotion_arc-demo.md -->


---

# Resources

### <img align="left" height=35px src='../img/CEPLAS_Icon.jpeg'/> CEPLAS Data Science

> Website: https://www.ceplas.eu/en/research/data-science-and-data-management/

### <img align="left" height=35px src='https://raw.githubusercontent.com/nfdi4plants/Branding/7e7d442aafeaa767b9c14a63a16e459dadcbdaaf/logos/DataPLANT/DataPLANT_logo_minimal_rounded_bg_darkblue.svg'/> DataPLANT (nfdi4plants)

> Website: https://nfdi4plants.org/
> Knowledge Base: https://nfdi4plants.org/nfdi4plants.knowledgebase/ 
> DataHUB: https://git.nfdi4plants.org
> GitHub: https://github.com/nfdi4plants

<!-- Source to slide(s) -->
<!-- ../custom/bricks/links-resources.md -->


---

# Acknowledgements

<style scoped>
section {
  font-size: 22px;  
}
ul {
    margin: 10; padding: 0;
}
</style>

**CEPLAS**

Björn Usadel, Andrea Schrader, Hajira Jabeen (until 2021)

**DataPLANT**

Kaiserslautern: Timo Mühlhaus, Christoph Garth
- Kevin Frey, Lukas Weil, Oliver Maus, Kevin Schneider  
(`ARC Commander`, `Swate`)
- Martin Kuhl (`Knowledge Base`)
- Jonas Lukasczyk (`ARCitect`)

Freiburg: Dirk von Suchodeletz
- Jonathan Bauer, Marcel Tschöpe (`DataHUB`, `Swobup`)
- Cristina Martins Rodrigues (`Knowledge Base`)

![bg right:40% w:550](./../custom/img/hackathon_group.png)

<!-- Source to slide(s) -->
<!-- ../custom/bricks/acknowledgements.md -->


---

## Contributors 

Slides presented here include contributions by 

- Dominik Brilhaus | [GitHub](https://github.com/brilator) | [ORCID](https://orcid.org/0000-0001-9021-3197)
- Cristina Martins Rodrigues  | [GitHub](https://github.com/CMR248) | [ORCID](https://orcid.org/0000-0002-4849-1537)
- Martin Kuhl  | [GitHub](https://github.com/Martin-Kuhl) | [ORCID](https://orcid.org/0000-0002-8493-1077)