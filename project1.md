---
title: The Last Lab and Final Project
---

### Overview
**Part 1, DUE FRIDAY 12/7 at midnight:** Use the template I've provided on my github site to make your own. 

- Here's what my site "looks" like in [github](https://dillonma.github.io/).
- Here's the "backend" for my [site](https://github.com/dillonma/dillonma.github.io) -- feel free to download it as a reference or click around. 
- Turn-in via blackboard -- just submit a link to your github site.

**Part 2, DUE ON MONDAY 12/10 at 9am:** Turn-in a one pager on your final project as a separate .md on github. Submit via link on blackboard.

**FINAL PERIOD, FRIDAY 12/14 from 8am-10am:** In 5 minutes, present your part 2 and/or any progress on your final project.

**Part 3 Final Project, DUE ON WEDNESDAY 12/19 at midnight:** Your final project as a "project" on your github. Submitted via link on blackboard.

### Part 1
You'll need to git (ha!) your github in shape for your final project. To do so, you may need to rearrange the projects you've already got on there. Notice on my [site backend](https://github.com/dillonma/dillonma.github.io) I only the `index.md` and `lastlab.md` in the root folder (along with the magic `_config.yml`) files. I have the index file point to **html** versions of the .md in the folders. 

Here are the things I'll look for.

1. Chose at least 4 maps (3 assignments from this class or another GIS class and 1 placeholder for the final project) to display on index page. The index page has similarly styled/sized (use a of 350px width) image. Each assignment page has the feature image (try 1300px width and 400px height) and text set. 
2. Each project has a write-up of the process of creating the map, the tools you used, what you "found" in your assignment, and how you would alter it in the future. The more inline images, the better. Remember to put in code as necessary.
3. Edited `config.yml` to adjust the page navigation. Used the title section on each page to set title and removed duplicate headings. 


**Folders:** In order create folders, you first create a file in the folder and github will automagically create the folder. [Check this out.](https://github.com/KirstieJane/STEMMRoleModels/wiki/Creating-new-folders-in-GitHub-repository-via-the-browser)

**Extra**: 

- If you want to change the fonts, do what I did with the [_sass](https://github.com/dillonma/dillonma.github.io/tree/master/_sass) folder. You can copy exactly what I did, or you find your own fonts using [Google Fonts](https://fonts.google.com/). Let's say you wanted to use [Roboto Condensed](https://fonts.google.com/specimen/Roboto+Condensed). In the top right, click ``SELECT THIS FONT`. Then open the little window that appears. Change the selection from `STANDARD` to `@IMPORT`. Then copy the import statement directly to your [_settings.scss](https://github.com/dillonma/dillonma.github.io/blob/master/_sass/_settings.scss) WITHOUT the `<style>` tags. Finally, change the font-family settings, BUT CAREFULLY follow the convention that is in the current settings file and not what Google Fonts shows.
- You can see there are all sorts of other things you can change in the [_settings.scss](https://github.com/dillonma/dillonma.github.io/blob/master/_sass/_settings.scss). Try them. Don't make it ugly.

### Part 2
Now create a separate .md in your *root* of your github site named 'final_proposal.md' -- you'll need to turn-in a link to this file for Part 2. 

To get a C:

- What are you going to do for the final project?
- What is your question?
- Where is the data coming from? Provide links? If you don't have - or can't find - the data, pick a different project.
- What three non-superficial elements from the class are you going to incorporate? Python? SQL? Moran's I? 3D mapping? Hexagonal analysis? Analysis in GeoDa? Something else? (Non-superficial meaning doing more than importing the data with python.)
- How will you know when you've answered your question?

To get an B, you'll need to create a new section of your markdown that will explain:

- What other component from the class will you incorporate?
- Why is more involved than the labs?
- Why did you choose this component?

To get an A and secure an A in the course, you'll need to create a new section of your markdown that will explain:
- Go above and beyond and trying something new - explain what it is that you learned on your own here.

### Part 3
Do what you said in Part 2 and make one of the projects from your github rework to link to address each section in Part 1 and Part 2.


