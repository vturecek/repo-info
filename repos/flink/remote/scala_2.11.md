## `flink:scala_2.11`

```console
$ docker pull flink@sha256:4d8fa64a037c4c6ca020be4c89ee68ccc86098fa4cbf28bc7fed57c86e867e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:scala_2.11` - linux; amd64

```console
$ docker pull flink@sha256:300ec3564351e5d31e6f471cb8b22405fd481780fe81671806583adcebe13f5d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.5 MB (444486364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d0406319c58794c5e94c9553a3e7ed440e3e568e0759de4a7eee089352439a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Sat, 28 Apr 2018 07:08:53 GMT
ADD file:9572fdb59dfbb9b032f3331bbc2a08b31e0aef5fbde44c8f2008d22bf5290cf2 in / 
# Sat, 28 Apr 2018 07:08:53 GMT
CMD ["bash"]
# Fri, 04 May 2018 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 04 May 2018 17:41:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 04 May 2018 23:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 04 May 2018 23:51:32 GMT
ENV LANG=C.UTF-8
# Fri, 04 May 2018 23:51:33 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 04 May 2018 23:51:34 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 04 May 2018 23:51:34 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 04 May 2018 23:51:34 GMT
ENV JAVA_VERSION=8u171
# Fri, 04 May 2018 23:51:34 GMT
ENV JAVA_DEBIAN_VERSION=8u171-b11-1~deb9u1
# Fri, 04 May 2018 23:51:35 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 04 May 2018 23:52:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 04 May 2018 23:52:34 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 05 May 2018 08:26:46 GMT
RUN set -ex;   apt-get update;   apt-get -y install libsnappy1v5;   rm -rf /var/lib/apt/lists/*
# Sat, 05 May 2018 08:26:46 GMT
ENV GOSU_VERSION=1.7
# Sat, 05 May 2018 08:26:53 GMT
RUN set -ex;   wget -nv -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)";   wget -nv -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc";   export GNUPGHOME="$(mktemp -d)";   gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true
# Sat, 05 May 2018 08:32:19 GMT
ENV FLINK_VERSION=1.4.2 HADOOP_VERSION=28 SCALA_VERSION=2.11
# Sat, 05 May 2018 08:32:19 GMT
ENV FLINK_HOME=/opt/flink
# Sat, 05 May 2018 08:32:19 GMT
ENV PATH=/opt/flink/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 May 2018 08:32:20 GMT
RUN groupadd --system --gid=9999 flink &&     useradd --system --home-dir $FLINK_HOME --uid=9999 --gid=flink flink
# Sat, 05 May 2018 08:32:20 GMT
WORKDIR /opt/flink
# Sat, 05 May 2018 08:32:21 GMT
ENV FLINK_URL_FILE_PATH=flink/flink-1.4.2/flink-1.4.2-bin-hadoop28-scala_2.11.tgz
# Sat, 05 May 2018 08:32:21 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.4.2/flink-1.4.2-bin-hadoop28-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.4.2/flink-1.4.2-bin-hadoop28-scala_2.11.tgz.asc
# Sat, 05 May 2018 08:32:21 GMT
COPY file:d9b980b40ddcfab2700a72e4088616452368e14c4f8fbee56f3258ac7f5dd913 in /KEYS 
# Sat, 05 May 2018 08:32:49 GMT
RUN set -ex;   wget -nv -O flink.tgz "$FLINK_TGZ_URL";   wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";   gpg --import /KEYS;   gpg --batch --verify flink.tgz.asc flink.tgz;   rm -rf "$GNUPGHOME" flink.tgz.asc;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     chown -R flink:flink .;
# Sat, 05 May 2018 08:32:49 GMT
COPY file:dd3a2212d5f0bbe552ac5e863e5fb1df12bcbb32cff887e6f4f3c81e2372b6c1 in / 
# Sat, 05 May 2018 08:32:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 05 May 2018 08:32:49 GMT
EXPOSE 6123/tcp 8081/tcp
# Sat, 05 May 2018 08:32:50 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:cc1a78bfd46becbfc3abb8a74d9a70a0e0dc7a5809bbd12e814f9382db003707`  
		Last Modified: Sat, 28 Apr 2018 09:27:54 GMT  
		Size: 45.3 MB (45318159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6861473222a6f5fb6abe08f0cdebf56b5f42758b0a7430bbbf47a3d365198e5e`  
		Last Modified: Fri, 04 May 2018 18:20:41 GMT  
		Size: 10.8 MB (10773612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0b9c3b5ae080d11df6df788ce96a45b684d7b050fd017c06b4ea5a40f58545`  
		Last Modified: Fri, 04 May 2018 18:20:39 GMT  
		Size: 4.3 MB (4335883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14ee39877acb45fb6c2157e51ddcd4690ac64ed50b0bbd417eb101518ef81d`  
		Last Modified: Sat, 05 May 2018 00:08:21 GMT  
		Size: 853.1 KB (853090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8085c1b536f02629bdd8a7a1ba474b47b4c842019776b964d5d34e9100a1c07a`  
		Last Modified: Sat, 05 May 2018 00:08:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1431e84c0ce069ca47afe14c3caab9012a2c46f70788f1bdf4b2ec5e4a7e63`  
		Last Modified: Sat, 05 May 2018 00:08:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c0569aaeea1b25b77653bb856a421badabc61741f46c2252b167a0add3e5e0`  
		Last Modified: Sat, 05 May 2018 00:08:53 GMT  
		Size: 155.2 MB (155206032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece988bd327b080fa11d94c361983046c747e22f7500451439633613f9e9e536`  
		Last Modified: Sat, 05 May 2018 00:08:20 GMT  
		Size: 272.1 KB (272057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40081ea0fef9c417da3904aaa459ee6eb4cc775ffbd4fe1920cf956b5929d0fd`  
		Last Modified: Sat, 05 May 2018 08:33:30 GMT  
		Size: 482.3 KB (482296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68f2afc794a1a545eafe9b5cc674e8d8d132acef9d6ddf8585065518f75d6ee`  
		Last Modified: Sat, 05 May 2018 08:33:30 GMT  
		Size: 819.2 KB (819183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766c32681651f6ef2e9d716faa5c0ca568b4f1319f76af355f421f530a20ea31`  
		Last Modified: Sat, 05 May 2018 08:39:41 GMT  
		Size: 4.7 KB (4650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cb3ac4d109e81e53813fa852141758db9b8409a4f784048bb27edbb7766a37`  
		Last Modified: Sat, 05 May 2018 08:39:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c080ccc6f3b5330538e118a29e55337c3fcac638d4d465ff3de1a416a3ca522`  
		Last Modified: Sat, 05 May 2018 08:39:41 GMT  
		Size: 59.3 KB (59338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a502222e3f206a591a84bb60c69be7a9cd21564cbde3ae188f5316287b9cb1a7`  
		Last Modified: Sat, 05 May 2018 08:39:57 GMT  
		Size: 226.4 MB (226360458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7a0bcbae2f7faa539125b92905ceec532725614b1493c383d1ddd3c3df1699`  
		Last Modified: Sat, 05 May 2018 08:39:41 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
