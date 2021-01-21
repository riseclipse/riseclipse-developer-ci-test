
### Building the fat jar SCL validator with Eclipse
* Install **Eclipse IDE for Java Developers**
* Install (*Help → Install New Software…*) **Eclipse plug-in development environment**
* Import the **fr.centralesupelec.edf.riseclipse.developer.eclipse** Eclipse project from the [riseclipse-developer Git repository](https://github.com/riseclipse/riseclipse-developer/)
* Open the **/fr.centralesupelec.edf.riseclipse.developer.eclipse/fr.centralesupelec.edf.riseclipse.developer.eclipse.target** file
* Click on *Set as Active Target Platform*
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
* *Right-click* on the **fr.centralesupelec.edf.riseclipse.iec61850.scl.validator** project, choose *Run As → Java Application*, type *riseclipse* in the search field and
select *RiseClipseValidatorSCL*; the short help message of the tool should be displayed in the Console view of Eclipse
* *Right-click* on the **fr.centralesupelec.edf.riseclipse.iec61850.scl.validator** project, choose *Export… → Java → Runnable JAR file*, select *RiseClipseValidatorSCL*
as *Launch configuration*, a suitable directory and name as *Export destination*, select *Package required libraries into generated JAR* and click on *Finish*
