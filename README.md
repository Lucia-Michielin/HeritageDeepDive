#Computational Research Deep Dive
Welcome to the Heritage Computational Research Deep Dive Repo. In here you can find material and code to analyse the Scottish Statistical Accounts Data and see computational methods in practice.

## Content of the Repository
The repository contains both the code and the material you are going to need to play around with the dataset. 
If you only want to visualise the notebook without running its content you can visualise it at [this address](https://htmlpreview.github.io/?https://github.com/DCS-training/EFIDeepDive/blob/main/EFIDeepDiveNoteable.html).


## How to use it

### Local installation of R and R Studio 
* R and RStudio are separate downloads and installations. R is the
underlying statistical computing environment, but using R alone is no
fun. RStudio is a graphical integrated development environment (IDE) that makes
using R much easier and more interactive. You need to install R before you
install RStudio.

##### Windows

> ### If you already have R and RStudio installed
>
> * Open RStudio, and click on "Help" > "Check for updates". If a new version is
> available, quit RStudio, and download the latest version for RStudio.
> * To check which version of R you are using, start RStudio and the first thing
>  that appears in the console indicates the version of R you are
>  running. Alternatively, you can type `sessionInfo()`, which will also display
>  which version of R you are running. Go on
>  the [CRAN website](https://cran.r-project.org/bin/windows/base/) and check
> whether a more recent version is available. If so, please download and install
> it. You can [check here](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#How-do-I-UNinstall-R_003f) for
> more information on how to remove old versions from your system if you wish to do so.

> ### If you don't have R and RStudio installed
>
> * Download R from
>  the [CRAN website](https://cran.r-project.org/bin/windows/base/release.htm).
> * Run the `.exe` file that was just downloaded
> * Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
> * Under *Installers* select **RStudio x.yy.zzz - Windows Vista/7/8/10** (where x, y, and z represent version numbers)
> * Double click the file to install it
> * Once it's installed, open RStudio to make sure it works and you don't get any
> error messages.


##### macOS

> ### If you already have R and RStudio installed
>
> * Open RStudio, and click on "Help" > "Check for updates". If a new version is
>	available, quit RStudio, and download the latest version for RStudio.
>	* To check the version of R you are using, start RStudio and the first thing
>	  that appears on the terminal indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will 
>	also display which version of R you are running. Go on
>	  the [CRAN website](https://cran.r-project.org/bin/macosx/) and check
>	  whether a more recent version is available. If so, please download and install
>	  it.
{: .solution}

> ### If you don't have R and RStudio installed
>
> * Download R from
>   the [CRAN website](https://cran.r-project.org/bin/macosx/).
> * Select the `.pkg` file for the latest R version
> * Double click on the downloaded file to install R
> * It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed
>   by some packages)
> * Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
> * Under *Installers* select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)**
>   (where x, y, and z represent version numbers)
> * Double click the file to install RStudio
> * Once it's installed, open RStudio to make sure it works and you don't get any
>   error messages.

##### Linux

* Follow the instructions for your distribution
 from [CRAN](https://cloud.r-project.org/bin/linux), they provide information
 to get the most recent version of R for common distributions. For most
 distributions, you could use your package manager (e.g., for Debian/Ubuntu run
 `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we
 don't recommend this approach as the versions provided by this are
 usually out of date. In any case, make sure you have at least R 3.5.1.
* Go to the [RStudio download
  page](https://www.rstudio.com/products/rstudio/download/#download)
* Under *Installers* select the version that matches your distribution, and
   install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i
   rstudio-x.yy.zzz-amd64.deb` at the terminal).
* Once it's installed, open RStudio to make sure it works and you don't get any
   error messages.

## Set up Packages needed
Once you have installed R and R studio you can open the notebook we are going to use by double clicking on 'DeepDivePosit.Rmd'


Please also run the following code to install the packages needed. The same installation commands are present at the start of the document but they are commented out. 
To run them you need to remove all the # you see in the first two cells of code.

'install.packages("rmarkdown")
install.packages("remotes")
library(remotes)
install_github("r-spatial/sf")
install.packages("tmap")
install.packages("quanteda")
install.packages("RColorBrewer")
install.packages("here")
install.packages("tidyverse")
install.packages("data.table")
'
To run a cell in rmarkdown you can press the triangle symbol on the top right corner of each cell 

### On Posit 
1. Go to https://posit.cloud/
2. Signup either via Gmail or GitHub
3. Go on New Project
4. New Project from Git Repository
5. Copy and Paste this repository URL [https://github.com/Lucia-Michielin/HeritageDeepDive](https://github.com/Lucia-Michielin/HeritageDeepDive) as the Repository URL
6. The Project directory name will filled in automatically

Congratulations you have now pulled the content of the repository on your Notable server space the last thing you need to do is to install the packages you will need for this tutorial.

#### Open the code file
1. Double-click on the `DeepDivePosit.Rmd`
2. This is an [R Markdown](http://rmarkdown.rstudio.com) Notebook. When you execute code within the notebook, the results appear beneath the code.
3. Try executing a chunk by clicking the *Run* button within the chunk or by placing your cursor inside it and pressing *Ctrl+Shift+Enter*.
4. The first block `Libraries Install and Load` will install and load the package you need. it may take some time to fully run. To install the packages you will need to remove all the # from the first two cells

## Data 
The data in here have been collected from the Scottish Statistical Accounts Data https://collectionsmanager.is.ed.ac.uk/handle/10683/119269 and the National Records of Scotland https://www.nrscotland.gov.uk/statistics-and-data/geography/our-products/other-national-records-of-scotland-nrs-geographies-datasets/historic-civil-parishes-pre-1891

## Licence of the material
All the material collected here is covered by a CC-BY-NC 4.0 License

