# Functional-Genomics
Learn and  Document tools, links, and methods in functional genomics

1. Installed Bio-Linux from http://environmentalomics.org/bio-linux/ . "Bio-Linux 8 adds more than 250 bioinformatics packages to an Ubuntu Linux 14.04 LTS base, providing around 50 graphical applications and several hundred command line tools. The Galaxy environment for browser-based data analysis and workflow construction is also incorporated in Bio-Linux 8." This required installation of Oracle's VM VirtuaBox from http://www.oracle.com/technetwork/server-storage/virtualbox/downloads/index.html . Instructions on the installation of Bio-Linux in VM are here: http://environmentalomics.org/bio-linux-installation/ . Notes: Dual-boot was discouraged by our IT experts. An article they referenced: https://www.lifewire.com/run-ubuntu-within-windows-virtualbox-2202098 . I am using Windows 7. Online tutorial to learn Bio-Linux: http://nebc.nerc.ac.uk/downloads/courses/Bio-Linux/bl8_latest.pdf . Recent comments by the author of Bio-Linux made me put bio-Liunx on the backburner.

2. Installed Ubuntu 16.04 LTS version on my Linux laptop. It has 16GB RAM, Intel's i7 CPU (x4) at 2.5 GHz, 64-bit and 250 GB disk. Python 2.7 is extensively used in genomic data analysis. It is available in 16.04 with 'pytyon' command; python 3 is available with the python3 command. Checked with python -V and python3 -V. Signed up for the Biostar course at Penn State and the professional version of the handbook ($35) at https://www.biostarhandbook.com/ . One gets a certificate of completion when the course quizzes etc are completed. This course is also recommended by the author (Dr. Pevsner) of "Bioinformatics and Functional Genomics." I will be using this book also. I am also learning from "Primer to Analysis of Genomic Data Using R" by Cedric Gondro. USCS' Genome Browser has data and links that are very useful: https://genome.ucsc.edu/

3. Biostar course mentions these GUI tools in the first lecture, but emphasizes the use of the command line. Here are the GUI tools that hide the command line: Galaxy - see: https://galaxyproject.org/learn/ ; on reprocible bioinformatics - Gene Pattern - see https://software.broadinstitute.org/cancer/software/genepattern/; Cloud-based framework - GenomeSpace - see http://www.genomespace.org/what-is-genomespace ; Galaxy installation tutorial: https://galaxyproject.org/admin/get-galaxy/ . I cd-ed to my Genome directory and executed the production line of command: git clone -b release_17.05 https://github.com/galaxyproject/galaxy.git . Then I cd-ed to galaxy subdirectory and executed this: sh run.sh . Now launch the local copy at localhost:8080 in a browser window. 

4. Setting up my PC for the biostar course: Directions are given in the online book. They work. First initialize terminal configuration (section 1.1) and then install conda for creating 'bioinfo' environment (section 1.2). It uses python3. I installed doctor.py as per the online version of the handbook. It indicated that R is missing, along with a few optional program and an error. First, i will install R and then run doctor.py --fixme. Installing R on Linux requires update of /etc/apt/sources.list. See also: https://help.ubuntu.com/lts/serverguide/configuration.html . It cannot be done through LibreOffice Writer as it requires sudo. Here is the method: https://askubuntu.com/questions/197564/how-do-i-add-a-line-to-my-etc-apt-sources-list

5. use 'file <full file name>' to find out what type of file a document is. 

6. For R and RStudio installation, I used this: https://www.r-bloggers.com/how-to-install-r-on-linux-ubuntu-16-04-xenial-xerus/ . I used biostar's doctor.py script to verify that I had all the tools, inclusive of R, for bioinformatics, as per biostar. Note: The author of doctor.py recommends a local version of entrez-direct. 

7. Editor: Biostar recommends Sublime Text 2. Now,it is version 3. use the apt steps here: http://www.sublimetext.com/docs/3/linux_repositories.html 
