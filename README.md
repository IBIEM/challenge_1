
# Challenge 1: Mastering RStudio, Git, and Github

# Assignment
The goal of this challenge is to get you more comfortable with RStudio, git, Github, and submitting assignments through Github.  You will need to:

1. [Initialize a new project in RStudio](#initialize-a-new-project)

2. *Part 1:* [Modifiying an Existing R Markdown](#modifiying-an-existing-r-markdown)

3. *Part 2:* [Make a new R Markdown](#making-a-new-r-markdown)

4. [Submit the Assignment](#submitting-the-assignment)

## Initialize a New Project
1. On the main page for **this Github repository** click on the *Clone or download* button.
2. In the dialog box that pops up, click "Use SSH", then click on the clipboard icon to copy the repo URL.
3. In RStudio use the New Project command (from the Project menu)
4. Choose "Version Control" in the *Create Project* dialog box
5. Choose Git
6. Paste the repo URL into the *Repository URL*.  It should be something like `git@github.com:ibiem-2020/challenge-1-[USERNAME].git`, but with your Github username substituted for the `[USERNAME]` part.
7. For *Project directory name* put `challenge_1` or `challenge-1-[USERNAME]`
8. Leave *Create project as subdirectory of* as "~"
9. Click Create Project.

## Modifiying an Existing R Markdown
Your first task is to make some changes to an R Markdown that is included in this challenge repository.

### Getting Started
1. Be sure you are in your new *challenge_1* project (it should say "challenge_1" in the top right corner of the Rstudio window).
2. Open `challenge1_part1.Rmd` in RStudio
3. Before you start, [Knit the R Markdown to HTML](#knit-the-r-markdown) to get a feel for how it looks before you make changes.

### Modify the Header
1. Edit the YAML header (the stuff between the two sets of three dashes: `---`)
  1. Below the title add: `author: "YOUR NAME"`
  2. Below the author add: `date:` followed by the date (If you want to be super fancy you can  follow [these instructions](https://stackoverflow.com/a/23529410) for automatically updating the date).
2. Save these changes and [Knit to HTML](#knit-the-r-markdown) to check that your changes are reflected in the HTML output.
3. Once you are happy with the changes, it is a good idea to [commit them](#commit-changes).  You don't need to commit the HTML at this point, just the .Rmd file.

### Modify Colors
1. The colors I used for the regression line and the 95% confidence interval are hideous. Make them less ugly by replacing the colors in `color="green", fill="orange"` .  Just about any color you can think of will work (you can run `colors()` in an R chunk to see all the named colors that R knows about).
2. Save these changes and [Knit to HTML](#knit-the-r-markdown) to check that your changes are reflected in the HTML output.
3. Once you are happy with the changes, its a good idea to [commit them](#commit-changes)

## Making a New R Markdown
1. Use the *File* menu to to open a new R Markdown
2. Edit the YAML header (the stuff between the two sets of three dashes: `---`)
    1. Change the title to "Challenge 1, Part 2"
    2. Below the title add: `author: "YOUR NAME"`
3. Delete everything below the YAML header (below the second `---` separator)
4. Leave a blank line below the YAML header, then add a section header: `# Comparing City and Highway Fuel Efficiency`
5. Below the section header, add the following chunk of R code:

```{r}
library(ggplot2)

ggplot(mpg, aes(cty, hwy, color = class)) + 
  geom_point()
```

6. Save the file as `challenge1_part2` (RStudio will automatically add ".Rmd") 
7. [Knit the Rmarkdown file to generate an HTML report](#knit-the-r-markdown)
8. Follow the directions below for [Committing Changes](#commit-changes).  For this part of the assignment you should commit:
    - challenge1_part2.Rmd: the R Markdown that you created
    - challenge1_part2.html: the HTML file you knitted from your R Markdown

## Knit the R Markdown
1. Knit the R Markdown to HTML by clicking on the triangle next to the *Knit* button (it might say *Preview* instead of *Knit*) and selecting *Knit to HTML*
2. If the knitting is successful, RStudio should pop open another window with the results.

## Commit Changes
1. Click on *Commit* in the *Git* pane to open the Commit dialog box.
2. Review the changes that you made. Once you decide that you are happy, click the checkbox under **Staged** to add the file to the repo.
3. Write an **informative** commit message in the *Commit message* box and click the *Commit* button.
4. Optional: Push changes to Github by clicking the *Push* button (sometimes the *Push* button just shows up as a green arrow pointing up). You don't need to do this every commit . . . but then again, why not? Who doesn't need more off-site backup?

## Submitting the Assignment
We are using *Github Classroom* for managing code related assignment  When you receive an individual assignment, *Github Classroom* automatically makes a personal copy of the assignment repository.  Since you are working in your own copy of the repository, you are the only one committing to it, so do not have to worry about conflicts.  At the assignment deadline *Github Classroom*  automatically submits the current state of your personal repository, so as long as you have committed your work by the deadline, there is nothing special you need to do to submit. In other words, you can **commit** and **push** *as many times as you want*.

For this assignment you should have these files commited before the deadline:

- `challenge1_part1.Rmd` : your modified version of the R Markdown that you received in your repo
- `challenge1_part1.html` : the output from knitting your revised `challenge1_part1.Rmd`
- `challenge1_part2.Rmd` : the R Markdown that you created
- `challenge1_part2.html` : the output from knitting your `challenge1_part2.Rmd`

