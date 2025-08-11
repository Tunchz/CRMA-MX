// to run project

// 1: generate all needed files and start current project
go generate ./...
go run *.go

// 2: build go project
go generate ./...
CGO_ENABLED=0 go build

