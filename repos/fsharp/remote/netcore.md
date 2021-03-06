## `fsharp:netcore`

```console
$ docker pull fsharp@sha256:97085039bc6b699b76f4f955eeb444fb54557d798bc3878603b7dfcbba9f21bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:859717e4a0974efda776827e06c704414ba9dea4c603a65404989e61f945485b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.8 MB (627811379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a556e38786def3aa662c334cfeb7fc8b3d56fb71426287ea57b1545da9f9e7`
-	Default Command: `["fsharpi"]`

```dockerfile
# Sat, 28 Apr 2018 07:09:59 GMT
ADD file:ec5be7eec56a749752ca284359ece04f5eb0b981eac08b8855454c6b16e3893c in / 
# Sat, 28 Apr 2018 07:09:59 GMT
CMD ["bash"]
# Sat, 05 May 2018 04:33:41 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Sat, 05 May 2018 04:33:42 GMT
ENV MONO_THREADS_PER_CPU=50
# Sat, 05 May 2018 04:41:49 GMT
RUN MONO_VERSION=5.8.0.127 &&     FSHARP_VERSION=10.0.2 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stretch/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get install -y apt-transport-https &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Sat, 05 May 2018 04:41:49 GMT
WORKDIR /root
# Sat, 05 May 2018 04:41:50 GMT
CMD ["fsharpi"]
# Sat, 05 May 2018 04:53:10 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Sat, 05 May 2018 04:53:10 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.6.2-api/
# Sat, 05 May 2018 04:53:10 GMT
ENV NUGET_XMLDOC_MODE=skip
# Sat, 05 May 2018 04:53:18 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl3     libgcc1     libgssapi-krb5-2     libicu57     liblttng-ust0     libssl1.0.2     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Sat, 05 May 2018 04:53:28 GMT
RUN DOTNET_SDK_VERSION=2.1.104 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=813334694667f8c1389d88cd3128a7749f4f65b13a0a8e2cb47380823849b8fe7f4816ab66c2d77e589fac9cb5748390b262beae9673aef86cad5a3d8f24986e &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Sat, 05 May 2018 04:53:28 GMT
ENV DOTNET_CLI_TELEMETRY_OPTOUT=1
# Sat, 05 May 2018 04:54:01 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Sat, 05 May 2018 04:54:02 GMT
WORKDIR /root
```

-	Layers:
	-	`sha256:f2aa67a397c49232112953088506d02074a1fe577f65dc2052f158a3e5da52e8`  
		Last Modified: Sat, 28 Apr 2018 09:31:20 GMT  
		Size: 22.5 MB (22496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e914d22f23b3d6c1fbab26820f91cf3a79f765cc384d9871e7eb6889d9612df`  
		Last Modified: Sat, 05 May 2018 04:54:48 GMT  
		Size: 132.5 MB (132511477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b3bb49ef6076b67c258041c62226e313430343cbc093af1c5acb3b62510b01`  
		Last Modified: Sat, 05 May 2018 04:56:07 GMT  
		Size: 18.0 MB (17997623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d6ca0a2013c1f40e1a3d23e960c1b562e64877e76903b21a499ca00443d857`  
		Last Modified: Sat, 05 May 2018 04:56:30 GMT  
		Size: 164.3 MB (164322392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab00ba4cbd6981b81204951818f6e9ecff92e61fd079d6ca9b72aa3ca4b1ffd`  
		Last Modified: Sat, 05 May 2018 04:56:51 GMT  
		Size: 290.5 MB (290483858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
