# Robo Rally

## Table of content

* [Overview](#Overview)
* [Usage](#Overview)
* [Git](#Git)

## Overview

Robo Rally is a complex old board game. This project aims to provide an digital version of it but with a automated Hardware visualisation. This game is the cross product of version 1 and 2 (only V2 is purchasable today), as we took the best parts of both versions.

>  You can play the game without buying hardware for free

The hardware only is kind of a plug-in for the game. The hardware's job is to 'display' the state of the game on a analog map with real robots. But the game client has a visualization regardless.

The hosting of the game can be done by the client itself or by a dedicated server so the game can be played in LAN or online.

### For developers

The main goal of this project is extendibility. Every aspect of the game should be as easy as possible to alter or extend.

## Usage

To play the game you need the client (the game itself). The newest version will always be available at [github](https://github.com/FactoryRally/game-client/releases). The games are hosted at a client or server. If you create a game you automatically host it. If you like to play on a dedicated server you can add the server to the list by its IP or domain name. And then you can play the game online. The exact rules are to be found at [game-controller/documentation/rules.md](https://github.com/FactoryRally/game-controller/blob/master/documentation/rules.md). 

# Git

> This section is only important if you are a **developer**

**Repositories**

* The [`game-controller`](https://github.com/FactoryRally/game-controller/) is responsible for the complete logic (rules) and the flow of the game. Also the Dedicated Server is located here. It is used as dependency in the `game-client` to host games. Also the server is responsible to connect to hardware if present.
* The [`hardware`](https://github.com/FactoryRally/hardware) repo contains everything that is needed to build your own robots and board which can connect to a server. Also the code for microcontrollers drivers for chips and scripts for the main unit are found here.
* The [`game-client`](https://github.com/FactoryRally/game-client/) repo contains the graphic game client. This is our implementation with **Unity**. But due to our architecture you can easily create you own client. Whether it be a text based console version or a A+++ graphic title. > This repo is ***only*** for graphical representation and player control. Not a bit of the game logic is here.