# Paracraft Server App
This is a pure paracraft server. 

## Install Guide
Install [NPLRuntime](https://github.com/LiXizhi/NPLRuntime) first and then clone this respository and run `./start.sh`

```
git clone --recursive https://github.com/LiXizhi/paracraft.git
cd paracraft
./start.sh
```

package dependencies: (already included in git submodules)
- main
- paracraft

## Start Pure Server
Starting a pure server with the default port with `./start.sh`. It is recommended that you launch the server app in your docker container.
One can also start pure server with any world like `worlds/DesignHouse/test` and ip/port. See below.

```
npl world="worlds/DesignHouse/test" ip="0.0.0.0" port="6001" loadpackage="npl_packages/paracraft/"
```

One can also run from any folder like `/opt/server_001/` with the `dev` param. Please note the world directory must always be relative to dev folder or current working directory. 

```
npl world="worlds/DesignHouse/test" port="6001" loadpackage="npl_packages/paracraft/" dev="/opt/server_001/"
```

## Command Line Parameters
- `world`: the world directory that this server serves.  ==Note: the world must have a default home point set.==
- `ip`: default to "0.0.0.0", which is all ip addresses. If you are inside a docker, "127.0.0.1" is a better choice.
- `port`: default to 6001
- `autosave`:  How many minutes to automatically save the world. If not specified, the world is never saved, and your changes may be lost.
- `servermode`: default to true. 
- `loadpackage`: this should always be "npl_packages/paracraft/". Make sure you have latest version checked out from our git, in addition to "npl_packages/main/"
- `dev`: the development directory. The logics is intrinsic to NPLRuntime. The world directory is searched in dev folder first and then in current working directory. 

Here is an example with all parameters:
```
npl servermode="true" autosave="10" world="worlds/DesignHouse/test" port="6001" loadpackage="npl_packages/paracraft/" dev="/opt/server_001/"
```
