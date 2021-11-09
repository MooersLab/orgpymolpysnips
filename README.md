# orgpymolpysnips

## Introduction

This project supports the generation of reproducible molecular images using Org Mode and PyMOL.
It includes a yasnippet library of PyMOL code library written in Python rather than the PyMOL macro language (pml) library.
Each snippet is a code source block for org-mode. 
Org-mode is the scope of this library.
You use the library with Jupyter kernels that can access the Python API of PyMOL.


## Why is this library for org-mode beneficial for biologists?

- Org supports literate programming. You can run the code inside an Org document, and Org displays the output image from PyMOL below the code block. You use the powerful editing features of Emacs to edit the flanking explanatory prose. 

- You can generate a gallery of images. Such a gallery eases the selection of images for publication.

- After publishing a research paper, the gallery is valuable for generating images for news releases, review articles, book chapters, websites, seminars, and wall hanging artwork.

- You can convert the org document into a supplemental materials document for the research paper. This document would contain the code needed to generate the images used in the research paper. Such a document enables readers to reproduce the images of molecules in the research paper. This capability supports the practice of the FAIR principles and the practice of rigorous science.

- You can use Org documents in the journal package of Emacs as an electronic laboratory notebook. You store each day in a separate document. The source block of PyMOL code can be stored in the diary entry and retrieved later by a fuzzy search tool like fzf.


## Features of the library

- Each snippet is written in Python and is flanked by org-mode source block code.
- Snippets are divided into 20 categories.
- The categories appear as submenus in the yasnippet pulldown menu for org-mode.
- The snippets have tab triggers and tab stops to support fast insertion and editing.


## Requirements

- Emacs
- yasnippets package for Emacs
- org-mode package for Emacs
- org-babel package for Emacs
- Jupyter 
- PyMOL
- a jupyter kernel mapped to the Python interpreter of PyMOL.


## Installation

- Create the directory `~/.emacs.d/snippets/org-mode` for your personal snippets if this directory does not exist yet.
- Download this repo.
- Move the contents of `orgMode` to  `~/.emacs.d/snippets/org-mode`.

## Operation
q
- Open an Org document in Emacs.
- Select under the `YASnippet` pulldown `Reload everything` to load the snippets in an old session of PyMOL.
- Select under the `YASnippet` pulldown `org-mode` and then one sub-menu with the prefix `pymolpy-`. Select a snippet to insert it into the org document, or enter the key (== tab trigger) name in the org document and enter <tab> to insert the code.
- Enter <tab> to advance through the tab stops. Edit each tab stop as needed. For example, you may need to change the kernel's name or the color of a chain.
- Place the cursor inside the code block or on the first line of the source block and enter `C-c C-c` to execute the code. The output will appear below.
- You may have to merge code blocks from multiple snippets for complex analyses. The merger has to be done by manual copy and paste.
- You can also access the pymol shortcuts stored in the file [pymolshortcuts.py](https://github.com/MooersLab/pymolshortcuts). Load the file containing the shortcuts by running the command `cmd.do("run /Users/blaine/Scripts/PyMOLScripts/pymolshortcuts.py")`. For example, apply the ambient occlusion shortcut by entering `cmd.do(AO)`.

