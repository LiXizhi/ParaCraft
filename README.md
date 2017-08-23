# ParacraftBuildinMod
for making paracraft buildin mod package

## How to Use

### Method1: Use As a Package Zip File
run 
```
./build.bat
```
The final package file is generated at `./ParacraftBuildinMod.zip`.
Put above file in paracraft redist's `npl_package/ParacraftBuildinMod.zip` and restart paracraft to take effect.

### Method2: Use As It is
git clone this project to `npl_package/ParacraftBuildinMod` and then
run `npl_package/ParacraftBuildinMod/build.bat`

Restart paracraft for the latest version of buildin-mod to take effect. 

## Internals
- git pull all packages from git 
- copy and merge all files to `Mod, script, textures` folder
- zip folders as `./ParacraftBuildinMod.zip`

