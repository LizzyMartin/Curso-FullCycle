# Desafio Go

O objetivo desse exercício era subir um container no Docker Hub que ao ser executado exibisse "Code Education Rocks!". O código para exibir isso deveria ser feito em Golang e a imagem deveria ter menos de 2MB.

Criando nossa imagem:

```Docker
docker build -t relizabe/codeeducation .
```
- Para a imagem ficar pequena foi utilizado o conceito de [multi-stage builds](https://docs.docker.com/develop/develop-images/multistage-build/)

Colocando a imagem no Docker Hub:

```Docker
docker push relizabe/codeeducation
```

Executando o container:

```Docker
docker run relizabe/codeeducation
```

## Referência

https://www.ardanlabs.com/blog/2020/02/docker-images-part1-reducing-image-size.html
