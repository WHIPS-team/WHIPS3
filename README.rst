===========
WHIPS 3.1.1
===========

* **Project Title:** WHIPS
* **Purpose of Project:** Provide a well-documented, easy-to-use general-purpose processing module for processing satellite data
* **Version:** 3.1.1 (04/21/19)
* **Authors:** Tracey Holloway, Jacob Oberman, Peidong Wang
* **Contact:** taholloway@wisc.edu

Wisconsin Horizontal Interpolation Program for Satellites (WHIPS)
=================================================================

ACKNOWLEDGEMENT POLICY
----------------------
Whenever you publish research or present results generated with WHIPS,
please include the following acknowledgement or an appropriate
equivalent:

	*We wish to thank the University of Wisconsin-Madison for the* 
	*use and development of the Wisconsin Horizontal Interpolation*
	*Program for Satellites (WHIPS).  WHIPS was developed by Tracey* 
	*Holloway, Jacob Oberman and Peidong Wang, with funding from* 
	*the NASA Air Quality Applied Science Team (AQAST) and* 
	*the NASA Health and Air Quality Applied Sciences Team (HAQAST).*


QUICK START
-----------


1. Install the program and run the built-in test module to confirm
that it is working properly.  Installation instructions can be found
in the WHIPS user guide.


2. Download whatever data you plan to process.  Currently, the program
is designed to process OMI NO2 DOMINO level 2 data, OMI NO2 NASA level
2 data, MOPITT CO data, NASA MODIS AOD level 2 data, and OMI SO2 level 2 data.  See the 
detailed documentation for the --filelist argument for locations of data.


3. Navigate to the folder where whips.py is located (or add it to
your path) and invoke it as:

     whips.py --help


4. Follow the on-screen instructions, adding each of the required
parameters.  If you need help with the projection attributes or the
output function attributes, invoke the built-in help as:

     whips.py --AttributeHelp <function_name>

For detailed explanations of all parameters and attributes, see the
"Parameter Details" section below.


5. Invoke whips.py once for each output file you'd like to create.
Note that the software creates output files with only a single
timestep, so you'll need to invoke the command once for each timestep
(IE if you want a month with timesteps every day, you'll probably want
to write a shell script that calls the command once for each day)


6. Additionally, you may create a grid file for your chosen grid by
including the --includeGrid flag followed by the desired filename.
A file containing the gridcells used by the projection will be written
to the same directory as the standard output file.


7. Concatenate your outputs if desired (the authors recommend the NCO
operators at http://nco.sourceforge.net/ if you're using a netCDF
output format) and carry on!

