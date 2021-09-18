# PoaCuda
POA Miner for Nvidia GPU's

Readme PoaCuda Version 2021-09-15 Beta.

This programs tries to mine PRCYcoin POA blocks using NVidia Cuda enabled graphic cards.
The program requires minimum the latest (1.0.0.8) version of the PRCY wallet to poll for the last POA Block.
The program waits default for 50 blocks after the last POA block before it starts to mine.
POA blocks will only be generated once per hour, so it would be a waste of energy to try to mine a block,
which we allready know will not be a POA block.

The miner mines one out of 24 POA blocks to my mining wallet as a reward for the effort I've put in to
programming this software. If you're not ok with that, then don't use the software.

Quick howto mine:

run the Miner with the benchmark option:

PoaCuda -o http://127.0.0.1:59683 --benchmark

The program will begin to search for your optimum Cuda configuration, and will tell you this after a couple of minutes
Look for the line with GPU #0 using launch configuration the last part for example T8x11 is the optimum Cuda configurationfor your graphics card.
Use that configuration in the command line to start the program, otherwise it will auto search for that configuration every time you start the program

So for example this would be my commandline with Cuda configuration parameters:

PoaCuda -o http://127.0.0.1:59683 -O rpcuser:rpcpassword -t 1 -l T15x15

NEW: Added the S parameter which defines how many blocks the miner should wait after the last poablock.
In above example it will wait 50 blocks before mining commences after the last poa block.

NEW: if the wallet isn't the latest version, or you are mining on DAPS, it will turn into DAPS mode.
Which will try to find a block continuously while getpoalastblockheight is not available through RPC.

All dll files in this zip file should be in the same directory as the PoaCuda.exe program.

Happy mining,
Rooie1971
 
