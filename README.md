export GITHUB_TOKEN=
export GITHUB_USERNAME=Ars1231
command -v apt && echo "Системный менеджер: APT" || echo "APT не найден"
/usr/bin/apt
Системный менеджер: APT
export PACKAGE_MANAGER=apt
export GPG_PACKAGE_NAME=gpg
sudo $PACKAGE_MANAGER install xclip
[sudo] пароль для Ars: 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Следующие НОВЫЕ пакеты будут установлены:
  xclip
Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 236 пакетов не обновлено.
Необходимо скачать 17,6 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 54,3 kB.
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 xclip amd64 0.13-3 [17,6 kB]
Получено 17,6 kB за 1с (16,0 kB/s)                                
Выбор ранее не выбранного пакета xclip.
(Чтение базы данных … на данный момент установлено 250473 файла и каталога.)
Подготовка к распаковке …/xclip_0.13-3_amd64.deb …
Распаковывается xclip (0.13-3) …
Настраивается пакет xclip (0.13-3) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …

alias gsed=sed
alias pbcopy='xclip -selection clipboard'
alias pbpaste='xclip -selection clipboard -o'
cd ${GITHUB_USERNAME}/workspace
pushd .
~/Ars1231/workspace ~/Ars1231/workspace
source scripts/activate
go get github.com/aktau/github-release
Команда «go» не найдена, но может быть установлена с помощью:
sudo snap install go         # version 1.24.2, or
sudo apt  install golang-go  # version 2:1.21~2
sudo apt  install gccgo-go   # version 2:1.21~2
См. 'snap info go', чтобы посмотреть дополнительные версии.

sudo apt install golang-go
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Будут установлены следующие дополнительные пакеты:
  golang-1.22-go golang-1.22-src golang-src
Следующие НОВЫЕ пакеты будут установлены:
  golang-1.22-go golang-1.22-src golang-go golang-src
