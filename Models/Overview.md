# Overview
Most of the models appear to be held in binary files in the afs folder.

### Characters
The files follow the pattern of "DAT" + Name of Character + ".BIN"
I have found the program Model Researcher to be able to extract the models from these files.

Here are some examples:

DATNIGHTS.BIN
![Nights' Model](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Models/pictures/DATNIGHTS_BIN.PNG)
There are multiple models layered on top of each other. It is easiest to make out NiGHTS hat at the top and left of the image.
I have found an offset of 0x2910 and a count of 7890 gives the cleanest reading

DATWIZE.BIN
![Wizeman's Model](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Models/pictures/DATWIZE.PNG)
Wizeman's 6 hands are the easiest point of reference because they show up distinctly in the front of everything else.


### Levels

 Levels appear to be broken up into chunks in one file and then put together based off of data from another.
 Files with the name schema "PNODM_ST" + Stage Number + "_PIA_GRDPS2.BIN" appear to hold the data for the level pieces.
 Files with the name schema "TNODM_ST" + Stage Number + "_PIA_GRDPS2.BIN" appear to be used with the previous file to create finished levels
 
Example:

Level 3

PNODM_ST03_PIA_GRDPS2.BIN
![Level 3 Parts](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Models/pictures/PNODM_ST03_PIA_GRDPS2.PNG)

TNODM_ST03_PIA_GRDPS2.BIN
![Level 3 Something](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Models/pictures/TNODM_ST03_PIA_GRDPS2.PNG)

This is pure guess work, but I feel comfortable stating that these two file types are used together in some version the described way. 
