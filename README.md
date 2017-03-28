# m2i
It is a Dockerfile for hosting [markdown2impress](https://github.com/yoshiki/markdown2impress) with docker.

## Getting Started
* git clone https://github.com/kakakikikeke/m2i.git
* cd m2i
* export MD_FILE=example.md
* docker build -t m2i .
* docker run -d -p 80:80 --name m2i-c m2i

Access http://localhost/ and be shown the presentation.

## Change other presentation
* docker cp example.md m2i-c:/root
* docker exec m2i-c ./markdown2impress.pl /root/example2.md
* docker exec m2i-c cp index.html /var/www/html/

## Link
* Pushed [Dockerhub](https://hub.docker.com/r/kakakikikeke/m2i/)