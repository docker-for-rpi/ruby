REPO ?= forrpi/ruby
TAG  ?= 2.5.1-alpine3.7

all: build push

build: Dockerfile
		docker build --rm  -t $(REPO):$(TAG) .
		docker tag $(REPO):$(TAG) $(REPO):latest

push:
		docker push $(REPO):$(TAG)
		docker push $(REPO):latest
