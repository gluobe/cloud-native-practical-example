# Single stage Docker build (root)

> NOTE: This is a demo repo, do not use any of this in production!

```
docker build --progress=plain -f Dockerfile.single.root -t exercise:single-root .
docker container run -d -p 8080:8080 exercise:single-root
docker container exec -ti $(docker container ls -qal) bash
# whoami
```

# Single stage Docker build (non root)

```
docker build --progress=plain -f Dockerfile.single -t exercise:single .
docker container run -d -p 8081:8080 exercise:single
docker container exec -ti $(docker container ls -qal) bash
$ whoami
```

# Multi-stage Docker build (non root)

```
docker build --progress=plain -f Dockerfile.multi -t exercise:multi .
docker container run -d -p 8082:8080 exercise:multi
```

# Size differences

```
docker image ls
```
