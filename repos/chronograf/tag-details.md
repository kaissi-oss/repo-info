<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.3`](#chronograf13)
-	[`chronograf:1.3.10`](#chronograf1310)
-	[`chronograf:1.3.10.0`](#chronograf13100)
-	[`chronograf:1.3.10.0-alpine`](#chronograf13100-alpine)
-	[`chronograf:1.3.10-alpine`](#chronograf1310-alpine)
-	[`chronograf:1.3-alpine`](#chronograf13-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.3`

```console
$ docker pull chronograf@sha256:8dd84876dfd91071011e7b344cb37d33d24d8f28049f4a53984d4dac37fd5ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.3` - linux; amd64

```console
$ docker pull chronograf@sha256:9445d6ed17ccad986247c9e70311d6c0bec9535c08fbdb807525a6696ea85017
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40312884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b2cd38520b58350df56fda93ae4e7644ace2e80df08ce60e2c738bc8d8179`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:43 GMT
ADD file:f30a8b5b7cdc9ba33a250899308b490baa9f7a9b29d3a85bd16200aa0a28a04a in / 
# Tue, 12 Dec 2017 01:44:43 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:56:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 03:56:53 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 03:57:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 03:57:04 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 03:57:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 03:57:05 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 03:57:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 03:57:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e7bb522d92ff6d4e5b2087409b0fc783c2e3b06acf87bee739ee47d90bf02e96`  
		Last Modified: Tue, 12 Dec 2017 01:54:56 GMT  
		Size: 22.5 MB (22485719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4d5c79d105adf7ea85108c1b312525f1c0ca344849101a049b1a067118636`  
		Last Modified: Tue, 12 Dec 2017 03:57:23 GMT  
		Size: 4.5 MB (4500164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653796862543b972fa1bd521d5272ddd10ea2f57a8533fd456840cfb44803862`  
		Last Modified: Tue, 12 Dec 2017 03:57:25 GMT  
		Size: 13.3 MB (13302605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d38f6d9d5133110f5833780a4a70f47026861df02a46b644af24288abf95d`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab31c9630ae82ce9df09223bdc5097c7416f2ebf5a101e638c08f30fa3f853a`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebfd0e2b07e68c7c3d76c17dcd8e6549826e893b851e0a2b440d1d8bc9d2330`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.3` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:02523412e9d023db715bf6f0d2bb47b13172d4cf23efa709657be56d2071eaf5
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35119379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c7f267f4c8bef0d4827df02a9eb3bee15d57c86f03787221a9eb64c9bd789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 13:33:42 GMT
ADD file:cfde12259adb7102e76690e986f1b9b07967a8984c85d0cead09969f5de8b8cc in / 
# Tue, 12 Dec 2017 13:33:42 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:06:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 14:06:40 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 14:06:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 14:07:01 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 14:07:11 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 14:07:20 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 14:07:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 14:07:21 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 14:07:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 14:07:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cd8b673adb84fd5eae3444d0475addad7e8908a8332704c4407baa97e9b0b284`  
		Last Modified: Tue, 12 Dec 2017 13:45:48 GMT  
		Size: 19.3 MB (19271028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90883f0b035a290249b13586f6f13f71096b60164a943d952ecda1e1efefc280`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 3.9 MB (3873001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939c27a4aaf65412f1640cdd0d3516ac7684c2125e6baa97329bcdb2f63632c1`  
		Last Modified: Tue, 12 Dec 2017 14:08:00 GMT  
		Size: 12.0 MB (11950950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2b291da09e5d23b21ebed513b5a8726e63dda1881f14ee6e23b582be1e585`  
		Last Modified: Tue, 12 Dec 2017 14:07:58 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5822037666784aae813617fd22e9c5509817892c745a0097f3c9489470459850`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73844d296577499389dc8a63175971dfb1806b60b75053a9f22802c7b588e43b`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.3` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1580944e14eb1f38b61ebf4c53f0d5c9b6df437486c6e706459a07ccd3874b80
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36580061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a7d863f44f362d04d1c904884349dfa6f4baba5d472d1d4d58f26b473ebb88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 18:34:13 GMT
ADD file:6e068c7cc5397bfb4ec60dab4d410c5d3ba724f20ad0129d2032fb509f0eadcd in / 
# Tue, 12 Dec 2017 18:34:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2017 23:21:57 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2017 23:21:57 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 19 Dec 2017 23:22:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2017 23:22:28 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2017 23:22:29 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2017 23:22:30 GMT
EXPOSE 8888/tcp
# Tue, 19 Dec 2017 23:22:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2017 23:22:32 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 19 Dec 2017 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2017 23:22:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcad8cfc11c78a53ccf9aafafcb3ded5044dbd181977e6255aea54fbe164f131`  
		Last Modified: Tue, 12 Dec 2017 18:49:05 GMT  
		Size: 20.3 MB (20331270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779229a74f0249d7f5a79cedc25be77365759cfd785b2c183b324862baaeeeb6`  
		Last Modified: Tue, 19 Dec 2017 23:22:52 GMT  
		Size: 4.1 MB (4074975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9eb2d7d4a74cc21ed39d440b27c2579551acd5a4ec964378499c6daa557fff`  
		Last Modified: Tue, 19 Dec 2017 23:22:55 GMT  
		Size: 12.1 MB (12149422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ec21ee5d0a5f84c40c9aecea361640ac7c0a101affc5f2ca5a8d1990eb2ccf`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0e9c0167abe1cdfed41b1f3bac607f440a62bb0c5be008df518556fba88111`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c083190db174f7feede62b3fe87c0bd6e2af64447e221eac24dcdb551ad6e6`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.3.10`

```console
$ docker pull chronograf@sha256:8dd84876dfd91071011e7b344cb37d33d24d8f28049f4a53984d4dac37fd5ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.3.10` - linux; amd64

```console
$ docker pull chronograf@sha256:9445d6ed17ccad986247c9e70311d6c0bec9535c08fbdb807525a6696ea85017
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40312884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b2cd38520b58350df56fda93ae4e7644ace2e80df08ce60e2c738bc8d8179`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:43 GMT
ADD file:f30a8b5b7cdc9ba33a250899308b490baa9f7a9b29d3a85bd16200aa0a28a04a in / 
# Tue, 12 Dec 2017 01:44:43 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:56:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 03:56:53 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 03:57:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 03:57:04 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 03:57:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 03:57:05 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 03:57:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 03:57:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e7bb522d92ff6d4e5b2087409b0fc783c2e3b06acf87bee739ee47d90bf02e96`  
		Last Modified: Tue, 12 Dec 2017 01:54:56 GMT  
		Size: 22.5 MB (22485719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4d5c79d105adf7ea85108c1b312525f1c0ca344849101a049b1a067118636`  
		Last Modified: Tue, 12 Dec 2017 03:57:23 GMT  
		Size: 4.5 MB (4500164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653796862543b972fa1bd521d5272ddd10ea2f57a8533fd456840cfb44803862`  
		Last Modified: Tue, 12 Dec 2017 03:57:25 GMT  
		Size: 13.3 MB (13302605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d38f6d9d5133110f5833780a4a70f47026861df02a46b644af24288abf95d`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab31c9630ae82ce9df09223bdc5097c7416f2ebf5a101e638c08f30fa3f853a`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebfd0e2b07e68c7c3d76c17dcd8e6549826e893b851e0a2b440d1d8bc9d2330`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.3.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:02523412e9d023db715bf6f0d2bb47b13172d4cf23efa709657be56d2071eaf5
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35119379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c7f267f4c8bef0d4827df02a9eb3bee15d57c86f03787221a9eb64c9bd789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 13:33:42 GMT
ADD file:cfde12259adb7102e76690e986f1b9b07967a8984c85d0cead09969f5de8b8cc in / 
# Tue, 12 Dec 2017 13:33:42 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:06:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 14:06:40 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 14:06:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 14:07:01 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 14:07:11 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 14:07:20 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 14:07:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 14:07:21 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 14:07:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 14:07:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cd8b673adb84fd5eae3444d0475addad7e8908a8332704c4407baa97e9b0b284`  
		Last Modified: Tue, 12 Dec 2017 13:45:48 GMT  
		Size: 19.3 MB (19271028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90883f0b035a290249b13586f6f13f71096b60164a943d952ecda1e1efefc280`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 3.9 MB (3873001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939c27a4aaf65412f1640cdd0d3516ac7684c2125e6baa97329bcdb2f63632c1`  
		Last Modified: Tue, 12 Dec 2017 14:08:00 GMT  
		Size: 12.0 MB (11950950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2b291da09e5d23b21ebed513b5a8726e63dda1881f14ee6e23b582be1e585`  
		Last Modified: Tue, 12 Dec 2017 14:07:58 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5822037666784aae813617fd22e9c5509817892c745a0097f3c9489470459850`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73844d296577499389dc8a63175971dfb1806b60b75053a9f22802c7b588e43b`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.3.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1580944e14eb1f38b61ebf4c53f0d5c9b6df437486c6e706459a07ccd3874b80
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36580061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a7d863f44f362d04d1c904884349dfa6f4baba5d472d1d4d58f26b473ebb88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 18:34:13 GMT
ADD file:6e068c7cc5397bfb4ec60dab4d410c5d3ba724f20ad0129d2032fb509f0eadcd in / 
# Tue, 12 Dec 2017 18:34:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2017 23:21:57 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2017 23:21:57 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 19 Dec 2017 23:22:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2017 23:22:28 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2017 23:22:29 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2017 23:22:30 GMT
EXPOSE 8888/tcp
# Tue, 19 Dec 2017 23:22:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2017 23:22:32 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 19 Dec 2017 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2017 23:22:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcad8cfc11c78a53ccf9aafafcb3ded5044dbd181977e6255aea54fbe164f131`  
		Last Modified: Tue, 12 Dec 2017 18:49:05 GMT  
		Size: 20.3 MB (20331270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779229a74f0249d7f5a79cedc25be77365759cfd785b2c183b324862baaeeeb6`  
		Last Modified: Tue, 19 Dec 2017 23:22:52 GMT  
		Size: 4.1 MB (4074975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9eb2d7d4a74cc21ed39d440b27c2579551acd5a4ec964378499c6daa557fff`  
		Last Modified: Tue, 19 Dec 2017 23:22:55 GMT  
		Size: 12.1 MB (12149422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ec21ee5d0a5f84c40c9aecea361640ac7c0a101affc5f2ca5a8d1990eb2ccf`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0e9c0167abe1cdfed41b1f3bac607f440a62bb0c5be008df518556fba88111`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c083190db174f7feede62b3fe87c0bd6e2af64447e221eac24dcdb551ad6e6`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.3.10.0`

```console
$ docker pull chronograf@sha256:8dd84876dfd91071011e7b344cb37d33d24d8f28049f4a53984d4dac37fd5ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.3.10.0` - linux; amd64

```console
$ docker pull chronograf@sha256:9445d6ed17ccad986247c9e70311d6c0bec9535c08fbdb807525a6696ea85017
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40312884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b2cd38520b58350df56fda93ae4e7644ace2e80df08ce60e2c738bc8d8179`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:43 GMT
ADD file:f30a8b5b7cdc9ba33a250899308b490baa9f7a9b29d3a85bd16200aa0a28a04a in / 
# Tue, 12 Dec 2017 01:44:43 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:56:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 03:56:53 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 03:57:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 03:57:04 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 03:57:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 03:57:05 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 03:57:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 03:57:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e7bb522d92ff6d4e5b2087409b0fc783c2e3b06acf87bee739ee47d90bf02e96`  
		Last Modified: Tue, 12 Dec 2017 01:54:56 GMT  
		Size: 22.5 MB (22485719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4d5c79d105adf7ea85108c1b312525f1c0ca344849101a049b1a067118636`  
		Last Modified: Tue, 12 Dec 2017 03:57:23 GMT  
		Size: 4.5 MB (4500164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653796862543b972fa1bd521d5272ddd10ea2f57a8533fd456840cfb44803862`  
		Last Modified: Tue, 12 Dec 2017 03:57:25 GMT  
		Size: 13.3 MB (13302605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d38f6d9d5133110f5833780a4a70f47026861df02a46b644af24288abf95d`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab31c9630ae82ce9df09223bdc5097c7416f2ebf5a101e638c08f30fa3f853a`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebfd0e2b07e68c7c3d76c17dcd8e6549826e893b851e0a2b440d1d8bc9d2330`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.3.10.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:02523412e9d023db715bf6f0d2bb47b13172d4cf23efa709657be56d2071eaf5
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35119379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c7f267f4c8bef0d4827df02a9eb3bee15d57c86f03787221a9eb64c9bd789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 13:33:42 GMT
ADD file:cfde12259adb7102e76690e986f1b9b07967a8984c85d0cead09969f5de8b8cc in / 
# Tue, 12 Dec 2017 13:33:42 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:06:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 14:06:40 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 14:06:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 14:07:01 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 14:07:11 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 14:07:20 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 14:07:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 14:07:21 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 14:07:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 14:07:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cd8b673adb84fd5eae3444d0475addad7e8908a8332704c4407baa97e9b0b284`  
		Last Modified: Tue, 12 Dec 2017 13:45:48 GMT  
		Size: 19.3 MB (19271028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90883f0b035a290249b13586f6f13f71096b60164a943d952ecda1e1efefc280`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 3.9 MB (3873001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939c27a4aaf65412f1640cdd0d3516ac7684c2125e6baa97329bcdb2f63632c1`  
		Last Modified: Tue, 12 Dec 2017 14:08:00 GMT  
		Size: 12.0 MB (11950950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2b291da09e5d23b21ebed513b5a8726e63dda1881f14ee6e23b582be1e585`  
		Last Modified: Tue, 12 Dec 2017 14:07:58 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5822037666784aae813617fd22e9c5509817892c745a0097f3c9489470459850`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73844d296577499389dc8a63175971dfb1806b60b75053a9f22802c7b588e43b`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.3.10.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1580944e14eb1f38b61ebf4c53f0d5c9b6df437486c6e706459a07ccd3874b80
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36580061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a7d863f44f362d04d1c904884349dfa6f4baba5d472d1d4d58f26b473ebb88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 18:34:13 GMT
ADD file:6e068c7cc5397bfb4ec60dab4d410c5d3ba724f20ad0129d2032fb509f0eadcd in / 
# Tue, 12 Dec 2017 18:34:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2017 23:21:57 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2017 23:21:57 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 19 Dec 2017 23:22:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2017 23:22:28 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2017 23:22:29 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2017 23:22:30 GMT
EXPOSE 8888/tcp
# Tue, 19 Dec 2017 23:22:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2017 23:22:32 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 19 Dec 2017 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2017 23:22:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcad8cfc11c78a53ccf9aafafcb3ded5044dbd181977e6255aea54fbe164f131`  
		Last Modified: Tue, 12 Dec 2017 18:49:05 GMT  
		Size: 20.3 MB (20331270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779229a74f0249d7f5a79cedc25be77365759cfd785b2c183b324862baaeeeb6`  
		Last Modified: Tue, 19 Dec 2017 23:22:52 GMT  
		Size: 4.1 MB (4074975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9eb2d7d4a74cc21ed39d440b27c2579551acd5a4ec964378499c6daa557fff`  
		Last Modified: Tue, 19 Dec 2017 23:22:55 GMT  
		Size: 12.1 MB (12149422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ec21ee5d0a5f84c40c9aecea361640ac7c0a101affc5f2ca5a8d1990eb2ccf`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0e9c0167abe1cdfed41b1f3bac607f440a62bb0c5be008df518556fba88111`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c083190db174f7feede62b3fe87c0bd6e2af64447e221eac24dcdb551ad6e6`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.3.10.0-alpine`

```console
$ docker pull chronograf@sha256:61181dd78667f32c2f46259dc3e33715b9a19a14595b8e98024383c979d08360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.3.10.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6d0c1e8bcca576d14d6ee4d328b949bbd7bd649d72b960dc1dcc451bc3779f30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8408999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09f0a8b407f4890d03765dfe26414c2ab8f540f0d35cab50135f9fafc94f242`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:26 GMT
ADD file:cb381165dec3689cf77e902c07ea78ca4da6bce4f5ac1909eebd40dba3273bfe in / 
# Fri, 01 Dec 2017 18:46:26 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2017 19:57:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2017 19:57:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2017 19:57:15 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Fri, 01 Dec 2017 19:57:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:bb4b392707bfb4ca737581b240f672796f5744c7220fea711a5d1f669992b912 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2017 19:57:27 GMT
EXPOSE 8888/tcp
# Fri, 01 Dec 2017 19:57:27 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2017 19:57:27 GMT
COPY file:70420cc587871e64a3833c5e0724565624ad66205b4febab38c9c37f93a25e28 in /entrypoint.sh 
# Fri, 01 Dec 2017 19:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2017 19:57:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1160f4abea84cbe2f316db6306839d2704f09a04af763ee493dd92cb066c0865`  
		Last Modified: Fri, 01 Dec 2017 18:50:17 GMT  
		Size: 2.0 MB (1991501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff176d481367411591b2d81a3bb7bc2d2e2c76822d5ad20ff82628dbc61c69`  
		Last Modified: Fri, 01 Dec 2017 19:57:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e711ab050183d8f8013c0aff7397f33117cde2345b501427ac61b511282d00`  
		Last Modified: Fri, 01 Dec 2017 19:57:45 GMT  
		Size: 351.0 KB (351003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efe8d2415fa35cc3b875b9b2d251aab061856e13c23af1a96efb23606b97a2f`  
		Last Modified: Fri, 01 Dec 2017 19:57:46 GMT  
		Size: 6.0 MB (6041967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b130cbf10fa93f2953f3dcff9cae15e135a13f5e0f6347c0ba1d0b80bed069`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedf11ebc0d390ff438dc5fa9d67a81e65649ffd60365b088c19eebcbb0477bb`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4e759d56d0601cc7c1adb7c3dee4f18c5a43beac130f08add7315581d17c0`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.3.10-alpine`

```console
$ docker pull chronograf@sha256:61181dd78667f32c2f46259dc3e33715b9a19a14595b8e98024383c979d08360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.3.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6d0c1e8bcca576d14d6ee4d328b949bbd7bd649d72b960dc1dcc451bc3779f30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8408999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09f0a8b407f4890d03765dfe26414c2ab8f540f0d35cab50135f9fafc94f242`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:26 GMT
ADD file:cb381165dec3689cf77e902c07ea78ca4da6bce4f5ac1909eebd40dba3273bfe in / 
# Fri, 01 Dec 2017 18:46:26 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2017 19:57:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2017 19:57:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2017 19:57:15 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Fri, 01 Dec 2017 19:57:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:bb4b392707bfb4ca737581b240f672796f5744c7220fea711a5d1f669992b912 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2017 19:57:27 GMT
EXPOSE 8888/tcp
# Fri, 01 Dec 2017 19:57:27 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2017 19:57:27 GMT
COPY file:70420cc587871e64a3833c5e0724565624ad66205b4febab38c9c37f93a25e28 in /entrypoint.sh 
# Fri, 01 Dec 2017 19:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2017 19:57:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1160f4abea84cbe2f316db6306839d2704f09a04af763ee493dd92cb066c0865`  
		Last Modified: Fri, 01 Dec 2017 18:50:17 GMT  
		Size: 2.0 MB (1991501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff176d481367411591b2d81a3bb7bc2d2e2c76822d5ad20ff82628dbc61c69`  
		Last Modified: Fri, 01 Dec 2017 19:57:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e711ab050183d8f8013c0aff7397f33117cde2345b501427ac61b511282d00`  
		Last Modified: Fri, 01 Dec 2017 19:57:45 GMT  
		Size: 351.0 KB (351003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efe8d2415fa35cc3b875b9b2d251aab061856e13c23af1a96efb23606b97a2f`  
		Last Modified: Fri, 01 Dec 2017 19:57:46 GMT  
		Size: 6.0 MB (6041967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b130cbf10fa93f2953f3dcff9cae15e135a13f5e0f6347c0ba1d0b80bed069`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedf11ebc0d390ff438dc5fa9d67a81e65649ffd60365b088c19eebcbb0477bb`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4e759d56d0601cc7c1adb7c3dee4f18c5a43beac130f08add7315581d17c0`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.3-alpine`

```console
$ docker pull chronograf@sha256:61181dd78667f32c2f46259dc3e33715b9a19a14595b8e98024383c979d08360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.3-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6d0c1e8bcca576d14d6ee4d328b949bbd7bd649d72b960dc1dcc451bc3779f30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8408999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09f0a8b407f4890d03765dfe26414c2ab8f540f0d35cab50135f9fafc94f242`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:26 GMT
ADD file:cb381165dec3689cf77e902c07ea78ca4da6bce4f5ac1909eebd40dba3273bfe in / 
# Fri, 01 Dec 2017 18:46:26 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2017 19:57:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2017 19:57:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2017 19:57:15 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Fri, 01 Dec 2017 19:57:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:bb4b392707bfb4ca737581b240f672796f5744c7220fea711a5d1f669992b912 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2017 19:57:27 GMT
EXPOSE 8888/tcp
# Fri, 01 Dec 2017 19:57:27 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2017 19:57:27 GMT
COPY file:70420cc587871e64a3833c5e0724565624ad66205b4febab38c9c37f93a25e28 in /entrypoint.sh 
# Fri, 01 Dec 2017 19:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2017 19:57:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1160f4abea84cbe2f316db6306839d2704f09a04af763ee493dd92cb066c0865`  
		Last Modified: Fri, 01 Dec 2017 18:50:17 GMT  
		Size: 2.0 MB (1991501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff176d481367411591b2d81a3bb7bc2d2e2c76822d5ad20ff82628dbc61c69`  
		Last Modified: Fri, 01 Dec 2017 19:57:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e711ab050183d8f8013c0aff7397f33117cde2345b501427ac61b511282d00`  
		Last Modified: Fri, 01 Dec 2017 19:57:45 GMT  
		Size: 351.0 KB (351003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efe8d2415fa35cc3b875b9b2d251aab061856e13c23af1a96efb23606b97a2f`  
		Last Modified: Fri, 01 Dec 2017 19:57:46 GMT  
		Size: 6.0 MB (6041967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b130cbf10fa93f2953f3dcff9cae15e135a13f5e0f6347c0ba1d0b80bed069`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedf11ebc0d390ff438dc5fa9d67a81e65649ffd60365b088c19eebcbb0477bb`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4e759d56d0601cc7c1adb7c3dee4f18c5a43beac130f08add7315581d17c0`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:61181dd78667f32c2f46259dc3e33715b9a19a14595b8e98024383c979d08360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:6d0c1e8bcca576d14d6ee4d328b949bbd7bd649d72b960dc1dcc451bc3779f30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8408999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09f0a8b407f4890d03765dfe26414c2ab8f540f0d35cab50135f9fafc94f242`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:26 GMT
ADD file:cb381165dec3689cf77e902c07ea78ca4da6bce4f5ac1909eebd40dba3273bfe in / 
# Fri, 01 Dec 2017 18:46:26 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2017 19:57:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2017 19:57:15 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2017 19:57:15 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Fri, 01 Dec 2017 19:57:26 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:bb4b392707bfb4ca737581b240f672796f5744c7220fea711a5d1f669992b912 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2017 19:57:26 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2017 19:57:27 GMT
EXPOSE 8888/tcp
# Fri, 01 Dec 2017 19:57:27 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2017 19:57:27 GMT
COPY file:70420cc587871e64a3833c5e0724565624ad66205b4febab38c9c37f93a25e28 in /entrypoint.sh 
# Fri, 01 Dec 2017 19:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2017 19:57:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1160f4abea84cbe2f316db6306839d2704f09a04af763ee493dd92cb066c0865`  
		Last Modified: Fri, 01 Dec 2017 18:50:17 GMT  
		Size: 2.0 MB (1991501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff176d481367411591b2d81a3bb7bc2d2e2c76822d5ad20ff82628dbc61c69`  
		Last Modified: Fri, 01 Dec 2017 19:57:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e711ab050183d8f8013c0aff7397f33117cde2345b501427ac61b511282d00`  
		Last Modified: Fri, 01 Dec 2017 19:57:45 GMT  
		Size: 351.0 KB (351003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efe8d2415fa35cc3b875b9b2d251aab061856e13c23af1a96efb23606b97a2f`  
		Last Modified: Fri, 01 Dec 2017 19:57:46 GMT  
		Size: 6.0 MB (6041967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b130cbf10fa93f2953f3dcff9cae15e135a13f5e0f6347c0ba1d0b80bed069`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dedf11ebc0d390ff438dc5fa9d67a81e65649ffd60365b088c19eebcbb0477bb`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f4e759d56d0601cc7c1adb7c3dee4f18c5a43beac130f08add7315581d17c0`  
		Last Modified: Fri, 01 Dec 2017 19:57:44 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:8dd84876dfd91071011e7b344cb37d33d24d8f28049f4a53984d4dac37fd5ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:9445d6ed17ccad986247c9e70311d6c0bec9535c08fbdb807525a6696ea85017
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40312884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8b2cd38520b58350df56fda93ae4e7644ace2e80df08ce60e2c738bc8d8179`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 01:44:43 GMT
ADD file:f30a8b5b7cdc9ba33a250899308b490baa9f7a9b29d3a85bd16200aa0a28a04a in / 
# Tue, 12 Dec 2017 01:44:43 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 03:56:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 03:56:53 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 03:57:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 03:57:04 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 03:57:04 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 03:57:05 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 03:57:05 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 03:57:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 03:57:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e7bb522d92ff6d4e5b2087409b0fc783c2e3b06acf87bee739ee47d90bf02e96`  
		Last Modified: Tue, 12 Dec 2017 01:54:56 GMT  
		Size: 22.5 MB (22485719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4d5c79d105adf7ea85108c1b312525f1c0ca344849101a049b1a067118636`  
		Last Modified: Tue, 12 Dec 2017 03:57:23 GMT  
		Size: 4.5 MB (4500164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653796862543b972fa1bd521d5272ddd10ea2f57a8533fd456840cfb44803862`  
		Last Modified: Tue, 12 Dec 2017 03:57:25 GMT  
		Size: 13.3 MB (13302605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028d38f6d9d5133110f5833780a4a70f47026861df02a46b644af24288abf95d`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab31c9630ae82ce9df09223bdc5097c7416f2ebf5a101e638c08f30fa3f853a`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebfd0e2b07e68c7c3d76c17dcd8e6549826e893b851e0a2b440d1d8bc9d2330`  
		Last Modified: Tue, 12 Dec 2017 03:57:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:02523412e9d023db715bf6f0d2bb47b13172d4cf23efa709657be56d2071eaf5
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35119379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8c7f267f4c8bef0d4827df02a9eb3bee15d57c86f03787221a9eb64c9bd789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 13:33:42 GMT
ADD file:cfde12259adb7102e76690e986f1b9b07967a8984c85d0cead09969f5de8b8cc in / 
# Tue, 12 Dec 2017 13:33:42 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:06:33 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 12 Dec 2017 14:06:40 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 12 Dec 2017 14:06:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Dec 2017 14:07:01 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 12 Dec 2017 14:07:11 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Dec 2017 14:07:20 GMT
EXPOSE 8888/tcp
# Tue, 12 Dec 2017 14:07:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Dec 2017 14:07:21 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 12 Dec 2017 14:07:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Dec 2017 14:07:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cd8b673adb84fd5eae3444d0475addad7e8908a8332704c4407baa97e9b0b284`  
		Last Modified: Tue, 12 Dec 2017 13:45:48 GMT  
		Size: 19.3 MB (19271028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90883f0b035a290249b13586f6f13f71096b60164a943d952ecda1e1efefc280`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 3.9 MB (3873001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939c27a4aaf65412f1640cdd0d3516ac7684c2125e6baa97329bcdb2f63632c1`  
		Last Modified: Tue, 12 Dec 2017 14:08:00 GMT  
		Size: 12.0 MB (11950950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa2b291da09e5d23b21ebed513b5a8726e63dda1881f14ee6e23b582be1e585`  
		Last Modified: Tue, 12 Dec 2017 14:07:58 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5822037666784aae813617fd22e9c5509817892c745a0097f3c9489470459850`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73844d296577499389dc8a63175971dfb1806b60b75053a9f22802c7b588e43b`  
		Last Modified: Tue, 12 Dec 2017 14:07:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1580944e14eb1f38b61ebf4c53f0d5c9b6df437486c6e706459a07ccd3874b80
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36580061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a7d863f44f362d04d1c904884349dfa6f4baba5d472d1d4d58f26b473ebb88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Dec 2017 18:34:13 GMT
ADD file:6e068c7cc5397bfb4ec60dab4d410c5d3ba724f20ad0129d2032fb509f0eadcd in / 
# Tue, 12 Dec 2017 18:34:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2017 23:21:57 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2017 23:21:57 GMT
ENV CHRONOGRAF_VERSION=1.3.10.0
# Tue, 19 Dec 2017 23:22:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2017 23:22:28 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2017 23:22:29 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2017 23:22:30 GMT
EXPOSE 8888/tcp
# Tue, 19 Dec 2017 23:22:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2017 23:22:32 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Tue, 19 Dec 2017 23:22:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2017 23:22:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcad8cfc11c78a53ccf9aafafcb3ded5044dbd181977e6255aea54fbe164f131`  
		Last Modified: Tue, 12 Dec 2017 18:49:05 GMT  
		Size: 20.3 MB (20331270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779229a74f0249d7f5a79cedc25be77365759cfd785b2c183b324862baaeeeb6`  
		Last Modified: Tue, 19 Dec 2017 23:22:52 GMT  
		Size: 4.1 MB (4074975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9eb2d7d4a74cc21ed39d440b27c2579551acd5a4ec964378499c6daa557fff`  
		Last Modified: Tue, 19 Dec 2017 23:22:55 GMT  
		Size: 12.1 MB (12149422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ec21ee5d0a5f84c40c9aecea361640ac7c0a101affc5f2ca5a8d1990eb2ccf`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0e9c0167abe1cdfed41b1f3bac607f440a62bb0c5be008df518556fba88111`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c083190db174f7feede62b3fe87c0bd6e2af64447e221eac24dcdb551ad6e6`  
		Last Modified: Tue, 19 Dec 2017 23:22:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
