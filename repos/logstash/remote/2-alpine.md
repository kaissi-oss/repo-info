## `logstash:2-alpine`

```console
$ docker pull logstash@sha256:59f3168ea8dd234580512c83143af526b3a0a8708a36821e0a678aef8f0c993b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `logstash:2-alpine` - linux; amd64

```console
$ docker pull logstash@sha256:1db64645f2f71f55ceee52c48ecb09167ffe5e025c0baa7db61304f6fba00cff
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143714562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b8ed6eafec985c7bde306110314faaaf6b25af6137099139015d69a30fe89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["-e",""]`

```dockerfile
# Fri, 01 Dec 2017 18:48:48 GMT
ADD file:2b00f26f6004576e2f8faeb3fb0517a14f79ea89a059fe096b54cbecf5da512e in / 
# Fri, 01 Dec 2017 18:48:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Dec 2017 03:42:44 GMT
ENV LANG=C.UTF-8
# Tue, 05 Dec 2017 03:42:45 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 05 Dec 2017 03:43:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Tue, 05 Dec 2017 03:43:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 05 Dec 2017 03:43:46 GMT
ENV JAVA_VERSION=8u151
# Tue, 05 Dec 2017 03:43:46 GMT
ENV JAVA_ALPINE_VERSION=8.151.12-r0
# Tue, 05 Dec 2017 03:43:51 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 05 Dec 2017 04:55:15 GMT
RUN addgroup -S logstash && adduser -S -G logstash logstash
# Tue, 05 Dec 2017 04:55:20 GMT
RUN apk add --no-cache 		bash 		libc6-compat 		libzmq
# Tue, 05 Dec 2017 04:56:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Dec 2017 04:56:03 GMT
ENV GPG_KEY=46095ACC8548582C1A2699A9D27D666CD88E42B4
# Tue, 05 Dec 2017 04:56:45 GMT
ENV LOGSTASH_PATH=/opt/logstash/bin
# Tue, 05 Dec 2017 04:56:45 GMT
ENV PATH=/opt/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 05 Dec 2017 04:56:45 GMT
ENV LOGSTASH_VERSION=2.4.1
# Tue, 05 Dec 2017 04:56:45 GMT
ENV LOGSTASH_TARBALL=https://download.elastic.co/logstash/logstash/logstash-2.4.1.tar.gz LOGSTASH_TARBALL_ASC= LOGSTASH_TARBALL_SHA1=5ee4f3fa0ad4b182b3f00b4181a20c4e31a907b4
# Tue, 05 Dec 2017 04:57:06 GMT
RUN set -ex; 		if [ -z "$LOGSTASH_TARBALL_SHA1" ] && [ -z "$LOGSTASH_TARBALL_ASC" ]; then 		echo >&2 'error: have neither a SHA1 _or_ a signature file -- cannot verify download!'; 		exit 1; 	fi; 		apk add --no-cache --virtual .fetch-deps 		ca-certificates 		gnupg 		openssl 		tar 	; 		wget -O logstash.tar.gz "$LOGSTASH_TARBALL"; 		if [ "$LOGSTASH_TARBALL_SHA1" ]; then 		echo "$LOGSTASH_TARBALL_SHA1 *logstash.tar.gz" | sha1sum -c -; 	fi; 		if [ "$LOGSTASH_TARBALL_ASC" ]; then 		wget -O logstash.tar.gz.asc "$LOGSTASH_TARBALL_ASC"; 		export GNUPGHOME="$(mktemp -d)"; 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY"; 		gpg --batch --verify logstash.tar.gz.asc logstash.tar.gz; 		rm -rf "$GNUPGHOME" logstash.tar.gz.asc; 	fi; 		dir="$(dirname "$LOGSTASH_PATH")"; 		mkdir -p "$dir"; 	tar -xf logstash.tar.gz --strip-components=1 -C "$dir"; 	rm logstash.tar.gz; 		apk del .fetch-deps; 		export LS_SETTINGS_DIR="$dir/config"; 	if [ -f "$LS_SETTINGS_DIR/log4j2.properties" ]; then 		cp "$LS_SETTINGS_DIR/log4j2.properties" "$LS_SETTINGS_DIR/log4j2.properties.dist"; 		truncate -s 0 "$LS_SETTINGS_DIR/log4j2.properties"; 	fi; 		for userDir in 		"$dir/config" 		"$dir/data" 	; do 		if [ -d "$userDir" ]; then 			chown -R logstash:logstash "$userDir"; 		fi; 	done; 		logstash --version
# Tue, 05 Dec 2017 04:57:07 GMT
COPY file:5073cf67fe0dccc616d2ced3f7df597d906363dd3dc278d0395d780f89073ce8 in / 
# Tue, 05 Dec 2017 04:57:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Dec 2017 04:57:07 GMT
CMD ["-e" ""]
```

-	Layers:
	-	`sha256:2fdfe1cd78c20d05774f0919be19bc1a3e4729bce219968e4188e7e0f1af679d`  
		Last Modified: Fri, 01 Dec 2017 18:50:32 GMT  
		Size: 2.1 MB (2064911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82630fd6e5ba7225587bd7986c7b6245801f8c7b001c9db318aecbb7fcb188a4`  
		Last Modified: Tue, 05 Dec 2017 03:44:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119d364c885d49cacd5587d152fc93747a1758e1cfdd3d10d627c00091c5b365`  
		Last Modified: Tue, 05 Dec 2017 03:46:37 GMT  
		Size: 54.5 MB (54453882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f984a0312d9a2c6bb1ea5258bae89c68b17907fb03766eab8c756d05c1c61468`  
		Last Modified: Tue, 05 Dec 2017 04:57:25 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a434c586c0a27cbe7406bf4a188ab014feebcbd8605e3757d4b8d858632480`  
		Last Modified: Tue, 05 Dec 2017 04:57:27 GMT  
		Size: 1.6 MB (1624547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd005d0c1502598c405eb4380ba3f514ae945c205b83ea68565a831208679e7`  
		Last Modified: Tue, 05 Dec 2017 04:57:25 GMT  
		Size: 96.9 KB (96937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548857af52ef7ea1d384e424ac9b1936cc3f1611b12f2e6f54a727f1685f32e9`  
		Last Modified: Tue, 05 Dec 2017 04:58:27 GMT  
		Size: 85.5 MB (85472484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97f241fdba8b0ff020e2102606705f0dda1214b491c991a374171267c376f77`  
		Last Modified: Tue, 05 Dec 2017 04:58:18 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
