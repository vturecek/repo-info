## `openjdk:11-ea-11-sid`

```console
$ docker pull openjdk@sha256:095213d85a4ecdf7a2e12b7df9fc85f7ffa3e707da78e0e2e75d95bcaaef83ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:11-ea-11-sid` - linux; amd64

```console
$ docker pull openjdk@sha256:f203b2e06cf83bd66a3400815d0e94a72f92ffd0a17528750b40c9208e3d4b65
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329021342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58644a8b209e51758748f6c63c077962b783c126735500ba335139397cc8f8a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Apr 2018 06:49:58 GMT
ADD file:229ad62fdc5e079bf925fb084264841ce27bf7125beb1fd821cbd6ed5132b37c in / 
# Sat, 28 Apr 2018 06:49:59 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 16:41:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 16:41:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 May 2018 09:09:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 09:09:43 GMT
ENV LANG=C.UTF-8
# Tue, 01 May 2018 09:09:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 04 May 2018 23:44:59 GMT
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 04 May 2018 23:45:00 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 04 May 2018 23:45:00 GMT
ENV JAVA_VERSION=11-ea+11
# Fri, 04 May 2018 23:45:00 GMT
ENV JAVA_DEBIAN_VERSION=11~11-2
# Fri, 04 May 2018 23:47:58 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-11-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 04 May 2018 23:47:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e7cb83f94a464daabb5fa4e63ae521d65d7956bfcb3619bc75857f7d598ff12c`  
		Last Modified: Sat, 28 Apr 2018 08:58:22 GMT  
		Size: 48.3 MB (48303234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d9e4316522ac259c31b51deac1204cdf4e714ddff3a1d4a1bce1d0d5cfce90`  
		Last Modified: Sat, 28 Apr 2018 20:33:31 GMT  
		Size: 8.6 MB (8617077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e07faf2012b70a40ec906e76db167c387c5d2bd39160622144d2bdd95cb490e`  
		Last Modified: Sat, 28 Apr 2018 20:33:31 GMT  
		Size: 9.5 MB (9459618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc1ead89531c8ed441139a3b4a3e5f2817c92f6853321ce4921565cd8e06cc0`  
		Last Modified: Tue, 01 May 2018 13:44:24 GMT  
		Size: 856.3 KB (856292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e6ff21efc5418a58d864a177c38144b3343e18d67f69e249ea6221d2f38337`  
		Last Modified: Tue, 01 May 2018 13:44:23 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7181e17b6f0db31a40af301b4c1e47f47a628cd3b710d1eb3247ca5c6a8344d0`  
		Last Modified: Fri, 04 May 2018 23:58:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038dd82959e6012f9ef0b76116ec34a821537bcd93580bcb144ad2ad521aa7b5`  
		Last Modified: Sat, 05 May 2018 00:01:20 GMT  
		Size: 261.8 MB (261784753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip