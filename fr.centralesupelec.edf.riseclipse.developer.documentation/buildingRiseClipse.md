
# Building Eclipse

### Building the command line fat jar SCL validator with Eclipse
*Tested on 21-01-2021 with Eclipse 2020-12 running with its included JRE (version 15.0.1)*
* Install **Eclipse IDE for Eclipse Committers**
* Import the **fr.centralesupelec.edf.riseclipse.developer.eclipse** Eclipse project from the [riseclipse-developer Git repository](https://github.com/riseclipse/riseclipse-developer/)
* Open the **/fr.centralesupelec.edf.riseclipse.developer.eclipse/fr.centralesupelec.edf.riseclipse.developer.eclipse.target** file
  * Click on *Set as Active Target Platform*; the resolution of the target platform will take some time (needed artifacts are downloaded),
the clicked text will change to *Reload Target Platform* when this is finished

* Import the following Eclipse projects:
  * **fr.centralesupelec.edf.riseclipse.main** from [riseclipse-main Git repository](https://github.com/riseclipse/riseclipse-main/)
  * **fr.centralesupelec.edf.riseclipse.iec61850.scl** from [riseclipse-metamodel-scl2003 Git repository](https://github.com/riseclipse/riseclipse-metamodel-scl2003)
  * **fr.centralesupelec.edf.riseclipse.iec61850.scl.edit** from [riseclipse-metamodel-scl2003 Git repository](https://github.com/riseclipse/riseclipse-metamodel-scl2003)
  * **fr.centralesupelec.edf.riseclipse.iec61850.scl.utilities** from [riseclipse-metamodel-scl2003 Git repository](https://github.com/riseclipse/riseclipse-metamodel-scl2003)
  * **fr.centralesupelec.edf.riseclipse.iec61850.nsd** from [riseclipse-metamodel-nsd2016 Git repository](https://github.com/riseclipse/riseclipse-metamodel-nsd2016)
  * **fr.centralesupelec.edf.riseclipse.iec61850.nsd.edit** from [riseclipse-metamodel-nsd2016 Git repository](https://github.com/riseclipse/riseclipse-metamodel-nsd2016)
  * **fr.centralesupelec.edf.riseclipse.iec61850.nsd.utilities** from [riseclipse-metamodel-nsd2016 Git repository](https://github.com/riseclipse/riseclipse-metamodel-nsd2016)
  * **fr.centralesupelec.edf.riseclipse.validation.ocl** from [riseclipse-validator-ocl Git repository](https://github.com/riseclipse/riseclipse-validator-ocl)
  * **fr.centralesupelec.edf.riseclipse.iec61850.scl.validator** from [riseclipse-validator-scl2003 Git repository](https://github.com/riseclipse/riseclipse-validator-scl2003/)
* *Right-click* on the **fr.centralesupelec.edf.riseclipse.iec61850.scl.validator** project
  * choose *Run As → Java Application*
  * type *riseclipse* in the search field and select *RiseClipseValidatorSCL*
  * the short help message of the tool should be displayed in the Console view of Eclipse
* *Right-click* on the **fr.centralesupelec.edf.riseclipse.iec61850.scl.validator** project
  * choose *Export… → Java → Runnable JAR file*
  * select *RiseClipseValidatorSCL* as *Launch configuration*
  * choose a suitable directory and name as *Export destination*
  * select *Package required libraries into generated JAR*
  * click on *Finish*

### Building the command line fat jar SCL validator with Maven
*Tested on 25-01-2021 with Maven version 3.6.3 running with Java 8.0.275*

**Warning:** The unpack200 tool is needed, it is available in JDK up to version 13

**Warning:** It may be a good idea to delete an existing local maven repository before building

* Clone in the same folder the following Git repositories from GitHub:
  * [riseclipse-developer](https://github.com/riseclipse/riseclipse-developer/)
  * [riseclipse-main](https://github.com/riseclipse/riseclipse-main/)
  * [riseclipse-metamodel-scl2003](https://github.com/riseclipse/riseclipse-metamodel-scl2003)
  * [riseclipse-metamodel-nsd2016](https://github.com/riseclipse/riseclipse-metamodel-nsd2016)
  * [riseclipse-validator-ocl](https://github.com/riseclipse/riseclipse-validator-ocl)
  * [riseclipse-validator-scl2003](https://github.com/riseclipse/riseclipse-validator-scl2003/)
* Open a Terminal, go to the choosen folder
  * `cd riseclipse-developer`
  * `cd fr.centralesupelec.edf.riseclipse.developer.maven.validator.scl`
  * `mvn install`
* The fat jar will be available in **riseclipse-validator-scl2003/fr.centralesupelec.edf.riseclipse.iec61850.scl.validator/target**


