murka2006@murka:~$  export GITHUB_USERNAME=Mari-Mur-Meow
murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .
~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ source scripts/activate
murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab07 lab08
Клонирование в «lab08»...
remote: Enumerating objects: 95, done.
remote: Counting objects: 100% (95/95), done.
remote: Compressing objects: 100% (47/47), done.
remote: Total 95 (delta 40), reused 87 (delta 37), pack-reused 0 (from 0)
Получение объектов: 100% (95/95), 43.73 КиБ | 422.00 КиБ/с, готово.
Определение изменений: 100% (40/40), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace$  cd lab08
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ git submodule update --init
Подмодуль «third-party/gtest» (https://github.com/google/googletest) зарегистрирован по пути «third-party/gtest»
Клонирование в «/home/murka2006/Mari-Mur-Meow/workspace/lab08/third-party/gtest»...
Submodule path 'third-party/gtest': checked out 'e2239ee6043f73722e7aa812a459f54a28552929'
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ git remote remove origin
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab08
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat > Dockerfile <<EOF
> FROM ubuntu:18.04
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat >> Dockerfile <<EOF
> COPY . print/
WORKDIR print
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat >> Dockerfile <<EOF
> RUN cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install
RUN cmake --build _build
RUN cmake --build _build --target install
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat >> Dockerfile <<EOF
> ENV LOG_PATH /home/logs/log.txt
> EOF

murka2006@murka:~$ cd Mari-Mur-Meow/workspace/lab08
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat >> Dockerfile <<EOF
> VOLUME /home/logs
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat >> Dockerfile <<EOF
> WORKDIR _install/bin
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat >> Dockerfile <<EOF
> ENTRYPOINT ./demo
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker build -t logger .
Команда «docker» не найдена, но может быть установлена с помощью:
sudo snap install docker         # version 27.5.1, or
sudo apt  install docker.io      # version 26.1.3-0ubuntu1~24.04.1
sudo apt  install podman-docker  # version 4.9.3+ds1-1ubuntu0.2
См. 'snap info docker', чтобы посмотреть дополнительные версии.
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ sudo snap install docker  
[sudo] пароль для murka2006: 
docker 27.5.1 from Canonical✓ installed
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker build -t logger .
ERROR: permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ getent group docker
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ groups
murka2006 adm cdrom sudo dip plugdev users lpadmin
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ sudo usermod -aG docker murka2006
usermod: группа «docker» не существует
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ sudo groupadd docker
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ sudo usermod -aG docker murka2006
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ groups
murka2006 adm cdrom sudo dip plugdev users lpadmin

murka2006@murka:~$ cd Mari-Mur-Meow/workspace/lab08
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker build -t logger .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  19.69MB
Step 1/10 : FROM ubuntu:18.04
18.04: Pulling from library/ubuntu
7c457f213c76: Pull complete 
Digest: sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e43c98
Status: Downloaded newer image for ubuntu:18.04
 ---> f9a80a55f492
Step 2/10 : COPY . print/
 ---> f29536edc378
Step 3/10 : WORKDIR print
 ---> Running in 611c899f01b1
 ---> Removed intermediate container 611c899f01b1
 ---> 6f48ec71fbd3
Step 4/10 : RUN cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install
 ---> Running in 365bdf960b63
/bin/sh: 1: cmake: not found
The command '/bin/sh -c cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install' returned a non-zero code: 127
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cmake --version
cmake version 3.28.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat > Dockerfile <<EOF
> FROM ubuntu:20.04
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker build -t logger .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  19.69MB
Step 1/1 : FROM ubuntu:20.04
20.04: Pulling from library/ubuntu
13b7e930469f: Pull complete 
Digest: sha256:8feb4d8ca5354def3d8fce243717141ce31e2c428701f6682bd2fafe15388214
Status: Downloaded newer image for ubuntu:20.04
 ---> b7bab04fd9aa
Successfully built b7bab04fd9aa
Successfully tagged logger:latest
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
<none>       <none>    6f48ec71fbd3   4 minutes ago   82.5MB
logger       latest    b7bab04fd9aa   4 weeks ago     72.8MB
ubuntu       20.04     b7bab04fd9aa   4 weeks ago     72.8MB
ubuntu       18.04     f9a80a55f492   23 months ago   63.2MB
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$  mkdir logs
murka2006@murka:~$ cd Mari-Mur-Meow/workspace/lab08
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker build -t logger .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  19.69MB
Step 1/10 : FROM ubuntu:18.04
18.04: Pulling from library/ubuntu
7c457f213c76: Pull complete 
Digest: sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e43c98
Status: Downloaded newer image for ubuntu:18.04
 ---> f9a80a55f492
Step 2/10 : COPY . print/
 ---> f29536edc378
Step 3/10 : WORKDIR print
 ---> Running in 611c899f01b1
 ---> Removed intermediate container 611c899f01b1
 ---> 6f48ec71fbd3
Step 4/10 : RUN cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install
 ---> Running in 365bdf960b63
/bin/sh: 1: cmake: not found
The command '/bin/sh -c cmake -H. -B_build -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=_install' returned a non-zero code: 127
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cmake --version
cmake version 3.28.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat > Dockerfile <<EOF
> FROM ubuntu:20.04
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker build -t logger .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  19.69MB
Step 1/1 : FROM ubuntu:20.04
20.04: Pulling from library/ubuntu
13b7e930469f: Pull complete 
Digest: sha256:8feb4d8ca5354def3d8fce243717141ce31e2c428701f6682bd2fafe15388214
Status: Downloaded newer image for ubuntu:20.04
 ---> b7bab04fd9aa
Successfully built b7bab04fd9aa
Successfully tagged logger:latest
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
<none>       <none>    6f48ec71fbd3   4 minutes ago   82.5MB
logger       latest    b7bab04fd9aa   4 weeks ago     72.8MB
ubuntu       20.04     b7bab04fd9aa   4 weeks ago     72.8MB
ubuntu       18.04     f9a80a55f492   23 months ago   63.2MB
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$  mkdir logs
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker run -it -v "$(pwd)/logs/:/home/logs/" logger
text1
text2
text3
<C-D>
root@16d40953e4d1:/# 
root@16d40953e4d1:/# 
root@16d40953e4d1:/# 
root@16d40953e4d1:/# 
root@16d40953e4d1:/# 
root@16d40953e4d1:/# text1: команда не найдена
text2: команда не найдена
text3: команда не найдена
bash: синтаксическая ошибка рядом с неожиданным маркером «newline»
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker run -it -v "$(pwd)/logs/:/home/logs/" logger
text1
text2
text3
root@7527863f1944:/# exit
text1: команда не найдена
text2: команда не найдена
text3: команда не найдена
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ ^C
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker run -it -v "$(pwd)/logs/:/home/logs/" logger
root@c5e283c7e9f6:/# text1
bash: text1: command not found
root@c5e283c7e9f6:/# text1
bash: text1: command not found
root@c5e283c7e9f6:/# exit
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker run -it -v "$(pwd)/logs/:/home/logs/" logger
root@281e6327ca0d:/# exit
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker inspect logger
[
    {
        "Id": "sha256:b7bab04fd9aa0c771e5720bf0cc7cbf993fd6946645983d9096126e5af45d713",
        "RepoTags": [
            "logger:latest",
            "ubuntu:20.04"
        ],
        "RepoDigests": [
            "ubuntu@sha256:8feb4d8ca5354def3d8fce243717141ce31e2c428701f6682bd2fafe15388214"
        ],
        "Parent": "",
        "Comment": "",
        "Created": "2025-04-08T10:42:48.947155373Z",
        "DockerVersion": "24.0.7",
        "Author": "",
        "Config": {
            "Hostname": "",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/bash"
            ],
            "Image": "sha256:a4f4aac46bc2829ab75a33c79ebe803110dd26e79bbd1dce17875492019b230c",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {
                "org.opencontainers.image.ref.name": "ubuntu",
                "org.opencontainers.image.version": "20.04"
            }
        },
        "Architecture": "amd64",
        "Os": "linux",
        "Size": 72813617,
        "GraphDriver": {
            "Data": {
                "MergedDir": "/var/snap/docker/common/var-lib-docker/overlay2/a9a243a1f43ec5a10f27f716086edd1fd9bb6970b7361c0d3d9c36a06d4df9de/merged",
                "UpperDir": "/var/snap/docker/common/var-lib-docker/overlay2/a9a243a1f43ec5a10f27f716086edd1fd9bb6970b7361c0d3d9c36a06d4df9de/diff",
                "WorkDir": "/var/snap/docker/common/var-lib-docker/overlay2/a9a243a1f43ec5a10f27f716086edd1fd9bb6970b7361c0d3d9c36a06d4df9de/work"
            },
            "Name": "overlay2"
        },
        "RootFS": {
            "Type": "layers",
            "Layers": [
                "sha256:470b66ea5123c93b0d5606e4213bf9e47d3d426b640d32472e4ac213186c4bb6"
            ]
        },
        "Metadata": {
            "LastTagTime": "2025-05-11T23:45:58.383836055+03:00"
        }
    }
]
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$  cat logs/log.txt
cat: logs/log.txt: Нет такого файла или каталога


murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ docker run -it -v "$(pwd)/logs:/home/logs" logger bash -c "cat > /home/logs/log.txt"
text1
text
text3
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ ^C
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ cat logs/log.txt
text1
text
text3
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$  gsed -i 's/lab07/lab08/g' README.md
Команда «gsed» не найдена. Возможно, вы имели в виду:
  команда 'msed' из deb-пакета mblaze (1.1-1)
  команда 'gsd' из deb-пакета python3-gsd (3.0.1-3build1)
  команда 'sed' из deb-пакета sed (4.9-2)
  команда 'gted' из deb-пакета gnome-text-editor (46.3-0ubuntu2)
  команда 'gsec' из deb-пакета firebird3.0-utils (3.0.11.33637.ds4-2ubuntu2)
  команда 'ssed' из deb-пакета ssed (3.62-8)
  команда 'gsnd' из deb-пакета ghostscript (10.02.1~dfsg1-0ubuntu7.5)
  команда 'gsad' из deb-пакета gsad (22.8.0-1)
Попробуйте: sudo apt install <имя_deb-пакета>
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ sed -i 's/lab07/lab08/g' README.md
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ vim .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ vim .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ git add Dockerfile
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ git add .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ git commit -m"adding Dockerfile"
[master da0f64c] adding Dockerfile
 2 files changed, 14 insertions(+), 12 deletions(-)
 create mode 100644 Dockerfile
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$  git push origin master
Username for 'https://github.com': Mari-Mur-Meow
Password for 'https://Mari-Mur-Meow@github.com': 
Перечисление объектов: 99, готово.
Подсчет объектов: 100% (99/99), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (47/47), готово.
Запись объектов: 100% (99/99), 44.06 КиБ | 14.69 МиБ/с, готово.
Всего 99 (изменений 41), повторно использовано 94 (изменений 40), повторно использовано пакетов 0
remote: Resolving deltas: 100% (41/41), done.
To https://github.com/Mari-Mur-Meow/lab08
 * [new branch]      master -> master
murka2006@murka:~/Mari-Mur-Meow/workspace/lab08$ 
