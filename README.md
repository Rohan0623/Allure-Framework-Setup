# Setup Allure-report in Local Machine and in Jenkins


Versions I tried with:

1. Java 1.8.0_261
2. Selenium 3.141.59
3. TestNG 6.14.3
4. Apache Maven 3.6.3
5. Maven cleaner plugin 3.1.0
6. Maven compiler 3.8.0

_Add the TestNg dependency and maven plugins in the pom.xml file. The dependencies are mentioned in the file in allure-testng folder_ 


A) Steps to setup in Local machine
  
  1. In the pom.xml file install the allure-testng maven dependency. 
  2. Install Allure Binary binary file from the https://github.com/allure-framework/allure2/releases into a local machine and unzip it to a particular location.
  3. Set the path for the bin folder in the bashrc or bash_profile in your system command : **export PATH="path_to_bin_folder:$PATH"**
  4. Open the new terminal and type **allure --version** to validate the installation and check the version
  5. Run the project or any particular test.  **allure-results** folder will be generated which will contain one result and JSON file corresponding to each test   
     case 
  7. To generate the report go to the terminal, go the root folder of the project and type **allure serve** to generate the allure report

-----------------------------------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------------------------------


B) Steps to setup in Jenkins

  1. In jenkins go to the Manage Jenkins-> Manage Plugins -> Install the Allure Jenkins Plugin.
  2. Go to the Manage Jenkins -> Global Tool Configuration and Add Allure Commandline 
  3. Go to the particular Jenkins Job and click Configure. In the Post build Actions section add the path to the allure results folder. Click Advanced and add the   
     report path of the allure reports. 
     
     _Add the paths according to where the allure-results and allure reports are getting generated in your project. Report path has to be the target folder_
  
  4. Build your project. Allure report will be generated for the project.


  _Screenshots of setup in Jenkins is added in the screenshots folder_




