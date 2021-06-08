FROM golang
WORKDIR /src
COPY main.go .
RUN go build main.go

FROM scratch
COPY --from=0 /src/main .
CMD ["./main"]
