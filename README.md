murka2006@murka:~$ export GITHUB_USERNAME=Mari-Mur-Meow
murka2006@murka:~$ export GITHUB_TOKEN=
murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .
~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ source scripts/activate
murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab03 projects/lab04
Клонирование в «projects/lab04»...
remote: Enumerating objects: 56, done.
remote: Counting objects: 100% (56/56), done.
remote: Compressing objects: 100% (29/29), done.
remote: Total 56 (delta 19), reused 52 (delta 18), pack-reused 0 (from 0)
Получение объектов: 100% (56/56), 15.59 КиБ | 149.00 КиБ/с, готово.
Определение изменений: 100% (19/19), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects/lab04
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git remote remove origin
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab04
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ cat > .travis.yml <<EOF
> language: cpp
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ cat >> .travis.yml <<EOF
> script:
- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
- cmake --build _build
- cmake --build _build --target install
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ cat >> .travis.yml <<EOF
> addons:
  apt:
    sources:
      - george-edison55-precise-backports
    packages:
      - cmake
      - cmake-data
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ ex -sc '1i|<фрагмент_вставки_значка>' -cx README.md
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git add .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git add README.md
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git commit -m"added CI"
[master 3230758] added CI
 2 files changed, 13 insertions(+)
 create mode 100644 .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git push origin master
Username for 'https://github.com': Mari-Mur-Meow
Password for 'https://Mari-Mur-Meow@github.com': 
Перечисление объектов: 60, готово.
Подсчет объектов: 100% (60/60), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (32/32), готово.
Запись объектов: 100% (60/60), 16.04 КиБ | 8.02 МиБ/с, готово.
Всего 60 (изменений 21), повторно использовано 54 (изменений 19), повторно использовано пакетов 0
remote: Resolving deltas: 100% (21/21), done.
To https://github.com/Mari-Mur-Meow/lab04
 * [new branch]      master -> master
