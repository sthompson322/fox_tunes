# FOX TUNES
------------
**Goal:**
Help the Fox complete his playlist by traversing the city to find and collect CDs. In order to complete the playlist and win, the Fox must collect all 3 CDs from each of the 3 levels. The Fox has 3 lives within each level, which can be lost either by falling off a platform into the abyss or by touching fire. 

--------------
Fox's movement:

- **LEFT** BUTTON: moves Fox left
- **RIGHT** BUTTON: moves Fox right
- **UP** BUTTON: makes Fox jump up and to the left or up and to the right, depending on whether Fox is currently facing left or right.

- When Fox falls, he falls diagonally in the direction he is facing. This allows the player to "jump down" to lower platforms by walking off the edge of a platform.

---------------------------------------------------
Here is how to navigate my state machine:

**START STATE**: 
- press START button to go to MAP STATE
- press SELECT button to go to INSTRUCTIONS STATE

**INSTRUCTIONS STATE**: 
- press START button to go to MAP STATE
- press B button to go back to START STATE

**MAP STATE**: 
- if player has not beaten Level 1, pressing START BUTTON will lead to GAME1 STATE
- if player has beaten Level 1, but not Level 2, pressing START BUTTON will lead to GAME2 STATE
- if player has beaten Level 1 & 2, but not Level 3, pressing START BUTTON will lead to GAME3 STATE

**GAME1 STATE**: 
- press SELECT button to go to PAUSE STATE
- Beating level 1 by finding and collecting all 3 CDs takes you to the MAP STATE which is now set to go to level 2 upon pressing START button
- Losing all 3 lives takes you to the LOSE STATE

**GAME2 STATE**: 
- press SELECT button to go to PAUSE STATE
- Beating level 2 by finding and collecting all 3 CDs takes you to the MAP STATE which is now set to go to level 3 upon pressing START button
- Losing all 3 lives takes you to the LOSE STATE

**GAME3 STATE**: 
- press SELECT button to go to PAUSE STATE
- Beating level 3 by finding and collecting all 3 CDs takes you to the WIN STATE
- Losing all 3 lives takes you to the LOSE STATE

**PAUSE STATE**: 
- press SELECT button to go to START STATE (reseting the whole game)
- if the player paused the game while playing Level 1, pressing the START button will take them back to GAME1 STATE
- if the player paused the game while playing Level 2, pressing the START button will take them back to GAME2 STATE
- if the player paused the game while playing Level 3, pressing the START button will take them back to GAME3 STATE

**WIN STATE**: 
- press START button to go to START STATE

**LOSE STATE**: 
- press START button to go to START STATE

-------------------
**Cheat**: Press **BUTTON A** to automatically move to the next-highest static platform.

