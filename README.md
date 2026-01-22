# ORSHARDS_Repo_Template
This is an empty template package for an ORSHARDS style repository, compatible with the ORSHARDS documentation tool and A4IM documentation aims. This is an extension of the UNIX standard to hardware. To create your package, follow the directions below. 

/
The root folder must contain the following:
	- Readme.md: this is the page that appears from git repository readers. It should contain basic explanations about the device and the structure of the package, the list of new feature for each release, etc. It is meant to be read by package developers, not deployers or users.
	- LICENSE.txt: this is a copy of the license file.
	- moduleinfo.txt: this is needed by ORSHARDS to keep track of the dependencies (will be moved to /lib in future releases)
	- RiskAssessment.txt: proposed document to track the risk assessment of the device (will be moved to /doc in future releases)

/bin
This folder contains the compiled software that runs on the operating computer to interact with the device.

/doc
Contains the manuals, datasheet, compliance info, risk management procedure and all static documents related to the object after it is constructed. Do NOT place anything here that relates to the contruction and deployment stages, these goes to /lib or /src.

/dev
This folder is needed when the device is to be connected to the host computer. It contains the links to handle the hardware.

/lib
Contains all information related to pre-fabricated elements that are to be integrated into the device during its assembly. This package includes a template BOM and should also store any technical documentation about sub-modules or parts, possibly in a separate sub-directories. 
Do NOT include anythin that has to be built during the assembly process. Any element described here should be readily available prior to the assembly process, similarly to a software library is available during compile time. This is to make sure that this folder can be used to assess dependencies for the package.
This folder can also contain read-made software needed for the device once deployed, or standard test procedures to run for system monitoring or fault assessment.

/src
This folder contains all the information needed to build the device during the assembly process. This usually contains documents that need to be compiled or processed in some ways, therefore this folder is organised into sub-directories following UNIX conventions:
  /src/bin - contains the compiled firmware and assembly documentation readily available to the assembly process. The content of this document is described in more details in /src/README.md, it typically stores the HTML files that the ORSHARDS software displays in the web browser.
  
  /src/doc - This folder documents the processes required for the assembly and modification of the device, including maintenance. This includes the Technology-specific Documentation Criteria as per DIN3105: these are the documents that specify the requirements for each steps of the entire life cycle of the scanner. They must be properly licensed with due labelling.
  
  /src/lib - This folder contains all the information already known about the parts that are to be assembled during the construction of the device. This includes the blueprints, CAD models, circuit boards, software libraries and additional technical files or artwork, and more generally all the documents mentioned by the Technology-specific Documentation Criteria as per DIN3105.
  This folder may also contain the test procedure for commissionning and performance evaluations.
  
  /src/lib/img - In here we have any non-technical images files used to illustrate the above generation of documentation. This can include assembly steps, screen captures, small videos...
  
  /src/src - contains all the documents that need to be compiled for the purpose of the assembly process. This includes source code for the software, but also the assembly instruction documentation if needed (for instance if you need to generate HTML files from MarkDown). Note that the compiled firmware should be stored in /src/bin, and locally-run sofware in /bin. Note also that this folder should include reglementation and guidelines relevant to the system assembly, as these may be seen as assembly rules similar to a Makefile for software compilation.
 
/var
This folder contains any non-permanent file that need to be changed during the lifetime of the device that is being constructed. This may include (but is not limited to):
  /var/log: User log files: activities performed by users and the device, test results, calibration files obtained from the tests performed during the assembly process, commissioning or maintenance of the device, risk management log files with any incident to be reported for risk management, etc.
  /var/tmp: temporary files that should be deleted after the completion of a task. Can be used as a buffer during deployment to make a clean process.
