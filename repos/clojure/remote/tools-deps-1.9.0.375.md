## `clojure:tools-deps-1.9.0.375`

```console
$ docker pull clojure@sha256:5934827564326a60d2d8251ba18870b9b9d4caea4bb84a80ec956f868fedb595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `clojure:tools-deps-1.9.0.375` - linux; amd64

```console
$ docker pull clojure@sha256:cf69327d5aa7d294bcd7638a35bfba6f926b968a2ce1bfcadf1dd267c036218e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305941615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1353a6536c895889852cd131a5ca1caac2d64979ea75e7cf4b92c2b67e45fed8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Mar 2018 22:26:49 GMT
ADD file:b380df301ccb5ca09f0d7cd5697ed402fa55f3e9bc5df2f4d489ba31f28de58a in / 
# Tue, 13 Mar 2018 22:26:49 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:56:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:56:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Mar 2018 23:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 11:09:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 11:09:00 GMT
ENV LANG=C.UTF-8
# Wed, 14 Mar 2018 11:09:01 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 14 Mar 2018 11:09:02 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 14 Mar 2018 11:09:02 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 19 Mar 2018 21:22:52 GMT
ENV JAVA_VERSION=8u162
# Mon, 19 Mar 2018 21:22:53 GMT
ENV JAVA_DEBIAN_VERSION=8u162-b12-1~deb9u1
# Mon, 19 Mar 2018 21:22:53 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Mon, 19 Mar 2018 21:23:40 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 19 Mar 2018 21:23:43 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Mon, 23 Apr 2018 21:46:55 GMT
LABEL maintainer=Kirill Chernyshov <delaguardo@gmail.com>
# Mon, 23 Apr 2018 21:46:55 GMT
ENV CLOJURE_VERSION=1.9.0.375
# Mon, 23 Apr 2018 21:46:56 GMT
WORKDIR /tmp
# Mon, 23 Apr 2018 21:46:59 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh     && chmod +x linux-install-$CLOJURE_VERSION.sh     && ./linux-install-$CLOJURE_VERSION.sh
# Mon, 23 Apr 2018 21:47:09 GMT
RUN clojure -e "(clojure-version)"
```

-	Layers:
	-	`sha256:c73ab1c6897bf5c11da3c95cab103e7ca8cf10a6d041eda2ff836f45a40e3d3b`  
		Last Modified: Tue, 13 Mar 2018 22:52:31 GMT  
		Size: 45.1 MB (45135077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab373b3deaed929a15574ac1912afc6e173f80d400aba0e96c89f6a58961f2d`  
		Last Modified: Wed, 14 Mar 2018 00:46:17 GMT  
		Size: 11.1 MB (11108010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542772b417703c0311c0b90136091369bcd9c2176c0e3ceed5a0114d743ee3c`  
		Last Modified: Wed, 14 Mar 2018 00:46:16 GMT  
		Size: 4.3 MB (4335495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c8de432dbe337bb6cb1ad328e6c564303a3d3fd05b5e872fd9c47c16fdd02c`  
		Last Modified: Wed, 14 Mar 2018 00:47:09 GMT  
		Size: 50.0 MB (50023717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da44f64ae9991a9e8cb7c2af4dfd63608bd4026552b2b6a7f523dcfac960e1ac`  
		Last Modified: Wed, 14 Mar 2018 12:50:06 GMT  
		Size: 892.2 KB (892173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbc7b377a9155696eb0b684bd1999bc43937918552d73fd9697ea50ef46528a`  
		Last Modified: Wed, 14 Mar 2018 12:50:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6c70b3786f72e5255ccd51e27840d1c853a17561b5e94a4359b17d27494d50`  
		Last Modified: Wed, 14 Mar 2018 12:50:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bbcf733166f991331a80e1cd55a91111c4ba96fc7ce1ecabd05b450b7da7a3`  
		Last Modified: Mon, 19 Mar 2018 23:42:27 GMT  
		Size: 172.7 MB (172725313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d3e8de8ec6d87b8485a8a3b66d63125a033cfb0711f8af24b4f600f524e276`  
		Last Modified: Mon, 19 Mar 2018 23:41:54 GMT  
		Size: 272.1 KB (272122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d5a4202d075d44e49eddf013a8ef820a08ef06872682d0aca50fc2136ef319`  
		Last Modified: Mon, 23 Apr 2018 21:54:24 GMT  
		Size: 17.6 MB (17557966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2337b0c22b9a480fc56a034e4ad1db1c3587745b6dbd644b62df886d5ab7719`  
		Last Modified: Mon, 23 Apr 2018 21:54:22 GMT  
		Size: 3.9 MB (3891364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.9.0.375` - linux; arm variant v5

```console
$ docker pull clojure@sha256:9c7fba922f34230e80cdc34cbac0f79dbbb2d2647e60fb49952906fd9feeadb1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270691701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce0c098a4c8c26c68292ca5c2462f94538d9fa9ed4da3a3ad1f717656c168c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 14 Mar 2018 20:01:02 GMT
ADD file:df0457084f7e40c64d40dd7ffb2d5365160faee6f8b02c443bc3d1cb36a0f40d in / 
# Wed, 14 Mar 2018 20:01:03 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 20:46:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 20:46:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Mar 2018 20:47:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 22:49:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 22:49:38 GMT
ENV LANG=C.UTF-8
# Wed, 14 Mar 2018 22:49:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 14 Mar 2018 22:49:39 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 14 Mar 2018 22:49:40 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 20 Mar 2018 10:11:03 GMT
ENV JAVA_VERSION=8u162
# Tue, 20 Mar 2018 10:11:03 GMT
ENV JAVA_DEBIAN_VERSION=8u162-b12-1~deb9u1
# Tue, 20 Mar 2018 10:11:03 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 20 Mar 2018 10:12:01 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 20 Mar 2018 10:12:07 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 24 Apr 2018 08:53:07 GMT
LABEL maintainer=Kirill Chernyshov <delaguardo@gmail.com>
# Tue, 24 Apr 2018 08:53:08 GMT
ENV CLOJURE_VERSION=1.9.0.375
# Tue, 24 Apr 2018 08:53:11 GMT
WORKDIR /tmp
# Tue, 24 Apr 2018 08:53:15 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh     && chmod +x linux-install-$CLOJURE_VERSION.sh     && ./linux-install-$CLOJURE_VERSION.sh
# Tue, 24 Apr 2018 08:54:11 GMT
RUN clojure -e "(clojure-version)"
```

-	Layers:
	-	`sha256:25301cba2d4ef04878f7296fe55faa4b0b2fafbc29758d9fca5a199350d7827c`  
		Last Modified: Wed, 14 Mar 2018 20:12:18 GMT  
		Size: 43.8 MB (43819573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0783f4694c09bab63892aa1cd19490f94750d131d57747e09ec4307e9072c2`  
		Last Modified: Wed, 14 Mar 2018 20:56:19 GMT  
		Size: 10.2 MB (10206441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aaeaf8dbc82c078a47db8431ae04e72f7fe0ae39da82e4d92db0cc10836ffc`  
		Last Modified: Wed, 14 Mar 2018 20:56:18 GMT  
		Size: 4.2 MB (4153056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64debcbc218e3d8c57772d2bfa18b0bf274083c34858536accba655b0594a5c9`  
		Last Modified: Wed, 14 Mar 2018 20:56:55 GMT  
		Size: 48.2 MB (48233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fd315b1569d687c7138a41e66dccc32bf422799c8691d6400a0c71a920f31d`  
		Last Modified: Wed, 14 Mar 2018 23:13:55 GMT  
		Size: 884.4 KB (884431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64cce274cf151b34375620786ea1d7e23287ff059f4b75d58622ebabed23de7`  
		Last Modified: Wed, 14 Mar 2018 23:13:51 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c067c4522874cd9b08c8d17c6b717878e37b855cf6fc7030e381d9b8e2c7ae`  
		Last Modified: Wed, 14 Mar 2018 23:13:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49357f43f509c3aa08db422b07bfa26f9b1d30e8be4da63c8c73067c54b59758`  
		Last Modified: Tue, 20 Mar 2018 10:36:57 GMT  
		Size: 141.7 MB (141672814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bea645330fa2a57a0969ca59233cdbac94c33af0cf82cff4a658ca79e979474`  
		Last Modified: Tue, 20 Mar 2018 10:36:22 GMT  
		Size: 272.2 KB (272222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d2d062d4b482d7e07a7c0aba730d37d8380c0d8e011ea82973e8ca1e83c475`  
		Last Modified: Tue, 24 Apr 2018 08:55:32 GMT  
		Size: 17.6 MB (17558021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28290b863c1d9a6b1dc5627e6aacb2bc93a5d40d9731f0093434c76195a2f97`  
		Last Modified: Tue, 24 Apr 2018 08:55:30 GMT  
		Size: 3.9 MB (3891484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.9.0.375` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9541649c431fe4408f2a33935793dc73c587e0294a2ac74bcd319bbec90c1b7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285510630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7148f36fac14b79cb214c8d147bf810ecd5344386b51521aa31cf73c29e268ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 14 Mar 2018 17:30:57 GMT
ADD file:2ebfda145008a73d7d0f2dc29946bfc3ad65048b3a3f0ca0283263e413b692d4 in / 
# Wed, 14 Mar 2018 17:30:58 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:46:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Mar 2018 18:48:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 20:43:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 20:43:45 GMT
ENV LANG=C.UTF-8
# Wed, 14 Mar 2018 20:43:53 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 14 Mar 2018 20:43:57 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 14 Mar 2018 20:43:58 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 20 Mar 2018 10:55:32 GMT
ENV JAVA_VERSION=8u162
# Tue, 20 Mar 2018 10:55:33 GMT
ENV JAVA_DEBIAN_VERSION=8u162-b12-1~deb9u1
# Tue, 20 Mar 2018 10:55:33 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 20 Mar 2018 11:03:44 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 20 Mar 2018 11:04:04 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 24 Apr 2018 08:44:47 GMT
LABEL maintainer=Kirill Chernyshov <delaguardo@gmail.com>
# Tue, 24 Apr 2018 08:44:48 GMT
ENV CLOJURE_VERSION=1.9.0.375
# Tue, 24 Apr 2018 08:44:48 GMT
WORKDIR /tmp
# Tue, 24 Apr 2018 08:44:54 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh     && chmod +x linux-install-$CLOJURE_VERSION.sh     && ./linux-install-$CLOJURE_VERSION.sh
# Tue, 24 Apr 2018 08:45:10 GMT
RUN clojure -e "(clojure-version)"
```

-	Layers:
	-	`sha256:3476b6ec1aa77d47beaf22adc259097130bcc9eec853636fb1dcf4f5c2925a56`  
		Last Modified: Wed, 14 Mar 2018 17:45:20 GMT  
		Size: 42.9 MB (42907825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7dbcb22e5d9d968cd5d78dfb96bf92704a665b3d1710483048568abd1ba5b`  
		Last Modified: Wed, 14 Mar 2018 19:05:19 GMT  
		Size: 10.1 MB (10066603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8835ddfb1ea03693a4eb69d729fa15c982207e1518c3dd84f76336f920f9d`  
		Last Modified: Wed, 14 Mar 2018 19:05:18 GMT  
		Size: 4.1 MB (4087845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bade4a02b1a0af4c7b52bcd066c9d44034d712a06638e6e7dbb69c1127476aa9`  
		Last Modified: Wed, 14 Mar 2018 19:06:15 GMT  
		Size: 48.0 MB (47982966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017f2ff0740b0d2ee580e3e7cf9a3c5635e3510c54742d69bba7585c89fce020`  
		Last Modified: Wed, 14 Mar 2018 21:43:05 GMT  
		Size: 877.4 KB (877402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fea043b76dc779a9046b59c75f8354f9429bc318f291db53d8b103285e7c1e6`  
		Last Modified: Wed, 14 Mar 2018 21:43:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacb32a77f7b3a9290a2abe2735de8740c90d0cf3d62aa97267121dbed290cbc`  
		Last Modified: Wed, 14 Mar 2018 21:43:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df99662177ee893da701e714d6dc22d9a462d2fb7cdb5c2aa5315690b9e5d891`  
		Last Modified: Tue, 20 Mar 2018 12:12:46 GMT  
		Size: 157.9 MB (157866119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40498775571f78f58e2b1f63299b42e3ac873659fefcde3ee47ac84975fa9952`  
		Last Modified: Tue, 20 Mar 2018 12:11:58 GMT  
		Size: 272.1 KB (272135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92d3be3afa8e7b05a079e9ede9780183c60ed20c08158dfbaa2e7e0b84959ea`  
		Last Modified: Tue, 24 Apr 2018 08:49:32 GMT  
		Size: 17.6 MB (17557957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363e90cb272c1352448583c32268758b3a4ab42cf1f384f864c89db73dba357e`  
		Last Modified: Tue, 24 Apr 2018 08:49:29 GMT  
		Size: 3.9 MB (3891399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.9.0.375` - linux; 386

```console
$ docker pull clojure@sha256:588abb36f19c009006f56e001768951148a1bc476941b190a81749b87dba9403
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310992501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3ebd5b53fb343a5d8fe2573fd591fc9baa31e5133d3b57b548565609359b32`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Mar 2018 15:59:32 GMT
ADD file:3a8e11cd900f3ac48c7d30158b5a85e65d78680861eb910888c20ef4ae42756f in / 
# Tue, 27 Mar 2018 15:59:33 GMT
CMD ["bash"]
# Fri, 13 Apr 2018 22:13:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Apr 2018 22:13:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 13 Apr 2018 22:14:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 14 Apr 2018 02:57:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 14 Apr 2018 02:57:48 GMT
ENV LANG=C.UTF-8
# Sat, 14 Apr 2018 02:57:49 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 14 Apr 2018 02:57:49 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 14 Apr 2018 02:57:49 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 14 Apr 2018 02:57:50 GMT
ENV JAVA_VERSION=8u162
# Sat, 14 Apr 2018 02:57:50 GMT
ENV JAVA_DEBIAN_VERSION=8u162-b12-1~deb9u1
# Sat, 14 Apr 2018 02:57:50 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Sat, 14 Apr 2018 02:58:46 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 14 Apr 2018 02:58:48 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 24 Apr 2018 11:12:54 GMT
LABEL maintainer=Kirill Chernyshov <delaguardo@gmail.com>
# Tue, 24 Apr 2018 11:12:54 GMT
ENV CLOJURE_VERSION=1.9.0.375
# Tue, 24 Apr 2018 11:12:54 GMT
WORKDIR /tmp
# Tue, 24 Apr 2018 11:12:57 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh     && chmod +x linux-install-$CLOJURE_VERSION.sh     && ./linux-install-$CLOJURE_VERSION.sh
# Tue, 24 Apr 2018 11:13:04 GMT
RUN clojure -e "(clojure-version)"
```

-	Layers:
	-	`sha256:bebcce41445a0be67e63665c298f73217c532640d75de97624d019429de2dd93`  
		Last Modified: Thu, 15 Mar 2018 01:29:27 GMT  
		Size: 45.8 MB (45843420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af42cc296b8123184d1dd96e7066479319ac82b0deeef7c39eeb72cd9acf7eb`  
		Last Modified: Fri, 13 Apr 2018 22:31:55 GMT  
		Size: 11.2 MB (11151403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdce8568bfceab7fd8a5b9e3ed360d35113c4029501d684938ed686c50824f3`  
		Last Modified: Fri, 13 Apr 2018 22:31:53 GMT  
		Size: 4.6 MB (4554687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144ab27aa9f62df613b67603bb22e2ee0753d87a202961681483ecaa2ed4614e`  
		Last Modified: Fri, 13 Apr 2018 22:32:33 GMT  
		Size: 51.6 MB (51553527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c3dba506887dbcfbd2473b504e5cd3cb787478c0e92738aec9df406398c32f`  
		Last Modified: Sat, 14 Apr 2018 03:20:45 GMT  
		Size: 899.8 KB (899799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace77a6f8572e42bf7a3926066c510937294adb65d7c2501f87b827a95e220a`  
		Last Modified: Sat, 14 Apr 2018 03:20:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6283dc389b8615d990b483b4acc7c89e551ae35a5d3b745c23bb6e947873fa1b`  
		Last Modified: Sat, 14 Apr 2018 03:20:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bacaac48e14c4491c7ef2dacc52eee361fc2fc17696abde2ad8ba048b79bb50`  
		Last Modified: Sat, 14 Apr 2018 03:21:28 GMT  
		Size: 175.3 MB (175267769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c351f81880cdd1d397a28f01011b280018658a0b8551c7d88cf3b1bac993c06`  
		Last Modified: Sat, 14 Apr 2018 03:20:45 GMT  
		Size: 272.2 KB (272157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3050f3a07994305d6caf35bfa6c0750d61950697f29bd2c2d93f3b84de586ab4`  
		Last Modified: Tue, 24 Apr 2018 11:13:26 GMT  
		Size: 17.6 MB (17557972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0033a166db0d482701eea2cef20c13fc18d1b9f46b8978df963b85c78d827225`  
		Last Modified: Tue, 24 Apr 2018 11:13:25 GMT  
		Size: 3.9 MB (3891388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.9.0.375` - linux; ppc64le

```console
$ docker pull clojure@sha256:413a0e0882821d3d82890be552c1d7feb405e37e676f02d815034fde92ca03fd
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.2 MB (294182281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95984397b858f632af6595c5f5c1e9a5db1a18878a2db18f67985916e086cf0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 14 Mar 2018 00:34:58 GMT
ADD file:cd28b9ad859ce13c0d4fee241178bba68cc8f696eb1722a67ac3c62c2c64e087 in / 
# Wed, 14 Mar 2018 00:34:59 GMT
CMD ["bash"]
# Thu, 15 Mar 2018 02:11:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Mar 2018 02:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 02:14:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Mar 2018 04:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Mar 2018 04:58:57 GMT
ENV LANG=C.UTF-8
# Thu, 15 Mar 2018 04:59:02 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Mar 2018 04:59:10 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Mar 2018 04:59:13 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 20 Mar 2018 11:50:40 GMT
ENV JAVA_VERSION=8u162
# Tue, 20 Mar 2018 11:50:41 GMT
ENV JAVA_DEBIAN_VERSION=8u162-b12-1~deb9u1
# Tue, 20 Mar 2018 11:50:42 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 20 Mar 2018 11:57:10 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 20 Mar 2018 11:57:15 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 24 Apr 2018 08:22:05 GMT
LABEL maintainer=Kirill Chernyshov <delaguardo@gmail.com>
# Tue, 24 Apr 2018 08:22:06 GMT
ENV CLOJURE_VERSION=1.9.0.375
# Tue, 24 Apr 2018 08:22:07 GMT
WORKDIR /tmp
# Tue, 24 Apr 2018 08:22:11 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh     && chmod +x linux-install-$CLOJURE_VERSION.sh     && ./linux-install-$CLOJURE_VERSION.sh
# Tue, 24 Apr 2018 08:22:22 GMT
RUN clojure -e "(clojure-version)"
```

-	Layers:
	-	`sha256:1743854d776e01d7f49a30bb37dbbfb45e788dc99753cb027de750d2da47a89c`  
		Last Modified: Wed, 14 Mar 2018 00:42:50 GMT  
		Size: 45.4 MB (45377043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbff2499a166062800d8b7dc1a9f296fa4faea9e6fd79d6bab7f93bcc5e98a9a`  
		Last Modified: Thu, 15 Mar 2018 02:32:22 GMT  
		Size: 10.3 MB (10339816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c89f7b09fa962405ed41f0799ecc73d66a91b8ba2fde1dbd5ebd4d4e10deb8`  
		Last Modified: Thu, 15 Mar 2018 02:32:21 GMT  
		Size: 4.3 MB (4289466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8e6651c19a7ccc1b425e4054dddb7bae76e0e0c2b27d8fd9a44fb94408f6ce`  
		Last Modified: Thu, 15 Mar 2018 02:32:53 GMT  
		Size: 50.0 MB (50029116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8229185339443bc19193ef5ba90c302d96c018a844c3bd63bdf2a946bb8fb34`  
		Last Modified: Thu, 15 Mar 2018 06:07:28 GMT  
		Size: 886.1 KB (886149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddfd19e4e1ad45639af851b678bc8b13f2bc77c4812b94cd484a1f2784bfdfd`  
		Last Modified: Thu, 15 Mar 2018 06:07:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b121b24996481e8e11d09dedd0a5b46ecf04108c7396005302353b060ec187`  
		Last Modified: Thu, 15 Mar 2018 06:07:27 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974da1069adc28b0ee6a97c45bb8a91d72c47edf8b6e16db472b7402ba058d7f`  
		Last Modified: Tue, 20 Mar 2018 12:19:58 GMT  
		Size: 161.5 MB (161538734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8572cce38bfa10a0f76bedf84d4e38a29419c60055f61b1feec19d3634756b9`  
		Last Modified: Tue, 20 Mar 2018 12:19:19 GMT  
		Size: 272.1 KB (272097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1831379366c3ec7c6ca6875ec801d02f76cc85e77ce85aed923b18734409b8e`  
		Last Modified: Tue, 24 Apr 2018 08:23:48 GMT  
		Size: 17.6 MB (17558023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d049e83946944fc49ad40aabfe44be8e93f69829ed80d749e03a5f49bea04828`  
		Last Modified: Tue, 24 Apr 2018 08:23:46 GMT  
		Size: 3.9 MB (3891456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip