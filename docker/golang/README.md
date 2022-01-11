# Resposta Desafio Go - Criar container com executável Go com menos de 2MB

# Baixe a imagem
```
docker pull paulomulotto/codeeducation
docker images | grep paulomulotto/codeeducation
```

Será retornado o tamanho da imagem baixada, com 1,77MB.

# Execute a imagem
```
docker run paulomulotto/codeeducation
```
A saída é "Code.education Rocks!", gerado por uma aplicação go, como solicitado.

# Opcional - Criar imagem através do Dockerfile
Na pasta docker/golang, execute
```
docker build -t <usuario>/codeeducation .
docker run --rm <usuario>/codeeducation
```
A saída é "Code.education Rocks!", gerado por uma aplicação go, como solicitado.