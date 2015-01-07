assignment-0
============

Intro to R, Rstudio and Github

Congratulations!  You made it to github!

Here is the rest of your assignment:

 0. If you cloned the repository from within R studio, then skip to 4.
 1. Make note of the folder where this repository is
 2. Open up Rstudio
 3. Select `File -> New Project -> Existing Directory` and browse to this directory.  
 4. You should be in R and the working directory will be assignment-0.  R will have created two new files:
    - `.gitignore` is a simple text file that tells git hich files not to upload.  Go ahead.  Open it.  You won't hurt anything.  git doesn't work for very large binary files.  Git is designed for text-based source code.  By default, `Rdata` files will be ignored. You can delete this line if you really want to, but I wouldn't just yet.
    - `assignment-0.Rproj` is a file that defines the Rstudio project.  I don't think you can open it.  Just leave it there and let R do its thing.


  5. Create a new Rmarkdown file: Click on `File -> New File -> R Markdown...`  You can choose html, pdf or word for the output.  html is probably the most robust.  Word files can be opened in R, but a work of warning, you can't edit the file in Word and then go back to R.  Do all of your R work first, and then do your pretty editing later.  Give your file the name test.Rmd.
  6. R will drop you into the file window and create Rmarkdown with some example text.  Look through the file.
  7. Prepare yourself for awesomeness.  Don't worry, I'll wait here for you.
  8. Click `Knit html`

  That's Rmarkdown.  notice how you can weave together R code and text, and it all just works.  This is what reproducible science looks like.  You can always guarantee that the numbers you publish are the most current, up to date numbers.  No more stupid copy and paste errors leading to published results that later need to be retracted. If you click on the question mark icon at the top, you'll find some quick information about Markdown.
 9. Install Packrat: `install.packages('packrat')`
 10. Enable packrat: `packrat::init()`  and let R do her thing.  It will create a folder called packrat.  Here is a [walkthrough](http://rstudio.github.io/packrat/walkthrough.html) of packrat if you want more information.

## Make a change to the file:
We will add a plot to the file and push it up to github to complete the assignmeng
 1. At the command line, install the ggplot2 package with `install.packages('ggplot2')`
 2. Back in the markdown file:
   - Create a new section at the end of the file (see the markdown help for instructions on creating a section in markdown file)
   - Create a quick scatterplot  of diamond price vs size in carats.
   ```r
   library(ggplot2)
   head(diamond) # I always use head to see what a dataset looks like
   qplot(x=carat, y=price, data=diamond)
   ```
 3. Add text that describes how the distribution of price is related to diamond size.
 4. Save your Rmarkdown file.
 5. Knit the file again.

## Push the data back to github.

There are two methods, one from R, ond from git.
### Method A: From R
 1. Select `Git -> Comit...`.  You'll see a list of files that have changed since you cloned the repository.  
 2. You need to "stage" each file that you want git to manage.  Click the checkbox next to each.
 3. Push the file back to github...
