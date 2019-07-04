---
layout: page
title: Setup
---

## Setup instructions

**R** and **RStudio** are separate downloads and installations. R is the
underlying statistical computing environment, but using R alone is no
fun. RStudio is a graphical integrated development environment (IDE) that makes
using R much easier and more interactive. You need to install R before you
install RStudio. After installing both programs, you will need to install the
**`tidyverse`** package from within RStudio. Follow the instructions below for
your operating system, and then follow the instructions to install
**`tidyverse`** and **`RSQLite`**.

### Windows

#### If you already have R and RStudio installed

* Open RStudio, and click on "Help" > "Check for updates". If a new version is
	available, quit RStudio, and download the latest version for RStudio.
* To check which version of R you are using, start RStudio and the first thing
  that appears in the console indicates the version of R you are
  running. Alternatively, you can type `sessionInfo()`, which will also display
  which version of R you are running. Go on
  the [CRAN website](https://cran.r-project.org/bin/windows/base/) and check
  whether a more recent version is available. If so, please download and install
  it. You can [check here](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#How-do-I-UNinstall-R_003f) for
  more information on how to remove old versions from your system if you wish to do so.

#### If you don't have R and RStudio installed

* Download R from
  the [CRAN website](http://cran.r-project.org/bin/windows/base/release.htm).
* Run the `.exe` file that was just downloaded
* Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under *Installers* select **RStudio x.yy.zzz - Windows
  Vista/7/8/10** (where x, y, and z represent version numbers)
* Double click the file to install it
* Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.


### macOS

#### If you already have R and RStudio installed

* Open RStudio, and click on "Help" > "Check for updates". If a new version is
	available, quit RStudio, and download the latest version for RStudio.
* To check the version of R you are using, start RStudio and the first thing
  that appears on the terminal indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will also display which version of R you are running. Go on
  the [CRAN website](https://cran.r-project.org/bin/macosx/) and check
  whether a more recent version is available. If so, please download and install
  it.

#### If you don't have R and RStudio installed

* Download R from
  the [CRAN website](http://cran.r-project.org/bin/macosx/).
* Select the `.pkg` file for the latest R version
* Double click on the downloaded file to install R
* It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed
  by some packages)
* Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under *Installers* select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)**
  (where x, y, and z represent version numbers)
* Double click the file to install RStudio
* Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.


### Linux

* Follow the instructions for your distribution
  from [CRAN](https://cloud.r-project.org/bin/linux), they provide information
  to get the most recent version of R for common distributions. For most
  distributions, you could use your package manager (e.g., for Debian/Ubuntu run
  `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we
  don't recommend this approach as the versions provided by this approach are
  usually out of date. In any case, make sure you have at least R 3.3.1.
* Go to the
  [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
* Under *Installers* select the version that matches your distribution, and
  install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i
  rstudio-x.yy.zzz-amd64.deb` at the terminal).
* Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.


### For everyone

**After installing R and RStudio, you need to install the `tidyverse` package.**

* After starting RStudio, at the console type:
  `install.packages(c("tidyverse"))`
  
  
### Git 

<div id="git"> {% comment %} Start of 'Git' section. GitHub browser compatability	
           is given at https://help.github.com/articles/supported-browsers/{% endcomment %}	
  <h3>Git</h3>	
  <p>	
    Git is a version control system that lets you track who made changes	
    to what when and has options for easily updating a shared or public	
    version of your code	
    on <a href="https://github.com/">github.com</a>. You will need a	
    <a href="https://help.github.com/articles/supported-browsers/">supported</a>	
    web browser (current versions of Chrome, Firefox or Safari,	
    or Internet Explorer version 9 or above).	
  </p>	
  <p>	
    You will need an account at <a href="https://github.com/">github.com</a>	
    for parts of this lesson. **Create a GitHub account if you don't have one already.**	Basic GitHub accounts are free.
    You can also get a free GitHub Pro account for education. Use your university email address to create your GitHub account, then apply for an [education discount](https://education.github.com/benefits). 
    Please consider what personal information you'd like to reveal. For	
    example, you may want to review these	
    <a href="https://help.github.com/articles/keeping-your-email-address-private/">instructions	
    for keeping your email address private</a> provided at GitHub.	
  </p>	
   <div class="row">	
    <div class="col-md-4">	
      <h4 id="git-windows">Windows</h4>	
      <ol>	
        <li>Download the Git for Windows <a href="https://git-for-windows.github.io/">installer</a>.</li>	
        <li>Run the installer and follow the steps below:	
          <ol>	
            {% comment %} Git 2.18.0 Setup {% endcomment %}	
            <li>	
                Click on "Next" four times (two times if you've previously	
                installed Git).  You don't need to change anything	
                in the Information, location, components, and start menu screens.	
            </li>	
            <li>	
                <strong>	
                Select “Use the nano editor by default” and click on “Next”.	
                </strong>	
            </li>	
            {% comment %} Adjusting your PATH environment {% endcomment %}	
            <li>	
                Keep "Use Git from the Windows Command Prompt" selected and click on "Next".	
                If you forgot to do this programs that you need for the workshop will not work properly.	
                If this happens rerun the installer and select the appropriate option.	
            </li>	
            {% comment %} Choosing the SSH executable {% endcomment %}	
            <li>Click on "Next".</li>	
            {% comment %} Configuring the line ending conversions {% endcomment %}	
            <li>	
                Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".	
            </li>	
            {% comment %} Configuring the terminal emulator to use with Git Bash {% endcomment %}	
            <li>	
              <strong>	
                Select "Use Windows' default console window" and click on "Next".	
              </strong>	
            </li>	
            {% comment %} Configuring experimental performance tweaks {% endcomment %}	
            <li>Click on "Install".</li>	
            {% comment %} Installing {% endcomment %}	
            {% comment %} Completing the Git Setup Wizard {% endcomment %}	
            <li>Click on "Finish".</li>	
          </ol>	
        </li>	
        <li>
          To ensure that you can use git with RStudio:
          <ol>
            <li>Open RStudio.</li>
            <li>In the menu, click on "Tools > Global Options...".</li>
            <li>Click on "Git/SVN".</li>
            <li>Ensure the checkbox "Enable version control interface for RStudio projects" is selected.</li>
            <li>Under "Git executable" click on "Browse".</li>
            <li>Navigate to the location of <code>git.exe</code>. This is typically located in "C:\Users\&#60;Your-User-Name&#62;\AppData\Local\Programs\Git\bin".</li>
            <li>Click "Open".</li>
            <li>Click "OK".</li>
          </ol>
        </li>
      </ol>
      <p>This will provide you with both Git and Bash in the Git Bash program.</p>
    </div>
    <div class="col-md-4">	
      <h4 id="git-macosx">macOS</h4>	
      <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">Video Tutorial</a>	
      <ol>
        <li>	
          <strong>For OS X 10.9 and higher</strong>, install Git for Mac	
          by downloading and running the most recent "mavericks" installer from	
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">this list</a>.	
          Because this installer is not signed by the developer, you may have to	
          right click (control click) on the .pkg file, click Open, and click	
          Open on the pop up window. 	
          After installing Git, there will not be anything in your <code>/Applications</code> folder,	
          as Git is a command line program.	
          <strong>For older versions of OS X (10.5-10.8)</strong> use the	
          most recent available installer labelled "snow-leopard"	
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.	
        </li>
        <li>
          To ensure that you can use git with RStudio:
          <ol>
            <li>Open RStudio.</li>
            <li>In the menu, click on "Tools > Global Options...".</li>
            <li>Click on "Git/SVN".</li>
            <li>Ensure the checkbox "Enable version control interface for RStudio projects" is selected.</li>
            <li>Under "Git executable" click on "Browse".</li>
            <li>Navigate to the location of the <code>git</code> executable.</li>
            <li>Click "Open".</li>
            <li>Click "OK".</li>
          </ol>
        </li>
      </ol>	
    </div>	
    <div class="col-md-4">	
      <h4 id="git-linux">Linux</h4>
      <ol>
        <li>
          If Git is not already available on your machine you can try to	
          install it via your distro's package manager. For Debian/Ubuntu run	
          <code>sudo apt-get install git</code> and for Fedora run	
          <code>sudo dnf install git</code>.
        </li>
        <li>
          To ensure that you can use git with RStudio:
          <ol>
            <li>Open RStudio.</li>
            <li>In the menu, click on "Tools > Global Options...".</li>
            <li>Click on "Git/SVN".</li>
            <li>Ensure the checkbox "Enable version control interface for RStudio projects" is selected.</li>
            <li>Under "Git executable" click on "Browse".</li>
            <li>Navigate to the location of the <code>git</code> executable. This is typically located in "/usr/bin".</li>
            <li>Click "Open".</li>
            <li>Click "OK".</li>
          </ol>
        </li>
      </ol>
    </div>	
  </div>	
</div> {% comment %} End of 'Git' section. {% endcomment %}


