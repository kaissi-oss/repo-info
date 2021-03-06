## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:fce830894c1b3f54f6ecf091dbcdba158424ed6a155b4d90993ba0876d540847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:05ded20d349a0b42e121c31fb15a7826b41678cd72475ee8d7ef30e90dcdc282
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3408359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8eafe26d51758993e4a64dc14e04b8682ad1a92824fb20b4dcbca70cecf9d0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 19 Dec 2017 18:59:56 GMT
COPY file:0eb5f0998e5218da31d53f7e49b5b4aae6e2b715282ddb388dc5236127def4df in /nats-streaming-server 
# Tue, 19 Dec 2017 18:59:56 GMT
EXPOSE 4222/tcp 8222/tcp
# Tue, 19 Dec 2017 18:59:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 19 Dec 2017 18:59:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:fc1eced9799119b6b7e9e9c0cb15273eb1d5cec6f9f4ba8599a8886b7ba979e9`  
		Last Modified: Tue, 19 Dec 2017 19:00:10 GMT  
		Size: 3.4 MB (3408359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:57c3aa6818243a81fe585bb58ad054a5588b1fa9b708a48013df7c515b1249c7
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3186691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7151602c5f8cb4b1d1e7abdae578c52b8ee4a25fa8e883535e1e258f11b45b7`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 20 Dec 2017 00:27:24 GMT
COPY file:c3ac650d6c5b53052faa9d9aeec05315822a8e432bc2555e2b88a3075fcb58cb in /nats-streaming-server 
# Wed, 20 Dec 2017 00:27:25 GMT
EXPOSE 4222/tcp 8222/tcp
# Wed, 20 Dec 2017 00:27:25 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 20 Dec 2017 00:27:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:59a7098e2e4f6e1dee1b73ad44d54b5c378ad5c53fa9f6fe6d9cd25880173665`  
		Last Modified: Wed, 20 Dec 2017 00:27:35 GMT  
		Size: 3.2 MB (3186691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:adfd8d361e9e012fcc6e8f27a15551461f1eea611cf5f0d9ca29846284f45666
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3106974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64efc89b1ad1d9f833ef04a4aaab8a54f776b0d8148deb4d9954ca41480025b`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 20 Dec 2017 01:27:31 GMT
COPY file:dad2b1cae21d39f28b583601a7e37358571746398cc01bb64d04e0b97df1fdb4 in /nats-streaming-server 
# Wed, 20 Dec 2017 01:27:31 GMT
EXPOSE 4222/tcp 8222/tcp
# Wed, 20 Dec 2017 01:27:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 20 Dec 2017 01:27:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2d99707846ff6807246e5a6f54ae8d815580f96497913f49617d1501293bd885`  
		Last Modified: Wed, 20 Dec 2017 01:27:46 GMT  
		Size: 3.1 MB (3106974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
