# Docker MERN Starter Blog

This repo is forked from [Hashnode/mern-starter](https://github.com/Hashnode/mern-starter), it can build with docker in rancher.

![](http://i.giphy.com/3o6ozl0scfmBuRRP0c.gif)

# How To Build

**Add Service**

Add one service named db and select `mongo:3` image, then add another service named mern and select `tonypai/docker-mern` image.

**Port Map & Service Link**

Create a service link to db service, then add a port map like this...

![](http://i.imgur.com/pGJoOPP.png)

**ENV Setting**

Mern service needs to link mongodb or it will crash, so you can change the mongo url and web server port by setting environment variables.

```
MONGO_URL=mongodb://db:27017/mern
PORT=8000
```

And it's done!

**Stack Graph**

After you finish these steps, it should perfectly running on your server, and it's the stack graph.

![](http://i.imgur.com/rrVSVag.png)
