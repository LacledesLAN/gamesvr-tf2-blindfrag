# LL Team Fortress 2 Blind Frag Dedicated Server in Docker

Docker image for LL [Team Fortress 2](http://store.steampowered.com/app/440/) "Bind Frag" servers.

* Uses the sourcemod plugin [TF2 Class Restrictions](https://forums.alliedmods.net/showthread.php?p=642353?p=642353) to limit all players to 'heavy'.

## Linux Container

[![](https://images.microbadger.com/badges/version/lacledeslan/gamesvr-tf2-blindfrag.svg)](https://microbadger.com/images/lacledeslan/gamesvr-tf2-blindfrag "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/lacledeslan/gamesvr-tf2-blindfrag.svg)](https://microbadger.com/images/lacledeslan/gamesvr-tf2-blindfrag "Get your own image badge on microbadger.com")

### Download

```shell
docker pull lacledeslan/gamesvr-tf2-blindfrag;
```

### Run self tests

```shell
docker run -it --rm lacledeslan/gamesvr-tf2-blindfrag ./ll-tests/gamesvr-tf2-blindfrag.sh;
```

### Run simple interactive server

```shell
docker run -it --net=host lacledeslan/gamesvr-tf2-blindfrag ./srcds_run -game tf -usercon +map koth_harvest_final +maplist mapcycle_quickplay_koth +rcon_password \"test123\"
```
