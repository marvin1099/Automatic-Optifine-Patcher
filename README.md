# Automatic-Optifine-Patcher

## Info
Patches optifine to work as jar mod file,  
it can then be used with something like PrismLauncher,  
it also works for any optifine version from optifine.net fully automatic,  
with the official minecraft client downloaded from minecraft.net,  
so you can add it to your forge / fabric mod folder right away.

## Important
Keep in mind if you are on minecraft version 1.16.5 or above i strongly recomend using sodium,  
as it gives way better performace and is more compatible with other mods and newer versions.

## Requirements
To use download python from [here](https://www.python.org/downloads/).  
Or use your package manager (recommend).  
The package manager on windows, for example is winget.  
To use the package manager open your store.  
Or use the cmd / terminal and type somthing like:
```
winget search python3
```
python3 should be replaced with a winget result and so run:
```
winget install python3
```
Keep in mind the command is different on linux.

Download java as it is needed for the patching itself.  
For that i highly recomend using your package manager.  
As it will setup java to be accessible globaly.  
If you install java manually like from [here](https://www.openlogic.com/openjdk-downloads).  
Then you will have to add it to your path enviroment var manually.  
To do that check out [add java to enviroment variable under windows](https://confluence.atlassian.com/doc/setting-the-java_home-variable-in-windows-8895.html).  
If you on linux you problay used the package manager anyway.

## Download
Then download the patcher file from [here](https://codeberg.org/marvin1099/Automatic-Optifine-Patcher/src/branch/main/optifine_patcher.py),  
then click on the download button somewhere at the top right  
and place the python file in a empty folder.

## Use It
Finaly open the cmd / terminal and type:
```
cd "PATH/TO/PYTHON/FILE"
./optifine-patcher.py -l 1.9
```
The `PATH/TO/PYTHON/FILE` will need to be replaced,  
with the folder path of the `optifine_patcher.py`.

This will show all versions avalible for `1.9.x`.  
Then use one version from the results (for example `1.9.4`).  
And type in the cmd / terminal:
```
./optifine-patcher.py -d 1.9.4
```

Now if this has worked the patched optifine file will be at:  
`PATH/TO/PYTHON/FILE/$VERSION`.  
and it will be named optifine-$VERSION-MOD.jar.   
$VERSION will be replaced by the version you have downloaded.

# Custom Java Path
If you dont want to add java as enviroment variable you can also use:
```
./optifine-patcher.py -j "/PATH/TO/JAVA" -d 1.9.4
```  
where `/PATH/TO/JAVA` will need to be replaced by the java bin/exe path.