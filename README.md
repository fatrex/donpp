# DoNPP

**Do**cker  
**N**ginx  
**P**ostgreSQL  
**P**HP

> A starter kit to try PHP packages, frameworks or cms in docker

## Why
As a full-stack JavaScript developer my development machine is not configured to run PHP. But I'm a curious dev so I wanted to explore some new framework/cms in the PHP world.
The quick thing to do was to setup a docker environment to try everything without installing all the packages needed by PHP.

## How to use
If you want to use `DoNPP` you can simply clone this repository in a folder of your choice, remove the `.git` and start everything.

If you have **Node.js** installed, you can clone the repo using:
```bash
npx degit https://github.com/dnlnrs/donpp <folder>
```

To start:
```bash
docker-compose up
```

Your PHP environment is ready to show everything you throw in the `app` folder.