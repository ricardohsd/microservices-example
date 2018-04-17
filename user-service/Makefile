build:
		protoc -I. --go_out=plugins=micro:$(GOPATH)/src/github.com/ricardohsd/microservices-example/user-service \
				  proto/user/user.proto
		docker build -t user-service .

run:
		docker run -p 50052:50051 -e MICRO_SERVER_ADDRESS=:50051 -e MICRO_REGISTRY=mdns user-service
