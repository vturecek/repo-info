## `julia:jessie`

```console
$ docker pull julia@sha256:1139d10a52bdd3e7c5018d870e181bc5bb1414bec1494cf353c4013fbd1e505c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `julia:jessie` - linux; amd64

```console
$ docker pull julia@sha256:b7016c4f6dc365f59e4549b6d30cc7c2c7e42f372a958fb5748c7af69bfb0c82
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128344280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed9a187f7b2124ddb4f786fc1f2773f65d9d80355942cc248083b50dcacf793`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 28 Apr 2018 06:44:15 GMT
ADD file:3e6141c0c9cb74b14a281eb3ab7aaf162a625733e652c3948b323bb2ec8b4343 in / 
# Sat, 28 Apr 2018 06:44:16 GMT
CMD ["bash"]
# Tue, 01 May 2018 07:51:55 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ca-certificates 		curl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 07:51:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 01 May 2018 07:51:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 01 May 2018 07:51:56 GMT
ENV JULIA_VERSION=0.6.2
# Tue, 01 May 2018 07:52:03 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='dc6ec0b13551ce78083a5849268b20684421d46a7ec46b17ec1fab88a5078580' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='1c37aa7cba7372d949a91de53f53609b1b0c9cbeca436eb2fe7f5083d9f62c82' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='19a8945bdb3d35b7bf0432a9e066fb7831d11d1c1acfe56abd8fcabbf1ebddb4' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='099e39ad958aff2ef63841a812f5df62f8553aafc6dd33abb0eb0c67142c5e49' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${JULIA_VERSION%[.-]*}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${JULIA_VERSION%[.-]*}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz
# Tue, 01 May 2018 07:52:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 May 2018 07:52:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d77ce4481b119f00e53bee9b4a443469c42c224db954ddaa2e6b74cd73cd5d0`  
		Last Modified: Sat, 28 Apr 2018 08:24:47 GMT  
		Size: 54.3 MB (54262566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5411096dfd7d336481a27872ed23e3cc959e1f5b5194242489dce7bb1e5e628`  
		Last Modified: Tue, 01 May 2018 07:52:35 GMT  
		Size: 5.1 MB (5069014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34c2c6923ecab08f8e3d67f847e7df3c77a809894f5b987345271a6f9f78910`  
		Last Modified: Tue, 01 May 2018 07:52:48 GMT  
		Size: 69.0 MB (69012700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
