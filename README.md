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

> Note: the world must have a default home point set. 
