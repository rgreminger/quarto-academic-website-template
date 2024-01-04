# quarto-academic-website-template
This is a template for a simple academic website in Quarto. The template differs from the basic Quarto website by providing customized lists that present journal information, information on co-authors, and a small preview image. Moreover, I adjusted the title block so that it also shows this information on the project pages. 

## How to use this template 

This template uses Quarto to build and show the website. You can install it from here: [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)

After installing Quarto, you can just fork this repository and use Quarto Preview to preview the website. You can find general information on how to create, preview, and publish websites with Quarto here: [https://quarto.org/docs/websites/](https://quarto.org/docs/websites/)

Below, I am providing an overview of the files and folders. This overview should give an idea of where options and settings can be adjusted to change the look and feel of the website. You can also find more detailed explanations in the individual files. 

I use Quarto with Visual Studio Code, which works well with previewing the website in the IDE. RStudio should work equally well. 

## Main files and folders

The template sets up the below main files and folders. 

`_quarto.yml`: this file determines website settings like the title, navigation bar, theme, and fontsize. The [Quarto Website Documentation](https://quarto.org/docs/websites/website-navigation.html) shows the various options available.

`index.qmd`: landing page. This is the markdown file for the landing page that opens first. The comments in the file provide further details on how this can be adjusted.   

`research.qmd`, `code.qmd`, and `teaching.qmd`: individual pages linked to from the navigation bar (set in `_quarto.yml`).  These are markdown files that can be easily adjusted. They also determine which lists to display. The comments in these files provide more details. 

`pub`, `wp` and `wip`: folders containing markdown files for the different projects in different stages. They will be displayed in the publication, working paper, and work in progress lists used by `research.qmd` to show the different projects. These files contain comments providing details on the available options.

`code`: folder with the markdown files for different repositories listed by `code.qmd`. 

`files`: folder with files that visitors can download. Note, these files need to be also added in `_quarto.yml`. Otherwise, users won't be able to download them. 

`images`: folder containing images that are displayed on the page.  

`partials`: files that overwrite part of css. For now, this is just the title block that is used for the different project pages. 

`ejs`: this folder contains the files that determine the format of the lists in the research and code pages. The respective ejs files are selected within the different individual pages.

## Some important notes for using this template

- To add files that visitors can download, they need to be added to the resources part of `_quarto.yml`. 
- There is an issue with Quarto: if the repository lives in a folder that is synced with Dropbox, Quarto cannot preview the site. To solve this, it is necessary to temporarily deactivate Dropbox sync (hopefully this will be fixed in the future). 