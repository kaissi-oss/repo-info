## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:5519d35a2fbe24e710565f2157878fbde047e240401eac59d3fd3febab5a9be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.1944; amd64

### `nats-streaming:latest` - linux; amd64

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

### `nats-streaming:latest` - linux; arm variant v7

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

### `nats-streaming:latest` - linux; arm64 variant v8

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

### `nats-streaming:latest` - windows version 10.0.14393.1944; amd64

```console
$ docker pull nats-streaming@sha256:abc76051637063548d4bf5c8be4a2e892f33c98252f046d2fa61ce73e0074df4
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.2 MB (402170705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5148af5deaa4178cc4b6362a73fe55525aa9671d0748b8ae6c1afb30592885b`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Mon, 11 Dec 2017 21:42:41 GMT
RUN Install update 10.0.14393.1944
# Tue, 12 Dec 2017 23:29:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Dec 2017 23:29:57 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Tue, 19 Dec 2017 23:20:05 GMT
RUN cmd /S /C #(nop) COPY file:7cb5604408645c8d53c674cce139187ac02319c1f621bdbdf9aa64bce09f7c43 in nats-streaming-server.exe 
# Tue, 19 Dec 2017 23:20:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 8222/tcp
# Tue, 19 Dec 2017 23:20:07 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Last Modified: Tue, 13 Dec 2016 10:47:17 GMT  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4806a44e00a0febaf206c2414777a070782c559757658199cf5e0d8f0ead2bba`  
		Last Modified: Mon, 11 Dec 2017 21:42:41 GMT  
		Size: 146.0 MB (146023673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2735b5da9778b2ec6c898da8d2a6d18ea0847d7829b0dfeb84c4984ff081b6b2`  
		Last Modified: Tue, 12 Dec 2017 23:30:21 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffdeb52d1d9a81b52afe50aed5444de9bbe059e24e2fd279c8e8709a61609cb`  
		Last Modified: Tue, 12 Dec 2017 23:30:20 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64a258b789d666ed3af6a4a7e9ea6b02c98c3349921f5dfb6b1dd6e8a8624bc`  
		Last Modified: Tue, 19 Dec 2017 23:20:25 GMT  
		Size: 3.5 MB (3452086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d02d67a3a5f495cdec69fb1ed9f47e76f8de1a352b868c3e28ccaa6073874a`  
		Last Modified: Tue, 19 Dec 2017 23:20:23 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebf44c4ea453a9042e7caccb8a2c3fe2847441ceb5f1279b5a97833e9fa610c`  
		Last Modified: Tue, 19 Dec 2017 23:20:23 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
