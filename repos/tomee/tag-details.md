<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `tomee`

-	[`tomee:8-jre-1.7.5-jaxrs`](#tomee8-jre-175-jaxrs)
-	[`tomee:8-jre-1.7.5-plume`](#tomee8-jre-175-plume)
-	[`tomee:8-jre-1.7.5-plus`](#tomee8-jre-175-plus)
-	[`tomee:8-jre-1.7.5-webprofile`](#tomee8-jre-175-webprofile)
-	[`tomee:8-jre-7.0.0-plume`](#tomee8-jre-700-plume)
-	[`tomee:8-jre-7.0.0-plus`](#tomee8-jre-700-plus)
-	[`tomee:8-jre-7.0.0-webprofile`](#tomee8-jre-700-webprofile)
-	[`tomee:8-jre-7.0.1-plume`](#tomee8-jre-701-plume)
-	[`tomee:8-jre-7.0.1-plus`](#tomee8-jre-701-plus)
-	[`tomee:8-jre-7.0.1-webprofile`](#tomee8-jre-701-webprofile)
-	[`tomee:8-jre-7.0.2-plume`](#tomee8-jre-702-plume)
-	[`tomee:8-jre-7.0.2-plus`](#tomee8-jre-702-plus)
-	[`tomee:8-jre-7.0.2-webprofile`](#tomee8-jre-702-webprofile)
-	[`tomee:8-jre-7.0.3-plume`](#tomee8-jre-703-plume)
-	[`tomee:8-jre-7.0.3-plus`](#tomee8-jre-703-plus)
-	[`tomee:8-jre-7.0.3-webprofile`](#tomee8-jre-703-webprofile)
-	[`tomee:8-jre-7.0.4-plume`](#tomee8-jre-704-plume)
-	[`tomee:8-jre-7.0.4-plus`](#tomee8-jre-704-plus)
-	[`tomee:8-jre-7.0.4-webprofile`](#tomee8-jre-704-webprofile)
-	[`tomee:latest`](#tomeelatest)

## `tomee:8-jre-1.7.5-jaxrs`

```console
$ docker pull tomee@sha256:bc3d6afc42b7a35481acb0560d6f8950b089bf1e2e4c744eb870b4e5899b7f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:8-jre-1.7.5-jaxrs` - linux; amd64

```console
$ docker pull tomee@sha256:d922a73b9eb51b8b4999c3de97f8aa3c16208af64790a93f3061883b38817078
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261546511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76f6f1b25c571cf56e5310798fcc979e6ab95068950cb121f942fcc3cb0ff3f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:37:41 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 17:22:39 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-jaxrs-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-jaxrs-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:22:40 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:22:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66b65c13df185835f71eb63164136a5bd9736b8b894132429090f84a2fa9efc`  
		Last Modified: Wed, 13 Dec 2017 17:25:53 GMT  
		Size: 26.8 KB (26832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f57967c117b000e537e2a4f23760d996f254c2b3abd68d0f21609e1abb532ad`  
		Last Modified: Wed, 13 Dec 2017 17:25:54 GMT  
		Size: 34.4 MB (34436749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-jaxrs` - linux; arm variant v5

```console
$ docker pull tomee@sha256:f52a17ea8e3789b8dffc2f15b7f0f5c591ac50e1d4ab55dfb437c30bbc140f8b
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230335023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7cfe702b3c848c522f388ab679555b675720965f8f6b6cb2c6d2f3dad5524f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:45:55 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 20:17:42 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-jaxrs-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-jaxrs-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:17:42 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:17:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06353a9260dd6456f8a0541e8a55da39ec69ae4925e94f89e16664661ef5fc1`  
		Last Modified: Wed, 13 Dec 2017 20:22:08 GMT  
		Size: 26.9 KB (26888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89dfff8186052cb6e2dd8f62a0660c221493c5ef078fc8e67d212830f358543`  
		Last Modified: Wed, 13 Dec 2017 20:22:13 GMT  
		Size: 34.4 MB (34437006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-jaxrs` - linux; arm variant v7

```console
$ docker pull tomee@sha256:d6e21eac86f0a8b2ba4a92944bad2171ac8eeb41c6da25c7b05e0ed9a5d2d9f3
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240841771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa834d458f413c94c3526327f209665ba1c8a9eba0a34233b8e487b5b870a1c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:02:02 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:02:35 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 10:10:48 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-jaxrs-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-jaxrs-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:10:48 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:10:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd18573caab4686f121ebbe87b1f959be200d0b47b5b8321378cfec39936052`  
		Last Modified: Thu, 14 Dec 2017 10:15:58 GMT  
		Size: 26.9 KB (26863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb9d0d1b4c4ec595eda254480ee2d3e5c969f09c1ecba3deb197f8d9d8b84c7`  
		Last Modified: Thu, 14 Dec 2017 10:16:02 GMT  
		Size: 34.4 MB (34437016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-jaxrs` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:ce127066d49dddf08338f184c57c948e28d5219e921a0d8240b0e7e7654c82e9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245585517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e034979e09fc2b676a06bdd22d6c799495a23486d535666321860d57ff42e62`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:29:09 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:29:48 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 20 Dec 2017 08:31:58 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-jaxrs-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-jaxrs-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 20 Dec 2017 08:31:59 GMT
EXPOSE 8080/tcp
# Wed, 20 Dec 2017 08:31:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854c2813ea0033b39bf2d048d52062732fdae43084e35939ed5807cde165c98d`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65e77b30af9000ae6edf476683aff54268bb44639c446e3e5101a72ed889d31`  
		Last Modified: Wed, 20 Dec 2017 08:33:06 GMT  
		Size: 34.4 MB (34436746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-jaxrs` - linux; 386

```console
$ docker pull tomee@sha256:3115fc5dead5aeb1559012d154a22dcd77ba249c3993207bd79882d08851aaba
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265455212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f55c9401bacf9d2d0f1b7708065f5a00b7097fb5cccd22fb6695e5c377471f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:45:02 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 21:45:13 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-jaxrs-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-jaxrs-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:45:22 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:45:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726c53aa2fa6a73388a2cd4d813f00f0b32a87796080932b3cb35583bfca993`  
		Last Modified: Wed, 13 Dec 2017 22:01:13 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7ba4f7072f3f0f091f2d3ceb4228821309f79f22557f5ecb9e8e8f628eacba`  
		Last Modified: Wed, 13 Dec 2017 22:01:18 GMT  
		Size: 34.4 MB (34436690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-jaxrs` - linux; ppc64le

```console
$ docker pull tomee@sha256:9a530c947510aa984492325f9da842e470dd5951c7db9a717f7b4a1c14fcca9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252110078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3568cda99996eea6b9da5e9bfadf14f95aa96316e31ec15d406b6d01c7aca266`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:07:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:07:45 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 00:49:07 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-jaxrs.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-jaxrs-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-jaxrs-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:49:09 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:49:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba963a1a2f8c732a2769da68d436102047a1129992a881c6b7f3ccdf77106a5`  
		Last Modified: Thu, 14 Dec 2017 00:53:26 GMT  
		Size: 26.9 KB (26881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b5536200b7afd17716f642f63626994f8e52ee564bf04e122d8b5409514978`  
		Last Modified: Thu, 14 Dec 2017 00:53:31 GMT  
		Size: 34.4 MB (34437002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-1.7.5-plume`

```console
$ docker pull tomee@sha256:80faf7c31cd61be1c8f7cdd3592035b4a1ade676722fea563e4f61d14b62e349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:8-jre-1.7.5-plume` - linux; amd64

```console
$ docker pull tomee@sha256:a871284bc662cfcecf4d24d6d27c7b54682bc8bf0f3440a88b5c043324404a30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (279033952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cbd6c3ada680b5e00f927f2c7113ffd54552020d0510b923342c4b3dd2d20c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:37:41 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 17:22:56 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:22:56 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:22:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66b65c13df185835f71eb63164136a5bd9736b8b894132429090f84a2fa9efc`  
		Last Modified: Wed, 13 Dec 2017 17:25:53 GMT  
		Size: 26.8 KB (26832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef329034b3f9f3273c8804da28a9ee8c70ca753184f3ed642153485341cb9c1d`  
		Last Modified: Wed, 13 Dec 2017 17:26:12 GMT  
		Size: 51.9 MB (51924190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plume` - linux; arm variant v5

```console
$ docker pull tomee@sha256:632efb4bddb6a10809726847fc6ad0878ed7ba388a35a61cd5ad178846a1daab
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247822440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1041156fad2c5b78e2943f50e9f88f2ad5f0affec5b25276d18a3789cbd1295`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:45:55 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 20:18:01 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:18:01 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:18:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06353a9260dd6456f8a0541e8a55da39ec69ae4925e94f89e16664661ef5fc1`  
		Last Modified: Wed, 13 Dec 2017 20:22:08 GMT  
		Size: 26.9 KB (26888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7368f86969f8f91d9fe309646ba0bf1d9c97837508b4bb01876453584be4246d`  
		Last Modified: Wed, 13 Dec 2017 20:22:31 GMT  
		Size: 51.9 MB (51924423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plume` - linux; arm variant v7

```console
$ docker pull tomee@sha256:b9fead86ac50ccf02cbbd4e75192c413ecb7547b3f84e046cb456d2727db3eb0
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258329157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc55abee99bb6babd74fc2a3aa4a62f6b521d6d65e34c22a8303a5d6ab0cdaf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:02:02 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:02:35 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 10:11:11 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:11:11 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:11:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd18573caab4686f121ebbe87b1f959be200d0b47b5b8321378cfec39936052`  
		Last Modified: Thu, 14 Dec 2017 10:15:58 GMT  
		Size: 26.9 KB (26863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63dce41f2e38c56e8ccb8368be0b002932885ff3e2b4c46f8efe7ef47420b0`  
		Last Modified: Thu, 14 Dec 2017 10:16:29 GMT  
		Size: 51.9 MB (51924402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:5790817a964416ef7fd5f38c9876e4620fa92ad40e58ed94ac7c94350356aa93
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263072965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f262619aac0bd957341698c2d170f34f74623114cb9d081267a1aa3928c0dd99`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:29:09 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:29:48 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Sat, 16 Dec 2017 08:30:23 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:30:24 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:30:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854c2813ea0033b39bf2d048d52062732fdae43084e35939ed5807cde165c98d`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936556cb1ef99a1c09378a89a9fd8ad922aeb2c0256522b2c652c8750f75b5c`  
		Last Modified: Sat, 16 Dec 2017 08:36:18 GMT  
		Size: 51.9 MB (51924194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plume` - linux; 386

```console
$ docker pull tomee@sha256:a0accdf5e5fa06db98d346e408f92f58d16a95c0485d3c5efc3bab4306400695
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282942700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c2a8b5a3b062425de29f38cefb8f94f7481a8b8c816891b7cb1a6310389cb2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:45:02 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 21:46:03 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:46:08 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:46:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726c53aa2fa6a73388a2cd4d813f00f0b32a87796080932b3cb35583bfca993`  
		Last Modified: Wed, 13 Dec 2017 22:01:13 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d957c6aeeda3ada03e16f40cc952353d0ee501b1a8adef7b85033f6e2e8b582f`  
		Last Modified: Wed, 13 Dec 2017 22:01:48 GMT  
		Size: 51.9 MB (51924178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plume` - linux; ppc64le

```console
$ docker pull tomee@sha256:fb65c3a39168b183f370b69e2fa797fff4472072979451bc493864b8a5cd084f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269597464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6b27e87dcc2eeab07ce7a24ccd8ec48b4287a39103f03d8110e2cef29ba301`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:07:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:07:45 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 00:50:09 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:50:11 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:50:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba963a1a2f8c732a2769da68d436102047a1129992a881c6b7f3ccdf77106a5`  
		Last Modified: Thu, 14 Dec 2017 00:53:26 GMT  
		Size: 26.9 KB (26881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0def45199a5863028169288c15cade268ced48292d618ab3c1c765880b0d9353`  
		Last Modified: Thu, 14 Dec 2017 00:53:48 GMT  
		Size: 51.9 MB (51924388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-1.7.5-plus`

```console
$ docker pull tomee@sha256:d295483c6c3e7769d0235003ab0306f64066f63b073d6f1450f924548606ad42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:8-jre-1.7.5-plus` - linux; amd64

```console
$ docker pull tomee@sha256:7411dd1c73b5c058b2cc4bb4c7f6e45367fa033cee851ad7ccecb29beb33622f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271375461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9eb50d7485c2d53d0fc17e9b02beec93be6464a18af3635fbe88839dc3d778`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:37:41 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 17:23:10 GMT
RUN set -x 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:23:10 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:23:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66b65c13df185835f71eb63164136a5bd9736b8b894132429090f84a2fa9efc`  
		Last Modified: Wed, 13 Dec 2017 17:25:53 GMT  
		Size: 26.8 KB (26832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521e11f0125b475fc518adce908c874db1a5e8d0cdd2286a2e485dd9e56d1ce0`  
		Last Modified: Wed, 13 Dec 2017 17:26:31 GMT  
		Size: 44.3 MB (44265699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plus` - linux; arm variant v5

```console
$ docker pull tomee@sha256:5d891343aad8fc544139facad1ac0453c35b586776aebee5ebbba45fffdfb27b
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240163969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b35b775f4ef715d43f01833f3cb634f6ca8e95050250f071cdab4b5f1a1c387`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:45:55 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 20:18:18 GMT
RUN set -x 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:18:18 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:18:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06353a9260dd6456f8a0541e8a55da39ec69ae4925e94f89e16664661ef5fc1`  
		Last Modified: Wed, 13 Dec 2017 20:22:08 GMT  
		Size: 26.9 KB (26888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5477fc188c90aa47572e7591fd78df123d73908b758165d751ce827afa654c4a`  
		Last Modified: Wed, 13 Dec 2017 20:22:51 GMT  
		Size: 44.3 MB (44265952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plus` - linux; arm variant v7

```console
$ docker pull tomee@sha256:f66cc39af9b6f7737f10290691a8a997830260cf678f56ec7eef3b9f5c617c02
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250670717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829cc76919343a975065607a910d7dc068f9885366e33f43eef95943bd086a47`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:02:02 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:02:35 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 10:11:30 GMT
RUN set -x 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:11:30 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:11:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd18573caab4686f121ebbe87b1f959be200d0b47b5b8321378cfec39936052`  
		Last Modified: Thu, 14 Dec 2017 10:15:58 GMT  
		Size: 26.9 KB (26863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553e1c6db4a3b74e96a1b749e9556b173a7892469d1f7f7c925e9ccfcac10bac`  
		Last Modified: Thu, 14 Dec 2017 10:16:51 GMT  
		Size: 44.3 MB (44265962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:5a751c383b7d5fdfac69b91cc1a3ef596342923ecc2d0e10e4e93545b270ebd0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255414455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fc8497b01647b54a97b1a6f791186eae00680f083a356b26a5ca66508eeb05`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:29:09 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:29:48 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Sat, 16 Dec 2017 08:30:38 GMT
RUN set -x 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:30:39 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:30:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854c2813ea0033b39bf2d048d52062732fdae43084e35939ed5807cde165c98d`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bc9c5343e423170478a6c176b04b10e324b2d56601f59ff011866961a20e9c`  
		Last Modified: Sat, 16 Dec 2017 08:36:52 GMT  
		Size: 44.3 MB (44265684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plus` - linux; 386

```console
$ docker pull tomee@sha256:e97edc70751ea1bceaedf78169bb6b85d2772b368d22a96c13a2303df9c85f95
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275284194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c947ab0dab492dabaa0bdf5d856ff77471d88f416d94a722981fbd4b8f7aeb05`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:45:02 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 21:46:33 GMT
RUN set -x 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:46:33 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:46:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726c53aa2fa6a73388a2cd4d813f00f0b32a87796080932b3cb35583bfca993`  
		Last Modified: Wed, 13 Dec 2017 22:01:13 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d122770aa18c0e29276ad9053cf56bdc0dad67a488a51ada4ff3788177db8f01`  
		Last Modified: Wed, 13 Dec 2017 22:02:44 GMT  
		Size: 44.3 MB (44265672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-plus` - linux; ppc64le

```console
$ docker pull tomee@sha256:2a4de3f9776c0e1d5b5f96f0e521d57ae8cef389d2ceee19ceb8482d69bc2ae8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261939005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1e91b19cf953ec21c596b481aaefde9177771ed4c4731a6050f1dc9679f370`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:07:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:07:45 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 00:50:33 GMT
RUN set -x 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://repo.maven.apache.org/maven2/org/apache/openejb/apache-tomee/1.7.5/apache-tomee-1.7.5-plus.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:50:35 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:50:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba963a1a2f8c732a2769da68d436102047a1129992a881c6b7f3ccdf77106a5`  
		Last Modified: Thu, 14 Dec 2017 00:53:26 GMT  
		Size: 26.9 KB (26881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd4084c337dc2939b78a94a623de7452c4061293a94e978d3655d35db54cfc9`  
		Last Modified: Thu, 14 Dec 2017 00:54:05 GMT  
		Size: 44.3 MB (44265929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-1.7.5-webprofile`

```console
$ docker pull tomee@sha256:be500cc07d5853b3e39d3454f6a07e012b2f0a86f5fd036bad60e7afcac5e9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:8-jre-1.7.5-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:90b273f30acc64cb2607a8005c128e7314f37317fbfcfa1571fa4cfa28a878a8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258102946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2611941652fbd0d75adddbb94a96d443e5f8400382e955ecd3f684add629954`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:37:41 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 17:23:24 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:23:25 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:23:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66b65c13df185835f71eb63164136a5bd9736b8b894132429090f84a2fa9efc`  
		Last Modified: Wed, 13 Dec 2017 17:25:53 GMT  
		Size: 26.8 KB (26832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d28ebfea7b3846b0b8bbf5935abe5094e6eddd149a4895fd1e550b1519a8d9`  
		Last Modified: Wed, 13 Dec 2017 17:26:47 GMT  
		Size: 31.0 MB (30993184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-webprofile` - linux; arm variant v5

```console
$ docker pull tomee@sha256:407cdf89f45fe3117f7238db7a42c86ad98aeb87d2767e086d82e92cb7f88710
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226891454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019758312049ad49a85146e4db80cadcf89f2c373c37851bca3204c17c288c54`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:45:55 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 20:18:35 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:18:35 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:18:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06353a9260dd6456f8a0541e8a55da39ec69ae4925e94f89e16664661ef5fc1`  
		Last Modified: Wed, 13 Dec 2017 20:22:08 GMT  
		Size: 26.9 KB (26888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c2d93ca2e3db4667b28ffb1532d2f836074adf2602cef56280b036cf1d9778`  
		Last Modified: Wed, 13 Dec 2017 20:23:07 GMT  
		Size: 31.0 MB (30993437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-webprofile` - linux; arm variant v7

```console
$ docker pull tomee@sha256:cb970f54c609a4fbe9a383b31699e6dc4b52bc116eb7d698cfebb8828485d78f
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237398203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f6c0abaa4173a291490e82b48d5cfc71112f79fa9d224d9b6c109cae69147e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:02:02 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:02:35 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 10:11:50 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:11:51 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:11:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd18573caab4686f121ebbe87b1f959be200d0b47b5b8321378cfec39936052`  
		Last Modified: Thu, 14 Dec 2017 10:15:58 GMT  
		Size: 26.9 KB (26863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984eb72d4a0dfa2a3de96302532cee23a6d601f5e3482231cc1c99bc776b4d92`  
		Last Modified: Thu, 14 Dec 2017 10:17:11 GMT  
		Size: 31.0 MB (30993448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:e02d92b6401030f4146847bc5421f7824ba0fb2936de96acd65adf6eb83e8a3b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242141961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10d96c517cb837b1a20b7ded9740b4edb28ba00fba4316c62ec7a8d966b164a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:29:09 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:29:48 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Sat, 16 Dec 2017 08:31:16 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:31:17 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:31:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854c2813ea0033b39bf2d048d52062732fdae43084e35939ed5807cde165c98d`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ef328e06666ec7fae50a341df192002f8ff80a20bf61ad5362d28c39f6c78`  
		Last Modified: Sat, 16 Dec 2017 08:37:07 GMT  
		Size: 31.0 MB (30993190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-webprofile` - linux; 386

```console
$ docker pull tomee@sha256:5505f6e3275422012556fe2c4fa6ac298c436b96320e51ba7bf3b2aaa558bc0b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262011707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66e8cf57ae99685cd389c845e697930c17566e0a839b780edbcea443be35af0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:45:02 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 13 Dec 2017 21:47:03 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:47:47 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:47:48 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7726c53aa2fa6a73388a2cd4d813f00f0b32a87796080932b3cb35583bfca993`  
		Last Modified: Wed, 13 Dec 2017 22:01:13 GMT  
		Size: 26.8 KB (26830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912e9a3cd0d9285b5196a6b22e299f270d988b66eaf97692d9f622b7e3193e5f`  
		Last Modified: Wed, 13 Dec 2017 22:03:14 GMT  
		Size: 31.0 MB (30993185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-1.7.5-webprofile` - linux; ppc64le

```console
$ docker pull tomee@sha256:4739a6afd18cf0d7c07a858cd13b69c9a2d3a252ad9daf8b191e7e1118833579
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248666477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3104523d31ff36cc9ac5ce913f916feb1fefe2c5ed4e27cb7f99f38590778d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:07:33 GMT
ENV GPG_KEYS=BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF 	223D3A74B068ECA354DC385CE126833F9CF64915 	7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF 	82D8419BA697F0E7FB85916EE91287822FDB81B1 	9056B710F1E332780DE7AF34CBAEBE39A46C4CA1 	A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1 	B7574789F5018690043E6DD9C212662E12F3E1DD 	B8B301E6105DF628076BD92C5483E55897ABD9B9 	DBCCD103B8B24F86FFAAB025C8BB472CD297D428 	F067B8140F5DD80E1D3B5D92318242FE9A0B1183 	FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:07:45 GMT
RUN set -xe 	&& for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 Dec 2017 00:51:08 GMT
RUN set -x 	&& curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL http://apache.rediris.es/tomee/tomee-1.7.5/apache-tomee-1.7.5-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-1.7.5/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-1.7.5 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:51:09 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:51:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba963a1a2f8c732a2769da68d436102047a1129992a881c6b7f3ccdf77106a5`  
		Last Modified: Thu, 14 Dec 2017 00:53:26 GMT  
		Size: 26.9 KB (26881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce68ef7d28ca70fe47f88d0f5a146762dbb9a7f7762f610634ab9b0d435924a`  
		Last Modified: Thu, 14 Dec 2017 00:54:44 GMT  
		Size: 31.0 MB (30993401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.0-plume`

```console
$ docker pull tomee@sha256:d05a6385f1fa9301b0e4d0d41a937c2e389845a6cca8580b09e72b796635c82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.0-plume` - linux; amd64

```console
$ docker pull tomee@sha256:e3452ec34fe7062b29463ccd7e1bd541e757e37235bebd069d68480403083196
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284413801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fd9de02c4a120e3b7eeb2e32fd5aae7426dcb5c0cb3f93adb18129aa2c8994`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:39:42 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:39:42 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:39:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0498b1e91978d5a1d5463196c9d745df24f3380153973109a197ee395469839`  
		Last Modified: Tue, 12 Dec 2017 18:43:30 GMT  
		Size: 57.3 MB (57263866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plume` - linux; arm variant v5

```console
$ docker pull tomee@sha256:248d534da26bd77d7733f0228d5f8dd9fece6b170e7e0ea3cc51aed745542230
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253202133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f425295f02b51888f8922c64404b3924907b0f362908ae22ab587c45ae204fc9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:49:03 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:49:04 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:49:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0109baca588a2ac8a658a6e581b8e96459f5a188ba171e651c556c74c90f9f8`  
		Last Modified: Wed, 13 Dec 2017 02:53:19 GMT  
		Size: 57.3 MB (57263963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plume` - linux; arm variant v7

```console
$ docker pull tomee@sha256:859bd6cfd7020ab736c27855f2ebd9ffff79b5cabe6e8f104700b8220de2dd68
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263709006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce46d0ccc1acd91cf5a33a64978ea5915d7f15e0b743de287ef368cd384c9b11`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:05:34 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:05:34 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:05:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fa903eeb2b22d99f90aaa3e9841d87bc0aaf9edc097d133d7aa7b70c205f3e`  
		Last Modified: Tue, 12 Dec 2017 20:10:59 GMT  
		Size: 57.3 MB (57264085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:e77f06c00145a6791207ceaa30cd1bc1a53b170acb19b6ff3c9523ef71e772c2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268452873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04812f0ae103766d208499b5b441dbbf39a90b400ab141de44f8e60d2a2d0d2b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:31:47 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:31:48 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:31:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8230943e7a7912c537aebac8dc04da594ef7a62280a39ddbe692c46d62e9c95`  
		Last Modified: Sat, 16 Dec 2017 08:37:26 GMT  
		Size: 57.3 MB (57263931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plume` - linux; 386

```console
$ docker pull tomee@sha256:d56a63f6aaceb53d5c3e1bada379788ceafaed34dd0642d2d644fbffa164aeb6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.3 MB (288322575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3248c24ab349b405f42d8afd285c1539cab85cd026e139db0b4849543b4193`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:48:32 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:48:53 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:48:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0d21d701b41d58012af16e9e6e1f3cdb77451c44d41d97adb1e6b1c482ab94`  
		Last Modified: Wed, 13 Dec 2017 22:03:38 GMT  
		Size: 57.3 MB (57263875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plume` - linux; ppc64le

```console
$ docker pull tomee@sha256:69f5dbf9a599cf8580c05734e22ec2367f1f0621fe275c9ab9f9041c503b9d43
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274977229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a74237bf0ce72ce0cbc3d3f08084fe1b39e7c3d299d1213f8cd01e5568d912`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:09:58 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:10:00 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:10:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0c97ac04182d95bfe8890af43a351e834c1631e48520c9309611c0114536d`  
		Last Modified: Tue, 12 Dec 2017 12:14:42 GMT  
		Size: 57.3 MB (57263986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plume` - linux; s390x

```console
$ docker pull tomee@sha256:112486b8d7b25ce44b14d9e364590e82e8cc31b28b7ea5b3b70384d34a5d36f3
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256715902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7059179652994673262d59ad726dfdc198a12da4c76d8957e41e07968f81c24`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:40:55 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:40:57 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:40:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666abc3b032afa0474f863c91604068c57e8b6421a701af8e6461a872fccdb3`  
		Last Modified: Sat, 04 Nov 2017 17:43:38 GMT  
		Size: 57.3 MB (57263898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.0-plus`

```console
$ docker pull tomee@sha256:f6054e1cfa7785dbff1c87f59835af73f9dbabfc3caa300ae2eccf928a139694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.0-plus` - linux; amd64

```console
$ docker pull tomee@sha256:ced282a20d9c56c95b1eb5287bfa2225683e6a11e971e259fe2b3ddb5cadf4d9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277326143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71a24a9b6d462024fad17a70690675bd98b959a8d82b48177d4de32baa4f992`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:39:56 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:39:56 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:39:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38f75a7264e45ea3cdd149772ad214f61b975c4e55b32f101893cdc625bfbf6`  
		Last Modified: Tue, 12 Dec 2017 18:44:05 GMT  
		Size: 50.2 MB (50176208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plus` - linux; arm variant v5

```console
$ docker pull tomee@sha256:0c7f42f0effdc66b13a7cfa738c36f62090486604a85f880b1dcebb5ef869620
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246114523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1869b87889e326b25092ec2f6d3712b86dba85ee7cca96623bb3b8c875ee93a2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:49:23 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:49:24 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:49:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc0c8846d37b04c3523cdbb5fc22b6062cd5059b82c4971c17e819b4636570c`  
		Last Modified: Wed, 13 Dec 2017 02:53:50 GMT  
		Size: 50.2 MB (50176353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plus` - linux; arm variant v7

```console
$ docker pull tomee@sha256:936d9391a81cacd8de0634923441582e3e3aed6337c5bc936665d67141e9a2a1
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256621257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c24beb490baa7fcba529fb18800b46c87298a5e314e5da9f270be6373362726`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:05:54 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:05:54 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:05:55 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21927ee846bdf169207534bc3182540aa5723f47d7815b8055e6885caa15e349`  
		Last Modified: Tue, 12 Dec 2017 20:11:22 GMT  
		Size: 50.2 MB (50176336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:38ab256e596a4bfe954d2647f9d2997cb5907a25a193c295d42ec78efe073b36
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261365154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d00e2f3b41da149b7d9e58e5de0050b6f9d32c803101d4c0e73db38b7cfa661`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:32:04 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:32:04 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:32:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b48df3279165c475c1693e9a6d95406eaaa65738c63af68fe980357f1edec8f`  
		Last Modified: Sat, 16 Dec 2017 08:37:44 GMT  
		Size: 50.2 MB (50176212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plus` - linux; 386

```console
$ docker pull tomee@sha256:116da21c4348fdac0e5a5901fa9e0cc3dbd6cd245b325bbd97e238071e61652e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281234911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d75003d40b23b3c39900df5bfe7767cb937b653c2116306b1e88192c3a1f847`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:49:23 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:49:23 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:49:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b5cff7956385400425ac3f7c40120f9acb68b659d93e8d7df3e14848dbe857`  
		Last Modified: Wed, 13 Dec 2017 22:05:24 GMT  
		Size: 50.2 MB (50176211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plus` - linux; ppc64le

```console
$ docker pull tomee@sha256:9aeddb38cbd1a9e414c5eabd9d5534cda8923139c5bcfdd53fb107427bf5441c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267889558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b788747c3566b696856bf3ea7915bb2052f9fc083511a17ff5aebc1f9d74fc33`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:10:18 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:10:20 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:10:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b5692ee3cfc99e12389d281832ef02bbd15d700403c6507c15f942672d3db5`  
		Last Modified: Tue, 12 Dec 2017 12:14:59 GMT  
		Size: 50.2 MB (50176315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-plus` - linux; s390x

```console
$ docker pull tomee@sha256:4dbfe8b4588240e8a318061e461cc968114313b8282f8f67ecab03bf216c73d9
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249628217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0113adcc14f4da9aaafe848c8bff8dede4429996a53618561b64bbbbb6c98469`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:41:09 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:41:10 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:41:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e730f747222ab0d3ebe42c56343713a60dbb4894fc03f7ef3f2ce645dc246670`  
		Last Modified: Sat, 04 Nov 2017 17:43:49 GMT  
		Size: 50.2 MB (50176213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.0-webprofile`

```console
$ docker pull tomee@sha256:c5f8576684c3fed749f5449fada0a31c6c2a1683491616bda51463ffb294219a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.0-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:8a96966b6a21ae31cb303ed64246b301903f9d9180052be6fdc9009dd2584d06
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262335947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05b4517dc482a6f2f9bc683abbfd0b8695fbc311ea024650bd46acefc58c425`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:40:10 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:40:10 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:40:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a92ec4e1be56687134e9806bcfdd5253c305bb619358d0d67fc126194f30eb9`  
		Last Modified: Tue, 12 Dec 2017 18:44:28 GMT  
		Size: 35.2 MB (35186012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-webprofile` - linux; arm variant v5

```console
$ docker pull tomee@sha256:47b0325b0270d66968ebdad30cc1c00b87f3f35d83692b7916df9ab77c979324
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231124421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcc3b95ff5c4b67d17c24b912b0ead599e99ea170ab44aeb78e9287b6d220cc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:49:41 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:49:41 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:49:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d3cdf5decb79c10d051b7dcbc14f2677581d9c8a5138d85e70896f0cb1ff6`  
		Last Modified: Wed, 13 Dec 2017 02:54:08 GMT  
		Size: 35.2 MB (35186251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-webprofile` - linux; arm variant v7

```console
$ docker pull tomee@sha256:bb6ba3e9641a512e93153fbbad162082ea59b7c5ce2c5ae4a0c275f0bc7ae9b9
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241631190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141a8915786f7d3b979de1272c823209905a054d6f768b6de6b26fad874c1f81`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:06:28 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:06:28 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:06:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58512f23963d3def766da27d897becd9f9089d5ab325c680ba006a2d7ef63a97`  
		Last Modified: Tue, 12 Dec 2017 20:11:51 GMT  
		Size: 35.2 MB (35186269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:db66ea58ba0839597aeb00adc682da7eafe117fe6281100f2cb688ecc7d3e74f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246374963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b634fb4c1283f0e008cbe4448c8530260f6714e89e5d23f02b5ae004d74817`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:32:19 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:32:19 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:32:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bcde09a7577b81461c0bdbb922cafb0f6d78e933a6762c825541e244fff1ef`  
		Last Modified: Sat, 16 Dec 2017 08:37:59 GMT  
		Size: 35.2 MB (35186021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-webprofile` - linux; 386

```console
$ docker pull tomee@sha256:e20a962c591300dbe7f9c1ac42ed5e721c04ce0dff725b8993af8e1c17f3515f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266244722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa054e3bb9409a9ce974753722c9cdd4bacc7f359ec4694e95312a59007e079`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:49:58 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:49:58 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:49:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4df840a9e2a3976bfffa222f19c0cf7d124923c64448b9f0207e8b88fe09a`  
		Last Modified: Wed, 13 Dec 2017 22:05:51 GMT  
		Size: 35.2 MB (35186022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-webprofile` - linux; ppc64le

```console
$ docker pull tomee@sha256:ff08d4e82b32c26fadb8c7f8ef8490b74a74633c5eb1c080ac55bec8c4f3b388
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252899520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd25fe5f082c200435c5e263773a4b39272b6c395d48f581bbcf4390d38eaea`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:10:35 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:10:38 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:10:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6ab0a432c0c82f3f147e106667e960cce0b330140f72b41c7174b97948f213`  
		Last Modified: Tue, 12 Dec 2017 12:15:15 GMT  
		Size: 35.2 MB (35186277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.0-webprofile` - linux; s390x

```console
$ docker pull tomee@sha256:a189ac70bfb7f875ae320ef6c2d466563c70e572da4ee919822ac3016bd7846e
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234638058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4751e944cdaeb32b7f60c559b95f75d4713667ad103817096abc951e0833841b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:41:19 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.0/apache-tomee-7.0.0-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.0/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.0 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:41:21 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:41:21 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2486037314644ae02997a6a5e787dc2356cdcf41359090adc7f733fae9e7375a`  
		Last Modified: Sat, 04 Nov 2017 17:44:00 GMT  
		Size: 35.2 MB (35186054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.1-plume`

```console
$ docker pull tomee@sha256:0b241f225ac93bd6e92ac64c1c448fd5c9603705f4be9630038916b81a38c099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.1-plume` - linux; amd64

```console
$ docker pull tomee@sha256:3b15666e956e3ec9bc9f635b18932a6c4ff9d54b4e2135afd248ddb97a803623
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284445934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db129c8dd3fc7793c1817f2aaf9c935c8c0a4725b4a876503c8464034d572076`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:40:21 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:40:22 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:40:22 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b60f5a96b91c3611fddbba97b716b1f6a6e7a9928db7c11f64ce2f30ccbb5fd`  
		Last Modified: Tue, 12 Dec 2017 18:44:49 GMT  
		Size: 57.3 MB (57295999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plume` - linux; arm variant v5

```console
$ docker pull tomee@sha256:eaa0f9f1757a5282115f514f40c3825ffc4938ac49b6caac50afba1c5f6433ab
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253234301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f797e977b6616043c0699620f4033cb8e7de4b2f46715a7c49051164fc8f739`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:50:06 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:50:06 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:50:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b16b626e2a9be5c6ced29fc85f108fdb1054ace8f3e643ecb25df2e7b61169`  
		Last Modified: Wed, 13 Dec 2017 02:54:36 GMT  
		Size: 57.3 MB (57296131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plume` - linux; arm variant v7

```console
$ docker pull tomee@sha256:68ef14fa72564acb19a3dc7de816de82d4b7306b89bcf1753a7d2593fff833c9
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263741016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64148e73d6e7c27ae6485b8cc6ac11aaddcf3098ff827709f51555d5700f646e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:06:51 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:06:51 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:06:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ec3a8261c75b6798f24e9b9ed011e1ac21e8741c2dc914b870da9d83f61329`  
		Last Modified: Tue, 12 Dec 2017 20:12:17 GMT  
		Size: 57.3 MB (57296095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:29063d50ae1f9ed78a36db2f8bf0da77451c75485b60725fa2acc5c30085dbac
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268484948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfe1418dac29d9060305a86f9960707d6f3d75596c01d72bc8f25ead72e01d6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:32:35 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:32:36 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:32:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a57f97cd3c072aba2859a71e8a454f0f46638e1689bcd1145daebf14efc97a3`  
		Last Modified: Sat, 16 Dec 2017 08:38:22 GMT  
		Size: 57.3 MB (57296006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plume` - linux; 386

```console
$ docker pull tomee@sha256:d38318e94a711a7cf12989b23058e7fb297fcc7fb0874c799d715598b1a69525
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288354722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d89a8eb7aa6f13ac70466ce7a6258cb795d119b1e36a8dd671d5355959b1d9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:50:13 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:50:14 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:50:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18323d26097965848e0aa87d29a59b1a9ca6658e695515bae35cd2a25a8ca04`  
		Last Modified: Wed, 13 Dec 2017 22:06:23 GMT  
		Size: 57.3 MB (57296022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plume` - linux; ppc64le

```console
$ docker pull tomee@sha256:c905e1cf2db22dc1deec030a23aad6a6583b50a1a1fac01eab808f3abd04c85a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (275009374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d900311e3c7842e33d6f5bb292e8cd2ed5184f75320c8022d702d69326b4ed5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:10:57 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:11:00 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:11:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cce84d225e11fc2e6f117b4e52363c267fdd38e12dc80a3513b01544674465b`  
		Last Modified: Tue, 12 Dec 2017 12:15:32 GMT  
		Size: 57.3 MB (57296131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plume` - linux; s390x

```console
$ docker pull tomee@sha256:5923f18c19c22a3e45bdc942fc233fa26752c6b5581da4344c6bd5096125108c
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256748024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646648d137f410749d9255037faa0ea72b9015d4701d0e244b835532d0906501`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:41:33 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:41:33 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:41:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae2b5f9d5c8606995c8a86b7739573e65b8f12da3a42fdc6ed8cd7cbdaf850a`  
		Last Modified: Sat, 04 Nov 2017 17:44:16 GMT  
		Size: 57.3 MB (57296020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.1-plus`

```console
$ docker pull tomee@sha256:d2ff2f2c225cc8a51fe99073d2ff6b88d20d65d77655ef0970d93f7028d8633a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.1-plus` - linux; amd64

```console
$ docker pull tomee@sha256:b297ce84a3f9a8ef5f0e36d9aa6fe2b61b164aee574db36c4b509c97b77b2d50
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277356655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4d846498062362f0e3ab7a554ec9e548cd9c301beb3cfa22fb7e1fe47ea2f5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:40:34 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:40:40 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:40:40 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6977ade56da206ac919a25953cd333152f4f93f871441df2ed022e6729b036e`  
		Last Modified: Tue, 12 Dec 2017 18:45:13 GMT  
		Size: 50.2 MB (50206720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plus` - linux; arm variant v5

```console
$ docker pull tomee@sha256:234c8ea59b09d9f2a3ee8eb1c38f66802fbd53cd25d75ed181be07eefb9e5897
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246145146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d83a09bd24c2ff695afa7a7dff9b8e39835b104a8a3467bf6462d9440c208fe`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:50:24 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:50:25 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:50:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53fb5481efbeaac1a90bc7894fe2c1bf3cad3eba0d370580d9b0980a3ff28af7`  
		Last Modified: Wed, 13 Dec 2017 02:54:55 GMT  
		Size: 50.2 MB (50206976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plus` - linux; arm variant v7

```console
$ docker pull tomee@sha256:9936337b65f52c9ff74e836dd18781a71f4aa11fac4950d2b5d1e55b757f2001
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256651882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b324f107e779e86e9593498dccd73a48344f4bdd25fcfeb07de9fe2b85b8db73`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:07:38 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:07:39 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:07:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0afd838fcc933ff6cadceb787d7fea3ed066accc8915cbd8c0eaa9088daf9b`  
		Last Modified: Tue, 12 Dec 2017 20:12:37 GMT  
		Size: 50.2 MB (50206961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:dbf476eea487b9c164b664d4bf944fb9c3828c6b40134db5ddf2ccc91efcf0d8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261395721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984711c6148f748aafe523ca2e8bf88fbef007b212726afb85e83cd58d05a781`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:32:51 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:32:51 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:32:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e829f701ceb456430b0368688b91a066ea2ea6fbf37044715780db550f083f68`  
		Last Modified: Sat, 16 Dec 2017 08:38:41 GMT  
		Size: 50.2 MB (50206779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plus` - linux; 386

```console
$ docker pull tomee@sha256:f456372cfd51b4f3abdef3e2aa959fa9eaa7171ff729ed4175770398e90c61fd
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342adb666ece0032cb9fa7e8b3dcc799d92b67be5de7893f73da98def69f26f6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:53:34 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:53:34 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:53:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae50d66f6b70d237991ac862414ecf84ca630d38a130783122e957a95d5b1196`  
		Last Modified: Wed, 13 Dec 2017 22:06:54 GMT  
		Size: 50.2 MB (50206774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plus` - linux; ppc64le

```console
$ docker pull tomee@sha256:7dffc9fcb8696a70f7654fe122c4eb58d1fedbb2a9b7912b0c6dd70c6be26ac6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267920216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8f7408bdaa08271fceb303aed31150705e0f7f76b66031400f8f218e31aac1`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:11:19 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:11:21 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:11:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849c315c65bbdc1306bca741fd4e70ff8c0417566998924245f4429e21e38c03`  
		Last Modified: Tue, 12 Dec 2017 12:15:49 GMT  
		Size: 50.2 MB (50206973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-plus` - linux; s390x

```console
$ docker pull tomee@sha256:108a8d0b270c29a4807734c0289ab41724846e851a25eca5f6c19c0659045ef1
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249658763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb74879e96f42c687002c093a5d988a888e2f12feccb393ba66dd1cd5b788ae`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:41:48 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:41:49 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:41:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648a3a4b72752f7a75ae0932aa36c7536b7c5d37881528f0b66fa74692ff63f3`  
		Last Modified: Sat, 04 Nov 2017 17:44:28 GMT  
		Size: 50.2 MB (50206759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.1-webprofile`

```console
$ docker pull tomee@sha256:afb87bb513b6440c757bd1bba13574cd60a16d7df8488834bb4adffbeb455547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.1-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:e3e5ee74bd109786c1b4d487f61f89ad4edbb431cfe41bb36859d5ff4ad4755d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262365067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba67ddbe5ca4afe380e0feba73cfeb9ab7d6bf21ebdc68633789a5a8aee5ed`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:40:52 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:40:58 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:40:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bacc1b3b0d63562db869e55165237009ee9b50fec52a729fd4e84ae4985bbd4`  
		Last Modified: Tue, 12 Dec 2017 18:45:30 GMT  
		Size: 35.2 MB (35215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-webprofile` - linux; arm variant v5

```console
$ docker pull tomee@sha256:0d9483c4a24a9451ca87370584540ca5b4e82598a03cc4153a6bf72b64385281
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231153463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c788fa11cddd2bfb0259a840251466af1c39d6289b1edc47f4ed620f6442272`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:50:48 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:50:49 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:50:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ef595f96b31ef19538fd8c0785e5f2eba67f91490df3701af1950f06cd512d`  
		Last Modified: Wed, 13 Dec 2017 02:55:12 GMT  
		Size: 35.2 MB (35215293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-webprofile` - linux; arm variant v7

```console
$ docker pull tomee@sha256:d637b4450b0aa67f45b1f0a7d0f97ce2d96d97ccd264201b97237d35379793b5
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241660225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5113852559e294c7527291c28318dc4275f24d2b262513ca64dad4f6f211208`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:08:00 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:08:01 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:08:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6edd5b6e3ab23f10ad87e4d157457e234340639226bc8ecdae2a2491c9ca95`  
		Last Modified: Tue, 12 Dec 2017 20:12:57 GMT  
		Size: 35.2 MB (35215304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:77b5448906b9084ea496d4ea78abe4d3447d3e0af899698b1d61b0d1977d9dce
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246403986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc1ef3e4dd26bef86191e4ad19164837af9b57be5d6cf81434db880086a8f2b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:33:06 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:33:07 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:33:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246a76f20e2974220fc57eb4d1676ee7c3eb96d27f63d5c2423ed5d567e63229`  
		Last Modified: Sat, 16 Dec 2017 08:38:59 GMT  
		Size: 35.2 MB (35215044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-webprofile` - linux; 386

```console
$ docker pull tomee@sha256:3151f62e884427f62e7b94d1cacfcc9827bbf5361ff9bf172b8d8c4d13c05494
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266273813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc90f4851fdf139dc27650a7f927224033e1ad0443ba494a7c5b0d554335f85`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:53:58 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:53:58 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:53:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de257a297bf0c347be1c8caeab94a80e160863ca8ac4f0966519457c3469fb9c`  
		Last Modified: Wed, 13 Dec 2017 22:07:16 GMT  
		Size: 35.2 MB (35215113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-webprofile` - linux; ppc64le

```console
$ docker pull tomee@sha256:e6bfd6784ab636de2e80ac79ec434942fdc0c079f1ff7db97898eb2aa0199980
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252928555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d828d89a54cb73724f32597e2b35b81aa5a969131810ca59065dc303073ada`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:11:42 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:11:43 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:11:45 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4ba0784d6e8553652cc52027339be494a5a23b3341aa984291731ce528743f`  
		Last Modified: Tue, 12 Dec 2017 12:16:05 GMT  
		Size: 35.2 MB (35215312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.1-webprofile` - linux; s390x

```console
$ docker pull tomee@sha256:26f021d09b45d6978691f802d497c07f0aec3459f5386cae7e8aa29c991e231d
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234667145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d459676432adc13f6a90f7a7df4d8211c9feb9d757ff4e53586a6894a55d03`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:42:03 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.1/apache-tomee-7.0.1-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.1/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.1 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:42:03 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:42:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcaf3a7a736ebc7987c46f16ff7b7a98fb7f692d39a8e8198fa0c2475c6e270`  
		Last Modified: Sat, 04 Nov 2017 17:44:43 GMT  
		Size: 35.2 MB (35215141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.2-plume`

```console
$ docker pull tomee@sha256:1aa8e012c605a8c078aa7fc84bf9de2bff32dcf578abee4ba2da23130defac51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.2-plume` - linux; amd64

```console
$ docker pull tomee@sha256:992393f89ce557a1e2dad74c6be50fd692e5bf409e834b9be0f3ce056bb6228c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285039651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae15126d68d7c79335edb3da30242ef1f7d3584c0338583c71d4c509958435a7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:41:20 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:41:22 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:41:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03398641349b4d5f4a0616fa3cf285744b5373a9217a3aeda7f68f5a6366ae27`  
		Last Modified: Tue, 12 Dec 2017 18:45:54 GMT  
		Size: 57.9 MB (57889716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plume` - linux; arm variant v5

```console
$ docker pull tomee@sha256:31197724117b1d693ab62ab79e10dbe85fc75a0f83834e7c22624cd648c96cd1
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253828169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938d1c0beac18e810a8083af8c8ae0b68483aaeb3cf8ca5f489e9ea6b32dadde`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:51:06 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:51:06 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:51:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d44c7bbc366ab72e1dd7b13182ab8e7a7b73ae0f9785fc16757cb7c5dafba5`  
		Last Modified: Wed, 13 Dec 2017 02:55:31 GMT  
		Size: 57.9 MB (57889999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plume` - linux; arm variant v7

```console
$ docker pull tomee@sha256:e9b5e57fa34f064a214c6e9786221073b9d353ab30be0e2862ead23040e5d10b
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264334911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9231a04f6928084f06513de34274354ef1b3699852f20855ff2e29f364a9e3f9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:08:40 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:08:41 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:08:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d7a6b5b9e2750213052c3c2a7b0ce41ef9bddc3f6c194d8f44ad145ad75e02`  
		Last Modified: Tue, 12 Dec 2017 20:13:22 GMT  
		Size: 57.9 MB (57889990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:9fb5cb5249ae9e47097401fb91f5ae871ce335b565b84aeee92873cd491db6ab
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269078668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecbe084e8cfa617662fc2d8a7c489eb968126e77d5eaec0f1481bda89b78eff`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:33:22 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:33:23 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:33:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15be4f842301920f242cbfe04c674d72143b2b8073f64dd795527d073995d20`  
		Last Modified: Sat, 16 Dec 2017 08:39:18 GMT  
		Size: 57.9 MB (57889726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plume` - linux; 386

```console
$ docker pull tomee@sha256:9bffc7aa5afcb0528164bd4842ba8e4fb08f5b72b66f6591c5bee496e6c17cd8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288948406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98e2f3474dda2a1717715a3fde7433fc7efff016f030d99159939d6a232e285`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:54:14 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:54:14 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:54:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47a7ce1996b50d710c26d324245522d254e150b0ccf7fc41940fb393cd7e568`  
		Last Modified: Wed, 13 Dec 2017 22:07:41 GMT  
		Size: 57.9 MB (57889706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plume` - linux; ppc64le

```console
$ docker pull tomee@sha256:91c08feb4ed25040a78c1eef04f16047b8f12512e610d827c04f5fac2600d19d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275603212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4860746f7447ec6db051f853f63efdb5062b3881449918f9b9d7f81c85249bc7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:12:02 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:12:04 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:12:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead56e47679a3be1734e81c4f656c9bcf97c6439e5d61e542694ca8ffa78e05`  
		Last Modified: Tue, 12 Dec 2017 12:16:29 GMT  
		Size: 57.9 MB (57889969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plume` - linux; s390x

```console
$ docker pull tomee@sha256:0c32f08a238af9f1d4fab374a42cdaf3aa3d874dea68c5de9e47760af143dcfd
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257341720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90e391761a393b5bed080c293c0c562bee4fa528031d56cd71b3e137b8b7f1c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:42:15 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:42:18 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:42:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7a5f6e1b14491030373af7998cbe984b02c7f5bda75bba4e2583d3014c0bd9`  
		Last Modified: Sat, 04 Nov 2017 17:44:57 GMT  
		Size: 57.9 MB (57889716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.2-plus`

```console
$ docker pull tomee@sha256:7b02d629df8b7d496777054bfba76e82d14ccfe3797c02df18cabd0116c64ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.2-plus` - linux; amd64

```console
$ docker pull tomee@sha256:7fa71e7903a9d53e854d49be4f31b07295c8286e46854bc3725ba834d07b2a3e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278084865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36fc60eee06b04ba363949f2a422225ffd10e6de3b5a72cd10450fb87eb795e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:41:43 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:41:47 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:41:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c752ff042952b005c7285b89b3c3bb1c761450fb7c75e29d0025d1ad0fccb8ec`  
		Last Modified: Tue, 12 Dec 2017 18:46:16 GMT  
		Size: 50.9 MB (50934930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plus` - linux; arm variant v5

```console
$ docker pull tomee@sha256:c06f613a28bef7c726feb9ab0353a25de39e6dfe7f766046d5b4d322bce0750f
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246873512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e11398cc113efa307bbf21bcd158a3c5e3432b355ea447a1ec07fc1d5ee2006`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:51:30 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:51:31 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:51:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfee48557c5c1645fcbed12b4829f1a1a14dd51e1dcb25dcc6d1c4008fa7f06`  
		Last Modified: Wed, 13 Dec 2017 02:55:50 GMT  
		Size: 50.9 MB (50935342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plus` - linux; arm variant v7

```console
$ docker pull tomee@sha256:91707a25750394fa839153b219e200d71d4c2674da30e00d76566538b82f92fe
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257380232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa284d3fb659f823330c9f757a3d042e3aa7676bf43e6634f89e23a3e8e9b3d9`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:09:04 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:09:05 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:09:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213f3727897275ce370346b58a989729e738b6b86249051f02b347210fda8764`  
		Last Modified: Tue, 12 Dec 2017 20:13:45 GMT  
		Size: 50.9 MB (50935311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:19eb9c50d44bd806c05578a6f7d89cdeb8e000e4c0cadc4f932a45976116eaa4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262123818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f8fb0f15ca134ced36b6aba7ebccaf9c3bb4430c43de15b080818391970716`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:33:38 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:33:39 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:33:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053eb42c7ad914f227558520368bc92f194073a34d7a71d4f64b78365e3a6b02`  
		Last Modified: Sat, 16 Dec 2017 08:39:35 GMT  
		Size: 50.9 MB (50934876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plus` - linux; 386

```console
$ docker pull tomee@sha256:55b30c3f8546c38487a0c67cc731a4da2e8a195fc0692258bbd7b6bc7e396e60
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 MB (281993612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8004fb2fdf45efed82894ca1f653f8dc29abaae21cf06373dec0f177868d87`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:54:29 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:54:30 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:54:30 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f64a631405d74958a9d838e92dd478b02cb089764d5e44f616bf13d0f2d58c7`  
		Last Modified: Wed, 13 Dec 2017 22:08:10 GMT  
		Size: 50.9 MB (50934912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plus` - linux; ppc64le

```console
$ docker pull tomee@sha256:73503250bdea99887a92f7f71ad8216b9a26f2fac548535b5b2f9dad6a064166
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268648536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91048135f3fd5457c12e1def68ebf9cf3e5ffb4da3a8e9f518666ad568aeff20`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:12:32 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:12:34 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:12:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c817cba31186d5b1805f7928dafff4412a0163f21459dd42a66b712537dd9117`  
		Last Modified: Tue, 12 Dec 2017 12:16:47 GMT  
		Size: 50.9 MB (50935293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-plus` - linux; s390x

```console
$ docker pull tomee@sha256:37e6cdad6aadfb4135dcabd7e3010aae264295320df30168899587bfddaebdec
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0285b9a85fad9cd2cb7637d969e3a9fe1aab5fc400f8964ebd914074da452b19`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:42:32 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:42:33 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:42:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b963bf3a0a95f129a61dbc51734c0cc68ef06a8e3c28aecddcb5f82029c88e08`  
		Last Modified: Sat, 04 Nov 2017 17:45:09 GMT  
		Size: 50.9 MB (50934873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.2-webprofile`

```console
$ docker pull tomee@sha256:1fc2af687b6ce29fba1d4a8b3226a7ff6213960ca61d65b62ee9334d6d062c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.2-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:9c45d6e13e24a5b5f42f5ab9ac7486398a085fbd0aeae73d902f5da2956cdde4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262522557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcf210cab8ffb2e562bace7d8d01156db3f3169b87e3a36cbeeb9bc0a050b05`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:42:06 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:42:06 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:42:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42e1730d6da46bd6e6084d57090f768ca60d0f0f7c31073448f95fe1398a57c`  
		Last Modified: Tue, 12 Dec 2017 18:46:33 GMT  
		Size: 35.4 MB (35372622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-webprofile` - linux; arm variant v5

```console
$ docker pull tomee@sha256:a71bf9543b19c8fa9161f95a7aa08ad8de8a53c90d0ca8f96d048666e2727089
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231310900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283b7075a6fd822dba0f93bc3cc815403202366f5b31cc2805a10809f12d889`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:51:48 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:51:49 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:51:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eea127167ff77d93db316eade67810aa2d1d1f72e373d1328beda01b482069`  
		Last Modified: Wed, 13 Dec 2017 02:56:10 GMT  
		Size: 35.4 MB (35372730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-webprofile` - linux; arm variant v7

```console
$ docker pull tomee@sha256:ad36222df9a28875b2b4b53fd0514c6c158027761caa6de3f01ca5de38bef37d
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241817668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83692256005089874d5199ede67a776b8eec585df8b5fa19809a0fb6fe6e9064`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:09:30 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:09:30 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:09:31 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2524aef183b94daecb929cfbea416f29c82499f610cb9cd3c0fe906df980cfdf`  
		Last Modified: Tue, 12 Dec 2017 20:14:07 GMT  
		Size: 35.4 MB (35372747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:0311f75277dfd873b95cee942b1dc63cd99be0057c99984a8c7181fce786643b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246561573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c650d3159af1d54aa686440d718d2f2188a80ad9dc9ade7f8b9f8780fd1cbe`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:33:51 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:33:51 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:33:52 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaa8dbe8ef80fe5b619b66ff0c8bc50b2cfa174ec96af081efc21508484a636`  
		Last Modified: Sat, 16 Dec 2017 08:39:50 GMT  
		Size: 35.4 MB (35372631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-webprofile` - linux; 386

```console
$ docker pull tomee@sha256:8b5f34c00404cd6b578ae906d077f1daf5eab5b2c17aed197a2c2a8b2a1d2007
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266431344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d804cb0f0e589f241a7dbcbbc08e271878a52d61887bb4123b4885b6abbece8f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:55:51 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:55:51 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:55:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab70c816a75663c5668de18f9a2c0828bca253b6e0f93e28b0476bebdc10aff`  
		Last Modified: Wed, 13 Dec 2017 22:10:01 GMT  
		Size: 35.4 MB (35372644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-webprofile` - linux; ppc64le

```console
$ docker pull tomee@sha256:a53d457af6c283a190b58f01bba869a9892fb85a5359b559400d18fef1262874
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253085984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0c1df609f2a235e29726e0b5993f8671475c0fc3759a21875429c7552fa75f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:12:58 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:13:04 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:13:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d79de6fa9c9f70ffa8be95747be8583f253af931fdcc2b424749f390966a8d`  
		Last Modified: Tue, 12 Dec 2017 12:17:05 GMT  
		Size: 35.4 MB (35372741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.2-webprofile` - linux; s390x

```console
$ docker pull tomee@sha256:d40a1fc39d6d7eb1c1aae03f0d26194ad62ba53de2ea75b002b6ecfa06ee54cd
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234824673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fa59bf06a7d747baa4ba33296e3e3852812cf8d341cd608ecc49cd6fd152c0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:42:43 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.2/apache-tomee-7.0.2-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.2/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.2 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:42:43 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:42:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459eaa015df42b40f4694a1be89b806a7ac51c9d09c17fdee11e6d4c292fffa0`  
		Last Modified: Sat, 04 Nov 2017 17:45:19 GMT  
		Size: 35.4 MB (35372669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.3-plume`

```console
$ docker pull tomee@sha256:9e866cde60304f0cfb4c754aba860a8c4eddd4ca7631eac2fa25627c2db9dafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.3-plume` - linux; amd64

```console
$ docker pull tomee@sha256:6ad658e9523f3febd83e2f9cacc0e62a00b9869cbae645aef91b322c178679d2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285092918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4047e2bdd31df17a0d278b47c30eac56c907f7039436927bd54f04ba6c582ab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:42:18 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:42:24 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:42:24 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4e15edfb2788956e80e98678ced6cf879395f64adb8e4b187a2b76e758096f`  
		Last Modified: Tue, 12 Dec 2017 18:46:52 GMT  
		Size: 57.9 MB (57942983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plume` - linux; arm variant v5

```console
$ docker pull tomee@sha256:9f844d6eac6c492151465faac81e52af47cbbdbc392986bd540a44726ba69357
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253881512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bac7659e9aee3bfdf292a14f5625838dbd806f68c230ee6aee16db3048f0c7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:52:14 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:52:15 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:52:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845ddd92bae4f582d32a550146be3b60b504b9743e6cc1282a4de17cc6ce53e4`  
		Last Modified: Wed, 13 Dec 2017 02:56:30 GMT  
		Size: 57.9 MB (57943342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plume` - linux; arm variant v7

```console
$ docker pull tomee@sha256:3db6d14b1b9577ac63515e6fd1ee7240f32b54bb3b8de950bc7ac4f36450243b
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264388255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e11b0d923ebfd4150cf8c8458a54452a96f33c1d288c4e118de1f60c166770`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:09:49 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:09:50 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:09:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854df4dcc458fbffd0c869e147a85108be6f066ce07fe9cc84cded46142bfcd`  
		Last Modified: Tue, 12 Dec 2017 20:14:29 GMT  
		Size: 57.9 MB (57943334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:8a4be71a460e1d466a597a0e1dcf1480c100d9195090f1bee0a7b3b681dc6e9c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269131980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2fc7f45412ccb4d5a1051e47ab47eb460db4e8de69b75f11863274b5412231`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:34:08 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:34:09 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:34:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec471a29927910fa794aecb673df6494b33e7695ab4c5da3ecee9a9d4ab77665`  
		Last Modified: Sat, 16 Dec 2017 08:40:08 GMT  
		Size: 57.9 MB (57943038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plume` - linux; 386

```console
$ docker pull tomee@sha256:3abf6df945b71be3c62790f5c6b904a3619bf1fcf72de8a2323b41d34e6398c0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289001710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a44f19e31dbdcb41c814323a15bd98ff1c80ebf8d1690884c8e82653e0d9ede`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:56:08 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:56:12 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:56:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0623a06497f1e83776d25c5445deb9f9f084e9ed6fe515237c5db7a93a081ce`  
		Last Modified: Wed, 13 Dec 2017 22:11:54 GMT  
		Size: 57.9 MB (57943010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plume` - linux; ppc64le

```console
$ docker pull tomee@sha256:444fa9370f51cc7b0e69b9cec945f3be44d3e3b5163f1c6518f5c8fcd5c57291
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275656557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f57406dc2c3d32d09e873eb8831e1cd53d6ccd4e496484524d2158fd953dc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:13:28 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:13:31 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:13:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fed6c518fa910e315c4b5d0415064fcb1e9852daafd30f1fbba7dfda8f7b12`  
		Last Modified: Tue, 12 Dec 2017 12:17:22 GMT  
		Size: 57.9 MB (57943314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plume` - linux; s390x

```console
$ docker pull tomee@sha256:a18694a4cabd38293b6b81193a85c34ccfb5e9ad3993dd8b37ba6b7fa666761f
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257395026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b214f0b6574c6fab519342e0009b6fba90b14a837334b21682ee2afa245ac2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:42:57 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:42:58 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:42:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c4e445494459ef718de9210334ec2c0de950de6548a49297a0114fe0874c50`  
		Last Modified: Sat, 04 Nov 2017 17:45:31 GMT  
		Size: 57.9 MB (57943022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.3-plus`

```console
$ docker pull tomee@sha256:2d82b1894e5ab941960e1c62a25b254f5837156ed6cfadb426a6f1958a54e3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.3-plus` - linux; amd64

```console
$ docker pull tomee@sha256:f193f522cfa588ddcaa2a827a1e806edebd48c7aa61ec5c26232b062b6a0cf59
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278133112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113e9d3815d9e86dc54827f77f183d06d9cb16bb947542037cb3da3a45006440`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:42:43 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:42:49 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:42:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070a7b0295606d2e43c94b858715c79c337f046c9b65fc754e3635756cf19b0`  
		Last Modified: Tue, 12 Dec 2017 18:47:14 GMT  
		Size: 51.0 MB (50983177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plus` - linux; arm variant v5

```console
$ docker pull tomee@sha256:2ea6c361fb382c1bf0a0a8b2324b4190369b83e962affeb2f25977aef70a4b80
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246921488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746d901fd0fe86a1c2e2e2e44fd662833288521225f71ff3760476179087aa7e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:52:32 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:52:32 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:52:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c71c9c91eafecd86f822c562b1dd1c1775100ff7e6e3360d80e68de4be52367`  
		Last Modified: Wed, 13 Dec 2017 02:56:50 GMT  
		Size: 51.0 MB (50983318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plus` - linux; arm variant v7

```console
$ docker pull tomee@sha256:ddf41fae8f2e98fcd8bb90d82995d0800f8751b48a95e92bf4d62fa944e65083
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257428243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3598b8ee8f02eb50451d5bb0b34a38cb812bd9d78790540c29e71b349c8d01e0`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:10:09 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:10:10 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:10:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206f7a7ad8745c3fb27a59c15006e82f54a9c0dd7345f8a24af9a8f40f5f57ab`  
		Last Modified: Tue, 12 Dec 2017 20:14:53 GMT  
		Size: 51.0 MB (50983322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:b82a05085c1ee29678da18bff0cb1de185739bb3435567abf401dbd0b2726b8e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262172146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11485d8e44939bd373bcbe6dc087cb64eece84d4632c721a6a65b7a6a50425a6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:34:26 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:34:26 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:34:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d8fd1ec63d0f58ab9387daa454574cbb34115be4346ccaa0cec84975c7378b`  
		Last Modified: Sat, 16 Dec 2017 08:40:25 GMT  
		Size: 51.0 MB (50983204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plus` - linux; 386

```console
$ docker pull tomee@sha256:9871f71e54ba5ccb234492ca38c22e347706bade9cbc15efee6968cdd75085a9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 MB (282041881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7522256f9dd075f31061d9fe67b798a65b75bb5ba60f38c97e4bf814a8fda0c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:56:27 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:56:27 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:56:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf31ccb985f027c947cdac12b2cf7eac5c976e451277c8c7f74b5810a458f30f`  
		Last Modified: Wed, 13 Dec 2017 22:12:23 GMT  
		Size: 51.0 MB (50983181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plus` - linux; ppc64le

```console
$ docker pull tomee@sha256:3ae1717363df340f6423da9edae9874b332ed4d64ccce369667cd64917cb854a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268696493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bb4747a09e298ed7b43f399fa3cfda8b10aa0f05b78d4dafa6611a036c6f1c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:13:56 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:14:00 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:14:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8953fddc4a76ae3a6dad75edc93f6c63091e67ca28633e9e34b9d932bc2e711d`  
		Last Modified: Tue, 12 Dec 2017 12:17:41 GMT  
		Size: 51.0 MB (50983250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-plus` - linux; s390x

```console
$ docker pull tomee@sha256:87a06921f84a4a61a884e321f5a46272c8090904c62b95b19fc3ba7e49398b52
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250435214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1a295821fe7caaa2de56e922f6442e821e2ad363006e2dbffec63935042b8f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:43:11 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:43:11 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:43:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1120f39ad0d46b58ceef771d4fe745309cd7bca36f4b8ec59dc98521c5d3b`  
		Last Modified: Sat, 04 Nov 2017 17:45:43 GMT  
		Size: 51.0 MB (50983210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.3-webprofile`

```console
$ docker pull tomee@sha256:464536d6e6630df7e0e123b984c3321139cf0ce03d6404636dbb031c6ba4f356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomee:8-jre-7.0.3-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:d332bd158edda11ad23c2c73581bd708866aa6fe8d5a6141287510f1ecf77cc6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262565964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5ca12910c02777998021cb9200c7d0d32891383420a2c334d677832bb01d57`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 18:43:08 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 18:43:08 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 18:43:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af739cd4a013dd983173a03770b1c3e7ac156a7da2c7e8218bd7521194a958c`  
		Last Modified: Tue, 12 Dec 2017 18:47:39 GMT  
		Size: 35.4 MB (35416029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-webprofile` - linux; arm variant v5

```console
$ docker pull tomee@sha256:8c16eca3a7c6946fac8558c8a9bc83131a83809f81aec390af93f144f3b4561a
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231354386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b966df922bc69cc87e48e3d1908f787a679d2b1152a1ac667cc57447011dde34`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 02:52:56 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 02:52:56 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 02:52:56 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56c80a4656a9559ef288034d1ee995a1c9c86800b4254d86ede62cfb4540769`  
		Last Modified: Wed, 13 Dec 2017 02:57:07 GMT  
		Size: 35.4 MB (35416216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-webprofile` - linux; arm variant v7

```console
$ docker pull tomee@sha256:28641a9f2cf77eb7e7695f7cd4e0e807450c76f03e33f393ef0bf4cdde18ed1b
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241861136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ec2e9bf3d4f4a3827d713f68bdd8e37850a94b5e35ecf412c5c64eb4944f0b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 20:10:32 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 20:10:32 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 20:10:32 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7cb13b75fab5cdd77a03767c4105eef80a33426081a322cb87f6d27c271e15`  
		Last Modified: Tue, 12 Dec 2017 20:15:13 GMT  
		Size: 35.4 MB (35416215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:bc6451415e7e17a343130ba5170cb15c255bb8ecb83803f8d71a87f1ad5d3f31
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246604962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22234db7012315f789057f746541a9f96a7f5022412fb37dd53a7774f9e6104d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:34:40 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:34:40 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:34:41 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477492600cb930cdd6fad03b1c70456f3c28fc81997aa25ef365f64576d9e0bc`  
		Last Modified: Sat, 16 Dec 2017 08:40:40 GMT  
		Size: 35.4 MB (35416020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-webprofile` - linux; 386

```console
$ docker pull tomee@sha256:9813c10b797f4a16d26eafbc6307c8b2065dc13aa9bccdeeca7d76beec311815
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266474726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf9cbb02e87ef95486e0888cfb0ded71242c80bbfcfa498a820555512808772`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:58:33 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:59:05 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:59:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15955488db11ea0eda234fcb2d620700c575a27cf2a25bfebc739e23cc8a4b8`  
		Last Modified: Wed, 13 Dec 2017 22:19:18 GMT  
		Size: 35.4 MB (35416026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-webprofile` - linux; ppc64le

```console
$ docker pull tomee@sha256:e5f15a6dcf551ef9198aef894b1b9c33bbc6a5afb6070a354518d9aaf971e010
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253129421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f148f1fed3a3e55583f69210c485439b58a8b90db0e6a552b2be36d208902b6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Tue, 12 Dec 2017 12:14:17 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Tue, 12 Dec 2017 12:14:19 GMT
EXPOSE 8080/tcp
# Tue, 12 Dec 2017 12:14:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e05540576fcbdf343570d599db1392469e7488b220f7eaf40b1c72c5d643f3a`  
		Last Modified: Tue, 12 Dec 2017 12:17:57 GMT  
		Size: 35.4 MB (35416178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.3-webprofile` - linux; s390x

```console
$ docker pull tomee@sha256:1530f316759bfc8358b613e00f22f0986f83d0531171448156ef01c23708d4ec
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234868033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec69da5fa228894a58ab711fb8653dfe01f2dd31ba291c878b5ad74e0e1f6a67`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:19 GMT
ADD file:11704b7d478d6b95a0cfeb557a4a4a03c02fde3849dd3e01da2d1228c6b815f0 in / 
# Mon, 09 Oct 2017 21:44:19 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 16:45:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Nov 2017 22:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2017 22:47:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Nov 2017 22:47:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 Nov 2017 22:47:04 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 Nov 2017 22:47:05 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Sat, 04 Nov 2017 16:56:31 GMT
ENV JAVA_VERSION=8u151
# Sat, 04 Nov 2017 16:56:32 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Sat, 04 Nov 2017 16:56:32 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 04 Nov 2017 16:57:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 16:57:22 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 04 Nov 2017 17:39:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 17:39:06 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 04 Nov 2017 17:39:06 GMT
WORKDIR /usr/local/tomee
# Sat, 04 Nov 2017 17:40:36 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 04 Nov 2017 17:40:51 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 04 Nov 2017 17:43:20 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.3/apache-tomee-7.0.3-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.3/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.3 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 04 Nov 2017 17:43:20 GMT
EXPOSE 8080/tcp
# Sat, 04 Nov 2017 17:43:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6630da1278315ced68910beef5ac605807b880918d11d0c02c4d3eac7307008`  
		Last Modified: Mon, 09 Oct 2017 21:48:41 GMT  
		Size: 45.0 MB (44972760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b5e0a1749d0366c28b4b88ae0139119ba36640fa31f7ed3d2ec974ae1127b`  
		Last Modified: Mon, 09 Oct 2017 22:21:54 GMT  
		Size: 10.7 MB (10667715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4441405fed16180511630210e0428e6a62bd44a3f42a816606844080c8ae600a`  
		Last Modified: Thu, 02 Nov 2017 16:56:23 GMT  
		Size: 4.4 MB (4365981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650969eeff938a3da424993dd865091d3a87cff585865d1e50ddd3f88bbdc81`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 863.1 KB (863064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b48a30ee3de70325a19d84681a4c1b175a747bfc6770658eabb685872f5365`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878fb440e35ac40bd45dd99097a1345db23eda98fa8736a2ae3494937f055936`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f026d0986cd1a555fda1b69c4ede0e372b2db7a1d58f9aafb1bf4e48640c1c`  
		Last Modified: Sat, 04 Nov 2017 17:04:29 GMT  
		Size: 138.2 MB (138242845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e91bc6a3869bec65e58199b5a49cdae6d9ac95ee145a37194947f23af8ff48`  
		Last Modified: Sat, 04 Nov 2017 17:04:08 GMT  
		Size: 272.2 KB (272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ddb28ea1f1b1887617405047c4575b28f682f7a5dca9308f1ba0fe798e8026`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6a97ca5aa576185198e2a4979e5e2f5c0d4c7046d6205f123655443c3209d`  
		Last Modified: Sat, 04 Nov 2017 17:43:33 GMT  
		Size: 66.9 KB (66949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ca11930919f66f33e44509e0ca5db490e78122655990ae154f20c23fd342e`  
		Last Modified: Sat, 04 Nov 2017 17:45:52 GMT  
		Size: 35.4 MB (35416029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.4-plume`

```console
$ docker pull tomee@sha256:f0aefbb619095208c68c7695fad29c17eb6cf7a9386dcdd3d06bb6cdd5d058c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:8-jre-7.0.4-plume` - linux; amd64

```console
$ docker pull tomee@sha256:6fb9b6ef67124d09b8bd2678a10b1a058516708cb029e332cbe9111a12b54757
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290912106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e799f7361d9492cf2128250362c3421b68cbd904ff65ce6e3e08b269d4c14ad`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 17:25:14 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:25:14 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:25:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd50df29c3cebfa9a822739bd92ca403d54dc93546281afe31c1da9b5d08852`  
		Last Modified: Wed, 13 Dec 2017 17:27:07 GMT  
		Size: 63.8 MB (63762171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plume` - linux; arm variant v5

```console
$ docker pull tomee@sha256:6150b15958ac25c884563261b22c35b8d8912c8ad770bc791f23664073db8a37
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259700442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304918736c6836251bd0ce2347b469b8be417b8253fd6c49551be7b0e024f4d6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 20:21:15 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:21:15 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:21:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102033a089488dc75beb39983c96b40c1e6751a82383026f09df644e090be549`  
		Last Modified: Wed, 13 Dec 2017 20:23:28 GMT  
		Size: 63.8 MB (63762272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plume` - linux; arm variant v7

```console
$ docker pull tomee@sha256:662edc377eb8898e75fb98502da8780817acddc579a5936d938f4f73c86934ef
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270207195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907b7bc909a6175339eb574f195f812daac8d628ff6ad04ef83177af05048d5f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 10:14:57 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:14:57 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:14:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102abd45a926769ddd4aee19136ab99277f9fd5449613109dc1358aec24631f`  
		Last Modified: Thu, 14 Dec 2017 10:17:36 GMT  
		Size: 63.8 MB (63762274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plume` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:6eae9cbd4f6ce645738e9fc4a47cf53f6a0907d8f1480c99d6bff7f9d1429233
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274951131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b12a65c18b3f13049e77575362bdd19a3c65607b7841a1146448b27d8c84b6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:34:55 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:34:56 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:34:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeae1143e2c9ff30f206a295c8ed599d7394714a00a1bf7cfbbef881eca4afba`  
		Last Modified: Sat, 16 Dec 2017 08:40:59 GMT  
		Size: 63.8 MB (63762189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plume` - linux; 386

```console
$ docker pull tomee@sha256:02e34a21ef8bcec6f6382c01dc6913bd5a16de39500d94d6c2ebaf853c81b813
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294820858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842daf3fcb2a0048a67e101fc4235aeee5b60b6ab51fde090fd53c27074bd799`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 21:59:41 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 21:59:47 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 21:59:47 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5cd7fede1936ed4a5b8cf64e32d0d0a27b426440d95bbedf4c831741cee6c51`  
		Last Modified: Wed, 13 Dec 2017 22:20:32 GMT  
		Size: 63.8 MB (63762158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plume` - linux; ppc64le

```console
$ docker pull tomee@sha256:1999426bd92d415c7b0f8ef6b9f27b64a0414986de805309b802477b59452f77
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281475572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cd548fc6280025bc454324e2ef2437f110785cfe46a6243ea3e21493e16604`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 00:52:31 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plume.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plume-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plume-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:52:32 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:52:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec5b7e5d2913682d1778dc75bc6a226d5d2e1e63985d0af2403418d159f6475`  
		Last Modified: Thu, 14 Dec 2017 00:55:05 GMT  
		Size: 63.8 MB (63762329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.4-plus`

```console
$ docker pull tomee@sha256:46c8ccaa6d0119e9054dfdc4dad0b5105ca23e3db19f2403d870d9db4362fcdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:8-jre-7.0.4-plus` - linux; amd64

```console
$ docker pull tomee@sha256:2e03f10e177fd6479bebe4e38430b5ad55d3854c574df0f8a6d93da8080ee135
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283945737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c111d6e1fbb1a98243a826c67bcac590dc24ab4c2fab8fe9a0b21951301fc1f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 17:25:26 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:25:26 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:25:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc6b751350b1674b2afaa00749c90bcba3ed5fb3f592f141340444e57501a2b`  
		Last Modified: Wed, 13 Dec 2017 17:27:28 GMT  
		Size: 56.8 MB (56795802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plus` - linux; arm variant v5

```console
$ docker pull tomee@sha256:e27e6ef7ebd4ef3a7fc7b6e4969a0bcfc105fd446e9603740d14e4b1ba88139c
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252734058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ada43e2ba0dd4539caec72d305dc742867ab0465f4cb38d658b8fec54ac4a4b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 20:21:34 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:21:34 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:21:34 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77800734699a09191c644cac27a7dc35a03fd8ccd1ba96e909e8817433085233`  
		Last Modified: Wed, 13 Dec 2017 20:23:48 GMT  
		Size: 56.8 MB (56795888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plus` - linux; arm variant v7

```console
$ docker pull tomee@sha256:96b75fcec887e18a54a18dbc909df35a07282fe84e69766d4aa6f372a3e510ff
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263240781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74894686110f62d06f717b3eb62a8ea75e0471bed086d670d327a773de3e1881`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 10:15:17 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:15:18 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:15:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b81465262384ff3210338b433840711a51cf2536b1111b881116733a8bdeb82`  
		Last Modified: Thu, 14 Dec 2017 10:17:59 GMT  
		Size: 56.8 MB (56795860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:3efa14302d707493b5d00d5f0cb098a39287203886415363de347c22bcb9126d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267984782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16689388eed6dc9d7c7ad1f6c1ac13424f7db5d7202c4889848a45a5e61c50a2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:35:11 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:35:12 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:35:12 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f6af54bab23fdeddd8b658e0e31dd71c7c7e43a8ece602b41100c3c5199c95`  
		Last Modified: Sat, 16 Dec 2017 08:41:16 GMT  
		Size: 56.8 MB (56795840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plus` - linux; 386

```console
$ docker pull tomee@sha256:26e85487e2c918f6f5311d0bc46825c2c60b90372f06c5bf5fe5bac505064966
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287854518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0177bb14ff24b565cde04d857d74e0406e8810d6fdcbcca80e9863b4b7e7725f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 22:00:14 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 22:00:19 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 22:00:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422cf8f1be81dff1ca8cafdc91ecdee6ff4c72231ef0e530c2f19c056cb64952`  
		Last Modified: Wed, 13 Dec 2017 22:21:00 GMT  
		Size: 56.8 MB (56795818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-plus` - linux; ppc64le

```console
$ docker pull tomee@sha256:4f2485f88dda82f4ed0affe92285503c34a5705c4bdea1d79a04201f85476916
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274509129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc56165c7335771c41fd408f2e77dc73e1854a8e1a224dc016d9036f5ecf4fa8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 00:52:48 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-plus.tar.gz -o tomee.tar.gz     && gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-plus-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-plus-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:52:50 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:52:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb3e95909cd9d14a457f755eeac02f63e23fc57c5606b50acb643fb50e5e202`  
		Last Modified: Thu, 14 Dec 2017 00:55:23 GMT  
		Size: 56.8 MB (56795886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:8-jre-7.0.4-webprofile`

```console
$ docker pull tomee@sha256:c0926f193cb13d332ec596bf0314521199184c6513511dacb56fe329f98ec717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:8-jre-7.0.4-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:a971711ce844166367a99706951ac938be08fb86f2a40232aa8170a803fbc505
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267203241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db888c6edb03217f325aef1b684bdb729895b2164d0cafa404204847ec6195ee`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 17:25:36 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:25:36 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:25:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc387e765737a287ec6cce9860182bece48cb8895774c7e65930262eeebb08c`  
		Last Modified: Wed, 13 Dec 2017 17:27:45 GMT  
		Size: 40.1 MB (40053306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-webprofile` - linux; arm variant v5

```console
$ docker pull tomee@sha256:762f5dcf23e97741922aa33ff77276a525ab2c8cd498f1471e099a42c628d5c7
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235991702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb83d9263ca3d9cd789b44cd7f7921bee3d5fec37aa7dc115732b6ff2ed81bf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 20:21:51 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:21:51 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:21:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d26f968f1bc5601336958db173e500bd92f60fe84d28d506176dbf18ccc0ff4`  
		Last Modified: Wed, 13 Dec 2017 20:24:07 GMT  
		Size: 40.1 MB (40053532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-webprofile` - linux; arm variant v7

```console
$ docker pull tomee@sha256:40e6326fbe74694d1c5b70718cd1b941e8786c9ed0a06be115bcd71818bd9978
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246498462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efa45d608dfa620db29a9e6e71f354cbfd4e6ca442e8928359fdb75b0163599`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 10:15:37 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:15:38 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:15:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535d22682a6cb88bae95f20fb362e08365ddc927765f2bb707e00306603109f3`  
		Last Modified: Thu, 14 Dec 2017 10:18:20 GMT  
		Size: 40.1 MB (40053541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-webprofile` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:059180a0b7a80be43a2701a7aeadeb0da0e94b2f0fd5c2d7a517ee66e3bd862e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251242244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992c6b19de362511f703f4e92ddd3b9d1b53b321cbb1d605a419f8313976af25`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:35:25 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:35:26 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:35:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6019b82ba0418ecd05c9625140ca370d2f5ec69ec8e7aa5aefb962beb897cb93`  
		Last Modified: Sat, 16 Dec 2017 08:41:31 GMT  
		Size: 40.1 MB (40053302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-webprofile` - linux; 386

```console
$ docker pull tomee@sha256:da1580a4767a51cce4df8a23262007a0e70acf81f48c4c1ca284ee0dc0181b25
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271111991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3ec9e1dcf4ab3edd77ee219acd8897b1b7f92ea8e6abc0d2f48f67ea89d612`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 22:00:43 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 22:00:50 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 22:00:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093fcfc6534ea853806974814c6b6bf468893190ef359d52b479788007db33ca`  
		Last Modified: Wed, 13 Dec 2017 22:22:42 GMT  
		Size: 40.1 MB (40053291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:8-jre-7.0.4-webprofile` - linux; ppc64le

```console
$ docker pull tomee@sha256:3426240f3122ffca6db8dcd12822f955b93e6075459f036a3dcf50d66b5899d2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257766827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a817254bc2451a42c4af9327688aac83b4af02f9d22d9278021571a63bf427`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 00:53:07 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:53:09 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:53:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a20ad6fa0c3b45e22ee44a7eb59290635d0108df240630108e638ebae653de`  
		Last Modified: Thu, 14 Dec 2017 00:55:40 GMT  
		Size: 40.1 MB (40053584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:latest`

```console
$ docker pull tomee@sha256:c0926f193cb13d332ec596bf0314521199184c6513511dacb56fe329f98ec717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `tomee:latest` - linux; amd64

```console
$ docker pull tomee@sha256:a971711ce844166367a99706951ac938be08fb86f2a40232aa8170a803fbc505
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267203241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db888c6edb03217f325aef1b684bdb729895b2164d0cafa404204847ec6195ee`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:20 GMT
ADD file:eb2519421c9794ccc99d483c07f59ba305531bc9b4dc294e74d2ddb7de69e52a in / 
# Tue, 12 Dec 2017 01:44:21 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:54:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:16:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:16:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:16:25 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:16:26 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:16:26 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:17:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:17:36 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 18:37:20 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 18:37:21 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 18:37:21 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 18:39:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 18:39:35 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 17:25:36 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 17:25:36 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 17:25:36 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:723254a2c089166d4bcfa917be0181ddbecd94971ebfe85792d96e7e29be9c68`  
		Last Modified: Tue, 12 Dec 2017 01:53:22 GMT  
		Size: 45.1 MB (45121631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe15a44e12f84b4aac20d4f2b450ec8638cc0b176c9130d1802cb4fed17d953`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 11.1 MB (11107352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409a28e3cc3de08700c9d37c809a6d3aa43dc076402943919f4a78c286c60a0b`  
		Last Modified: Tue, 12 Dec 2017 08:03:48 GMT  
		Size: 4.3 MB (4335420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9511c68044accc89061e19e40356126f629c1e3ace2ef524b0e3f02e64e6b10`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 852.3 KB (852274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1b16e30bc84a10c110be2c4f0a35dce542c7d55869cf2f99b7753763aabdb1`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a09c924277c26642af87cc8a057633582a6fb462141245d46a638d0f8cf5`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34976006493631a54114beee079e51dd165df33f8f5ebfc04b0eeb12613bedb`  
		Last Modified: Tue, 12 Dec 2017 16:20:31 GMT  
		Size: 165.4 MB (165393574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b70003f0c1097e6b4f30f66e223ce759edec1331f5c1a4569e24ce8f4d41632`  
		Last Modified: Tue, 12 Dec 2017 16:19:57 GMT  
		Size: 272.2 KB (272151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65c4698577e3e4dd9ee9a7407728288478ba7b1855749830b2a67a21bb6f1b`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c174c9e4ec54b34c66afe38f60c85abf32e6cc1da0e8fa6d7be4e007ecaf1c8c`  
		Last Modified: Tue, 12 Dec 2017 18:43:24 GMT  
		Size: 67.0 KB (67005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc387e765737a287ec6cce9860182bece48cb8895774c7e65930262eeebb08c`  
		Last Modified: Wed, 13 Dec 2017 17:27:45 GMT  
		Size: 40.1 MB (40053306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:latest` - linux; arm variant v5

```console
$ docker pull tomee@sha256:762f5dcf23e97741922aa33ff77276a525ab2c8cd498f1471e099a42c628d5c7
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235991702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb83d9263ca3d9cd789b44cd7f7921bee3d5fec37aa7dc115732b6ff2ed81bf`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 21:01:46 GMT
ADD file:f8517f9f02293861c50bd41f708eb4f907ae9a1d2f9b6c917602b677f174fbc0 in / 
# Tue, 12 Dec 2017 21:01:46 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:59:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:36:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:36:43 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:36:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:36:44 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 23:36:45 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 23:36:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 23:37:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 23:37:49 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 02:45:31 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 02:45:32 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 02:45:33 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 02:48:31 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 02:48:56 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 20:21:51 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 20:21:51 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 20:21:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b858507a828940bb4f637f38191bc4c62a00a6857fcddefc11c003815277c27d`  
		Last Modified: Tue, 12 Dec 2017 21:11:55 GMT  
		Size: 43.8 MB (43809184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74be0ad93d15611aa7313f4b3b2f81efdd2d1cebe0f55d451508e2c2e4f7d55e`  
		Last Modified: Tue, 12 Dec 2017 23:10:09 GMT  
		Size: 10.2 MB (10205777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f61dac7c9bed094566a8a214c493eee51438fae13aa7858d076f887bd66e84`  
		Last Modified: Tue, 12 Dec 2017 23:10:07 GMT  
		Size: 4.2 MB (4153069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9804479cf1e639741aa254ac81a4015289b2fd29e0f96fb11399f3da4eb5f2a6`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 845.3 KB (845258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5bbca10dd29a270431be20cd28bd556f35a383ca261185cce461464e07c52`  
		Last Modified: Tue, 12 Dec 2017 23:55:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004b0dad62c3ce0fa38525e55815be655eec6ddf2cb4b424b5be78083703c68`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e9f3476e4dec79e3bc4fee88e47e73aa4a1d03089a7afbf86876e9c4abc63`  
		Last Modified: Tue, 12 Dec 2017 23:56:19 GMT  
		Size: 136.6 MB (136585086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079713298db36f47023a35e01ec24e350b977194d7f4920a5510b78ea95d2242`  
		Last Modified: Tue, 12 Dec 2017 23:55:44 GMT  
		Size: 272.2 KB (272193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c039eb40c1b02c297cb904c22aebb217dc90bf026cb6b6c2f2b5d5f643e8fd1`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b6de1a17b8c8d3740d736687e6bec31935612dd35b869161a9a49ceb32bb0`  
		Last Modified: Wed, 13 Dec 2017 02:53:11 GMT  
		Size: 67.0 KB (67041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d26f968f1bc5601336958db173e500bd92f60fe84d28d506176dbf18ccc0ff4`  
		Last Modified: Wed, 13 Dec 2017 20:24:07 GMT  
		Size: 40.1 MB (40053532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:latest` - linux; arm variant v7

```console
$ docker pull tomee@sha256:40e6326fbe74694d1c5b70718cd1b941e8786c9ed0a06be115bcd71818bd9978
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246498462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efa45d608dfa620db29a9e6e71f354cbfd4e6ca442e8928359fdb75b0163599`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 13:32:59 GMT
ADD file:d49e67cdc6ae27f43c5c002d96bff764fd43188dd7e8036f5d5f8c44eb12dcad in / 
# Tue, 12 Dec 2017 13:32:59 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:21:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:17:47 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:17:48 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:17:49 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 15:17:50 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 15:17:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 15:18:38 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 15:18:41 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 20:02:00 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 20:02:01 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 20:02:01 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 20:04:54 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 20:05:29 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 10:15:37 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 10:15:38 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 10:15:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0e10ef01c84000f6f5865b480436e689e2d437a4a8b63b01d5ce85532872b636`  
		Last Modified: Tue, 12 Dec 2017 13:44:34 GMT  
		Size: 41.8 MB (41849695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed40614ea2a08dbc6237155db97d58d7051efa214bab1fd556c4414db68cb7c`  
		Last Modified: Tue, 12 Dec 2017 14:34:18 GMT  
		Size: 9.8 MB (9824565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ea8727ac09b97803f430b101f4c67cbf9c7bc372a44c190f5a9719f5fb1e9`  
		Last Modified: Tue, 12 Dec 2017 14:34:16 GMT  
		Size: 3.9 MB (3912457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e19d2e402a95ffb0b0b26518934225f625f543f50bc37297dd2162a15be3`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 829.7 KB (829674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef58246d333ca0dca1acc2153268c6140ee89ca45aa6c1c65365e081a55fbb7`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a85ac361d453f46d538411d80979e7e719231a04266dfaaf6c320b73abf7f`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa9dcb950c7711e156b24161dfbab83fb85330261b6d8ef7321be4253b880e9`  
		Last Modified: Tue, 12 Dec 2017 15:36:00 GMT  
		Size: 149.7 MB (149688872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3cf1155796a26a9f16b6d0c99d3204c229710eed6a75994501c95d9591319b`  
		Last Modified: Tue, 12 Dec 2017 15:35:22 GMT  
		Size: 272.1 KB (272068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02e1b500be586f27d077d73b22de5a4d2af08f5544c66bb057696e20241a10d`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556a38048131b41fdce3acf67e478a4d46d51c0592916c286be1992afd346321`  
		Last Modified: Tue, 12 Dec 2017 20:10:51 GMT  
		Size: 67.0 KB (67029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535d22682a6cb88bae95f20fb362e08365ddc927765f2bb707e00306603109f3`  
		Last Modified: Thu, 14 Dec 2017 10:18:20 GMT  
		Size: 40.1 MB (40053541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:latest` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:059180a0b7a80be43a2701a7aeadeb0da0e94b2f0fd5c2d7a517ee66e3bd862e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251242244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992c6b19de362511f703f4e92ddd3b9d1b53b321cbb1d605a419f8313976af25`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 18:33:14 GMT
ADD file:ae07a2e0bd59c986cf9cec3d7ce9a3db8f8034bac7b69938557e472980c70cdc in / 
# Tue, 12 Dec 2017 18:33:14 GMT
CMD ["bash"]
# Fri, 15 Dec 2017 16:14:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 16:14:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 20:58:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 20:58:37 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 20:58:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 20:58:41 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 20:58:42 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 20:58:43 GMT
ENV JAVA_VERSION=8u151
# Fri, 15 Dec 2017 20:58:44 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 15 Dec 2017 20:58:45 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 15 Dec 2017 21:04:54 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 15 Dec 2017 21:05:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 16 Dec 2017 08:29:05 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2017 08:29:07 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 16 Dec 2017 08:29:08 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2017 08:31:27 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Sat, 16 Dec 2017 08:31:39 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Sat, 16 Dec 2017 08:35:25 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Sat, 16 Dec 2017 08:35:26 GMT
EXPOSE 8080/tcp
# Sat, 16 Dec 2017 08:35:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:91ea0aed359111bf5beb30e4bebd50fac25bc40a69e1bb3bf0f8e3c6dcd5fa7f`  
		Last Modified: Tue, 12 Dec 2017 18:47:08 GMT  
		Size: 42.9 MB (42912813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2797c29bc6ab5e2ad91b16dea60d7b6f0d4fffb5261f539870b43a7ffca40e`  
		Last Modified: Fri, 15 Dec 2017 17:19:24 GMT  
		Size: 10.1 MB (10066285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edcd3d8093caa7ca86f40f4413c1ae7ca97ae1480289f06339fff174a2a7d6a`  
		Last Modified: Fri, 15 Dec 2017 17:19:21 GMT  
		Size: 4.1 MB (4087788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f31246b5599b4756f87191a766804687d5f15a88e38a5b108d7613423ab64c8`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 838.6 KB (838563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84785722d48b3ef39cace79c620140140e100cce300e268f5270d590e3f27e3d`  
		Last Modified: Fri, 15 Dec 2017 21:22:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958399e00727fffe5a1dfdd3f64b57aa5d3146002cda35d3ce71e21759e90af2`  
		Last Modified: Fri, 15 Dec 2017 21:22:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea374b82a560199da7b95231208f6c3fa2a26e756c9b0d38810372fa085599b`  
		Last Modified: Fri, 15 Dec 2017 21:23:31 GMT  
		Size: 152.9 MB (152943803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada60257965e0220f59accda053fdc32841d2f63b4890e56d892b2c287c5fe0b`  
		Last Modified: Fri, 15 Dec 2017 21:22:48 GMT  
		Size: 272.1 KB (272148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a6e4aca8e89f363ebae042b689a9bc0e718c677b458aa9de32f0c440969cd`  
		Last Modified: Sat, 16 Dec 2017 08:35:41 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61810bf7da657c582b8e4aa922b738b937f78f891f16a382d14c011f187f157d`  
		Last Modified: Sat, 16 Dec 2017 08:37:16 GMT  
		Size: 67.0 KB (67013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6019b82ba0418ecd05c9625140ca370d2f5ec69ec8e7aa5aefb962beb897cb93`  
		Last Modified: Sat, 16 Dec 2017 08:41:31 GMT  
		Size: 40.1 MB (40053302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:latest` - linux; 386

```console
$ docker pull tomee@sha256:da1580a4767a51cce4df8a23262007a0e70acf81f48c4c1ca284ee0dc0181b25
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271111991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3ec9e1dcf4ab3edd77ee219acd8897b1b7f92ea8e6abc0d2f48f67ea89d612`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 14:28:39 GMT
ADD file:a6cfca6b73e41be73fc4e964d25ccb94f9c3538d1bd6623f5f203d3594167a5f in / 
# Tue, 12 Dec 2017 14:28:39 GMT
CMD ["bash"]
# Wed, 13 Dec 2017 14:45:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 14:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Dec 2017 15:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2017 15:21:28 GMT
ENV LANG=C.UTF-8
# Wed, 13 Dec 2017 15:21:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Wed, 13 Dec 2017 15:21:30 GMT
ENV JAVA_VERSION=8u151
# Wed, 13 Dec 2017 15:21:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Wed, 13 Dec 2017 15:21:31 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Wed, 13 Dec 2017 15:22:49 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Wed, 13 Dec 2017 15:22:52 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Wed, 13 Dec 2017 21:44:54 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Dec 2017 21:44:55 GMT
RUN mkdir -p /usr/local/tomee
# Wed, 13 Dec 2017 21:44:55 GMT
WORKDIR /usr/local/tomee
# Wed, 13 Dec 2017 21:48:13 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Wed, 13 Dec 2017 21:48:24 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Wed, 13 Dec 2017 22:00:43 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Wed, 13 Dec 2017 22:00:50 GMT
EXPOSE 8080/tcp
# Wed, 13 Dec 2017 22:00:50 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:50d72515450fee13bee4f8be703ed400c6fc2f1bc9a5699f1d6917eb6dde6aa0`  
		Last Modified: Tue, 12 Dec 2017 15:01:52 GMT  
		Size: 45.8 MB (45827066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9ff72840f920dca068cca81368ea4b369a74d6ec40929d4cb4a6b4e6d2264`  
		Last Modified: Wed, 13 Dec 2017 14:58:26 GMT  
		Size: 11.2 MB (11150413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e33c1d09c88921e13b6b46cc0476040037bbe57b669dbbc9d16f17cde6298`  
		Last Modified: Wed, 13 Dec 2017 14:58:25 GMT  
		Size: 4.6 MB (4554619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9934e17bca1f4fdf8114e6baf80eb11eb18b0d425c8568b35fac04d2913dee5`  
		Last Modified: Wed, 13 Dec 2017 15:40:37 GMT  
		Size: 861.1 KB (861149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f54df81eda17ba5ce500a3bbd23abd9db02eb57b697611b88f6249bb15cdfd`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ba1f721572ed69c9b8af65e4025129031d6cc4cf7aceb610cd20f66310723a`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b226ae3de1d490bbc8f2cc5f9fa5f67d1b6a38b6c12f8b43f2e6e1ebc5865`  
		Last Modified: Wed, 13 Dec 2017 15:41:29 GMT  
		Size: 168.3 MB (168325773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f9e2d852693f2983e4d5ff8d80cdb2479dccaa6679adea10c6f53c6dd8e76`  
		Last Modified: Wed, 13 Dec 2017 15:40:36 GMT  
		Size: 272.1 KB (272145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66410009a8afe148fcd3895837876efe95fff3b5e53f9dfbd3725cc575d4acff`  
		Last Modified: Wed, 13 Dec 2017 22:01:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9ed087c729d01ef4df468927de7a227b02924a054f7ca1811c5937f7d1817`  
		Last Modified: Wed, 13 Dec 2017 22:03:31 GMT  
		Size: 67.0 KB (67008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093fcfc6534ea853806974814c6b6bf468893190ef359d52b479788007db33ca`  
		Last Modified: Wed, 13 Dec 2017 22:22:42 GMT  
		Size: 40.1 MB (40053291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:latest` - linux; ppc64le

```console
$ docker pull tomee@sha256:3426240f3122ffca6db8dcd12822f955b93e6075459f036a3dcf50d66b5899d2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257766827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a817254bc2451a42c4af9327688aac83b4af02f9d22d9278021571a63bf427`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Dec 2017 01:35:21 GMT
ADD file:10937e86e38fefbf07c9463d2a6837b8404e73135bac36166b7b585c2f8e6359 in / 
# Tue, 12 Dec 2017 01:35:23 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:32:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 04:00:06 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 04:00:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 04:00:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 04:00:17 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 04:00:19 GMT
ENV JAVA_VERSION=8u151
# Tue, 12 Dec 2017 04:00:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 12 Dec 2017 04:00:23 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 12 Dec 2017 04:08:05 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 12 Dec 2017 04:08:11 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 12 Dec 2017 12:07:26 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2017 12:07:29 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 12 Dec 2017 12:07:31 GMT
WORKDIR /usr/local/tomee
# Tue, 12 Dec 2017 12:09:23 GMT
ENV GPG_KEYS=223D3A74B068ECA354DC385CE126833F9CF64915     678F2D98F1FD9643811639FB622B8F2D043F71D8     7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF     82D8419BA697F0E7FB85916EE91287822FDB81B1     9056B710F1E332780DE7AF34CBAEBE39A46C4CA1     A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1     B7574789F5018690043E6DD9C212662E12F3E1DD     B8B301E6105DF628076BD92C5483E55897ABD9B9     BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF     C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1     D11DF12CC2CA4894BDE638B967C1227A2678363C     DBCCD103B8B24F86FFAAB025C8BB472CD297D428     F067B8140F5DD80E1D3B5D92318242FE9A0B1183     FAA603D58B1BA4EDF65896D0ED340E0E6D545F97
# Tue, 12 Dec 2017 12:09:46 GMT
RUN set -xe     && for key in $GPG_KEYS; do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";     done
# Thu, 14 Dec 2017 00:53:07 GMT
RUN set -x 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz.asc -o tomee.tar.gz.asc 	&& curl -fSL https://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/7.0.4/apache-tomee-7.0.4-webprofile.tar.gz -o tomee.tar.gz 	&& gpg --batch --verify tomee.tar.gz.asc tomee.tar.gz 	&& tar -zxf tomee.tar.gz 	&& mv apache-tomee-webprofile-7.0.4/* /usr/local/tomee 	&& rm -Rf apache-tomee-webprofile-7.0.4 	&& rm bin/*.bat 	&& rm tomee.tar.gz*
# Thu, 14 Dec 2017 00:53:09 GMT
EXPOSE 8080/tcp
# Thu, 14 Dec 2017 00:53:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5427ba9c78c891da38836ae1e71d1f22cd1a75cae9cd5a7e1fc55e9b577e3517`  
		Last Modified: Tue, 12 Dec 2017 01:42:09 GMT  
		Size: 45.4 MB (45382357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c378a191e90f6d5b2a6f6d9850e8c81ea101737db5c068add4c764f2be3aced2`  
		Last Modified: Tue, 12 Dec 2017 03:55:34 GMT  
		Size: 10.3 MB (10339336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26b1cf177268cff23511322d11143dadc3f4326448d8aceedad9b759e57fb13`  
		Last Modified: Tue, 12 Dec 2017 03:55:32 GMT  
		Size: 4.3 MB (4289552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af22b7dd73b6bcf8874439d5b51e724084ca8aec7f568e47b43f55f43230cd`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 848.1 KB (848134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee542cd2f561e879deb9b66f2865f027eaccf879127bd9d4b300a1bc24bf4f76`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c114de097cab155446e90fbe0e0d89977a44fa271b233dd158bfcc37377649bc`  
		Last Modified: Tue, 12 Dec 2017 04:21:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5934bdea1bb5f4e8fdaa7e56ff3c98f85002bbbea995ba49d7a11725269f16b3`  
		Last Modified: Tue, 12 Dec 2017 04:22:33 GMT  
		Size: 156.5 MB (156514184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b19418383bf1d4546c68d2a9acb38b8cc70feba384be8539deefb8ca443357`  
		Last Modified: Tue, 12 Dec 2017 04:21:53 GMT  
		Size: 272.1 KB (272071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12e60c642f959d147da9473e9dfe4f9e610cf6798cbaae11294dc62d4f648a4`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59d62fe5312ac5ba4f722546e45da24ca5a6ad378c03e6a7cee2ba7bfe237f2`  
		Last Modified: Tue, 12 Dec 2017 12:14:35 GMT  
		Size: 67.0 KB (67048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a20ad6fa0c3b45e22ee44a7eb59290635d0108df240630108e638ebae653de`  
		Last Modified: Thu, 14 Dec 2017 00:55:40 GMT  
		Size: 40.1 MB (40053584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
