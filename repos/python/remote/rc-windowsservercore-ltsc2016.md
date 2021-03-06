## `python:rc-windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:a96c111c888815a3b21b4801bd659d24bd860f665f46ed57d9c3f23a4002f09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2189; amd64

### `python:rc-windowsservercore-ltsc2016` - windows version 10.0.14393.2189; amd64

```console
$ docker pull python@sha256:be1c519aa7e9015d4afb9978096666823dc869e76671e4e70baa7cb74dabe4d2
```

-	Docker Version: 17.10.0-ee-preview-3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 GB (5457006946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef520e5fee67ff29fcc91339906ceab77db72bc9e29041fdfba632068c9f8dd`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Fri, 06 Apr 2018 21:38:52 GMT
RUN Install update 10.0.14393.2189
# Fri, 27 Apr 2018 09:14:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 05 May 2018 09:14:25 GMT
ENV PYTHON_VERSION=3.7.0b4
# Sat, 05 May 2018 09:14:26 GMT
ENV PYTHON_RELEASE=3.7.0
# Sat, 05 May 2018 09:17:54 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.';
# Sat, 05 May 2018 09:17:55 GMT
ENV PYTHON_PIP_VERSION=10.0.1
# Sat, 05 May 2018 09:19:36 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Sat, 05 May 2018 09:19:38 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f3369c32b2e3183340664c2bd4babb9c71cedc116fba70fda326df3ef9e48cc`  
		Last Modified: Fri, 06 Apr 2018 21:38:52 GMT  
		Size: 1.3 GB (1324227515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a34e69c38a84789216f85ca14f1cd2fd80f3bf47f351a2a3130f2b3241a8db39`  
		Last Modified: Fri, 27 Apr 2018 09:24:43 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52870c3cafc17b357e83ad6b9b43740463b48beb97fbce492eb406030c60a55f`  
		Last Modified: Sat, 05 May 2018 09:34:31 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9090b73f34135ccdcd822f2196d88aebdd435a3b1b9f121c51ae8863ea055b`  
		Last Modified: Sat, 05 May 2018 09:34:28 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac792613e0d9df72c5187509bf8bff50c71deef35adc964bf3d8f34231ac0bb`  
		Last Modified: Sat, 05 May 2018 09:34:53 GMT  
		Size: 53.0 MB (53045304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85de32fbab6101cf34aa184a9da90fb9fcaa5f0541bdc5cb9ad6957dc7348de`  
		Last Modified: Sat, 05 May 2018 09:34:27 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10b846df36671e5f1c2b7aebda3ce95ccbcb88589a10b685dcb7e8240f6bbe7`  
		Last Modified: Sat, 05 May 2018 09:34:38 GMT  
		Size: 9.7 MB (9742244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f377412e9cc67275652a1dc05f18adafce571f0550956e9c101c372d5203be53`  
		Last Modified: Sat, 05 May 2018 09:34:28 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
