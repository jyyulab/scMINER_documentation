# scMINER Full Documentation
---

[scMINER](https://github.com/jyyulab/scMINER) documentation website was set up using [pkgdown](https://pkgdown.r-lib.org/) package. It contains four sections: 

- **`Home Page`**: built from README.md by pkgdown package
- **`Quick Tutorial`**: built from vignettes by pkgdown package
- **`Full Documentation`**: build and maintained independently with [bookdown](https://pkgs.rstudio.com/bookdown/) package
- **`Functions`**: built from man/Rd files by pkgdown package

This repository is used to maintain the **Full Documentation** of scMINER.


When some changes are made to scMINER R package:

- If there is nothing to modify in the Full Documentation, just re-build the documentation website by:
  1. Update the documentation if the codes of functions are modified;
  2. In main repository directory (containing **`index.md`** file) of scMINER project, run `pkgdown::build_site()` or `Addins-Build pkgdown`. This will update some files in **`/docs`**.
  3. Git commit and push to GitHub. The website page should automatically renewed.
  
- If the **Full Documentation** needs to be modified, then you will need update the book here before you re-build the documentation website:
  1. Modify the **`r markdown`** files accordingly;
  2. In main repository directory (containing **`index.md`** file) of this project, run `bookdown::render_book()` or `Build-Build Book`. This will update some files in **`/docs`**.
  3. Copy all updated files in **`/docs`** into **`scMINER/Docs/bookdown`** folder. We specified **`bookdown/index.html`** as the href of Full Documentation.
  4. Re-build the documentation website as described above.
