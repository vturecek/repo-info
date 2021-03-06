## `jenkins:latest`

```console
$ docker pull jenkins@sha256:00bc27808eb97fe90d914ef51724d944b975d0f9eee105e11c5cda8ee379a401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jenkins:latest` - linux; amd64

```console
$ docker pull jenkins@sha256:d1ae4069eefb1caa739bd403e8ee365ce34d988184b32dc4a2a1a74774d20878
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355122840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f178e3827f07ff27ed551cb10e48bfe0238f7b918dd73ea96cc6d2cb48bbb78`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/jenkins.sh"]`

```dockerfile
# Sat, 28 Apr 2018 07:08:53 GMT
ADD file:9572fdb59dfbb9b032f3331bbc2a08b31e0aef5fbde44c8f2008d22bf5290cf2 in / 
# Sat, 28 Apr 2018 07:08:53 GMT
CMD ["bash"]
# Fri, 04 May 2018 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 04 May 2018 17:41:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 04 May 2018 17:41:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 04 May 2018 23:53:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 04 May 2018 23:53:28 GMT
ENV LANG=C.UTF-8
# Fri, 04 May 2018 23:53:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 04 May 2018 23:53:29 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 04 May 2018 23:53:29 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 04 May 2018 23:53:30 GMT
ENV JAVA_VERSION=8u171
# Fri, 04 May 2018 23:53:30 GMT
ENV JAVA_DEBIAN_VERSION=8u171-b11-1~deb9u1
# Fri, 04 May 2018 23:53:30 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 04 May 2018 23:54:10 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 04 May 2018 23:54:13 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 05 May 2018 08:19:35 GMT
RUN apt-get update && apt-get install -y git curl && rm -rf /var/lib/apt/lists/*
# Sat, 05 May 2018 08:19:35 GMT
ARG user=jenkins
# Sat, 05 May 2018 08:19:35 GMT
ARG group=jenkins
# Sat, 05 May 2018 08:19:35 GMT
ARG uid=1000
# Sat, 05 May 2018 08:19:35 GMT
ARG gid=1000
# Sat, 05 May 2018 08:19:36 GMT
ARG http_port=8080
# Sat, 05 May 2018 08:19:36 GMT
ARG agent_port=50000
# Sat, 05 May 2018 08:19:36 GMT
ENV JENKINS_HOME=/var/jenkins_home
# Sat, 05 May 2018 08:19:36 GMT
ENV JENKINS_SLAVE_AGENT_PORT=50000
# Sat, 05 May 2018 08:19:37 GMT
# ARGS: agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN groupadd -g ${gid} ${group}     && useradd -d "$JENKINS_HOME" -u ${uid} -g ${gid} -m -s /bin/bash ${user}
# Sat, 05 May 2018 08:19:37 GMT
VOLUME [/var/jenkins_home]
# Sat, 05 May 2018 08:19:38 GMT
# ARGS: agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN mkdir -p /usr/share/jenkins/ref/init.groovy.d
# Sat, 05 May 2018 08:19:38 GMT
ENV TINI_VERSION=0.14.0
# Sat, 05 May 2018 08:19:39 GMT
ENV TINI_SHA=6c41ec7d33e857d4779f14d9c74924cab0c7973485d2972419a3b7c7620ff5fd
# Sat, 05 May 2018 08:19:42 GMT
# ARGS: agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN curl -fsSL https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-static-amd64 -o /bin/tini && chmod +x /bin/tini   && echo "$TINI_SHA  /bin/tini" | sha256sum -c -
# Sat, 05 May 2018 08:19:42 GMT
COPY file:c629bc0b9ecb5b7233000c973f65721df4ce1307a5d5b33ac3871ff61a9172ff in /usr/share/jenkins/ref/init.groovy.d/tcp-slave-agent-port.groovy 
# Sat, 05 May 2018 08:19:43 GMT
ARG JENKINS_VERSION
# Sat, 05 May 2018 08:19:43 GMT
ENV JENKINS_VERSION=2.60.3
# Sat, 05 May 2018 08:19:43 GMT
ARG JENKINS_SHA=2d71b8f87c8417f9303a73d52901a59678ee6c0eefcf7325efed6035ff39372a
# Sat, 05 May 2018 08:19:44 GMT
ARG JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.60.3/jenkins-war-2.60.3.war
# Sat, 05 May 2018 08:19:47 GMT
# ARGS: JENKINS_SHA=2d71b8f87c8417f9303a73d52901a59678ee6c0eefcf7325efed6035ff39372a JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.60.3/jenkins-war-2.60.3.war agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN curl -fsSL ${JENKINS_URL} -o /usr/share/jenkins/jenkins.war   && echo "${JENKINS_SHA}  /usr/share/jenkins/jenkins.war" | sha256sum -c -
# Sat, 05 May 2018 08:19:47 GMT
ENV JENKINS_UC=https://updates.jenkins.io
# Sat, 05 May 2018 08:19:47 GMT
ENV JENKINS_UC_EXPERIMENTAL=https://updates.jenkins.io/experimental
# Sat, 05 May 2018 08:19:48 GMT
# ARGS: JENKINS_SHA=2d71b8f87c8417f9303a73d52901a59678ee6c0eefcf7325efed6035ff39372a JENKINS_URL=https://repo.jenkins-ci.org/public/org/jenkins-ci/main/jenkins-war/2.60.3/jenkins-war-2.60.3.war agent_port=50000 gid=1000 group=jenkins http_port=8080 uid=1000 user=jenkins
RUN chown -R ${user} "$JENKINS_HOME" /usr/share/jenkins/ref
# Sat, 05 May 2018 08:19:48 GMT
EXPOSE 8080/tcp
# Sat, 05 May 2018 08:19:49 GMT
EXPOSE 50000/tcp
# Sat, 05 May 2018 08:19:49 GMT
ENV COPY_REFERENCE_FILE_LOG=/var/jenkins_home/copy_reference_file.log
# Sat, 05 May 2018 08:19:49 GMT
USER [jenkins]
# Sat, 05 May 2018 08:19:50 GMT
COPY file:26c3c5818bc87662d1f4905a3ed73bd55a0a75f731c7dc52d0599c00f51408e9 in /usr/local/bin/jenkins-support 
# Sat, 05 May 2018 08:19:50 GMT
COPY file:1a774b24a2bbd880e2ce47b3d642b8c04bbdbede0f2256dbdb11f62b65f696ba in /usr/local/bin/jenkins.sh 
# Sat, 05 May 2018 08:19:50 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/jenkins.sh"]
# Sat, 05 May 2018 08:19:51 GMT
COPY file:9f0a7faf8951842e0f42c1a3f3bb54ff4ec5263064508077347c57376da68b46 in /usr/local/bin/plugins.sh 
# Sat, 05 May 2018 08:19:51 GMT
COPY file:a4f750618f51f00d2f8268ac43fdd8d8ef5ce16e1d412afa5a9bc7492a5d975f in /usr/local/bin/install-plugins.sh 
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
	-	`sha256:3ec98735f56f2c1ad880156d0c969f405a8aa3077587870396782cbfbc43799d`  
		Last Modified: Fri, 04 May 2018 18:21:13 GMT  
		Size: 50.0 MB (50026250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55160131808f084fc2304dd05f27bbc1870237d9f1b78f94aa57770948f193bf`  
		Last Modified: Sat, 05 May 2018 00:10:11 GMT  
		Size: 892.4 KB (892433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dbacf623ffcaa9a39a8c1afe93ffdbee4b0b0c323c43becf5481605e9b9344`  
		Last Modified: Sat, 05 May 2018 00:10:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8145eb5a3756f6fc5fd37487b97192459ae78be657826ea66a6fe5881262f0b0`  
		Last Modified: Sat, 05 May 2018 00:10:11 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00673c707b5aead8a48acd3a861d70ac201905dde3ad85f7d33758ae8d2c6f1`  
		Last Modified: Sat, 05 May 2018 00:10:44 GMT  
		Size: 172.7 MB (172728116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21012f36779c0a491de043ad71e8bc2adb2c0cd68b488d3f7a3f5fe9b1322a4`  
		Last Modified: Sat, 05 May 2018 00:10:11 GMT  
		Size: 272.1 KB (272109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6152a1d29ac9636574b6940dc428c1e66594ef2c95c5bd49dd45d5fda0636fb`  
		Last Modified: Sat, 05 May 2018 08:20:08 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae434261c51dc7a2b554b84bad27f93f438c31378f074a8104f1a2fb20ba06ee`  
		Last Modified: Sat, 05 May 2018 08:20:06 GMT  
		Size: 4.2 KB (4184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd467134b3f82a2608f64639b4c5a8b76e347c887b65a5be7325c2fe61489b8f`  
		Last Modified: Sat, 05 May 2018 08:20:06 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c96ec9b6a38564102d43c7e18022df77b9a9ddbd6ac261d66056da995e034`  
		Last Modified: Sat, 05 May 2018 08:20:06 GMT  
		Size: 354.8 KB (354772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6548b0bd626df8374f9fd7e0eb74838969b74652d206bc37e5815f93c452f4`  
		Last Modified: Sat, 05 May 2018 08:20:06 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca52754e146ca28afe078332396ebb6e2430983e8fe8fd6f5aef1665ac17b26`  
		Last Modified: Sat, 05 May 2018 08:20:10 GMT  
		Size: 70.4 MB (70409108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dd39aed9546856120cd71127367ef6d9d3b6be6baed63ec3aa370169310299`  
		Last Modified: Sat, 05 May 2018 08:20:03 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfb4b526bcfc082d492f5260f16fbb2e21475b22ba3224466d16295bff087c8`  
		Last Modified: Sat, 05 May 2018 08:20:04 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce5fe5e7bf5e27babcfed6640e223acd7d86c1b09428ce978a9325255adc41`  
		Last Modified: Sat, 05 May 2018 08:20:04 GMT  
		Size: 838.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d14df9562d0478f68bf04707fc7ebbfd31415213603775ac1a7d945f9c36a67`  
		Last Modified: Sat, 05 May 2018 08:20:04 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d050852b0107e6d6d48558d487ba066d9bc0486c24ce6c6bb0677a5e840ddf5`  
		Last Modified: Sat, 05 May 2018 08:20:03 GMT  
		Size: 2.6 KB (2626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
