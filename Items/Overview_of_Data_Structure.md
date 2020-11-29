# Items

Items appear to be stored in "stage_" + # + "SDF.BIN" files in the afs folder.
They appear in a list usually below the stage info at the top of the page as shown below.
Their is also a corrosponding enemy normal list that follows after the item list. That will be discussed after the item list.

![Item List](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Items/pictures/itemListExample.PNG)


#### Data Structure

I have identified and been able translate the structure as follows using the below image.
![Item Example](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Items/pictures/exampleItemDecomposed.PNG)

##### Yellow: Header
##### Red: Incremental Bit
##### Blue: Counter
##### Black: Next Item Counter
##### Lime: Item Catagory?
##### Fuscia: Item Name

## Header

All items must start with the byte "04 00 00 00" before the word "item" to denote it is an item.

## Incremental Bit

While I can't tell what this does exactly, it appears to be a counter. It appears to be increasing by hex instead of the character you will notice the pattern starts as:
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

## Item Catagory

This bit appears to be consistent across all instances of an item and quite a few items share the number. I have compiled a list of most of the items below:

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


# Enemy Normal

![Item List](https://raw.githubusercontent.com/SmallMistake/Modding-NiD/main/Items/pictures/itemEnemyNormal.PNG)
