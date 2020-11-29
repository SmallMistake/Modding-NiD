# The players route is controlled by a data structure usually stored at the end of bin files for each stage.
The files can be found by looking for names that follow the pattern of "stage_#_boss_SDF.bin" or stage_#_SDF.bin in the afs folder.

The file stage_4_boss_SDF.bin is the easiest one to use for analyzing route data since it only contains said route data.

All routes are defined by:

## Headers will look like a varient of the below.

![Route Header](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/routeHeader.PNG) </br>
The most tell tale sign that is consistent across files is the two grouping of the four empty spaces appering in that arrangement.

## Route data will appear like below.

![Route Data](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/routeData.PNG) </br>
You will notice that all route data instances must be started with a 0A 00 00 00 byte.

## Route group sections will follow every route data section

![Route Group](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/routeGroup.PNG) </br>
Route Groups are denoted with a 0B 00 00 00 byte.
