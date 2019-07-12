---
title: "Research Project Organisation"
teaching: 10
exercises: 5
questions:
- "How to organise project folders?"
- "Where and how to save different types of files?"
- "Should I version control my data?"

objectives:
- "Build folder structure for a new project"
- "Understand where to save scripts, data, and other project files."
- "Understand when to version data."
- "Understand how to ignore data files with git."

keypoints:
- "Build and maintain a project directory that is easy to navigate."
- "Understand when and how to "
---


## Folder Structure

It's important to ensure that your project directory (also called your "working directory") is organised and easy to navigate. This will be useful for yourself, but also for anyone you decide to share your project with. Let's create a folder structure now. 

  - In the `Files` tab of the lower right hand pane of RStudio, click on the `New Folder` button. 
  - Create a folder named `data`
  - Repeat to create another folder called `scripts`, and another called `figures`. As you progress through your project, you may wish to create additional folders, such as `results` or `manuscript`. For this workshop, we will focus on R-related folders like Data, Scripts, and Figures.
  
Since we already have a script, let's move it into our `scripts` folder.
  - Tick the checkbox next to `Git_Setup.R` in the `Files` tab. 
  - In the top bar, click `More` > `Move...`.
  - In the popup window, navigate to the `scripts` folder and click `Save`. 
  
From now on, be careful to save any files in the appropriate folder. It will make everything much easier to find. As we will see later, this also has advantages for proper version control. 

When you name your directories, use clear, concise names. It is also a good idea to avoid spaces and special characters. Although newer versions of R deal with these pretty well, weird filenames can sometimes cause confusing errors that take a long time to track down. 

## Scripts and Data

The first major step after setting up a project is usually acquiring data for your project. You may have data in an excel spreadsheet, data that was formatted by some other piece of software, or data downloaded from the internet. Whatever format it is in, save the raw data inside your `data` folder. You should never directly alter or edit your raw data in any way. When you want to clean or reorganise your data, you should always make a copy first. 

Let's get some data to put in our Data folder. 
`download.file(url = "https://mq-software-carpentry.github.io/R-git-for-research/data/SAFI_messy.xlsx", destfile = "./data/SAFI_messy.xlsx", mode = "wb")`

If you write R code to retrieve your data, the way we have done here, it will be easier to figure out the source of the data later. Alternatively, you may choose to download data manually, but be sure to make note of the source of the data (perhaps in a text file or in your code's comments). Most computers automatically put downloaded files into the system's `Downloads` folder. If you decide to manually download data files, you will need to make sure they are moved to the  `data` folder in your project directory. 


## Ignoring stuff

Your raw data will remain the way it is, so there is no point in versioning it. 
GitHub is not a data repository and does not allow the upload of large data files. 
Furthermore, if you are working with sensitive data (such as personal identifiable data), it should never be uploaded to GitHub anyway! Be mindful what sort of data you upload. 

Data can be stored on GitHub if it's a small, public dataset. One solution is to publish your data in an online data repository, then provide code that will allow authorised users to access it (for example, the way we just did above). There are other solutions, but they will vary depending on your specific project and data. 

For the purposes of demonstration, let's make sure that our git repository does not track our raw data files. 
  - Tick the checkbox next to the data file in the Git tab.
  - Click `More` > `Ignore` in the top bar.
  - In the dialogue box, enter *.xlsx. This will ensure that excel files will not be tracked by git. 
  - Git can be taught to ignore file types (e.g. *.csv), specific files, or even entire folders. If you have many data files in a `raw_data` folder, telling Git to ignore the folder is enough.
  






