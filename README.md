# Laclede's LAN Team Fortress 2 Blind Frag Dedicated Server

![Laclede's LAN Team Fortress 2 Blind Frag Dedicated
Server](https://raw.githubusercontent.com/LacledesLAN/gamesvr-tf2-blindfrag/master/.misc/banner-tf2-blindfrag.png
"Laclede's LAN Team Fortress 2 Blind Frag Dedicated Server")

This repository is maintained by [Laclede's LAN](https://lacledeslan.com). Its contents are heavily tailored and tweaked
for use at our charity LAN-Parties. For third-parties we recommend using this repo only as a reference example and then
building your own using [gamesvr-tf2](https://github.com/LacledesLAN/gamesvr-tf2) as the base image for your customized
server.

Docker image for LL [Team Fortress 2](http://store.steampowered.com/app/440/) "Bind Frag" servers.

* Uses the sourcemod plugin [TF2 Class Restrictions](https://forums.alliedmods.net/showthread.php?p=642353?p=642353) to
limit all players to 'heavy'.

## Linux

### Download

```shell
docker pull lacledeslan/gamesvr-tf2-blindfrag;
```

### Run Self Tests

The image includes a test script that can be used to verify its contents. No changes or pull-requests will be accepted
to this repository if any tests fail.

```shell
docker run -it --rm lacledeslan/gamesvr-tf2-blindfrag ./ll-tests/gamesvr-tf2-blindfrag.sh;
```

### Run simple interactive server

```shell
docker run -it --net=host lacledeslan/gamesvr-tf2-blindfrag ./srcds_run -game tf -usercon +map koth_harvest_final +maplist mapcycle_quickplay_koth +rcon_password \"test123\"
```

## Getting Started with Game Servers in Docker

[Docker](https://docs.docker.com/) is an open-source project that bundles applications into lightweight, portable, self-
sufficient containers. For a crash course on running Dockerized game servers check out [Using Docker for Game
Servers](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/DockerAndGameServers.md). For tips, tricks,
and recommended tools for working with Laclede's LAN Dockerized game server repos see the guide for [Working with our
Game Server Repos](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/WorkingWithOurRepos.md). You can
also browse all of our other Dockerized game servers: [Laclede's LAN Game Servers
Directory](https://github.com/LacledesLAN/README.1ST/tree/master/GameServers).
