---
layout: post
title:  "A dip into Godot Networking"
date:   2025-07-22 08:51:00 -0000
categories: Godot
tags: [Godot, networking, simple]
---

# I had a simple idea

### Or not

So I was ( probably a few years ago now ) trying to make a simple example in godot. I wanted to make it so that if you were trying to make a multiplayer game, each player didn't have to be looking at the same scene but the server could still keep track of them.

At first I thought that, that might be pretty difficult and initially, because I had no idea what I was doing it was.

### a bit of background

lets start by understanding the basics of how [high level multiplayer](https://docs.godotengine.org/en/stable/tutorials/networking/high_level_multiplayer.html) in godot works. As far as this post is concerned we will just create a server and a client in the most bog standard way

```gd
# Server setup
var peer = ENetMultiplayerPeer.new()
peer.create_server(8910, 4)
multiplayer.multiplayer_peer = peer

# Client setup
var peer = ENetMultiplayerPeer.new()
peer.create_client("localhost", 8910)
multiplayer.multiplayer_peer = peer
```
