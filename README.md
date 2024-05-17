# Docker 
---

> Install docker hub from: [Docker](https://www.docker.com/products/docker-hub/)

> Install WSL from Microsoft Store

> Install Docker Extension for Visual Studio Code

Using Visual Studio Code:
* First Create a folder for your docker project or Select an existing one.
* Create a file named Dockerfile

  ![image](https://github.com/Yajmee/cloud-computing-reviewer/assets/99458710/87863d80-3fe6-46d2-9d0e-d413273777bd)

using terminal pull an image of ubuntu:

```bash
$> docker pull ubuntu
```

to run ubuntu type in command then hit enter:
```bash
$> docker run -it ubuntu
```

from docker file create a command for building a node js app:
```dockerfile
FROM node:20-alphine

WORKDIR /app

COPY ..

CMD node file_name.js
```

to build the app type the command and hit enter:
```bash
$> docker build -t imagename
```


to run it type the command and hit enter:
```bash
$> docker run imagename
```

alternatively you can run the command:
```bash
$> docker run it imagename sh
```

# React App
---

to install vite for react run the command:
```bash
$> npm create vite@latest foldername
```
> !You must have a node installed for npm to work!

create a dockerfile inside the folder of vite
from docker file create a command for the react file:
```dockerfile
FROM node:20-alphine

RUN addgroup app && adduser -S -G app app

USER app

WORKDIR /app

COPY package*.json ./

USER root
```
