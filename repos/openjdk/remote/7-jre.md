## `openjdk:7-jre`

```console
$ docker pull openjdk@sha256:a7a78601c321d73d6668ee0d2c2d2a1f41d064ab0a9fe3d5d025e6a87ad5a3be
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

### `openjdk:7-jre` - linux; amd64

```console
$ docker pull openjdk@sha256:61ad5905e7855ff2f0759b6e76cd51a106ec11d867ce04e43b604487d34101f9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189565074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37931cdaeeb8053cf8f92e8f5689404ad23e3c5ff16d5ea3da66584e673f4b53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 07:49:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:49:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:05:03 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:05:05 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:05:06 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:05:06 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:05:07 GMT
ENV JAVA_VERSION=7u151
# Tue, 12 Dec 2017 15:05:07 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-2~deb8u1
# Tue, 12 Dec 2017 15:06:21 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b491c575b06601bb07a2d88bfc3ace6c6005edc1b4d8da3ba6e37e04e9592d6`  
		Last Modified: Tue, 12 Dec 2017 08:00:34 GMT  
		Size: 19.3 MB (19266203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f79c7851951d3c8f33be3e165201911aa7d877f5102246c2acec2d041688ce`  
		Last Modified: Tue, 12 Dec 2017 16:16:32 GMT  
		Size: 795.6 KB (795596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381cea282a6be34394dfc7a7d190f36a6499bc53ffb1a80e32b019c5ffa12cac`  
		Last Modified: Tue, 12 Dec 2017 16:16:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2708823fce39173e1302ba02c18431c06824fe8067d5ea03424ac5909671a069`  
		Last Modified: Tue, 12 Dec 2017 16:16:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fd5a680ec1128a7c6395e4b1ae3c116bfba196eb1246bac1580f10907b6c99`  
		Last Modified: Tue, 12 Dec 2017 16:16:52 GMT  
		Size: 116.9 MB (116903202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; arm variant v5

```console
$ docker pull openjdk@sha256:d1b438b1e6e8f2c0e1fe8b2b960332cc4a6e64a4f970e8a653c5dd30d58f43cc
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164557333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71669e6c106511248dd8fbdc7f4b62063d7a4798b59902a9b7e8133a2b689ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 20:57:00 GMT
ADD file:2c2c6b8bfbbc9860c0ddd8a2ba3d769171576fc13d5d99fb50a852f6b03618d1 in / 
# Tue, 12 Dec 2017 20:57:00 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 22:52:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 22:52:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 23:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 23:30:32 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 23:30:33 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 23:30:34 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 23:30:34 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 23:30:34 GMT
ENV JAVA_VERSION=7u151
# Tue, 12 Dec 2017 23:30:34 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-2~deb8u1
# Tue, 12 Dec 2017 23:31:51 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:fbe67b6ec6f136174afee77eff07fd99e5764d9db2b13d0dc1189bf8203d289b`  
		Last Modified: Tue, 12 Dec 2017 21:06:47 GMT  
		Size: 50.9 MB (50882486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20452f83e704c3737bc38610443b6ca94edbe5388fb654b5c4c3c4308150785`  
		Last Modified: Tue, 12 Dec 2017 23:07:02 GMT  
		Size: 18.7 MB (18656894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b930f9216aa0b9f2067a575c4699301d17314cde5527230f2124bd9cec59b06d`  
		Last Modified: Tue, 12 Dec 2017 23:51:46 GMT  
		Size: 788.4 KB (788355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7391de06f5cf48a91f32bebe045bbceba82fcca8766420086976f8881f274e`  
		Last Modified: Tue, 12 Dec 2017 23:51:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82e3d1c9abbfbcceaed611e4aac6457213f90fe11ef4f5fbc24004bf5534d71`  
		Last Modified: Tue, 12 Dec 2017 23:51:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035cfa06bd0aa5d061e58a02930cee87001a1926a4ce52e39a3e1cdac0a1084c`  
		Last Modified: Tue, 12 Dec 2017 23:52:09 GMT  
		Size: 94.2 MB (94229222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:b88e516689b63c2fd704e28637b3d718196f19791ebdb1caebe569112aaae504
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170434303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afd3e5625add7e7e26f4a4463f984c647ab22413cf67fc2fecc488afa6cacfb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 15:11:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 15:11:13 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 15:11:15 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 15:11:16 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 15:11:16 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 15:11:17 GMT
ENV JAVA_VERSION=7u151
# Tue, 12 Dec 2017 15:11:17 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-2~deb8u1
# Tue, 12 Dec 2017 15:12:25 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791a7deca76d7c39c702fc73b82e890cf41d814232e44f42bcb5c9bb3fcd2c56`  
		Last Modified: Tue, 12 Dec 2017 15:32:04 GMT  
		Size: 763.0 KB (762967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17e9c406247b6027e3272e9389d03701af57bb39e7d71a41e8bf503e4ffffa7`  
		Last Modified: Tue, 12 Dec 2017 15:32:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f304cd96766badd3946a5b93e6b886c1975df41c267b010ea0d2ea4ae123e81`  
		Last Modified: Tue, 12 Dec 2017 15:32:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce44ffce3c45712dd8694ba14dc99a387705c41a1d3247608d1eb78e2d83693b`  
		Last Modified: Tue, 12 Dec 2017 15:32:25 GMT  
		Size: 102.7 MB (102714165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:828931e55e74861e1d74f00b4d79940a642b0eb8321f1adad2ba197dc5c2aaaf
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163905095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eeace4d0669f089986ac1775d3e08950948f3a48652b4098848e2772b3b7e88`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 09 Oct 2017 21:43:13 GMT
ADD file:1661271485aa5a1ca074498b8ca025f41e547bf2b33335b108d9aaa06717b2a5 in / 
# Mon, 09 Oct 2017 21:43:14 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:39:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Nov 2017 09:51:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Nov 2017 11:37:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Nov 2017 11:37:04 GMT
ENV LANG=C.UTF-8
# Fri, 03 Nov 2017 11:37:06 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 03 Nov 2017 11:37:07 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 03 Nov 2017 11:37:08 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 03 Nov 2017 11:37:09 GMT
ENV JAVA_VERSION=7u151
# Fri, 03 Nov 2017 11:37:09 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-1~deb8u1
# Fri, 03 Nov 2017 11:43:29 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:abcff42ba939437677463734d9b81de5e60df7354c734ee3ddd879c0d3d5d595`  
		Last Modified: Mon, 09 Oct 2017 21:52:08 GMT  
		Size: 49.9 MB (49929310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eea24e7c11451963104c40894381c41b9efc0c36165352be38c74f40da7cc7`  
		Last Modified: Mon, 09 Oct 2017 23:28:06 GMT  
		Size: 18.7 MB (18738058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eafce9019ca0df105982768a2666a19a2454327e40a736dfda0bf8c3c88f098`  
		Last Modified: Fri, 03 Nov 2017 11:54:41 GMT  
		Size: 789.5 KB (789488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64daa7d9e79c70025256f305392f4e85e8807bd7a8512fce47d4f01f0d52f0d`  
		Last Modified: Fri, 03 Nov 2017 11:54:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f0b713052fe2f2b400425f8ef1220094f9355adefebf27fb6b1771eae338a`  
		Last Modified: Fri, 03 Nov 2017 11:54:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6be68cfda5c66d7a7c53dc18f221d30e6ec413a14718a0cdddf4570e7007c3`  
		Last Modified: Fri, 03 Nov 2017 11:55:05 GMT  
		Size: 94.4 MB (94447860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; 386

```console
$ docker pull openjdk@sha256:ef4dd95af315056d993f2793b0da445c8a802ebc47be9a6b3b04e9b86805da12
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202769812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45acea1149aa2c6862a056653303355aa8ca22f6de21a5deb74538e7125c0374`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 14:19:55 GMT
ADD file:235a40e05b677eb2ae7e7a3cc5cbb0cda242ff15dddb87cb8dc9bb0cd2d6aed8 in / 
# Tue, 12 Dec 2017 14:19:55 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 16:53:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 16:53:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 18:34:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 18:34:26 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 18:34:27 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 18:34:28 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 18:34:28 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 18:34:29 GMT
ENV JAVA_VERSION=7u151
# Tue, 12 Dec 2017 18:34:29 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-2~deb8u1
# Tue, 12 Dec 2017 18:36:06 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:d99577c7ee3d4d82987bedaeb10f3244ff7e19e41c5259bb8cac00568d1c4271`  
		Last Modified: Tue, 12 Dec 2017 14:46:26 GMT  
		Size: 52.8 MB (52777369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94aafa6d6f35f82e1fdc93cd4f7f6ab829f6297c8defaaa911dfb2de063bf3d`  
		Last Modified: Tue, 12 Dec 2017 17:27:39 GMT  
		Size: 21.6 MB (21596374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41171fdc1dc83289b7f8c9d60a40536d15809bb538798b55ee6e0eb0afeba88f`  
		Last Modified: Tue, 12 Dec 2017 19:35:05 GMT  
		Size: 798.6 KB (798582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdd455ef9100bd829a49e9e9d9f9c13dfcdd6e0085edaae464cd1ead6675ca1`  
		Last Modified: Tue, 12 Dec 2017 19:35:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01a4360030553c8fee4c62b14901be137180668540d16a4fe36022091fd2756`  
		Last Modified: Tue, 12 Dec 2017 19:35:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fc3b433a8141a22d06f0b3a4416f9d0431e0a3ae9848df5188b8a040480592`  
		Last Modified: Tue, 12 Dec 2017 19:35:39 GMT  
		Size: 127.6 MB (127597108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; ppc64le

```console
$ docker pull openjdk@sha256:a41a410e8aeae75e828900ca661b2fe08f0774b3e4af7ccb4b7fe9ddc279e569
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167964701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe9cd97ef3196cd34ecebb4017b82077b83c34626ea62a6a24de684028c63c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 01:32:54 GMT
ADD file:a66da0d75afce2da6174648a861b98f8e9999028d4f04a59288ca92a090256e2 in / 
# Tue, 12 Dec 2017 01:32:56 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 02:52:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 02:52:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 15 Dec 2017 06:20:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 06:20:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Dec 2017 06:20:17 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 15 Dec 2017 06:20:20 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 15 Dec 2017 06:20:22 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 15 Dec 2017 06:20:22 GMT
ENV JAVA_VERSION=7u151
# Fri, 15 Dec 2017 06:20:24 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-2~deb8u1
# Fri, 15 Dec 2017 06:27:04 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:75c28926027fc0404a0d21450475473243a59e8fc55443a62d1d744693ec19e9`  
		Last Modified: Tue, 12 Dec 2017 01:38:17 GMT  
		Size: 51.8 MB (51808999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6994e7d2dd732e57cd3bac94b995dab8a2711f30cf738f70bd4730a512f403ca`  
		Last Modified: Tue, 12 Dec 2017 03:53:30 GMT  
		Size: 19.2 MB (19202627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edea1a8c5e37653b453f86ae51caed3c69f8552da4587858ffdaa251bc600df`  
		Last Modified: Fri, 15 Dec 2017 06:47:11 GMT  
		Size: 791.5 KB (791458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8239cd45f9992f7087bcb6c8751e3b0031a3423c6e1f8770b8e453bf59780d0`  
		Last Modified: Fri, 15 Dec 2017 06:47:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81df54ee8bba3f30ea9f2ce996888cfaf9e395d96828195971f92bc086a6ba6c`  
		Last Modified: Fri, 15 Dec 2017 06:47:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e4510849ccc5dc1ce1d61c37cf5fb0a4f1846bde092279481d2e3e4f8a7b1`  
		Last Modified: Fri, 15 Dec 2017 06:47:34 GMT  
		Size: 96.2 MB (96161237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jre` - linux; s390x

```console
$ docker pull openjdk@sha256:cfdf1f9c400c85f249d8fb40f8bec691c9f1ad86b9d2f9c37d7975fac42adb34
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168755863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b410de3890f3c87cf94047b6d5f04148622a72e83b41bf4a316e02134120122`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Dec 2017 06:22:40 GMT
ADD file:f85dc45c68f6f29cc10d6ef236674dedc10522f11b6fa2e8a6b10a4409ca0bc7 in / 
# Tue, 12 Dec 2017 06:22:40 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 06:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 06:53:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 07:36:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 07:36:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2017 07:36:31 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 12 Dec 2017 07:36:31 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 12 Dec 2017 07:36:32 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 12 Dec 2017 07:36:32 GMT
ENV JAVA_VERSION=7u151
# Tue, 12 Dec 2017 07:36:32 GMT
ENV JAVA_DEBIAN_VERSION=7u151-2.6.11-2~deb8u1
# Tue, 12 Dec 2017 07:37:29 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:98cfcbfa76c6d2a42223dc7a44505bdd260000bffd3ecbb983cb33213128499b`  
		Last Modified: Tue, 12 Dec 2017 06:28:05 GMT  
		Size: 52.8 MB (52790322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a54c25ad661f258cad7c32f6c27f8a2ff7d463df9cbd8752d4ec4b8b2d8bfd`  
		Last Modified: Tue, 12 Dec 2017 07:02:50 GMT  
		Size: 19.5 MB (19471919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698f33e686ddf8ded512528ec312746d578c010e44ef91ec21d7ed42b9d456b6`  
		Last Modified: Tue, 12 Dec 2017 07:46:40 GMT  
		Size: 804.2 KB (804245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50a2848aff3fd8817ab14d8760b7b1953f9381b6052b206090b9d3a9e816197`  
		Last Modified: Tue, 12 Dec 2017 07:46:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db2bcfc1fbb00772c6d1c80a00fd1baa017d67a8b4e2160182c87bcb8304fce`  
		Last Modified: Tue, 12 Dec 2017 07:46:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd3e02aec81601b4b5bbd0f9071e5a15744014c88992f604bbae91ca6199175`  
		Last Modified: Tue, 12 Dec 2017 07:46:53 GMT  
		Size: 95.7 MB (95688999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
