#docker run -it --mount type=bind,source="$(pwd)"/desafio/go,target=/go --rm --name go golang
#docker build -t paulomulotto/hello .
# Criação do executável golang
FROM golang:1.17-alpine AS builder

WORKDIR /app

COPY go.mod ./

COPY hello.go .

RUN go build -o hello

ENTRYPOINT [ "./hello" ]


# Criando a imagem apenas com o executável
FROM scratch

COPY --from=builder /app/hello hello

CMD [ "./hello" ]