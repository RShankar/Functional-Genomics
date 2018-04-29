# Functional-Genomics
Learn and  Document tools, links, and methods in functional genomics

1. Ignore this step: Started installing Bio-Linux from http://environmentalomics.org/bio-linux/ . "Bio-Linux 8 adds more than 250 bioinformatics packages to an Ubuntu Linux 14.04 LTS base, providing around 50 graphical applications and several hundred command line tools. The Galaxy environment for browser-based data analysis and workflow construction is also incorporated in Bio-Linux 8." This required installation of Oracle's VM VirtuaBox from http://www.oracle.com/technetwork/server-storage/virtualbox/downloads/index.html . Instructions on the installation of Bio-Linux in VM are here: http://environmentalomics.org/bio-linux-installation/ . Notes: Dual-boot was discouraged by our IT experts. An article they referenced: https://www.lifewire.com/run-ubuntu-within-windows-virtualbox-2202098 . I am using Windows 7. Online tutorial to learn Bio-Linux: http://nebc.nerc.ac.uk/downloads/courses/Bio-Linux/bl8_latest.pdf . Recent comments by the author of Bio-Linux made me **put bio-Liunx on the backburner**.

2. Installed Ubuntu 16.04 LTS version on my Linux laptop. It has 16GB RAM, Intel's i7 CPU (x4) at 2.5 GHz, 64-bit and 250 GB disk. Python 2.7 is extensively used in genomic data analysis. It is available in 16.04 with 'pytyon' command; python 3 is available with the python3 command. Checked with python -V and python3 -V. Signed up for the Biostar course at Penn State and the professional version of the handbook ($35) at https://www.biostarhandbook.com/ . One gets a certificate of completion when the course quizzes etc are completed. This course is also recommended by the author (Dr. Pevsner) of "Bioinformatics and Functional Genomics." I will be using this book also. I am also learning from "Primer to Analysis of Genomic Data Using R" by Cedric Gondro. USCS' Genome Browser has data and links that are very useful: https://genome.ucsc.edu/. Following text and exercises in two other books: Functional Genomics book by Pevsner and Intro to Computational Genomics by Cristianini and Hahn. 

3. Biostar course mentions these GUI tools in the first lecture, but emphasizes the use of the command line. Here are the GUI tools that hide the command line: Galaxy - see: https://galaxyproject.org/learn/ ; on reproducible bioinformatics - Gene Pattern - see https://software.broadinstitute.org/cancer/software/genepattern/; Cloud-based framework - GenomeSpace - see http://www.genomespace.org/what-is-genomespace ; Galaxy installation tutorial: https://galaxyproject.org/admin/get-galaxy/ . I cd-ed to my Genome directory and executed the production line of command: git clone -b release_17.05 https://github.com/galaxyproject/galaxy.git . Then I cd-ed to galaxy subdirectory and executed this: sh run.sh . Now launch the local copy at localhost:8080 in a browser window. 

4. Setting up my PC for the biostar course: Directions are given in the online book. They work. First initialize terminal configuration (section 1.1) and then install conda for creating 'bioinfo' environment (section 1.2). It uses python3. I installed doctor.py as per the online version of the handbook. It indicated that R is missing, along with a few optional program and an error. First, i will install R and then run doctor.py --fixme. Installing R on Linux requires update of /etc/apt/sources.list. See also: https://help.ubuntu.com/lts/serverguide/configuration.html . It cannot be done through LibreOffice Writer as it requires sudo. Here is the method: https://askubuntu.com/questions/197564/how-do-i-add-a-line-to-my-etc-apt-sources-list . Note: I have not, as of 11/6/17, gone beyond the Unix introduction; so, I am not sure whether conda has bioconductor packages - supposed to - and if so, where. So, I am installing them for my work on the R Primer (see #9 below).

5. use 'file <full file name>' to find out what type of file a document is. 

6. For R and RStudio installation, I used this: https://www.r-bloggers.com/how-to-install-r-on-linux-ubuntu-16-04-xenial-xerus/ . I used biostar's doctor.py script to verify that I had all the tools, inclusive of R, for bioinformatics, as per biostar. Note: The author of doctor.py recommends a local version of entrez-direct. 

7. Editor: Biostar recommends Sublime Text 2. Now,it is version 3. use the apt steps here: http://www.sublimetext.com/docs/3/linux_repositories.html . I also downloaded and installed PyCharm (community edition), useful for both text editing and programming in Python. Untar and save in the /opt directory. Cd to /opt/bin and run: sh pycharm.sh. The GUI for Pycharm opens up. Enabled opening files and projects from the command line by clicking on a box. Script path: **/usr/local/bin/charm**

