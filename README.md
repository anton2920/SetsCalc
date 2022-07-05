# SetsCalc — A free powerful sets calculator 

## Brief usage description
### For sets input: 
#### There are several ways to fill up the gaps:
	• {ai, ai+1, ..., an}
	• INT_ALL (to fill up with all integers)
	• INT(A, B) (to fill up with integers from A to B)
	• FILE("<path_to_file>") (to fill up with necessary set from file)
	• RAND(N, A, B) (to fill up with N random elements from A to B)

### For expression input:
	• Use only «A», «B», «C» and «-», «+», «*», «\», «v» or «V», «^»

### Notes:
	• The program will go on forever 'till you press «No» in continue menu
	• Contact anton2920@gmail.com if any issue occurs
	• Enjoy! :)

## Installation guide
To install this program you need `libm.so`, `libncurses.so` and `libdialog.so` dynamic libraries.
Then perform: 
```bash
sh ./autogen.sh
./configure
make
sudo make install
```

## Licence
It distributes only under GPLv2 licence. Go to https://www.gnu.org/licenses/ for more information

## Copyright 
© Anton, 2018-2022
