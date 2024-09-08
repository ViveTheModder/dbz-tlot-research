# dbz-tlot-research
What I have gathered from analyzing The Legacy of Tenkaichi, another fanmade BT3 mod that takes after BT4.

# Trivia
* When selected, Dragon History crashes the game. That is because the ISO was not made with the story mode in mind.

Fortunately, I have provided a solution (``DBZP.bin``), which simply makes Dragon History redirect you back to the Main Menu.

* Much like BT4, the ISO's contents are inaccessible through normal means. 

Unlike BT4 however, they did not remove the header information from the AFS (effectively turning it into a VOL file, which BT1 uses). 
Instead, they went for an older solution of theirs, which is to zero out all file sizes and only keep the address of the first file.

That way, without source code modification, the game can automatically figure out what the addresses originally were.

* In addition, all costume files have a watermark added. As in, right after the index (first 1016 bytes), they replaced the padding (8 bytes) to say ``BY TLOT``.

# Provided CSV Files
* ``characters.csv`` -> Character List (includes inaccessible characters, which are all copies of Saibaman)
* ``maps.csv`` -> Map List (the map names have been roughly/literally translated on purpose)