## `percona:latest`

```console
$ docker pull percona@sha256:449f3b46613b52c577c83eaaae6c4b4f1fac70a30011f81cc92318239eef6750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:latest` - linux; amd64

```console
$ docker pull percona@sha256:6a647e0600e36a4af2d8161ea3845fa804de80a98e81a5622e230e0347ec6f2e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141108901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53123ced18b5940fac03982bb08dcd1acb171909169a9d3107583c9f7b1b961`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Dec 2017 01:41:12 GMT
ADD file:1dd78a123212328bdc72ef7888024ea27fe141a72e24e0ea7c3c92b63b73d8d1 in / 
# Tue, 12 Dec 2017 01:41:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 02:17:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Dec 2017 02:22:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 12 Dec 2017 02:23:10 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 12 Dec 2017 02:23:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Dec 2017 02:38:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		apt-transport-https ca-certificates 		pwgen 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 02:38:33 GMT
ENV GPG_KEYS=430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	4D1BB29D63D98E422B2113B19334A25F8507EFA5
# Tue, 12 Dec 2017 02:38:36 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/percona.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 12 Dec 2017 02:38:37 GMT
RUN echo 'deb https://repo.percona.com/apt jessie main' > /etc/apt/sources.list.d/percona.list
# Tue, 12 Dec 2017 02:38:37 GMT
ENV PERCONA_MAJOR=5.7
# Tue, 19 Dec 2017 17:56:29 GMT
ENV PERCONA_VERSION=5.7.20-18-1.jessie
# Tue, 19 Dec 2017 17:57:03 GMT
RUN { 		for key in 			percona-server-server/root_password 			percona-server-server/root_password_again 			"percona-server-server-$PERCONA_MAJOR/root-pass" 			"percona-server-server-$PERCONA_MAJOR/re-root-pass" 		; do 			echo "percona-server-server-$PERCONA_MAJOR" "$key" password 'unused'; 		done; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		percona-server-server-$PERCONA_MAJOR=$PERCONA_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& sed -ri 's/^user\s/#&/' /etc/mysql/my.cnf 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 19 Dec 2017 17:57:07 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 19 Dec 2017 17:57:07 GMT
COPY file:ff55c7472da1028b4f65163094878d7e111bf055794e1db6f6adbc876a67481b in /usr/local/bin/ 
# Tue, 19 Dec 2017 17:57:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 19 Dec 2017 17:57:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2017 17:57:16 GMT
EXPOSE 3306/tcp
# Tue, 19 Dec 2017 17:57:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f49cf87b52c10aa83b4f4405800527a74400fb19ea1821d209293bc4d53966aa`  
		Last Modified: Tue, 12 Dec 2017 01:47:59 GMT  
		Size: 52.6 MB (52599697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78032de49d65ab1151d278821068401fa7a8964c16b2f4441a3ef9ac8dd02229`  
		Last Modified: Tue, 12 Dec 2017 02:23:47 GMT  
		Size: 2.1 KB (2087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837546b20bc4af04c4cd0b34ac6cb74418f0400fa80045d02d341aecbc70f928`  
		Last Modified: Tue, 12 Dec 2017 02:34:38 GMT  
		Size: 1.3 MB (1303017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8316af6cc601a268bccfd58f93c2598e4a5f8a6b101cb9ffe365bcd467cb8e`  
		Last Modified: Tue, 12 Dec 2017 02:34:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf376ff5a98933d3c67cab6adb1a5a81e906ca6897c969642075a7c4ae000026`  
		Last Modified: Tue, 12 Dec 2017 02:42:13 GMT  
		Size: 6.7 MB (6671940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9df53b4003260bf8073ebb405bd35c389e52bc898d7bef76e0bed848d67fb1`  
		Last Modified: Tue, 12 Dec 2017 02:42:09 GMT  
		Size: 4.7 KB (4679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d585cd2f11d440f78ff01fda4460b314ed1da81c6f74e8fb611b635860438168`  
		Last Modified: Tue, 12 Dec 2017 02:42:09 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfab51ec1f90f5c2aeaa9006ed8eb55cf44f73a1cb06a0e25e790e485146929`  
		Last Modified: Tue, 19 Dec 2017 17:57:48 GMT  
		Size: 80.5 MB (80524589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27aab41b4dc562aca27e331c448f2b53442963cd2dfb7852ad3f0fed221ca9`  
		Last Modified: Tue, 19 Dec 2017 17:57:35 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3b42ede5e813939608af87ddb3c75aa75ab2d5ff70a709f6053940ad1cfa7d`  
		Last Modified: Tue, 19 Dec 2017 17:57:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
