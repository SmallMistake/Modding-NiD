# Overview

### File Structure

The afs folder hold most of the music ques for the game.

I believe I have found that files with end with ".sfd" control the audio, ".csb" reference the audio used by a level, and files that end with ".adx" are the audio sources.

### Stages

Deleting the "st1.csb" will cause the stage to never load, but you can start from the boss just fine

Deleting the corrosponding adx files will still allow the level to load but the music/ sound effects in that file will not play.

Each stage has a three digit code followed by the # of the mare.

Ellie:
- Alp
- Gom
- Mag

Elliot
- Sea
- Snw
- Win

Final Level
- Mor

##### Playing with no Music

If you want to play any level with no music remove the corrosponding adx files.
You can also have specifc mares with no music by removing those adx files specifically.

### Menus

adx files that start with cdda control the menus music.

Deleting these will cause the menus to have no music

### Characters

Deleting a characters file like "nights.adx" does not seem to stop the corrosponding sound effects from playing.

# Playing ADX files/ Music

I have successfully been able to play all the adx files using an ADX player made for SA DX. 

![ADX Player](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Music/Pictures/ADX_Player.PNG)

# Massive Thing to Look Into Later 

".sfd" files reference using a "SofdecStream" to play audio. 

Referenced here: https://github.com/Hengle/VGMToolbox-1/blob/master/format/VGMToolbox/format/SofdecStream.cs
