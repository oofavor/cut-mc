# Idea
The project tries to cut cost of renting minecraft server by deleting VPS on which minecraft server is running and saving the current state of the world by copy-pasting it on the cut-mc server.

# How
Minecraft server will be started with the docker image that will both our minecraft server, a mini server that will expose minecraft server's console, and a script that will save a state of the world by copy-pasting it on the cut-mc server.

The example of how server will be bootstraped:

1. cut-mc recieves request to bootstrap a server (with modpack and version optionally)
2. cut-mc creates a VPS and sends Docker image to it (should we handle empty world folder?)