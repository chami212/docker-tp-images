## docker build -t mon_app_python
## docker build -t mon_app_python .
## docker run -p 5000:5000 mon_app_python
## docker run -d -p 5000:5000 mon_app_python
## docker build -t hello-flask:1.0.0 .
## docker rm 4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3
## docker rm -f 4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3
## docker run -d -p 5000:5000 hello-flask:1.0.0
## docker tag hello-flask:1.0.0 hello-flask:latest
## docker images

j'ai pu faire quelques commandes inutiles pour des tests et apprentissages






--- Console complète :








## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker build -t mon_app_python
ERROR: docker: 'docker buildx build' requires 1 argument

Usage:  docker buildx build [OPTIONS] PATH | URL | -

Run 'docker buildx build --help' for more information
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker build -t mon_app_python .
[+] Building 9.3s (10/10) FINISHED                                                                                         docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                       0.1s
 => => transferring dockerfile: 431B                                                                                                       0.0s
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                                        1.4s 
 => [internal] load .dockerignore                                                                                                          0.0s
 => => transferring context: 34B                                                                                                           0.0s 
 => [1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                  3.5s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                  0.0s 
 => => sha256:b9aab63c297c3a972f524d3f3c0c233d0f94720171fbe3b87e4adcb62acd8a9c 251B / 251B                                                 0.2s 
 => => sha256:5d7ccc6599a695634322e0346af751966d90030beb8b260c5af2b16dcc03d52e 12.11MB / 12.11MB                                           0.9s
 => => sha256:30dad65d3b2447a6e75deb634f85b4ca34d5f9a6e920f9f9c0bb916abafd965a 1.29MB / 1.29MB                                             0.5s 
 => => sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419 29.78MB / 29.78MB                                           1.6s 
 => => extracting sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419                                                  1.0s 
 => => extracting sha256:30dad65d3b2447a6e75deb634f85b4ca34d5f9a6e920f9f9c0bb916abafd965a                                                  0.2s 
 => => extracting sha256:5d7ccc6599a695634322e0346af751966d90030beb8b260c5af2b16dcc03d52e                                                  0.6s 
 => => extracting sha256:b9aab63c297c3a972f524d3f3c0c233d0f94720171fbe3b87e4adcb62acd8a9c                                                  0.0s 
 => [internal] load build context                                                                                                          0.1s 
 => => transferring context: 319B                                                                                                          0.0s 
 => [2/5] WORKDIR /app                                                                                                                     0.2s 
 => [3/5] COPY requirements.txt .                                                                                                          0.0s 
 => [4/5] COPY app.py .                                                                                                                    0.0s 
 => [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                                               2.3s 
 => exporting to image                                                                                                                     1.2s 
 => => exporting layers                                                                                                                    0.7s 
 => => exporting manifest sha256:590f217f913213b3d3a249224e0326d8776e7f5aa683896ba132fb408b362ede                                          0.0s 
 => => exporting config sha256:8d0afb217fe00d5dea5f4f1f72429b6bf6b71ca882b9adcdadd851316c9e40e0                                            0.0s 
 => => exporting attestation manifest sha256:e4b8fe0c567968774c87064080293a98db5f84237184b22ffac7958fb12b6ec6                              0.0s 
 => => exporting manifest list sha256:86f2a8bc2296a19fca1fe4c0bedd3c1b614446cad16375b4b7f89f638a7d1ddf                                     0.0s 
 => => naming to docker.io/library/mon_app_python:latest                                                                                   0.0s 
 => => unpacking to docker.io/library/mon_app_python:latest                                                                                0.4s 
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker run -p 5000:5000 mon_app_python
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://172.17.0.2:5000
Press CTRL+C to quit
172.17.0.1 - - [06/Mar/2026 13:27:07] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [06/Mar/2026 13:27:07] "GET /favicon.ico HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 13:27:07] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 13:27:10] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [06/Mar/2026 13:27:10] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 13:27:13] "GET /.well-known/appspecific/com.chrome.devtools.json HTTP/1.1" 404 -
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker run -d -p 5000:5000 mon_app_python
4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker build -t hello-flask:1.0.0 .
>> docker rm 4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3
[+] Building 0.9s (10/10) FINISHED                                                                        docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                      0.0s
 => => transferring dockerfile: 205B                                                                                      0.0s 
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                       0.6s 
 => [internal] load .dockerignore                                                                                         0.0s
 => => transferring context: 66B                                                                                          0.0s 
 => [1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf  0.0s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf  0.0s 
 => [internal] load build context                                                                                         0.0s 
 => => transferring context: 63B                                                                                          0.0s
 => CACHED [2/5] WORKDIR /app                                                                                             0.0s 
 => CACHED [3/5] COPY requirements.txt .                                                                                  0.0s 
 => CACHED [4/5] COPY app.py .                                                                                            0.0s 
 => CACHED [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                       0.0s 
 => exporting to image                                                                                                    0.1s 
 => => exporting layers                                                                                                   0.0s 
 => => exporting manifest sha256:590f217f913213b3d3a249224e0326d8776e7f5aa683896ba132fb408b362ede                         0.0s 
 => => exporting config sha256:8d0afb217fe00d5dea5f4f1f72429b6bf6b71ca882b9adcdadd851316c9e40e0                           0.0s 
 => => exporting attestation manifest sha256:db9a0a8438c2f35bc8b7da4299dded3335d8c47e01f28a6faff1b0a338fd5d4d             0.0s 
 => => exporting manifest list sha256:0ad5e6ffe6b4f5294ddc8c3fae7f2d3ffc6cc20409b641b0102d869f40780583                    0.0s 
 => => naming to docker.io/library/hello-flask:1.0.0                                                                      0.0s 
 => => unpacking to docker.io/library/hello-flask:1.0.0                                                                   0.0s 
Error response from daemon: cannot remove container "4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3": container is running: stop the container before removing or force remove
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker build -t hello-flask:1.0.0 .
>> docker rm -f 4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3
[+] Building 0.5s (10/10) FINISHED                                                                        docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                      0.0s
 => => transferring dockerfile: 205B                                                                                      0.0s 
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                       0.2s 
 => [internal] load .dockerignore                                                                                         0.0s
 => => transferring context: 66B                                                                                          0.0s 
 => [1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf  0.0s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf  0.0s 
 => [internal] load build context                                                                                         0.0s 
 => => transferring context: 63B                                                                                          0.0s
 => CACHED [2/5] WORKDIR /app                                                                                             0.0s 
 => CACHED [3/5] COPY requirements.txt .                                                                                  0.0s 
 => CACHED [4/5] COPY app.py .                                                                                            0.0s 
 => CACHED [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                       0.0s 
 => exporting to image                                                                                                    0.1s 
 => => exporting layers                                                                                                   0.0s 
 => => exporting manifest sha256:590f217f913213b3d3a249224e0326d8776e7f5aa683896ba132fb408b362ede                         0.0s 
 => => exporting config sha256:8d0afb217fe00d5dea5f4f1f72429b6bf6b71ca882b9adcdadd851316c9e40e0                           0.0s 
 => => exporting attestation manifest sha256:709586930e6903155fb3e691b8d613aea69b84f622ff5629950420c434cb9643             0.0s 
 => => exporting manifest list sha256:ce4b1278d2f0b780748f9ab8181245e9bd7f0291df9f4837a4f0fc45bc4b26d1                    0.0s 
 => => naming to docker.io/library/hello-flask:1.0.0                                                                      0.0s 
 => => unpacking to docker.io/library/hello-flask:1.0.0                                                                   0.0s 
4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker build -t hello-flask:1.0.0 .
>> docker rm 4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3   
[+] Building 0.6s (10/10) FINISHED                                                                        docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                      0.0s
 => => transferring dockerfile: 205B                                                                                      0.0s 
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                       0.2s 
 => [internal] load .dockerignore                                                                                         0.0s
 => => transferring context: 66B                                                                                          0.0s 
 => [1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf  0.0s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf  0.0s 
 => [internal] load build context                                                                                         0.0s 
 => => transferring context: 63B                                                                                          0.0s
 => CACHED [2/5] WORKDIR /app                                                                                             0.0s 
 => CACHED [3/5] COPY requirements.txt .                                                                                  0.0s 
 => CACHED [4/5] COPY app.py .                                                                                            0.0s 
 => CACHED [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                       0.0s 
 => exporting to image                                                                                                    0.1s 
 => => exporting layers                                                                                                   0.0s 
 => => exporting manifest sha256:590f217f913213b3d3a249224e0326d8776e7f5aa683896ba132fb408b362ede                         0.0s 
 => => exporting config sha256:8d0afb217fe00d5dea5f4f1f72429b6bf6b71ca882b9adcdadd851316c9e40e0                           0.0s 
 => => exporting attestation manifest sha256:6547d7e02469c27565c0a268a34658149cd54e22c7ee9087b27281c109cb3b16             0.0s 
 => => exporting manifest list sha256:e31129edc84218a08521ab9b9ebce2afebe7fb8b223a2ffde2280dcc8ec92844                    0.0s 
 => => naming to docker.io/library/hello-flask:1.0.0                                                                      0.0s 
 => => unpacking to docker.io/library/hello-flask:1.0.0                                                                   0.0s 
Error response from daemon: No such container: 4b4d860fd1a48c8d38dfb1c960d31db08b0ac610eacd27535ba76147b9e907d3
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker run -d -p 5000:5000 hello-flask:1.0.0
b42ab8b948eef22968e8b901a83230d97ef2f843cd7ba029fd4ca19130cbd325
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker tag hello-flask:1.0.0 hello-flask:latest
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> docker images
REPOSITORY                                TAG       IMAGE ID       CREATED         SIZE
mon_app_python                            latest    86f2a8bc2296   9 minutes ago   197MB
hello-flask                               1.0.0     e31129edc842   9 minutes ago   197MB
hello-flask                               latest    e31129edc842   9 minutes ago   197MB
kalilinux/kali-rolling                    latest    8913de4b58ee   4 months ago    192MB
anssi/fcsc2024-pwn-blind-attack           latest    f367da0196ef   22 months ago   14.8MB
anssi/fcsc2024-pwn-blind-attack-shovel    latest    69ba9950856b   22 months ago   212MB
anssi/fcsc2021-web-push-it-to-the-limit   latest    3377a2e2dc8e   2 years ago     647MB
tleemcjr/metasploitable2                  latest    e559450b37dc   8 years ago     2.3GB
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-1-flask> 