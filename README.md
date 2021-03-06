# JupyterHub Single Node Deployment #

Provide a very easy way to setup (and maintain) a JupyterHub that exists on only one node. 

## Why? ##

A single node running JupyterHub is a very valuable tool that supports a lot of use cases:

1. Run a workshop for two days on a AWS machine with some shared data.
2. Have a place for your 20 students class to play with Notebooks
3. Do data analysis for your small 5 person startup
4. Ration access from researches to a massive compute node with 3TB of RAM
5. And plenty more!

Running JupyterHub on one node is far simpler than running it as a distributed system across a large, elastic number of nodes. This repository aims to make it super simple - *under 20 mins* - to setup a fully functional JupyterHub system configured to your liking.

## What? ##

This deployment supports the following features in a very composable, pick what you want way:

1. A supported version of JupyterHub
2. The nginx based proxy (rather than the nodejs based one)
3. Systemd Spawner for spawning notebooks with equitable resource sharing (CPU / Memory / IO) between users
4. Choice of authenticators:
   1. GitHub
   2. Google / Google Apps
   3. PAM
   4. Google Sheets
5. Automatic SSL with Let's Encrypt

Note that most of these features aren't implemented yet. We will be making tagged releases of this repository over time, and migration paths will always be available.

## How? ##

Right now, you can check it out by doing the following:

1. Create a new VM running Ubuntu 16.04
2. Clone this repository to the VM
3. Run `sudo ./apply.bash`

This will setup a basic jupyterhub. We will eventually add configuration with hiera.
