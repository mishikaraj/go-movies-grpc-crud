# go-movies-grpc-crud

go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
$go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
$go mod init moviesapp.com/grpc
$export PATH="$PATH:$(go env GOPATH)/bin"
$protoc --go_out=. --go_opt=paths=source_relative \
    --go-grpc_out=. --go-grpc_opt=paths=source_relative \
    protos/moviesapp.proto
$go mod tidy
$go run server/main.go
#go run client/main.go
