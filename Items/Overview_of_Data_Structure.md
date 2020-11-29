# Items

Items appear to be stored in "stage_" + # + "SDF.BIN" files in the afs folder.
They appear in a list usually below the stage info at the top of the page as shown below.
There is also a corrosponding enemy normal list that follows after the item list. That will be discussed after the item list.

![Item List](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Items/pictures/itemListExample.PNG)


## Data Structure

I have identified and been able translate the following parts of the structure as follows.
![Item Example](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Items/pictures/itemExample_LI.jpg)

##### Yellow: Previous Item Counter
##### Red: Current Item Counter
##### Black: Item Catagory?
##### Brown: Item Name
##### Green: Item Declaration
##### Purple: Item ID

### Previous Item Counter

This spot denotes the count of the prevous number. 
It increments based on base ten, but whenever a new zero is introduced into the ending it will not include the zero before including it.

Example:

1 

10

100

101

102

...

109

11

110

111

### Current Item Counter

This spot is used to show the current count of the item.


### Item Catagory?

This bit appears to be consistent across all instances of an item, and quite a few items share their number. I have compiled a list of most of the items below:

#### Catagories

03 </br>
- owl

04 </br>
- gate </br>
- wind </br>
- dash </br>

05 </br>
- tree1 </br>
- windv </br>
- npian </br>
- cpian </br>
- sheep </br>
- signb </br>
- hunch </br>

06 </br>
- single </br>
- tree1v </br>
- regate </br>
- sonata </br>
- npiand </br>
- kpian </br>
- dummy </br>

07 </br>
- mandara </br>
- dummy45 </br>
- bigitem </br>

08 </br>
- pao_kira </br>
- gasagasa </br>

0A </br>
- background </br>
- anal </br>

0C </br>
- windv_delete </br>

### Item Name

Each item instance must have a name, but the name can be changed to anything that fits the space. The game is unaffected even when the name is changed.

### Item Declaration
This appears to be a declaration that this is an item. All items have the 04 00 00 00 byte then the word "item" in this position.

### Item ID
The last bit most likely is used to denote an id number of the item. It appears to be increasing by hex instead of the character. You will notice the pattern goes:
- 01 .
- 0A .
- 64 d
- 56 e
- 57 f
- 58 g

...
- 6d m
- 0B .
- 6e n

...
- 77 w
- 0C .
- 78 x

...
- 7A z
- 7B {
- 7C |

You will notice that every now and then the pattern breaks and increments by 0A -> 0B -> ect. I don't know why it does this.

# Enemy Normal

There is a list of enemies after the item list.

![Item List](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Items/pictures/itemEnemyNormal.PNG)
