# The website for the HydroEcology of Anthropogenic Landscapes (HEAL) group at the Kansas Geological Survey/University of Kansas (HEAL@KGS).
[![Netlify Status](https://api.netlify.com/api/v1/badges/8ab46337-8345-446c-8b42-45d8d73db848/deploy-status)](https://app.netlify.com/sites/samzipper/deploys)

Currently deployed at [samzipper.com](https://www.samzipper.com), with [code on GitHub](https://github.com/samzipper/website-HEAL).

 * Website made with Hugo and `blogdown` as described here: https://bookdown.org/yihui/blogdown/

## Theme reference: 
https://sourcethemes.com/academic/docs

Icons:
 * fab: https://fontawesome.com/icons?d=gallery&s=brands
 * fas, far: https://fontawesome.com/icons?d=gallery&s=regular,solid
 * ai: https://jpswalsh.github.io/academicons/

## To-Do List
 * Add dropdown menu to main page linking other resources
 * Lab logo
 * [Icon for browser tab](https://sourcethemes.com/academic/docs/customization/#website-icon)
 * Social media images

## Quick tips
 * Preview site: `blogdown::serve_site()`
 * Turn off preview: `servr::daemon_stop(1)`
 * Pushing site to internet is done automatically via Netlify
  * To manually compile site: `blogdown::build_site()`

## Adding a publication
 * Make a folder with a somewhat descriptive name in the `content/publication` folder (e.g., ZhangEtAl-2020-ChinaVirtualWater)
 * From Zotero, export a .bib file for that publication into the folder with the same filename
 * Copy an `index.md` file from another folder and fill in all the content (most can be grabbed from .bib)
    * in abstract, you might have to delete and backslashes (for example in front of `%`)
    * For the PDF, if not available online put a link into the `static/PDFs` folder.
    * If it should be on the main page, set `featured: true` (most recent 4 papers will be shown)
	* use "Samuel C. Zipper" for my name in index.md since that is linked to my author profile.
 * Add a tag for which core research area it is part of. Options: ["Water and Agriculture", "Land Use/Land Cover Change", "Ephemeral Hydrology", "Stream-Aquifer Interactions", "Human-Environment Interface"]
 * For publication_types: 2 = journal article, 4 = report

## Adding a new person
 * Go `content/authors`
 * Copy `blank` folder and give it the person's name
 * Name their picture `avatar.png`
 * Edit `_index.md`

## New post from Rmarkdown
 * Copy the .Rmd for a recent post, for example "2022-01-02-work-tracking-update.Rmd"
 * Write your post and make sure you are happy with everything.
 * Knit the file in Rstudio. This will make a .html file in the posts folder and store all the image files in the static folder.
	* The html file will have a weird header - that's OK.
 * Commit and push the changes to the web
 * Netlify should automatically render it. The URL will be https://www.samzipper.com/post/name_of_post/

## Update Hugo and Academic Theme
 * Make copy of website repository in case something breaks.
 * Updating Hugo: this is not necessary when site is deployed to Netlify
  * Check hugo version (`blogdown::hugo_version()`) and compare to current [release version](https://github.com/gohugoio/hugo/releases).
    * `blogdown::update_hugo()`
    * update version in `netlify.toml` file
 * Check version of academic theme: `themes/hugo-academic/data/academic.toml`
  * If update necessary, download [latest release](https://github.com/gcushen/hugo-academic/releases) of hugo-academic and replace your `themes/hugo-academic` folder
  * Fix all breaking changes from [hugo-academic release notes](https://sourcethemes.com/academic/updates/).
	* Make sure you update `netlify.toml` with the number that Academic theme tells you to

# Update history
 * 2020-06-10: update Academic to 4.8.0
 * 2019-12-31: update to 4.6.3
 * Original install: 4.4.0

## Colors (https://brand.ku.edu/guidelines/color)
KU colors:
  * KU Blue #0051ba
  * Crimson #e8000d
  * Jayhawk yellow #ffc82d
  * Signature grey #85898a