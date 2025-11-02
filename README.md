# ORSHARDS_Repo_Template
This is an empty template package for an ORSHARDS style repository, compatible with the ORSHARDS documentation tool and A4IM documentation aims. This is an extension of the UNIX standard to hardware. To create your package, follow the directions below. 

/
The root folder must contain the following:
	- Readme.md: this is the page that appears from git repository readers. It should contain basic explanations about the device and the structure of the package, the list of new feature for each release, etc. It is meant to be read by package developers, not deployers or users.
	- LICENSE.txt: this is a copy of the license file.
	- moduleinfo.txt: this is needed by ORSHARDS to keep track of the dependencies (will be moved to /lib in future releases)
	- RiskAssessment.txt: proposed document to track the risk assessment of the device (will be moved to /doc in future releases)

/doc
Contains the manuals, datasheet, compliance info, risk management procedure and all static documents related to the object after it is constructed. Do NOT place anything here that relates to the contruction and deployment stages, these goes to /lib or /src.

/lib
Contains all information related to pre-existing elements that are to be integrated into the device to be constructed. This package includes a template BOM, and any documentation about a sub-module can be added in a separate directory. 
Do NOT include anythin that has to be built by the assembly chain. Any element described here should be readily available during the assembly process, similarly to a software library is available during compile time.

/src
This folder contains all the information needed by the assembly chain to build the device. This usually contains documents that need to be compiled to be generated into the correct format, therefore this folder is organised into sub-directories following UNIC conventions:
  /src/bin - contains the assembly documentation readily available to the assembly chain. The content of this document is described in more details in /src/README.md
  
  /src/lib - In here we have HTML files that the ORSHARDS software will display in the web browser.
  
  /src/src - In here we have the files used to make/generate the assembly documentation. For example, this folder is used by the GitBuilding Tool to store MarkDown files that generate the final HTML documents after compilation.
  
  /src/img - In here we have the any images files used in the above generation of documentation.

/var
This folder contains any non-permanent file that need to be changed during the lifetime of the device that is being constructed. This may include (but is not limited to):
  User log files: activities performed by users.
  Risk management log files: any incident to be reported for risk management.
  Test results: log files and calibration files obtained from the tests performed during the assembly process, commissioning or maintenance of the device
