## `vault:latest`

```console
$ docker pull vault@sha256:e14889b08156b89eac8f72b49c409d03800b14cf395aa7afb59b7d688361816d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:0ba5cb920d179e82f90e9803c0d1ef01c7fa2d8bdf7f0924b334e2ed27fdc2f1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20362861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9475413e101ef80ef3c145b661d7e0153e8f2112b9a6eba0efec54e9b122065c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:26 GMT
ADD file:cb381165dec3689cf77e902c07ea78ca4da6bce4f5ac1909eebd40dba3273bfe in / 
# Fri, 01 Dec 2017 18:46:26 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2017 22:30:08 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Thu, 21 Dec 2017 21:31:38 GMT
ENV VAULT_VERSION=0.9.1
# Thu, 21 Dec 2017 21:31:39 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 21 Dec 2017 21:31:47 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init &&     gpg --keyserver pgp.mit.edu --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 21 Dec 2017 21:31:48 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 21 Dec 2017 21:31:49 GMT
VOLUME [/vault/logs]
# Thu, 21 Dec 2017 21:31:49 GMT
VOLUME [/vault/file]
# Thu, 21 Dec 2017 21:31:49 GMT
EXPOSE 8200/tcp
# Thu, 21 Dec 2017 21:31:49 GMT
COPY file:71f93573d5097ef42f7373b359230a67d5c04db40151c9f350d7d9c881341c67 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 21 Dec 2017 21:31:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Dec 2017 21:31:50 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:1160f4abea84cbe2f316db6306839d2704f09a04af763ee493dd92cb066c0865`  
		Last Modified: Fri, 01 Dec 2017 18:50:17 GMT  
		Size: 2.0 MB (1991501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d05086e561b9dbf96ec200de329968002358d6aacc5ce453a5c333fd228808`  
		Last Modified: Thu, 21 Dec 2017 21:32:09 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475ce29ee596937c74dc175cd4239bedd1d9d38d44010a1f32cf69123d1ed142`  
		Last Modified: Thu, 21 Dec 2017 21:32:16 GMT  
		Size: 18.4 MB (18368163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0552b33b9feb50c799b504a15f31ec2f81cb1f356a0fa9b2f01b512513d5e28`  
		Last Modified: Thu, 21 Dec 2017 21:32:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5836522b618a29f59ad5ed84e339b03d8fa9c622e845695a8c9d8002085fd6aa`  
		Last Modified: Thu, 21 Dec 2017 21:32:09 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
