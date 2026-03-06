## docker build -t chami59212/stats-api:1.0.0 .
## docker run -p 8080:8080 chami59212/stats-api:1.0.0
## docker push chami59212/stats-api:1.0.0
## docker build -t chami59212/stats-api:2.0.0 .
## docker push chami59212/stats-api:2.0.0
## docker run -p 8080:8080 chami59212/stats-api:2.0.0
## docker tag chami59212/stats-api:2.0.0 chami59212/stats-api:latest
## docker push chami59212/stats-api:latest
## docker pull chami59212/stats-api:1.0.0 pour la premiere version uniquement
## docker images 
pour voir la taille des images et celles présentes



PS C:\WINDOWS\System32> Invoke-RestMethod -Uri http://localhost:8080/api/stats `
>>   -Method POST `
>>   -ContentType "application/json" `
>>   -Body '{"numbers":[3,5,7]}'


average : 5,0
count   : 3
max     : 7
min     : 3
sum     : 15

PS C:\WINDOWS\System32> Invoke-RestMethod `
>>     -Uri http://localhost:8080/api/stats/median `
>>     -Method POST `
>>     -ContentType "application/json" `
>>     -Body '{"numbers":[3,5,7,9]}'

median
------
   6,0


PS C:\WINDOWS\System32>


## docker images

chami59212/stats-api                      2.0.0     81614ead6ceb   10 minutes ago      186MB
chami59212/stats-api                      latest    81614ead6ceb   10 minutes ago      186MB
chami59212/stats-api                      1.0.0     314a0ee84b70   48 minutes ago      202MB




Console complète : 






PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker build -t chami59212/stats-api:1.0.0
ERROR: docker: 'docker buildx build' requires 1 argument

Usage:  docker buildx build [OPTIONS] PATH | URL | -

Run 'docker buildx build --help' for more information
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker build -t chami59212/stats-api:1.0.0 .
[+] Building 5.8s (11/11) FINISHED                                                                                                                           docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                                                         0.0s
 => => transferring dockerfile: 205B                                                                                                                                         0.0s
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                                                                          0.7s
 => [auth] library/python:pull token for registry-1.docker.io                                                                                                                0.0s
 => [internal] load .dockerignore                                                                                                                                            0.0s
 => => transferring context: 2B                                                                                                                                              0.0s 
 => [1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                                    0.0s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                                    0.0s 
 => [internal] load build context                                                                                                                                            0.0s 
 => => transferring context: 656B                                                                                                                                            0.0s 
 => CACHED [2/5] WORKDIR /app                                                                                                                                                0.0s
 => [3/5] COPY requirements.txt .                                                                                                                                            0.0s 
 => [4/5] COPY app.py .                                                                                                                                                      0.1s 
 => [5/5] RUN pip install --no-cache-dir -r requirements.txt                                                                                                                 3.1s 
 => exporting to image                                                                                                                                                       1.3s 
 => => exporting layers                                                                                                                                                      0.7s 
 => => exporting manifest sha256:b0e446bcff085b9046afd536a9a72ea435e455faaf6fe49526d1046c372b372c                                                                            0.0s 
 => => exporting config sha256:fd10d13063da213612b4ff45854e9651f4f2aae0bfe7dc3fd04a4d5453321d97                                                                              0.0s 
 => => exporting attestation manifest sha256:9a8d52829340f932839dad07f04e3a9450da5cdf2f500fa23c1c50b4307ebd22                                                                0.0s 
 => => exporting manifest list sha256:314a0ee84b70201d59995251007e4228133373d2772d855f6ef060ae5e41a949                                                                       0.0s 
 => => naming to docker.io/chami59212/stats-api:1.0.0                                                                                                                        0.0s 
 => => unpacking to docker.io/chami59212/stats-api:1.0.0                                                                                                                     0.4s 
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker push chami59212/stats-api:1.0.0      
The push refers to repository [docker.io/chami59212/stats-api]
206356c42440: Pushed
b9aab63c297c: Pushed
5d7ccc6599a6: Pushed
b5e154c70e9e: Pushed
8acb589c3650: Pushed
239a80453a37: Pushed
2de25aa7d3dc: Pushed
2b5834023cc3: Pushed
30dad65d3b24: Pushed
1.0.0: digest: sha256:314a0ee84b70201d59995251007e4228133373d2772d855f6ef060ae5e41a949 size: 856
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker run -p 3000:3000 chami59212/stats-api:1.0.0
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8080
 * Running on http://172.17.0.2:8080
Press CTRL+C to quit
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker run -p 3000:3000 chami59212/stats-api:1.0.0
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8080
 * Running on http://172.17.0.2:8080
Press CTRL+C to quit
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker run chami59212/stats-api:1.0.0             
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8080
 * Running on http://172.17.0.2:8080
Press CTRL+C to quit
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker run -p 8080:8080 chami59212/stats-api:1.0.0
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8080
 * Running on http://172.17.0.2:8080
Press CTRL+C to quit
172.17.0.1 - - [06/Mar/2026 14:50:48] "GET / HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:50:49] "GET /favicon.ico HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:50:49] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:50:50] "GET / HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:50:50] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:50:56] "GET /sum HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:50:56] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:12] "GET /1 HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:12] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:18] "GET /11%201 HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:19] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:29] "GET /1%20+%201 HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:29] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:37] "GET /1+1 HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:51:37] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 14:55:47] "POST /api/stats HTTP/1.1" 415 -
172.17.0.1 - - [06/Mar/2026 14:55:53] "POST /api/stats HTTP/1.1" 415 -
172.17.0.1 - - [06/Mar/2026 14:57:10] "POST /api/stats HTTP/1.1" 200 -
172.17.0.1 - - [06/Mar/2026 15:05:08] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 15:05:10] "GET /1+1 HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 15:05:10] "GET /ws/ws HTTP/1.1" 404 -
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker run -p 8080:8080 chami59212/stats-api      
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.17.0.2:5000
Press CTRL+C to quit
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker build -t chami59212/stats-api:2.0.3
ERROR: docker: 'docker buildx build' requires 1 argument

