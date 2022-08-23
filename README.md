# network-programming
Course network programming by FICT ITMO

Command for local deploy in docker container
```
git clone https://github.com/itmo-ict-faculty/network-programming
cd network-programming
docker pull squidfunk/mkdocs-material
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```