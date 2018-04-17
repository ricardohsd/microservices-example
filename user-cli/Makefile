build:
	CGO_ENABLED=0 GOOS=linux go build -o user-cli -a -installsuffix cgo cli.go
	docker build -t user-cli .

run:
	docker run -e MICRO_REGISTRY=mdns user-cli