Usage:  docker buildx build [OPTIONS] PATH | URL | -

Run 'docker buildx build --help' for more information
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker build -t chami59212/stats-api:2.0.3 .
[+] Building 12.2s (16/16) FINISHED                                                                                                                          docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                                                         0.0s
 => => transferring dockerfile: 380B                                                                                                                                         0.0s 
 => [internal] load metadata for docker.io/library/python:3.12-alpine                                                                                                        1.3s 
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                                                                          0.6s 
 => [auth] library/python:pull token for registry-1.docker.io                                                                                                                0.0s 
 => [internal] load .dockerignore                                                                                                                                            0.0s
 => => transferring context: 34B                                                                                                                                             0.0s 
 => [builder 1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                            0.0s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                                    0.0s 
 => [runtime 1/4] FROM docker.io/library/python:3.12-alpine@sha256:7747d47f92cfca63a6e2b50275e23dba8407c30d8ae929a88ddd49a5d3f2d331                                          1.8s 
 => => resolve docker.io/library/python:3.12-alpine@sha256:7747d47f92cfca63a6e2b50275e23dba8407c30d8ae929a88ddd49a5d3f2d331                                                  0.0s
 => => sha256:89a8227ba99bcd9d5df82f6cb4e5ea1b222c3ec33685ba1a0d8c6db402f012ad 247B / 247B                                                                                   0.2s 
 => => sha256:6f3f43492c5b00f17f4a416bd78474116d69f3840b50bbc51c6654e4a4f88aa2 13.74MB / 13.74MB                                                                             0.8s 
 => => sha256:6de7811bee64ba64355c278198dcf2e22b4efba35aa596f23f6ed80278ac5afe 460.95kB / 460.95kB                                                                           0.4s 
 => => sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153 3.86MB / 3.86MB                                                                               0.6s 
 => => extracting sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153                                                                                    0.2s 
 => => extracting sha256:6de7811bee64ba64355c278198dcf2e22b4efba35aa596f23f6ed80278ac5afe                                                                                    0.2s 
 => => extracting sha256:6f3f43492c5b00f17f4a416bd78474116d69f3840b50bbc51c6654e4a4f88aa2                                                                                    0.6s 
 => => extracting sha256:89a8227ba99bcd9d5df82f6cb4e5ea1b222c3ec33685ba1a0d8c6db402f012ad                                                                                    0.0s 
 => [internal] load build context                                                                                                                                            0.0s 
 => => transferring context: 641B                                                                                                                                            0.0s 
 => CACHED [builder 2/5] WORKDIR /app                                                                                                                                        0.0s 
 => [builder 3/5] COPY requirements.txt .                                                                                                                                    0.1s 
 => [builder 4/5] RUN pip install --no-cache-dir --prefix=/install -r requirements.txt                                                                                       5.5s 
 => [runtime 2/4] WORKDIR /app                                                                                                                                               0.1s 
 => [builder 5/5] COPY app.py .                                                                                                                                              0.1s 
 => [runtime 3/4] COPY --from=builder /install /usr/local                                                                                                                    0.6s 
 => [runtime 4/4] COPY --from=builder /app /app                                                                                                                              0.1s 
 => exporting to image                                                                                                                                                       3.4s 
 => => exporting layers                                                                                                                                                      2.5s 
 => => exporting manifest sha256:1f8d8c3f3a49b25d404451eb41e82a5dbcae638914e9c25e9638d9064b6d0c1f                                                                            0.0s 
 => => exporting config sha256:35600c9a17fb600e68395d7c3610741adda430a13c119e1afd89427bd2e68e37                                                                              0.0s 
 => => exporting attestation manifest sha256:7170206a2467d40052b0a915d9a17d7919de93058542f8a0dab5ce0b909e2b86                                                                0.0s 
 => => exporting manifest list sha256:2599ecaf2a1a61fa291603e8a1c237e691cbbceecd67778f852a025c6ecdd6c5                                                                       0.0s 
 => => naming to docker.io/chami59212/stats-api:2.0.3                                                                                                                        0.0s 
 => => unpacking to docker.io/chami59212/stats-api:2.0.3                                                                                                                     0.8s 
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker build -t chami59212/stats-api:2.0.0 . 
[+] Building 0.6s (15/15) FINISHED                                                                                                                           docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                                                         0.0s
 => => transferring dockerfile: 380B                                                                                                                                         0.0s 
 => [internal] load metadata for docker.io/library/python:3.12-alpine                                                                                                        0.2s 
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                                                                          0.2s 
 => [internal] load .dockerignore                                                                                                                                            0.0s
 => => transferring context: 34B                                                                                                                                             0.0s 
 => [builder 1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                            0.0s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                                    0.0s 
 => [internal] load build context                                                                                                                                            0.0s 
 => => transferring context: 63B                                                                                                                                             0.0s 
 => [runtime 1/4] FROM docker.io/library/python:3.12-alpine@sha256:7747d47f92cfca63a6e2b50275e23dba8407c30d8ae929a88ddd49a5d3f2d331                                          0.0s
 => => resolve docker.io/library/python:3.12-alpine@sha256:7747d47f92cfca63a6e2b50275e23dba8407c30d8ae929a88ddd49a5d3f2d331                                                  0.0s 
 => CACHED [runtime 2/4] WORKDIR /app                                                                                                                                        0.0s 
 => CACHED [builder 2/5] WORKDIR /app                                                                                                                                        0.0s 
 => CACHED [builder 3/5] COPY requirements.txt .                                                                                                                             0.0s 
 => CACHED [builder 4/5] RUN pip install --no-cache-dir --prefix=/install -r requirements.txt                                                                                0.0s 
 => CACHED [builder 5/5] COPY app.py .                                                                                                                                       0.0s 
 => CACHED [runtime 3/4] COPY --from=builder /install /usr/local                                                                                                             0.0s 
 => CACHED [runtime 4/4] COPY --from=builder /app /app                                                                                                                       0.0s 
 => exporting to image                                                                                                                                                       0.1s 
 => => exporting layers                                                                                                                                                      0.0s 
 => => exporting manifest sha256:1f8d8c3f3a49b25d404451eb41e82a5dbcae638914e9c25e9638d9064b6d0c1f                                                                            0.0s 
 => => exporting config sha256:35600c9a17fb600e68395d7c3610741adda430a13c119e1afd89427bd2e68e37                                                                              0.0s 
 => => exporting attestation manifest sha256:3748de896b015c7c0d1f57280c7dd345433837ee45ee0ce951ecc9598a603102                                                                0.0s 
 => => exporting manifest list sha256:4da0a0eb4194587daaa8b4e51c042317b117214f493275c7d5246e4199676fb3                                                                       0.0s 
 => => naming to docker.io/chami59212/stats-api:2.0.0                                                                                                                        0.0s 
 => => unpacking to docker.io/chami59212/stats-api:2.0.0                                                                                                                     0.0s 
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker images
REPOSITORY                                TAG       IMAGE ID       CREATED              SIZE
chami59212/stats-api                      2.0.0     4da0a0eb4194   About a minute ago   186MB
chami59212/stats-api                      2.0.3     2599ecaf2a1a   About a minute ago   186MB
chami59212/stats-api                      1.0.0     314a0ee84b70   38 minutes ago       202MB
chami59212/weather-api                    1.0.0     41d62b29316b   About an hour ago    196MB
chami59212/weather-api                    latest    41d62b29316b   About an hour ago    196MB
hello-flask                               1.0.0     e31129edc842   2 hours ago          197MB
hello-flask                               latest    e31129edc842   2 hours ago          197MB
mon_app_python                            latest    86f2a8bc2296   2 hours ago          197MB
chami59212/stats-api                      latest    bd5d7aee36c4   2 hours ago          197MB
chami59212/stats-api                      2.0.2     26a25f304048   2 hours ago          197MB
chami59212/stats-api                      2.0.1     61d97e7f8d2a   2 hours ago          197MB
kalilinux/kali-rolling                    latest    8913de4b58ee   4 months ago         192MB
anssi/fcsc2024-pwn-blind-attack           latest    f367da0196ef   22 months ago        14.8MB
anssi/fcsc2024-pwn-blind-attack-shovel    latest    69ba9950856b   22 months ago        212MB
anssi/fcsc2021-web-push-it-to-the-limit   latest    3377a2e2dc8e   2 years ago          647MB
tleemcjr/metasploitable2                  latest    e559450b37dc   8 years ago          2.3GB
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker rmi chami59212/stats-api:2.0.0
>>
Untagged: chami59212/stats-api:2.0.0
Deleted: sha256:4da0a0eb4194587daaa8b4e51c042317b117214f493275c7d5246e4199676fb3
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker build -t chami59212/stats-api:2.0.0 .
[+] Building 0.8s (15/15) FINISHED                                                                                                                           docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                                                                         0.0s
 => => transferring dockerfile: 380B                                                                                                                                         0.0s 
 => [internal] load metadata for docker.io/library/python:3.12-alpine                                                                                                        0.4s 
 => [internal] load metadata for docker.io/library/python:3.12-slim                                                                                                          0.4s 
 => [internal] load .dockerignore                                                                                                                                            0.0s
 => => transferring context: 34B                                                                                                                                             0.0s 
 => [builder 1/5] FROM docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                            0.0s 
 => => resolve docker.io/library/python:3.12-slim@sha256:ccc7089399c8bb65dd1fb3ed6d55efa538a3f5e7fca3f5988ac3b5b87e593bf0                                                    0.0s 
 => [internal] load build context                                                                                                                                            0.0s 
 => => transferring context: 63B                                                                                                                                             0.0s 
 => [runtime 1/4] FROM docker.io/library/python:3.12-alpine@sha256:7747d47f92cfca63a6e2b50275e23dba8407c30d8ae929a88ddd49a5d3f2d331                                          0.0s
 => => resolve docker.io/library/python:3.12-alpine@sha256:7747d47f92cfca63a6e2b50275e23dba8407c30d8ae929a88ddd49a5d3f2d331                                                  0.0s 
 => CACHED [runtime 2/4] WORKDIR /app                                                                                                                                        0.0s 
 => CACHED [builder 2/5] WORKDIR /app                                                                                                                                        0.0s 
 => CACHED [builder 3/5] COPY requirements.txt .                                                                                                                             0.0s 
 => CACHED [builder 4/5] RUN pip install --no-cache-dir --prefix=/install -r requirements.txt                                                                                0.0s 
 => CACHED [builder 5/5] COPY app.py .                                                                                                                                       0.0s 
 => CACHED [runtime 3/4] COPY --from=builder /install /usr/local                                                                                                             0.0s 
 => CACHED [runtime 4/4] COPY --from=builder /app /app                                                                                                                       0.0s 
 => exporting to image                                                                                                                                                       0.1s 
 => => exporting layers                                                                                                                                                      0.0s 
 => => exporting manifest sha256:1f8d8c3f3a49b25d404451eb41e82a5dbcae638914e9c25e9638d9064b6d0c1f                                                                            0.0s 
 => => exporting config sha256:35600c9a17fb600e68395d7c3610741adda430a13c119e1afd89427bd2e68e37                                                                              0.0s 
 => => exporting attestation manifest sha256:1d1e404ddbef2b277818e25f7716cd2909ba1fe0cdc13143331d9e861fc56a07                                                                0.0s 
 => => exporting manifest list sha256:81614ead6cebbe317e36c064fd211ddb2ac37c05a64ba589a80a1fb59c736d6a                                                                       0.0s 
 => => naming to docker.io/chami59212/stats-api:2.0.0                                                                                                                        0.0s 
 => => unpacking to docker.io/chami59212/stats-api:2.0.0                                                                                                                     0.0s 
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> docker run -p 8080:8080 chami59212/stats-api:2.0.0
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:8080
 * Running on http://172.17.0.2:8080
Press CTRL+C to quit
172.17.0.1 - - [06/Mar/2026 15:24:31] "GET / HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 15:24:31] "GET /ws/ws HTTP/1.1" 404 -
172.17.0.1 - - [06/Mar/2026 15:25:06] "POST /api/stats/median HTTP/1.1" 200 -
PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-3-stats-api> 