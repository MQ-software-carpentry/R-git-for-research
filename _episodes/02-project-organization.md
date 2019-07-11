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
  - Create a folder named `Data`
  - Repeat to create another folder called `Scripts`, and another called `Figures`. As you progress through your project, you may wish to create additional folders, such as `Results` or `Manuscript`. For this workshop, we will focus on R-related folders like Data, Scripts, and Figures.
  
Since we already have a script, let's move it into our `Scripts` folder.
  - Tick the checkbox next to `Git_Setup.R` in the `Files` tab. 
  - In the top bar, click `More` > `Move...`.
  - In the popup window, navigate to the `Scripts` folder and click `Save`. 
  
From now on, be careful to save any files in the appropriate folder. It will make everything much easier to find. As we will see later, this also has advantages for proper version control. 

When you name your directories, use clear, concise names. It is also a good idea to avoid spaces and special characters. Although newer versions of R deal with these pretty well, weird filenames can sometimes cause confusing errors that take a long time to track down. 

## Scripts and Data

The first major step after setting up a project is usually acquiring data for your project. You may have data in an excel spreadsheet, data that was formatted by some other piece of software, or data downloaded from the internet. Whatever format it is in, save the raw data inside your `Data` folder. You should never directly alter or edit your raw data in any way. When you want to clean or reorganise your data, you should always make a copy first. 

Let's get some data to put in our Data folder. 
(Download with RCurl directly into project folder?)
(Download and show people how to retrieve it from downloads?)

## Ignoring stuff

Your raw data will remain the way it is, so there is no point in versioning it. 
GitHub is not a data repository and does not allow the upload of large data files. 
Furthermore, if you are working with sensitive data, it should never be uploaded to GitHub anyway! 

Data can be stored on GitHub if it's a small, public dataset. A better solution is to publish your data in an online data repository, then provide code that will allow authorised users to access it (for example, the way we just did above).

We need to make sure that our git repository does not track our data files. 
  - Tick the checkbox next to the data file in the Git tab.
  - Click `More` > `Ignore` in the top bar.
  - In the dialogue box, enter *.csv. This will ensure that csv files will not be tracked by git. 
  - Git can be taught to ignore file types, specific files, or even entire folders. If you have many data files in a Raw_Data folder, telling Git to ignore the folder is enough.
  
(screenshots??)
(Excercises??)
  




