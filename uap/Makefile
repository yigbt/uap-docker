docker-build-1.0.0:
	docker build \
		--network host \
		--tag yigbt/uap:1.0.0 \
		--file Dockerfile.uap.1.0.0 \
		. # Current folder is the Docker build context

docker-build-no-cache-1.0.0:
	docker build \
		--network host \
		--no-cache \
		--tag yigbt/uap:1.0.0 \
		--file Dockerfile.uap.1.0.0 \
		. # Current folder is the Docker build context

docker-run-1.0.0:
	@docker run \
		--interactive \
		--name uap \
		--network host \
		--rm \
		--tty \
		yigbt/uap:1.0.0 ${ARGS}

docker-build-1.0.0-ChIPseq:
	docker build \
		--network host \
		--tag yigbt/uap:1.0.0-ChIPseq \
		--file Dockerfile.uap.1.0.0-ChIPseq \
		. # Current folder is the Docker build context

docker-build-no-cache-1.0.0-ChIPseq:
	docker build \
		--network host \
		--no-cache \
		--tag yigbt/uap:1.0.0-ChIPseq \
		--file Dockerfile.uap.1.0.0-ChIPseq \
		. # Current folder is the Docker build context

docker-run-1.0.0-ChIPseq:
	@docker run \
		--interactive \
		--name uap-ChIPseq \
		--network host \
		--rm \
		--tty \
		yigbt/uap:1.0.0-ChIPseq ${ARGS}

docker-build-1.0.0-RNAseq:
	docker build \
		--network host \
		--tag yigbt/uap:1.0.0-RNAseq-data-download \
		--file Dockerfile.uap.1.0.0-RNAseq-data-download \
		. # Current folder is the Docker build context
	docker build \
		--network host \
		--no-cache \
		--tag yigbt/uap:1.0.0-RNAseq \
		--file Dockerfile.uap.1.0.0-RNAseq \
		. # Current folder is the Docker build context

docker-build-no-cache-1.0.0-RNAseq:
	docker build \
		--network host \
		--no-cache \
		--tag yigbt/uap:1.0.0-RNAseq \
		--file Dockerfile.uap.1.0.0-RNAseq \
		. # Current folder is the Docker build context

docker-run-1.0.0-RNAseq:
	@docker run \
		--interactive \
		--name uap-RNAseq \
		--network host \
		--rm \
		--tty \
		yigbt/uap:1.0.0-RNAseq ${ARGS}

# Push created DMS docker image to registry
docker-push:
	docker login
	docker push yigbt/uap:1.0.0

.PHONY: docker-build docker-build-no-cache docker-run docker-push
