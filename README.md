# Word-Search

Hello, I am currently working on a project and I am having trouble with the attached code.  I am having trouble understanding why my checkRightUp, checkLeftUp, checkRightDown, and checkLeftDown functions are not working.  I have attached the three different txt files that my program is searching as well as the command line arguements.  My main issue is that when all of the functions listed above are implemented, the 2020matrix file says there is a segmentation fault but if I remove all 4 of the functions it works fine.  On the 1520 matrix for some reason one of the times the word "is" is printed three spaces too far to the left and one space too far up which I do not understand why this is happening because when the word "hard" is printed in the same direction, it is printed in the right place.  The 0505 matrix works completely fine so I think the issues are with all the functions besides checkRightUp.

Here are the command line arguements which correspond to the names of the txt files:

./a.out tcnj go < 0505matrix
./a.out this project is hard < 1520matrix
./a.out you enjoy this project < 2020matrix
