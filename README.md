# samzipper.github.io
Messing around with GitHub Pages.

 * Website made with Hugo and `blogdown` as described here: https://bookdown.org/yihui/blogdown/
 * Useful tips, especially for connecting website build repository and public repository: https://jdeines.github.io/post/r-blogdown-hugo-and-github-website/

## Theme reference: 
https://sourcethemes.com/academic/docs

Icons:
 * fab: https://fontawesome.com/icons?d=gallery&s=brands
 * fas, far: https://fontawesome.com/icons?d=gallery&s=regular,solid
 * ai: https://jpswalsh.github.io/academicons/

## Quick tips
 * Preview site: `blogdown::serve_site()`
 * Turn off preview: `servr::daemon_stop(1)`
 * Pushing site to internet:
  * Compile site: `blogdown::build_site()`
  * Commit everything in public folder: `cd public`; `git add -A`; `git commit -m "changes"`; `git push`

## To-Do List
 * Add blog posts as links, update Open Science page
 * Teaching section
 * Make 'Lab Alums' section
 * Lab logo
 * Icon for browser tab
 * Social media images

## Setting up on a new computer
*Do the following steps in Git Bash, not RStudio*
 * [Set up GitHub SSH connection](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
 * Clone `website-HEAL` repository [recursively](https://stackoverflow.com/questions/11358082/empty-git-submodule-folder-when-repo-cloned): `git clone https://github.com/samzipper/website-HEAL.git --recursive`
 * You might have to go into the submodule folder and [initialize it as a branch](https://gist.github.com/Noitidart/7af2e120bb83e2be9aa4cc3ca0a37722): `cd public`; `git checkout master`

## Adding a publication
 * Make a folder with a somewhat descriptive name in the `content/publication` folder (e.g., ZhangEtAl-2020-ChinaVirtualWater)
 * From Zotero, export a .bib file for that publication into the folder with the same filename
 * Copy contents of .bib file into `content/publication/publications.bib`
 * Copy an `index.md` file from another folder and fill in all the content (most can be grabbed from .bib)
    * in abstract, you might have to delete and backslashes (for example in front of `%`)
    * For the PDF, if not available online put a link into the `static/PDFs` folder.
    * If it should be on the main page, set `featured: true` (most recent 4 papers will be shown)
 * Add a tag for which core research area it is part of. Options:
    * Water and Agriculture
    * Land Use/Land Cover Change
    * Ephemeral Hydrology
    * Stream-Aquifer Interactions
    * Human-Environment Interface

## Adding a new person
 * Go `content/authors`
 * Copy `blank` folder and give it the person's name
 * Name their picture `avatar.png`
 * Edit `_index.md`

## Colors (https://brand.ku.edu/guidelines/color)
KU colors:
  * KU Blue #0051ba
  * Crimson #e8000d
  * Jayhawk yellow #ffc82d
  * Signature grey #85898a

## Logo brainstorming
Corn plant and house inside water drop?