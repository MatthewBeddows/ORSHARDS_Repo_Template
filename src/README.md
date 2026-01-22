This folder is dedicated to the generation of the assembly files. In the context of ORSCHARDS, this is similar to the space needed to pre-compile a code before the final build. 

Ideally, preparatory document such as MarkDown files should be stored in /src/src, and the final instruction files should be stored in /src/bin.
BOM and STL files (or similar) should be in /src/lib.
Illustrative images should be in /src/doc/img or similar, depending on their use.

When writing the assembly documentation, please follow the requirements below:

- The main page of the documentation MUST contain the following information:
	- The name of the product with a unique identifier
	- The version number of the document
	- A time stamp corresponding to the last modification made to the documentation
	- The names of the authors for the documentation
	- Key functional elements 
	- Parts and components (can be listed automatically by GitBuilding)
	- Software needed
	- formulations, compositions, functionalities 
	- labelled pictorial representations (diagrams, photographs, and drawings) including sufficient explanation to understand the drawings and diagrams

For CE marking please remember:
	- Include the complete set of labels on the device in the assembly instructions, 
	- Include instruction pages for packing/unpacking the device for shipment, with details such as single unit packaging, sales packaging, transport packaging. 
	- Make sure the assembly documentation is written/translated in a languages accepted where the device will be sold
	- Include a final product testing procedure. Its outcomes must be saved in /var.
	- Add pages dedicated to the description and validation of the manufacturing processes.  
	
Future versions of ORSHARDS should include the following capabilities:
	- Provide clear designation and identification of all sites where manufacturing activities are performed (include suppliers and sub-contractors), or document this in /var if they are to be determined during the assembly process. Ideally, this will be handled automatically with future versions of ORSHARDS (assembly chains can be turned to packages).
	- Clear documentation about the design chain that led to the package (developers, company, responsible persons...)
	- Continuous monitoring method must be included in the deployment

