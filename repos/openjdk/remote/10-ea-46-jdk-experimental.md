## `openjdk:10-ea-46-jdk-experimental`

```console
$ docker pull openjdk@sha256:a7518dc513f4b3bf244a8ef989235f5e9dd8e5162c427a980b99956c5e73ec63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm variant v7

### `openjdk:10-ea-46-jdk-experimental` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:99476b559469fb27c25c05d04fdf8c2d29d739cb2de1711e35c41ebd709527be
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.3 MB (362311265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fb0970cf71feeaa8492e234cbf5495d2eeb46f6ccc1f58da2df184b02a1cc2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Mar 2018 12:30:24 GMT
ADD file:cf4220476786ea80d7a6f84bd9dc94b6d6ac8945750c25c3bfaacd81d179ad18 in / 
# Wed, 14 Mar 2018 12:30:25 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 13:16:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 13:16:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Mar 2018 13:17:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 13:50:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 13:50:54 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Wed, 14 Mar 2018 13:50:55 GMT
ENV LANG=C.UTF-8
# Wed, 14 Mar 2018 13:50:56 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 14 Mar 2018 13:50:57 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 14 Mar 2018 13:50:57 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 16 Mar 2018 01:26:29 GMT
ENV JAVA_VERSION=10-ea+46
# Fri, 16 Mar 2018 01:26:29 GMT
ENV JAVA_DEBIAN_VERSION=10~46-1
# Fri, 16 Mar 2018 01:27:40 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 16 Mar 2018 01:27:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4bebe725acb1248d8ff52284d58dd16fdca68548a367bc396431ad7bc5d34cdd`  
		Last Modified: Wed, 14 Mar 2018 12:42:11 GMT  
		Size: 44.0 MB (43986557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0693f5a3991162a5990e13b166d617b8f1fe371f4d92a04086448d19f61284b`  
		Last Modified: Wed, 14 Mar 2018 13:28:33 GMT  
		Size: 7.5 MB (7530551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56df267e9bb7c177688d09890d4bb7057540af666c61d9a1e741b8e886ece4cb`  
		Last Modified: Wed, 14 Mar 2018 13:28:33 GMT  
		Size: 8.6 MB (8563576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf9be025345a2e4ee4e9624a19b5f502e453281cdbbcc863a7fb162e2c960d6`  
		Last Modified: Wed, 14 Mar 2018 13:29:01 GMT  
		Size: 45.0 MB (45032882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29526685384522669b03ca17621c63977bff53de2b4cf3b1a1004d9a1b28dec`  
		Last Modified: Wed, 14 Mar 2018 14:20:17 GMT  
		Size: 869.2 KB (869181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8d79ba5138330b1c7e4dba47f97d66456b33566c8c080a973c0f70a386e473`  
		Last Modified: Wed, 14 Mar 2018 14:20:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be91b267c9216ad04aeab31a7800cd12efa760285c521d65c85f15bb4faec4c5`  
		Last Modified: Wed, 14 Mar 2018 14:20:16 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078060b66c68b2c6d4b17b5296812d45052dcd16923e9ca046f844929ec16d6`  
		Last Modified: Wed, 14 Mar 2018 14:20:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeec6759c36ee7cef001dfcdf821bd664c57325d08c2d588b1b5aceae4585f3`  
		Last Modified: Fri, 16 Mar 2018 01:39:08 GMT  
		Size: 256.3 MB (256327927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip