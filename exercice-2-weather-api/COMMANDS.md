## docker build -t chami59212/weather-api:1.0.0 .
## docker run -p 3000:3000 chami59212/weather-api:1.0.0
## docker login
## docker push chami59212/weather-api:1.0.0
## docker tag chami59212/weather-api:1.0.0 chami59212/weather-api:latest
## docker push chami59212/weather-api:latest




Console complète : 





## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-2-weather-api> docker build -t chami59212/weather-api:1.0.0 .
[+] Building 9.5s (11/11) FINISHED                                                                        docker:desktop-linux
 => [internal] load build definition from Dockerfile                                                                      0.0s
 => => transferring dockerfile: 147B                                                                                      0.0s
 => [internal] load metadata for docker.io/library/node:18-alpine                                                         1.4s
 => [auth] library/node:pull token for registry-1.docker.io                                                               0.0s
 => [internal] load .dockerignore                                                                                         0.0s
 => => transferring context: 49B                                                                                          0.0s
 => [1/5] FROM docker.io/library/node:18-alpine@sha256:8d6421d663b4c28fd3ebc498332f249011d118945588d0a35cb9bc4b8ca09d9e   3.3s
 => => resolve docker.io/library/node:18-alpine@sha256:8d6421d663b4c28fd3ebc498332f249011d118945588d0a35cb9bc4b8ca09d9e   0.0s
 => => sha256:25ff2da83641908f65c3a74d80409d6b1b62ccfaab220b9ea70b80df5a2e0549 446B / 446B                                0.2s
 => => sha256:1e5a4c89cee5c0826c540ab06d4b6b491c96eda01837f430bd47f0d26702d6e3 1.26MB / 1.26MB                            0.4s 
 => => sha256:dd71dde834b5c203d162902e6b8994cb2309ae049a0eabc4efea161b2b5a3d0e 40.01MB / 40.01MB                          1.8s
 => => sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870 3.64MB / 3.64MB                            0.6s 
 => => extracting sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870                                 0.2s 
 => => extracting sha256:dd71dde834b5c203d162902e6b8994cb2309ae049a0eabc4efea161b2b5a3d0e                                 1.3s 
 => => extracting sha256:1e5a4c89cee5c0826c540ab06d4b6b491c96eda01837f430bd47f0d26702d6e3                                 0.1s 
 => => extracting sha256:25ff2da83641908f65c3a74d80409d6b1b62ccfaab220b9ea70b80df5a2e0549                                 0.0s 
 => [internal] load build context                                                                                         0.1s 
 => => transferring context: 1.15kB                                                                                       0.0s 
 => [2/5] WORKDIR /app                                                                                                    0.1s 
 => [3/5] COPY package.json .                                                                                             0.0s 
 => [4/5] RUN npm i                                                                                                       2.6s 
 => [5/5] COPY . .                                                                                                        0.1s 
 => exporting to image                                                                                                    1.2s 
 => => exporting layers                                                                                                   0.4s 
 => => exporting manifest sha256:5a9390389e144ddb566f7110335592ed9d4f0f8d1a66ebe069300ac68c74b501                         0.0s 
 => => exporting config sha256:946a9cc734324e9abd68f6c8b8e04eed880c539808d0660dde21ca53ae8ceaf2                           0.0s 
 => => exporting attestation manifest sha256:736197676e321270693091284946ed6aa4bbc16c1fa797bfe902dc85b9241116             0.0s 
 => => exporting manifest list sha256:41d62b29316bafd4eab8127cd2b3bef05c7c894613e1c753fe43ba761de19382                    0.0s 
 => => naming to docker.io/chami59212/weather-api:1.0.0                                                                   0.0s 
 => => unpacking to docker.io/chami59212/weather-api:1.0.0                                                                0.6s 
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-2-weather-api> docker run -p 3000:3000 chami59212/weather-api:1.0.0

> weather-api@1.0.0 start
> node index.js

API météo sur le port 3000
npm error path /app
npm error command failed
npm error signal SIGINT
npm error command sh -c node index.js
npm error A complete log of this run can be found in: /root/.npm/_logs/2026-03-06T14_14_34_690Z-debug-0.log
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-2-weather-api> docker login 
Authenticating with existing credentials... [Username: chami59212]

i Info → To login with a different account, run 'docker logout' followed by 'docker login'


Login Succeeded
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-2-weather-api> docker push chami59212/weather-api:1.0.0
The push refers to repository [docker.io/chami59212/weather-api]
c5bbc366b5d0: Pushed
1e5a4c89cee5: Pushed
f18232174bc9: Pushed
dd71dde834b5: Pushed
c0aa77d7328c: Pushed
6fd484923679: Pushed
47802b7aa033: Pushed
4b84b3fe8b0c: Pushed
25ff2da83641: Pushed
1.0.0: digest: sha256:41d62b29316bafd4eab8127cd2b3bef05c7c894613e1c753fe43ba761de19382 size: 856
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-2-weather-api> docker tag chami59212/weather-api:1.0.0 chami59212/weather-api:latest
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-2-weather-api> docker push chami59212/weather-api:latest
The push refers to repository [docker.io/chami59212/weather-api]
47802b7aa033: Already exists
1e5a4c89cee5: Layer already exists
f18232174bc9: Layer already exists
dd71dde834b5: Layer already exists
6fd484923679: Layer already exists
c5bbc366b5d0: Layer already exists
4b84b3fe8b0c: Layer already exists
25ff2da83641: Layer already exists
c0aa77d7328c: Layer already exists
latest: digest: sha256:41d62b29316bafd4eab8127cd2b3bef05c7c894613e1c753fe43ba761de19382 size: 856
## PS C:\Users\Hicha\Desktop\dev\cours-docker\docker-tp-images\exercice-2-weather-api> 