8. Free PDF of "Primer to Analysis of Genomic Data Using R" by Cedric Gondro can be downloaded from springerlink.com. Data files (from livestock research projects) can be downloaded from: http://www.springer.com/?SGWID=0-102-2-1505441-0 . The author uses R with for and if constructs - I would think that would be slower relative to some library calls based on underlying C code. The author does not use knitR for self-documenting. (Update: the for and if loops seem to be needed. I have started using them extensively). Typing which R in the terminal (or command line) window tells you where R is located, typically at **/usr/bin/R**. Typing rstudio in the same window will launch Rstudio. RStudio was outdated. I followed instructions to download version 1.1.383 for ubuntu 16.04. Installation instructions are as given here: https://www.r-bloggers.com/how-to-install-r-on-linux-ubuntu-16-04-xenial-xerus/, with the version # updated. Example in Chapter 1 completed (on R). Second chapter is about applying R for **microsatellites**. 

9. Install bioconductor. Chapter 2 of the R Primer book requires packages from bioconductor (made4 etc). Installation instructions: https://www.bioconductor.org/install/ . First start R by typing R in a terminal window at the shell prompt. This step is needed first:  
source("https://bioconductor.org/biocLite.R"). Bioconductor core and other packages are then installed with biocLite(). biocLite() installs multiple core packages. To add others, use this format: biocLite(c("GenomicFeatures", "AnnotationDbi")). Downloaded packages are in /tmp/Rtmpp2hjZ/downloaded_Packages' . biocLite("made4") was used to install made4 needed in chapter 2 of the R Primer book. quit("yes") will terminate the R session. Type rstudio in the terminal window to keep going. Make sure you are in the correct subdirectory (?). library("made4") installs the package. R provides the appropriate paths. 

10. 11/20/17 -- Installed stringr through RStudio and used it in completing the quiz for data analytics using Unix (Quiz 3) in the Biostar series. I had already completed with the command shell window. I have not placed copies of these here since this is an on-going course. I am merely documenting my work here for future reference. 

11. 11/22/17 -- Installing "Biostrings" with this:  Start R and type the following, one line at a time:
source("https://bioconductor.org/biocLite.R")
biocLite("Biostrings")
I do see an installer ("BiocInstaller") in the Home/R in a subdirectory. Perhaps I should launch it from there, if I do not wish to use the source command. I will just use the source command. It worked. Chose to update all ('a') related files. 

12. Still trying to navigate around the Unix tree. The "/" is the root - relabeled as 'shankardell' (my PC name) in the File Explorer. It is easy to get to it in an terminal window with cd / , but click on the Pc name to find this root in the File Explorer. Clicking on Home will lead to user directories. Re-study all the sub folders you see there.

13. I will use this tutorial: https://web.stanford.edu/class/bios221/labs/biostrings/lab_1_biostrings.html to learn about biostrings. Uploaded the completed tutorial R file to Github (here).
14. I will now use BioStrings for exercises in "Introduction to Computational Genomics" By Cristianini and Hahn. R files
will be uploaded to the corresponding subdirectory at Github. 
15. As of 4/25/18: I could not download KEGGREST, an R package to access KEGG database, from CRAN, i.e., directly in RStudio from the Tools tab. This [site](https://bioconductor.org/packages/release/bioc/html/KEGGREST.html) gives directions that I used. Had already updated the R version to 3.4.4, assuming that was the reason for this non-availability. The steps for R update are given earlier. Also, KEGGREST update is similar to step 11 above, as it is available as part of the bioconductor suite. XML and rtracklayer had non-zero exit status. That means, they are not loaded/up-to-date. Here is instruction for XML from this [reference](https://support.bioconductor.org/p/54969/) : Try this at the unix command line: sudo apt-get install -y libcurl-dev libxml2-dev Then try installing XML again. This time the msg was about explicitly selecting a specific non-virtual package. From a help site: install libcurl4-gnutls-dev. Did that. Now reinstalling KEGGREST. Still the same problem - now xml and rtracklayer had non-zero exits. 

16. Update from a blog site: 
    Install curl-devel and libxml with the Linux command line:

$ sudo yum install curl curl-devel
$ sudo yum -y install libxml2 libxml2-devel

    On R console, restart the R session and install the RCurl and XML package:

>> install.packages("RCurl")
>> install.packages("XML")

    Load the libraries:

>> library(RCurl)
>> library(XML)

