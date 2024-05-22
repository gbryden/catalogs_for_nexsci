# Catalogs for NExScI
Catalogs are specified as lists of state vectors, usually grouped by target name.
The RUNID must be included on each line.

Current contents:
1. Catalogs to mausoleum

## Catalogs to mausoleum
1. All files ending in nexsci.sv.txt will be concatenated into one file when building the mausoleum
2. Release/Tag the place you want to turn into a mausoleum
3. Go to any of the mentor machines
   1. cd to your esp repository
   2. run script: `.ci/inter.sh /some/path/tag`
  
Let us look at the last command. `.ci/inter.sh` taks a single argument and that is the path of where to put the mausoleum when done represented as `/some/path/tag` in the instructions. The mausoleum is likely to take up a lot of space. Therefore a good concreete example would be `/proj/sdp/data/${USER}` for a start. However, that directory may already contain loads of stuff so you may want to collect the mausoleums in a subdirectory. For simplicity we will call it `mausoleum`. That would update the path to `/proj/sdp/data/${USER}/mausoleum`. For the complete path still need to include the tag portion. The tag portion is the same as the one defined in (2). The first release/tag we have is 2.0.0 as it can be seen [here](https://github.com/gbryden/catalogs_for_nexsci/releases). The complete path would then be `/proj/sdp/data/${USER}/mausoleum/2.0.0`. What would then be distributed is `/proj/sdp/data/${USER}/mausoleum/2.0.0.tga`
