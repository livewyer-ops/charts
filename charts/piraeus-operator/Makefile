APP_VERSION := $(shell yq e '.appVersion' ./Chart.yaml)

.PHONY: update

update:
	git clone --branch $(APP_VERSION) https://github.com/piraeusdatastore/piraeus-operator.git .upstream
	rsync -avz --delete-after --exclude "Makefile" .upstream/charts/piraeus/ ./
	rm -rf .upstream
