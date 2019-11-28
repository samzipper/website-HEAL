# samzipper.github.io
Messing around with GitHub Pages.

 * Website made with Hugo and `blogdown` as described here: https://bookdown.org/yihui/blogdown/
 * Useful tips, especially for connecting website build repository and public repository: https://jdeines.github.io/post/r-blogdown-hugo-and-github-website/

## Theme reference: 
https://sourcethemes.com/academic/

Icons: https://fontawesome.com/icons?d=gallery

## Quick tips
 * Preview site: `blogdown::serve_site()`
 * Turn off preview: `servr::daemon_stop(1)`
 * Compile site: `blogdown::build_site()`

## Adding a publication
 * Make a folder with a somewhat descriptive name in the `content/publication` folder (e.g., ZhangEtAl-2020-ChinaVirtualWater)
 * From Zotero, export a .bib file for that publication into the folder with the same filename
 * Copy contents of .bib file into `content/publication/publications.bib`
 * Copy an `index.md` file from another folder and fill in all the content (most can be grabbed from .bib)
    * in abstract, you might have to delete and backslashes (for example in front of `%`)
    * For the PDF, if not available online put a link into the `static/PDFs` folder.

## Colors (https://brand.ku.edu/guidelines/color)
KU colors:
  * KU Blue #0051ba
  * Crimson #e8000d
  * Jayhawk yellow #ffc82d
  * Signature grey #85898a

## Logo brainstorming
Corn plant and house inside water drop?