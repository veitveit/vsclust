**Welcome to the repository of VSClust**
developed at the

[Protein Research Group](http://www.sdu.dk/en/Om_SDU/Institutter_centre/Bmb_biokemi_og_molekylaer_biologi/Forskning/Forskningsgrupper/Protein.aspx)  
Department of Biochemistry and Molecular Biology  
[University of Southern Denmark](http://www.sdu.dk)  

## Shiny app

### Web service

You can use our web server http://computproteomics.bmb.sdu.dk:

http://computproteomics.bmb.sdu.dk/Apps/VSClust

Be aware that the tool does allow only one user to run the operations at a time. Therefore the app might become temporarily irresponsive. 

### Implementation on own computer
You can run the shiny app from the server.R or ui.R files using [Rstudio](http://rstudio.com), run the app on a shiny-server

Be aware that you need to have all files *and* the modified e1071 library installed.


### Installation
Download the files into a folder and install the library *e1071FuzzVec*. You might need to compile the library on your computer:  
Run *R CMD INSTALL e1071FuzzVec_Installation* from the command line. You need to be in the VSClust folder. For Windows users, replace *R* by *InstallationPath/R.exe*.

### Install and use Docker image
A Dockerfile has been created on the basis of an OpenSuse distribution. Copy the repository to a folder and carry out the following command to build the images (takes a while)

*sudo docker build -t shiny-server*

You can run the image by

*sudo docker run -t -i -p 3838:3838 shiny-server*

and access the server through http://localhost:3838/VSClust/

## Command line 

All operations but the gene set enrichment can be carried via command line running the R script runVSClust.R

### Usage

Given that you installed the *e1071FuzzVec* library, open the R script and change the relevant file names and parameters.

### Installation
The *e1071FuzzVec* library needs to be compiled and installed, see above.


## Contact
For software issues and general questions, please submit an issue.

## License
GPL-2 or higher