Обновлено 0 пакетов, установлено 4 новых пакетов, для удаления отмечено 0 пакетов, и 236 пакетов не обновлено.
Необходимо скачать 45,7 MB архивов.
После данной операции объём занятого дискового пространства возрастёт на 228 MB.
Хотите продолжить? [Д/н] Д
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 golang-1.22-src all 1.22.2-2ubuntu0.3 [19,7 MB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 golang-1.22-go amd64 1.22.2-2ubuntu0.3 [25,9 MB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 golang-src all 2:1.22~2build1 [5 078 B]
Пол:4 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 golang-go amd64 2:1.22~2build1 [43,9 kB]
Получено 45,7 MB за 36с (1 275 kB/s)                                           
Выбор ранее не выбранного пакета golang-1.22-src.
(Чтение базы данных … на данный момент установлено 250485 файлов и каталогов.)
Подготовка к распаковке …/golang-1.22-src_1.22.2-2ubuntu0.3_all.deb …
Распаковывается golang-1.22-src (1.22.2-2ubuntu0.3) …
Выбор ранее не выбранного пакета golang-1.22-go.
Подготовка к распаковке …/golang-1.22-go_1.22.2-2ubuntu0.3_amd64.deb …
Распаковывается golang-1.22-go (1.22.2-2ubuntu0.3) …
Выбор ранее не выбранного пакета golang-src.
Подготовка к распаковке …/golang-src_2%3a1.22~2build1_all.deb …
Распаковывается golang-src (2:1.22~2build1) …
Выбор ранее не выбранного пакета golang-go:amd64.
Подготовка к распаковке …/golang-go_2%3a1.22~2build1_amd64.deb …
Распаковывается golang-go:amd64 (2:1.22~2build1) …
Настраивается пакет golang-1.22-src (1.22.2-2ubuntu0.3) …
Настраивается пакет golang-src (2:1.22~2build1) …
Настраивается пакет golang-1.22-go (1.22.2-2ubuntu0.3) …
Настраивается пакет golang-go:amd64 (2:1.22~2build1) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …

go get github.com/aktau/github-release
go: go.mod file not found in current directory or any parent directory.
	'go get' is no longer supported outside a module.
	To build and install a command, use 'go install' with a version,
	like 'go install example.com/cmd@latest'
	For more information, see https://golang.org/doc/go-get-install-deprecation
	or run 'go help get' or 'go help install'.

go install github.com/aktau/github-release@latest
go: downloading github.com/aktau/github-release v0.10.1

git clone https://github.com/${GITHUB_USERNAME}/lab08 projects/lab09
Клонирование в «projects/lab09»...
remote: Enumerating objects: 950, done.
remote: Counting objects: 100% (950/950), done.
remote: Compressing objects: 100% (292/292), done.
remote: Total 950 (delta 635), reused 943 (delta 632), pack-reused 0 (from 0)
Получение объектов: 100% (950/950), 607.24 КиБ | 19.00 КиБ/с, готово.
Определение изменений: 100% (635/635), готово.

git remote remove origin
cd projects/lab09
git remote add origin https://github.com/${GITHUB_USERNAME}/lab09
gsed -i 's/lab08/lab09/g' README.md
sudo $PACKAGE_MANAGER install ${GPG_PACKAGE_NAME}
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Уже установлен пакет gpg самой новой версии (2.4.4-2ubuntu17.2).
gpg помечен как установленный вручную.
Обновлено 0 пакетов, установлено 0 новых пакетов, для удаления отмечено 0 пакетов, и 236 пакетов не обновлено.

gpg --list-secret-keys --keyid-format LONG

gpg --full-generate-key
gpg (GnuPG) 2.4.4; Copyright (C) 2024 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Выберите тип ключа:
   (1) RSA and RSA
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (9) ECC (sign and encrypt) *default*
  (10) ECC (только для подписи)
  (14) Existing key from card
Ваш выбор? 1
длина ключей RSA может быть от 1024 до 4096.
Какой размер ключа Вам необходим? (3072) 
Запрошенный размер ключа - 3072 бит
Выберите срок действия ключа.
         0 = не ограничен
      <n>  = срок действия ключа - n дней
      <n>w = срок действия ключа - n недель
      <n>m = срок действия ключа - n месяцев
      <n>y = срок действия ключа - n лет
Срок действия ключа? (0) 0
Срок действия ключа не ограничен
Все верно? (y/N) y

GnuPG должен составить идентификатор пользователя для идентификации ключа.

Ваше полное имя: Ars
Адрес электронной почты: Ars89036698220potapov@yandex.ru
Примечание: 
Вы выбрали следующий идентификатор пользователя:
    "Ars <Ars89036698220potapov@yandex.ru>"

Сменить (N)Имя, (C)Примечание, (E)Адрес; (O)Принять/(Q)Выход? o
Необходимо получить много случайных чисел. Желательно, чтобы Вы
в процессе генерации выполняли какие-то другие действия (печать
на клавиатуре, движения мыши, обращения к дискам); это даст генератору
случайных чисел больше возможностей получить достаточное количество энтропии.
gpg: создан каталог '/home/Ars/.gnupg/openpgp-revocs.d'
gpg: сертификат отзыва записан в '/home/Ars/.gnupg/openpgp-revocs.d/ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD.rev'.
открытый и секретный ключи созданы и подписаны.

pub   rsa3072 2025-05-13 [SC]
      ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
uid                      Ars <Ars89036698220potapov@yandex.ru>
sub   rsa3072 2025-05-13 [E]

gpg --list-secret-keys --keyid-format LONG
gpg: проверка таблицы доверия
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: глубина: 0  достоверных:   1  подписанных:   0  доверие: 0-, 0q, 0n, 0m, 0f, 1u
/home/Ars/.gnupg/pubring.kbx
----------------------------------
sec   rsa3072/AB4F6155CFC9F4BD 2025-05-13 [SC]
      ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
uid               [  абсолютно ] Ars <Ars89036698220potapov@yandex.ru>
ssb   rsa3072/2ACC4DF7391A5D3A 2025-05-13 [E]

gpg -K ${GITHUB_USERNAME}
sec   rsa3072 2025-05-13 [SC]
      ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
uid         [  абсолютно ] Ars <Ars89036698220potapov@yandex.ru>
ssb   rsa3072 2025-05-13 [E]

GPG_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep ssb | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
GPG_SEC_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep sec | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
gpg --armor --export ${GPG_KEY_ID} | pbcopy
pbpaste

git config user.signingkey ${GPG_SEC_KEY_ID}
git config gpg.program gpg
test -r ~/.bash_profile && echo 'export GPG_TTY=$(tty)' >> ~/.bash_profile
echo 'export GPG_TTY=$(tty)' >> ~/.profile
cmake -H. -B_build -DCPACK_GENERATOR="TGZ"
-- Конфигурация завершена
-- Генерация завершена

cmake --build _build --target package
[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
Run CPack packaging tool...
CPack: Create package using TGZ
CPack: package: /home/Ars/Ars1231/workspace/projects/lab09/_build/print-0.1.0.0-Linux.tar.gz generated.

git tag -s v0.1.0.0 -m "Initial release version 0.1.0.0"
git tag -v v0.1.0.0
object cd0771df215b2660ddad45ecc4a00baad7024e00
type commit
tag v0.1.0.0
tagger Ars <Ars89036698220potacov@yandex.ru> 1747159204 +0300

Initial release version 0.1.0.0
gpg: Подпись сделана Вт 13 мая 2025 21:00:05 MSK
gpg:                ключом RSA с идентификатором ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
gpg: Действительная подпись пользователя "Ars <Ars89036698220potacov@yandex.ru>" [абсолютное]

git push origin master --tags
Username for 'https://github.com': Ars1231
Password for 'https://Ars1231@github.com': 
Перечисление объектов: 951, готово.
Подсчет объектов: 100% (951/951), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (290/290), готово.
Запись объектов: 100% (951/951), 607.77 КиБ | 202.59 МиБ/с, готово.
Всего 951 (изменений 635), повторно использовано 950 (изменений 635), повторно использовано пакетов 0
remote: Resolving deltas: 100% (635/635), done.
To https://github.com/Ars1231/lab09
 * [new branch]      master -> master
 * [new tag]         v0.1.0.0 -> v0.1.0.0

github-release --version
github-release v0.10.1

github-release info -u ${GITHUB_USERNAME} -r lab09
tags:
- v0.1.0.0 (commit: https://api.github.com/repos/Ars1231/lab09/commits/cd0771df215b2660ddad45ecc4a00baad7024e00)
releases:

github-release release \
    --user ${GITHUB_USERNAME} \
    --repo lab09 \
    --tag v0.1.0.0 \
    --name "libprint" \
    --description "my first release"

export PACKAGE_OS=`uname -s` PACKAGE_ARCH=`uname -m` 
export PACKAGE_FILENAME=print-${PACKAGE_OS}-${PACKAGE_ARCH}.tar.gz
github-release upload \
    --user ${GITHUB_USERNAME} \
    --repo lab09 \
    --tag v0.1.0.0 \
    --name "${PACKAGE_FILENAME}" \
    --file _build/*.tar.gz

github-release info -u ${GITHUB_USERNAME} -r lab09
tags:
- v0.1.0.0 (commit: https://api.github.com/repos/Ars1231/lab09/commits/cd0771df215b2660ddad45ecc4a00baad7024e00)
releases:
- v0.1.0.0, name: 'libprint', description: 'my first release', id: 218368513, tagged: 13/05/2025 at 18:00, published: 13/05/2025 at 18:50, draft: ✗, prerelease: ✗
  - artifact: print-Linux-x86_64.tar.gz, downloads: 0, state: uploaded, type: application/octet-stream, size: 5.9 kB, id: 254346779

wget https://github.com/${GITHUB_USERNAME}/lab09/releases/download/v0.1.0.0/${PACKAGE_FILENAME}
--2025-05-13 21:51:52--  https://github.com/Ars1231/lab09/releases/download/v0.1.0.0/print-Linux-x86_64.tar.gz
Распознаётся github.com (github.com)… 140.82.121.4
Подключение к github.com (github.com)|140.82.121.4|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
--2025-05-13 21:51:56--  https://objects.githubusercontent.com/github-production-release-asset-2e65be/982968093/000a1659-61a3-40b1-b270-6ba826213e60?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20250513%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250513T185155Z&X-Amz-Expires=300&X-Amz-Signature=886d3f8413d1358b65d06e4dd39e4ad61219f06801a71fde5ba6c57fa0cfdbec&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dprint-Linux-x86_64.tar.gz&response-content-type=application%2Foctet-stream
Распознаётся objects.githubusercontent.com (objects.githubusercontent.com)… 185.199.111.133, 185.199.109.133, 185.199.110.133, ...
Подключение к objects.githubusercontent.com (objects.githubusercontent.com)|185.199.111.133|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 5868 (5,7K) [application/octet-stream]
Сохранение в: ‘print-Linux-x86_64.tar.gz’
print-Linux-x86_64.tar 100%[===========================>]   5,73K  --.-KB/s    за 0s      
2025-05-13 21:52:01 (33,0 MB/s) - ‘print-Linux-x86_64.tar.gz’ сохранён [5868/5868]

tar -ztf ${PACKAGE_FILENAME}
print-0.1.0.0-Linux/cmake/
print-0.1.0.0-Linux/cmake/print-config.cmake
print-0.1.0.0-Linux/cmake/print-config-noconfig.cmake
print-0.1.0.0-Linux/lib/
print-0.1.0.0-Linux/lib/libprint.a
print-0.1.0.0-Linux/include/
print-0.1.0.0-Linux/include/print.hpp
print-0.1.0.0-Linux/bin/
print-0.1.0.0-Linux/bin/demo

git add .
git commit -m"final commit"
[master e6c9d7e] final commit
 2 files changed, 95 insertions(+), 95 deletions(-)
 create mode 100644 print-Linux-x86_64.tar.gz

git push origin master 
Username for 'https://github.com': Ars1231
Password for 'https://Ars1231@github.com': 
Перечисление объектов: 6, готово.
Подсчет объектов: 100% (6/6), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (4/4), готово.
Запись объектов: 100% (4/4), 6.63 КиБ | 6.63 МиБ/с, готово.
Всего 4 (изменений 2), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Ars1231/lab09
   cd0771d..e6c9d7e  master -> master


