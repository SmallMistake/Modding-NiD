# Route Data

Route data is stored in a collection of route_data containers. They are headed by the byte "0A 00 00 00."

I have defined one segment of route data as being everything starting from the header to the empty space before the next header as seen below.

![Segment Example](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/RouteData.PNG)


### Segment 1
I cant figure out what this one does, becuase interchanging them amoung other routes does not seem to make any difference. For example, you can put boss 2's into stage 1 and nothing will happen or crash.

### Segment 2
Segment two seems to be used to state whether or not the stage is a boss stage or a normal stage.

Normal Stages are denoted by 01 00 00 00.

Boss Stages are denoted by 02 00 00 00

Stage 1:

![Stage 1 Segment 2](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/stage_1_segment_2.PNG)

Stage 2:

![Stage 2 Segment 2](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/stage_2_segment_2.PNG)

Stage 2 Boss:

![Stage 2 Boss Segment 2](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/stage_2_boss_segment_2.PNG)

Ignore the extra highlight; that section goes with the next segment.

There is an oddity with a few of these segments that include an extra bit after route_data as seen in stage_2_boss. Zeroing this does not crash the game and their does not seem to be any difference.



### Segment 3

Segment 3 appears to control the location of the track and partially the shape of the track.

This can most be demonstrated by inserting Boss 2's data into other levels' corrosponding parts. If you will remember, the opera lady has you going thru a circular level and various rooms.
The way this is accomplished is by having the track only cover about 2/3rds of the circle. The player is then teleported to the other side of the track once they reach the end of the other side.
This ensures that the level can unload parts of the level in such a way so that the player never even knows they are not really going all the way around.

Putting boss two's code into boss three shows this fact off best.

![Boss 4 with Boss2's segment](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/segment3Edited.png)

You will notice that the mice do not go all the way around. Once a mouse, Nights, or even the boss goes past the teleport point they loop back around on the other side. Furthermore, you will notice that track has been moved outside of the arena.

Putting this same code into any boss produces the same results.


Level one has a slightly different reaction.

![Level 1 with Boss2's Segment](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/levelOneTP.png) </br>
Ellie will start like normal but, NiGHTS will not be in their palace. Going into the palace will start you as NiGHTS in the middle of nowhere as shown above.

![Level 1 TP Point](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Route_Data/pictures/levelOneTPPoint.png) </br>
Going left or right for a small bit will TP you back to the track and every thing will be normal. However, going back into the area that holds the palace will TP you back into the middle of nowhere. You can not move on to the next mare because you can not put the idia into the palace. Obviously, the only conclusion that can be drawn is that Ben is haunting my game.
