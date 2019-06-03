# nanojoin-generator

## compiling

The build directory contains a makefile. Simply executing the make command should create a nanojoin.out executable.

## running

The syntax of the nanojoin command is the following

```
./nanojoin.out [-e] [-r <r>] -pent <p> -hex <h> -hept <s> 
```

followed by a list of halftube parameters separated by a space. The variables p, h and s are resp. upper limits on the number of pentagons, hexagons and heptagons the join can have. To generate all nanojoins for 3 halftubes with parameters (6, 0), (5, 1) and (4, 2) with a maximum number of 1 pentagons, 6 hexagons and 7 heptagons, the command

```
./nanojoin.out -pent 1 -hex 6 -hept 7 6 0 5 1 4 2
```
should be executed.

When the -e option is present, the generator will only output the nanojoins that have exactly p pentagons, h heptagons and s heptagons. 
Nanojoins with fewer faces will however also be constructed in the algorithm, just not written out. There is also an option -r that 
adds additional rings to the halftubes of the nanojoin. When the option -r 2 is given to the program, it will add 2 rings of hexagons 
to all halftubes of all generated nanojoin before outputting it. Both those options are also available in the CaGe GUI.
