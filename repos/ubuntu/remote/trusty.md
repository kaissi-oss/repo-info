## `ubuntu:trusty`

```console
$ docker pull ubuntu@sha256:084989eb923bd86dbf7e706d464cf3587274a826b484f75b69468c19f8ae354c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty` - linux; amd64

```console
$ docker pull ubuntu@sha256:2f0438beaa7f3be4724bbf0fbd59d8b18938bd71f49b966221846a7db7e24746
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72963044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67759a80360cbaef77ec1eee8aa0590f07ba04c26ef496efbc90391f217fd9d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 14 Dec 2017 20:59:20 GMT
ADD file:1e105449468a2d88e99909d47bb68f49b2da9303f9f5289721720b3a30308f8e in / 
# Thu, 14 Dec 2017 20:59:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 14 Dec 2017 20:59:22 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 14 Dec 2017 20:59:23 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 14 Dec 2017 20:59:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 14 Dec 2017 20:59:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:050aa9ae81a93949af7c06a5fd6b1f0f995dc8c1b082882b14b1892c74ba23f2`  
		Last Modified: Thu, 14 Dec 2017 21:01:25 GMT  
		Size: 72.9 MB (72888752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb2c989bc049f8d7234a7b25d7cef4aaa2e85370b22a1626060c5cfe59b0a95`  
		Last Modified: Thu, 14 Dec 2017 21:01:14 GMT  
		Size: 72.6 KB (72649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e83780ccda0924d2154d8aaf10fe15a413cb3fd20ffe7ee41890a53693d4e6`  
		Last Modified: Thu, 14 Dec 2017 21:01:15 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dec31d7323cfebc7ae2dcb7851fe852ba9a8f935c0012df62ade3063a1c8cea`  
		Last Modified: Thu, 14 Dec 2017 21:01:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286f32949bdc7850bd03deeda0128f84c48a6ccac548642e88747fa025d4af76`  
		Last Modified: Thu, 14 Dec 2017 21:01:14 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:0e763fdb701e350ba37e612391f6050ce215da521bcf4862be0a370c585607e5
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66483130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da137c6450acb33b40a5ab1a21ea7c75a7e8af7dd79a6e4d67740de9914a558`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 15 Dec 2017 13:51:37 GMT
ADD file:dd1487cabc9f8e2188e6103671470ce7f41c66710ed2696ec8e26bd5047c5b47 in / 
# Fri, 15 Dec 2017 13:51:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 15 Dec 2017 13:51:40 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 13:51:40 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Fri, 15 Dec 2017 13:51:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 15 Dec 2017 13:51:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:50e2643b13d6ea73d22c1b004246a2bff43a5c025fcfbbc755748127e28c3e78`  
		Last Modified: Fri, 15 Dec 2017 13:53:11 GMT  
		Size: 66.4 MB (66404695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f428909f2234cd44a20cf86c0d66eba3f5c1a55afb113882878461edbad6b7`  
		Last Modified: Fri, 15 Dec 2017 13:52:51 GMT  
		Size: 76.8 KB (76768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443904308a1cee3b77fa8c25a3d53350efdd954e5a5f31baa343d655914e2753`  
		Last Modified: Fri, 15 Dec 2017 13:52:51 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355edca5c4b0e249be5f4e3014d4e533bb8ff090178d51c0b2b06a42aecf8e76`  
		Last Modified: Fri, 15 Dec 2017 13:52:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378c801492144c7285209c23d67c82b19b651fdb9eb1dfd3fd4c520db719d54d`  
		Last Modified: Fri, 15 Dec 2017 13:52:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9b56114aa33a0b092819ff1f15073908b4286c477337fc3c3e7bb628677633cf
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67752689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664216841fbe7eb85e1de34baffd4791fc44a2c69e21b2b9060a67d3ca9d8a09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 15 Dec 2017 15:01:23 GMT
ADD file:8aadbfe4a40536f740963c51b675ab6c8193cd57e3d31c0b1e2b72060663e3eb in / 
# Fri, 15 Dec 2017 15:01:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 15 Dec 2017 15:01:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 15:01:29 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Fri, 15 Dec 2017 15:01:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 15 Dec 2017 15:01:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:612f35d0fc5bf2558fece9956f0ae9c8458f302cd8494f4bc8b92075f1cbd7fb`  
		Last Modified: Fri, 15 Dec 2017 15:03:37 GMT  
		Size: 67.7 MB (67691952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71047af42ff6fc2806fe22f4f594a421de10078fd6910731a3c81ef03a59881e`  
		Last Modified: Fri, 15 Dec 2017 15:03:12 GMT  
		Size: 59.1 KB (59096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860c8fbc23f935305c177e6f4dd8ef1c5e824a064a4b4015131511396cb4db9a`  
		Last Modified: Fri, 15 Dec 2017 15:03:11 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a467c39ac31c8f93205e483de34f0192468906a54165c4a6bfa38cf722fe32d`  
		Last Modified: Fri, 15 Dec 2017 15:03:12 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77056b7ee035853054f607c46c11e386597fc5be9de9c5a9abe3422e297551db`  
		Last Modified: Fri, 15 Dec 2017 15:03:12 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; 386

```console
$ docker pull ubuntu@sha256:075ba975a77f45eec54bb69a18f4629dd92714257f57a82348aae07cad188ba6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70319339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3204165faa054b1f5fa0773362e6d840d979fa6e856b5452b3bba043cfebb85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 15 Dec 2017 04:42:16 GMT
ADD file:7b5c6aa131bde26d5623f1df036db48ac3e6b6e202bc52cfbc26eb3ee77129b7 in / 
# Fri, 15 Dec 2017 04:42:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 15 Dec 2017 04:42:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 04:42:18 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Fri, 15 Dec 2017 04:42:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 15 Dec 2017 04:42:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:22d3711b8e85ec67c0052e270fd39efa29409522205a9cf124ab9fec2ab64d7b`  
		Last Modified: Fri, 15 Dec 2017 04:55:05 GMT  
		Size: 70.3 MB (70252874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b928ba379023b3df547a261c587216939b416718084ceed17ea5c1e46bbdb`  
		Last Modified: Fri, 15 Dec 2017 04:54:43 GMT  
		Size: 64.9 KB (64853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b0c311355a5314aabf73c3b3a43312fe1a8c9c899bf00d59eeae8eed37f713`  
		Last Modified: Fri, 15 Dec 2017 04:54:42 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7206e65eeddf2f8a6ee5757242ecac80ed1fc957684eb36d98ba990f22f3cdf2`  
		Last Modified: Fri, 15 Dec 2017 04:54:43 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b0670c0d07463656e02bfbdebcb9c71b2566dc23cfb08f9be39be64dfeb64`  
		Last Modified: Fri, 15 Dec 2017 04:54:43 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cfc560820baa9ce029571d8d51e3aee31034e8b7b6d21d6d726ebaf3c6df95dd
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74420440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a8e89ad9c811e97e4b8904bedc633f295948805dbdbe2e52b8defc5c1843f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 15 Dec 2017 03:40:59 GMT
ADD file:c1e82458eb31b3c13212d09b241c7f1f9eabee7ce92f4c15593973a53d9afe90 in / 
# Fri, 15 Dec 2017 03:41:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 15 Dec 2017 03:41:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 15 Dec 2017 03:41:32 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Fri, 15 Dec 2017 03:41:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 15 Dec 2017 03:41:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84aa0b41cf098a013a5e819a69415aad5675a8b3c1daa9ef69daab5dead9438f`  
		Last Modified: Fri, 15 Dec 2017 03:43:58 GMT  
		Size: 74.4 MB (74355323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40bba927ea8cf230d5c0742d19200c155205c9d8155d856b7e91f2162d5119d`  
		Last Modified: Fri, 15 Dec 2017 03:43:37 GMT  
		Size: 63.4 KB (63415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91062512c3e5ef566ff426c22c212f1baaa8b1d117221e69437ea60fb48bd4ac`  
		Last Modified: Fri, 15 Dec 2017 03:43:37 GMT  
		Size: 659.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274f739a500431c46ca0fdcb481fa0adf902ab7e91335d149c29694f2c097346`  
		Last Modified: Fri, 15 Dec 2017 03:43:37 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504d71281c9a2512f2a3be597e201351f12d8a707f067cec410113ebaec5579`  
		Last Modified: Fri, 15 Dec 2017 03:43:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
