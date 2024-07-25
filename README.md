# Catalogs for NExScI
Catalogs are specified as lists of state vectors, usually grouped by target name.
The RUNID must be included on each line.

Current contents:
1. 2021_wfc3_catalog_nexsci.sv.txt : HST/WFC3 spectra for 61 planets (from Roudier+ 2021)
2. 2024_spitzer_phasecurve_catalog_nexsci.sv.txt : Spitzer phase curves for 34 planets (from Swain+ 2024, Table 1)

## Catalogs to mausoleum
1. All files ending in nexsci.sv.txt will be concatenated into one file when building the mausoleum
2. Release/Tag the place you want to turn into a mausoleum
3. Go to any of the mentor machines (NOT mentor3)
   1. cd to your esp repository
   2. run script: `.ci/inter.sh /proj/sdp/data/niessner/mausoleam/2.X.X`
   3. distribute `proj/sdp/data/niessner/mausoleam/2.X.X/tag.tgz` a gzipped tarfile

Let us look at the command in (3.ii). `.ci/inter.sh` takes a single argument that is the path of where to put the mausoleum when done and is represented as `/some/path/tag` in the instructions. The mausoleum is likely to need a lot of storage space. Therefore a good concreete example would be `/proj/sdp/data/${USER}` for a start. However, that directory may already contain stuff so you may want to collect the mausoleums in a subdirectory. For simplicity we will call it `mausoleum`. That would update the path to be `/proj/sdp/data/${USER}/mausoleum`. For the complete path, we still need to include the tag portion. The tag portion is the same as the one defined in (2). The first release/tag we have is 2.0.0 as it can be seen [here](https://github.com/gbryden/catalogs_for_nexsci/releases). The complete path would then be `/proj/sdp/data/${USER}/mausoleum/2.0.0`. What would then be distributed is `/proj/sdp/data/${USER}/mausoleum/2.0.0.tgz`
