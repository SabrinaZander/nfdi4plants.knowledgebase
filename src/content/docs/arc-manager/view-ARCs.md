---
title: View ARCs
sidebar:
  order: 3
authors:
  - ursula-eberhardt
  - lucas-beuter
  - alexander-kirbis
lastUpdated: 2025-01-13
---

For the sake of simplicity, we are here using the term "ARC" for (DataHUB) "Project", because the DataHUB does not make any distinction between projects that have the ARC folder and file structure and those that have not. Both are initially shown in the ARCmanager, but the primary use case of the ARCmanager is viewing and editing ARCs 

### List and filter ARCs

Once you are logged in, you have several options for selecting which ARCs to view:

With the `LOAD ARC` button (Fig. 1), all ARCs on the DataHUB will be listed for which you have at least viewing rights. This includes ARCs that are set to public, ARCs to which you were added as a member, and ARCs owned by you. Your own ARCs are additionally highlighted in color.

---

![](@images/arc-manager/view/01-load-arcs.png)

**Fig. 1** Get a list of all publicly visible ARCs and your private ARCs with the `LOAD ARCS` button.

---

Use the `Your Arcs` check-box (Fig. 2) to filter the list of ARCs for those in which you are member and your own ARCs. Your own ARCs are again highlighted in color.

---

![](@images/arc-manager/view/02-your-arcs.png)

**Fig. 2** Only show your own ARCs and those to which you were added as a member by using the `Your Arcs` check-box.

---

By default, the ARCs are sorted by the date of the last changes in descending order from latest to earliest.

If you are looking for a specific ARC, use the search bar above the ARC list to search for the title of the ARC.

Next to each listed ARC are two buttons to access the following functions:

- the lense button (Fig. 3, 1) will open the DataHUB page of your ARC in a new browser window

- the downward arrow button (Fig.3, 2) expands the ARC and allows you to browse its contents and interact with it

---

![](@images/arc-manager/view/03-interact.png)

**Fig. 3** List of ARCs and buttons to interact with them. (1) Open DataHUB page of the ARC in a new browser window, (2) View ARC contents inside ARCmanager.

---

### View ARC contents

Expanding an ARC allows you to view files and directories that are contained within the ARC. The file structure of the ARC is depicted on the left side of the main window in the form of a tree view. The content of the currently selected directory is also shown in the main part of the window. Here, you can access additional features, like creating new directories or editing ISA files.

On the top of the main window, multiple buttons provide access to additional functions that will be explained in detail later in the manual.

---

![](@images/arc-manager/view/04-detailed-view.png)

**Fig. 4** Detailed view of ARC contents and buttons to access additional functions after expanding an ARC.

---

You can hide the ARC contents by clicking inside the `List ARC content` field above the list of files and directories (Fig. 5).

---

![](@images/arc-manager/view/05-hide-content.png)

**Fig. 5** A Left-click inside the highlighted area hides ARC contents. Click again to bring back the list of files and directories.

---

Navigate through the ARC directories with a left-click, either in the tree view or in the main window. After clicking a directory, its contents will be displayed. You can go back one level in the directory hierarchy by using the `Return` field above the list of files (Fig. 6). Alternatively, you can click on the respective subdirectory in the path displayed above the `Return` field to jump directly to this position.

---

![](@images/arc-manager/view/06-return.png)

**Fig. 6** Use the `Return` field to go back one step in the directory hierarchy of your ARC.

---

When you click on a file instead of a directory, another panel on the right side will open that allows you to view the contents of the selected file (Fig. 7). You can display images, pdf files, text based files, and more.

Plain text files (.md, .txt or similar) can be modified directly in this editor. Do not forget to save your changes and synchronize with the DataHUB by using the `SAVE` button when you are done.

---

![](@images/arc-manager/view/07-text-editor.png)

**Fig. 7** When selecting a text file with a left-click, a text editor panel will open on the right side of the browser window. Here, you can edit the file directly and save changes.

---

When selecting an ISA file, the editor panel will open as well, but instead of a text editor you will see a form that allows you to add metadata entries to the ISA file (Fig. 8). To learn more about adding metadata using the ARCmanager, visit the corresponding [manual page](/nfdi4plants.knowledgebase/arc-manager/adding-metadata).

---

![](@images/arc-manager/view/08-open-isa.png)

**Fig. 8** Opening an ISA file with a left-click will bring up a form that can be used to add metadata entries to the file.

---

You can hide/view the editor panel by clicking the double arrow symbol at the top of the panel (Fig. 9).

![](@images/arc-manager/view/09-hide-panel.png)

**Fig. 9** The panel on the right side of the browser window can be hidden/displayed with the double arrow symbol.

---

When you expand the editor window without selecting a file to be edited first, a list of recent changes to the ARC will be shown instead (Fig. 10).

You can hide them by unchecking the checkbox, as well as switch to a different branch in the ARC (highlighted in red).
After switching the branch you need to reload the ARC through the reload button.

---

![](@images/arc-manager/view/10-history.png)

**Fig. 10** The right side contains a list of changes by default, as well as the option to switch branches

---

The `NEW FOLDER` button below the listed ARC content (Fig. 11, #1) can be used to create new folders, e.g. to further organize raw data inside the dataset subdirectories. 

These custom folders can be renamed (Fig. 11, #2) or deleted (Fig. 11, #3). This is in contrast to the directories which are part of the ARC specification (e.g. studies, assays, etc.), which can not be renamed or deleted via the ARCmanager.

---

![](@images/arc-manager/view/11-edit-folders.png)

**Fig. 11** UI elements to create (#1), edit (#2), and delete (#3) custom folders in an ARC using the ARCmanager.

---

### ARC quick validation

When you click the `Validate` button, a basic validation process is started that checks your ARC.

---

![](@images/arc-manager/view/12-validate.png)

**Fig. 12** Start the validation process by clicking the highlighted button.

---

Different requirements for a publication ready ARC are checked, like complete ARC structure (all necessary folders and files), all necessary fields filled out in the isa.investigation file, all contacts have names, email, and affiliation and more.

Afterwards, a highlighted card structure will show you the results of the validation process. In case your ARC did not pass the validation test, the results will tell you exactly which information or element is missing.

---

![](@images/arc-manager/view/13-validate-results.png)

**Fig. 13** Validation results displayed in a card view
