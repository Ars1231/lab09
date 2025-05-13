murka2006@murka:~$ export GITHUB_TOKEN=g/,,,,
murka2006@murka:~$ export GITHUB_USERNAME=Mari-Mur-Meow
murka2006@murka:~$ command -v apt && echo "Системный менеджер: APT" || echo "APT не найден"
/usr/bin/apt
Системный менеджер: APT
murka2006@murka:~$ export PACKAGE_MANAGER=apt
murka2006@murka:~$ export GPG_PACKAGE_NAME=gpg
murka2006@murka:~$ $PACKAGE_MANAGER install xclip
E: Не удалось открыть файл блокировки /var/lib/dpkg/lock-frontend - open (13: Отказано в доступе)
E: Невозможно получить блокировку внешнего интерфейса dpkg (/var/lib/dpkg/lock-frontend); у вас есть права суперпользователя?
murka2006@murka:~$ sudo $PACKAGE_MANAGER install xclip
[sudo] пароль для murka2006: 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Следующий пакет устанавливался автоматически и больше не требуется:
  libllvm17t64
Для его удаления используйте «sudo apt autoremove».
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
murka2006@murka:~$ alias gsed=sed
murka2006@murka:~$  alias pbcopy='xclip -selection clipboard'
murka2006@murka:~$ alias pbpaste='xclip -selection clipboard -o'
murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .
~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$  source scripts/activate
murka2006@murka:~/Mari-Mur-Meow/workspace$ go get github.com/aktau/github-release
Команда «go» не найдена, но может быть установлена с помощью:
sudo snap install go         # version 1.24.2, or
sudo apt  install golang-go  # version 2:1.21~2
sudo apt  install gccgo-go   # version 2:1.21~2
См. 'snap info go', чтобы посмотреть дополнительные версии.
murka2006@murka:~/Mari-Mur-Meow/workspace$ sudo apt  install golang-go
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Следующий пакет устанавливался автоматически и больше не требуется:
  libllvm17t64
Для его удаления используйте «sudo apt autoremove».
Будут установлены следующие дополнительные пакеты:
  golang-1.22-go golang-1.22-src golang-src
Предлагаемые пакеты:
  bzr | brz mercurial subversion
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
murka2006@murka:~/Mari-Mur-Meow/workspace$ go get github.com/aktau/github-release
go: go.mod file not found in current directory or any parent directory.
	'go get' is no longer supported outside a module.
	To build and install a command, use 'go install' with a version,
	like 'go install example.com/cmd@latest'
	For more information, see https://golang.org/doc/go-get-install-deprecation
	or run 'go help get' or 'go help install'.
murka2006@murka:~/Mari-Mur-Meow/workspace$ go install github.com/aktau/github-release@latest
go: downloading github.com/aktau/github-release v0.10.1
go: finding module for package github.com/voxelbrain/goptions
go: finding module for package github.com/github-release/github-release/github
go: finding module for package github.com/dustin/go-humanize
go: downloading github.com/dustin/go-humanize v1.0.1
go: downloading github.com/github-release/github-release v0.10.1
go: downloading github.com/voxelbrain/goptions v0.0.0-20180630082107-58cddc247ea2
go: found github.com/dustin/go-humanize in github.com/dustin/go-humanize v1.0.1
go: found github.com/github-release/github-release/github in github.com/github-release/github-release v0.10.1
go: found github.com/voxelbrain/goptions in github.com/voxelbrain/goptions v0.0.0-20180630082107-58cddc247ea2
go: finding module for package github.com/tomnomnom/linkheader
go: finding module for package github.com/kevinburke/rest/restclient
go: downloading github.com/tomnomnom/linkheader v0.0.0-20180905144013-02ca5825eb80
go: downloading github.com/kevinburke/rest v0.0.0-20240617045629-3ed0ad3487f0
go: found github.com/kevinburke/rest/restclient in github.com/kevinburke/rest v0.0.0-20240617045629-3ed0ad3487f0
go: found github.com/tomnomnom/linkheader in github.com/tomnomnom/linkheader v0.0.0-20180905144013-02ca5825eb80
murka2006@murka:~/Mari-Mur-Meow/workspace$ go get github.com/aktau/github-release
go: go.mod file not found in current directory or any parent directory.
	'go get' is no longer supported outside a module.
	To build and install a command, use 'go install' with a version,
	like 'go install example.com/cmd@latest'
	For more information, see https://golang.org/doc/go-get-install-deprecation
	or run 'go help get' or 'go help install'.
murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab08 projects/lab09
Клонирование в «projects/lab09»...
remote: Enumerating objects: 950, done.
remote: Counting objects: 100% (950/950), done.
remote: Compressing objects: 100% (292/292), done.
remote: Total 950 (delta 635), reused 943 (delta 632), pack-reused 0 (from 0)
Получение объектов: 100% (950/950), 607.24 КиБ | 19.00 КиБ/с, готово.
Определение изменений: 100% (635/635), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace$ git remote remove origin
murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects/lab09
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab09
error: внешний репозиторий origin уже существует
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ ^C
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab09
error: внешний репозиторий origin уже существует
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ ^C
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ ^C
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ ^C
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git remote remove origin
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab09
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gsed -i 's/lab08/lab09/g' README.md
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ $PACKAGE_MANAGER install ${GPG_PACKAGE_NAME}
E: Не удалось открыть файл блокировки /var/lib/dpkg/lock-frontend - open (13: Отказано в доступе)
E: Невозможно получить блокировку внешнего интерфейса dpkg (/var/lib/dpkg/lock-frontend); у вас есть права суперпользователя?
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ sudo $PACKAGE_MANAGER install ${GPG_PACKAGE_NAME}
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Уже установлен пакет gpg самой новой версии (2.4.4-2ubuntu17.2).
gpg помечен как установленный вручную.
Следующий пакет устанавливался автоматически и больше не требуется:
  libllvm17t64
Для его удаления используйте «sudo apt autoremove».
Обновлено 0 пакетов, установлено 0 новых пакетов, для удаления отмечено 0 пакетов, и 236 пакетов не обновлено.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gpg --list-secret-keys --keyid-format LONG
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gpg --full-generate-key
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

Ваше полное имя: Mari-Mur-Meow
Адрес электронной почты: mashmar2006@mail.ru
Примечание: 
Вы выбрали следующий идентификатор пользователя:
    "Mari-Mur-Meow <mashmar2006@mail.ru>"

Сменить (N)Имя, (C)Примечание, (E)Адрес; (O)Принять/(Q)Выход? q
gpg: Создание ключа прервано.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gpg --full-generate-key
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

Ваше полное имя: Mari-Mur-Meow
Адрес электронной почты: mashmar2006@mail.ru
Примечание: 
Вы выбрали следующий идентификатор пользователя:
    "Mari-Mur-Meow <mashmar2006@mail.ru>"

Сменить (N)Имя, (C)Примечание, (E)Адрес; (O)Принять/(Q)Выход? o
Необходимо получить много случайных чисел. Желательно, чтобы Вы
в процессе генерации выполняли какие-то другие действия (печать
на клавиатуре, движения мыши, обращения к дискам); это даст генератору
случайных чисел больше возможностей получить достаточное количество энтропии.
gpg: agent_genkey failed: Операция отменена
Сбой при создании ключа: Операция отменена
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gpg --full-generate-key
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

Ваше полное имя: Mari-Mur-Meow
Адрес электронной почты: mashmar2006@mail.ru
Примечание: 
Вы выбрали следующий идентификатор пользователя:
    "Mari-Mur-Meow <mashmar2006@mail.ru>"

Сменить (N)Имя, (C)Примечание, (E)Адрес; (O)Принять/(Q)Выход? o
Необходимо получить много случайных чисел. Желательно, чтобы Вы
в процессе генерации выполняли какие-то другие действия (печать
на клавиатуре, движения мыши, обращения к дискам); это даст генератору
случайных чисел больше возможностей получить достаточное количество энтропии.
Необходимо получить много случайных чисел. Желательно, чтобы Вы
в процессе генерации выполняли какие-то другие действия (печать
на клавиатуре, движения мыши, обращения к дискам); это даст генератору
случайных чисел больше возможностей получить достаточное количество энтропии.
gpg: создан каталог '/home/murka2006/.gnupg/openpgp-revocs.d'
gpg: сертификат отзыва записан в '/home/murka2006/.gnupg/openpgp-revocs.d/ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD.rev'.
открытый и секретный ключи созданы и подписаны.

pub   rsa3072 2025-05-13 [SC]
      ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
uid                      Mari-Mur-Meow <mashmar2006@mail.ru>
sub   rsa3072 2025-05-13 [E]

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gpg --list-secret-keys --keyid-format LONG
gpg: проверка таблицы доверия
gpg: marginals needed: 3  completes needed: 1  trust model: pgp
gpg: глубина: 0  достоверных:   1  подписанных:   0  доверие: 0-, 0q, 0n, 0m, 0f, 1u
/home/murka2006/.gnupg/pubring.kbx
----------------------------------
sec   rsa3072/AB4F6155CFC9F4BD 2025-05-13 [SC]
      ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
uid               [  абсолютно ] Mari-Mur-Meow <mashmar2006@mail.ru>
ssb   rsa3072/2ACC4DF7391A5D3A 2025-05-13 [E]

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gpg -K ${GITHUB_USERNAME}
sec   rsa3072 2025-05-13 [SC]
      ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
uid         [  абсолютно ] Mari-Mur-Meow <mashmar2006@mail.ru>
ssb   rsa3072 2025-05-13 [E]

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ GPG_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep ssb | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ GPG_SEC_KEY_ID=$(gpg --list-secret-keys --keyid-format LONG | grep sec | tail -1 | awk '{print $2}' | awk -F'/' '{print $2}')
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ gpg --armor --export ${GPG_KEY_ID} | pbcopy
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ pbpaste
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ open https://github.com/settings/keysgs/keys
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ Gtk-Message: 20:50:11.498: Not loading module "atk-bridge": The functionality is provided by GTK natively. Please try to not load it.

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ open https://github.com/settings/keys
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ Gtk-Message: 20:52:34.635: Not loading module "atk-bridge": The functionality is provided by GTK natively. Please try to not load it.

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git config user.signingkey ${GPG_SEC_KEY_ID}
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git config gpg.program gpg
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ test -r ~/.bash_profile && echo 'export GPG_TTY=$(tty)' >> ~/.bash_profile
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ echo 'export GPG_TTY=$(tty)' >> ~/.profile
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ cmake -H. -B_build -DCPACK_GENERATOR="TGZ"
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:34 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_private_data.cmake:12 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:35 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_initialize.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/Hunter:36 (include)
  cmake/HunterGate.cmake:540 (include)
  CMakeLists.txt:4 (HunterGate)


-- The C compiler identification is GNU 13.3.0
-- The CXX compiler identification is GNU 13.3.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /home/murka2006/.hunter
-- [hunter] [ Hunter-ID: 23f1b5a | Toolchain-ID: fb15dbb | Config-ID: bf2be25 ]
CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:9 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_config_sha1.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:9 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_toolchain_sha1.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:10 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_set_config_location.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_apply_gate_settings.cmake:13 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_calculate_self.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_finalize.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_cache_run.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_load_from_cache.cmake:6 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:22 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_create_cache_meta_directory.cmake:5 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:4 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


CMake Deprecation Warning at /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_lock_directory.cmake:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.
Call Stack (most recent call first):
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_make_directory.cmake:7 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_save_to_cache.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_download.cmake:26 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/projects/GTest/hunter.cmake:8 (include)
  /home/murka2006/.hunter/_Base/Download/Hunter/0.23.308/23f1b5a/Unpacked/cmake/modules/hunter_add_package.cmake:62 (include)
  CMakeLists.txt:24 (hunter_add_package)


-- [hunter] GTEST_ROOT: /home/murka2006/.hunter/_Base/23f1b5a/fb15dbb/bf2be25/Install (ver.: 1.11.0)
-- Found GTest: /home/murka2006/.hunter/_Base/23f1b5a/fb15dbb/bf2be25/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.11.0")  
-- Configuring done (1.0s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab09/_build
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ cmake --build _build --target package
[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
Run CPack packaging tool...
CPack: Create package using TGZ
CPack: Install projects
CPack: - Run preinstall target for: print
CPack: - Install project: print []
CPack: Create package
CPack: - package: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab09/_build/print-0.1.0.0-Linux.tar.gz generated.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git tag -s v0.1.0.0
fatal: нет описания метки?
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git tag -s v0.1.0.0
fatal: нет описания метки?
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git tag -s v0.1.0.0
fatal: нет описания метки?
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git tag -s v0.1.0.0
fatal: нет описания метки?
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git tag -s v0.1.0.0 -m "Initial release version 0.1.0.0"
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git tag -v v0.1.0.0
object cd0771df215b2660ddad45ecc4a00baad7024e00
type commit
tag v0.1.0.0
tagger Mari-Mur-Meow <mashmar2006@mail.ru> 1747159204 +0300

Initial release version 0.1.0.0
gpg: Подпись сделана Вт 13 мая 2025 21:00:04 MSK
gpg:                ключом RSA с идентификатором ED49EAE025DEC4066BC80554AB4F6155CFC9F4BD
gpg: Действительная подпись пользователя "Mari-Mur-Meow <mashmar2006@mail.ru>" [абсолютное]
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git show v0.1.0.0
tag v0.1.0.0
Tagger: Mari-Mur-Meow <mashmar2006@mail.ru>
Date:   Tue May 13 21:00:04 2025 +0300

Initial release version 0.1.0.0
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEE7Unq4CXexAZryAVUq09hVc/J9L0FAmgjiKQACgkQq09hVc/J
9L1MjQv8DAJjz37vuoZKbn7oo5v0jfFKM6yxpWPEkMYUxsce6AdUlqwXj7W0YOfo
O1feKa7APFuHx08+r56omX9/mUvA/tu9EWezuHM1Tib5OCGP249N3/vpRGkzMa3P
LW23NApTquGTed5shyaSHskEaUsJ2ziYc+CTkPAVnmbLOiM866zizZpsIAlxJc9/
cBiQrTFw/UpaUAG1AQZcOehtwOB11gxoRq03HAzPC2hajM05qmtsOklyLWJrnzg2
hfh3rtVVE4vL9h96tcn2CDUHS/8FJ/Ji47GIQl9sRChKohUjcHNTYprBOugHc0Rb
0ip7BLyoyNaLxTb4Hq8Mjx0bVMv9P+4kc1/05YBeXbsj6RRCsQZcWvQlPbQz/hPV
LbIGqqazaGKxtG7bTT9Cf7LJaqwcpzIt9nGH8/z1sro/4uaZpjjEwXEccmbAe/in
gU+DtnW/J8qrEjjXT/KemLjicPmeTRFQ/F3AUwRpQwtKvGfYyvZNtflnL1j839Ds
x4M94qdO
=N1lH
-----END PGP SIGNATURE-----

commit cd0771df215b2660ddad45ecc4a00baad7024e00 (HEAD -> master, tag: v0.1.0.0)
Author: Mari-Mur-Meow <mashmar2006@mail.ru>
Date:   Mon May 12 22:39:01 2025 +0300

:
Tagger: Mari-Mur-Meow <mashmar2006@mail.ru>
Date:   Tue May 13 21:00:04 2025 +0300

Initial release version 0.1.0.0
-----BEGIN PGP SIGNATURE-----

iQGzBAABCgAdFiEE7Unq4CXexAZryAVUq09hVc/J9L0FAmgjiKQACgkQq09hVc/J
9L1MjQv8DAJjz37vuoZKbn7oo5v0jfFKM6yxpWPEkMYUxsce6AdUlqwXj7W0YOfo
O1feKa7APFuHx08+r56omX9/mUvA/tu9EWezuHM1Tib5OCGP249N3/vpRGkzMa3P
LW23NApTquGTed5shyaSHskEaUsJ2ziYc+CTkPAVnmbLOiM866zizZpsIAlxJc9/
cBiQrTFw/UpaUAG1AQZcOehtwOB11gxoRq03HAzPC2hajM05qmtsOklyLWJrnzg2
hfh3rtVVE4vL9h96tcn2CDUHS/8FJ/Ji47GIQl9sRChKohUjcHNTYprBOugHc0Rb
0ip7BLyoyNaLxTb4Hq8Mjx0bVMv9P+4kc1/05YBeXbsj6RRCsQZcWvQlPbQz/hPV
LbIGqqazaGKxtG7bTT9Cf7LJaqwcpzIt9nGH8/z1sro/4uaZpjjEwXEccmbAe/in
gU+DtnW/J8qrEjjXT/KemLjicPmeTRFQ/F3AUwRpQwtKvGfYyvZNtflnL1j839Ds
x4M94qdO
=N1lH
-----END PGP SIGNATURE-----

commit cd0771df215b2660ddad45ecc4a00baad7024e00 (HEAD -> master, tag: v0.1.0.0)
Author: Mari-Mur-Meow <mashmar2006@mail.ru>
Date:   Mon May 12 22:39:01 2025 +0300

    Update README.md

diff --git a/README.md b/README.md
index e69de29..47003e7 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1,3412 @@
+murka2006@murka:~$  export GITHUB_USERNAME=Mari-Mur-Meow^M
+murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace^M
+murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .^M
+~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace^M
+murka2006@murka:~/Mari-Mur-Meow/workspace$ source scripts/activate^M

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git push origin master --tags
Username for 'https://github.com': Mari-Mur-Meow
Password for 'https://Mari-Mur-Meow@github.com': 
Перечисление объектов: 951, готово.
Подсчет объектов: 100% (951/951), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (290/290), готово.
Запись объектов: 100% (951/951), 607.77 КиБ | 202.59 МиБ/с, готово.
Всего 951 (изменений 635), повторно использовано 950 (изменений 635), повторно использовано пакетов 0
remote: Resolving deltas: 100% (635/635), done.
To https://github.com/Mari-Mur-Meow/lab09
 * [new branch]      master -> master
 * [new tag]         v0.1.0.0 -> v0.1.0.0
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$  github-release --version
github-release: команда не найдена
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ sudo apt update
[sudo] пароль для murka2006: 
Попробуйте ещё раз.
[sudo] пароль для murka2006: 
Сущ:1 http://ru.archive.ubuntu.com/ubuntu noble InRelease
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]     
Пол:3 https://repo.yandex.ru/yandex-browser/deb beta InRelease [4 333 B]       
Пол:4 http://ru.archive.ubuntu.com/ubuntu noble-backports InRelease [126 kB]   
Пол:5 http://security.ubuntu.com/ubuntu noble-security InRelease [126 kB]      
Пол:6 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 Packages [1 067 kB]
Пол:7 http://ru.archive.ubuntu.com/ubuntu noble-updates/main i386 Packages [467 kB]
Пол:8 http://ru.archive.ubuntu.com/ubuntu noble-updates/main Translation-en [230 kB]
Пол:9 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 Components [161 kB]
Пол:10 http://ru.archive.ubuntu.com/ubuntu noble-updates/restricted amd64 Components [212 B]
Пол:11 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe i386 Packages [642 kB]
Пол:12 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 Packages [1 062 kB]
Пол:13 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 Components [376 kB]
Пол:14 http://ru.archive.ubuntu.com/ubuntu noble-updates/multiverse amd64 Components [940 B]
Пол:15 http://ru.archive.ubuntu.com/ubuntu noble-backports/main amd64 Components [7 096 B]
Пол:16 http://ru.archive.ubuntu.com/ubuntu noble-backports/restricted amd64 Components [212 B]
Пол:17 http://ru.archive.ubuntu.com/ubuntu noble-backports/universe amd64 Components [16,3 kB]
Пол:18 http://ru.archive.ubuntu.com/ubuntu noble-backports/multiverse amd64 Components [212 B]
Пол:19 https://packages.microsoft.com/repos/vscode stable InRelease [3 594 B]  
Пол:20 https://packages.microsoft.com/repos/code stable InRelease [3 590 B]    
Пол:21 http://security.ubuntu.com/ubuntu noble-security/main amd64 Packages [822 kB]
Пол:22 https://packages.microsoft.com/repos/vscode stable/main amd64 Packages [26,9 kB]
Пол:23 https://packages.microsoft.com/repos/code stable/main armhf Packages [19,4 kB]
Пол:24 https://packages.microsoft.com/repos/code stable/main amd64 Packages [19,1 kB]
Пол:25 https://packages.microsoft.com/repos/code stable/main arm64 Packages [19,3 kB]
Пол:26 http://security.ubuntu.com/ubuntu noble-security/main i386 Packages [279 kB]
Пол:27 http://security.ubuntu.com/ubuntu noble-security/main Translation-en [153 kB]
Пол:28 http://security.ubuntu.com/ubuntu noble-security/main amd64 Components [21,6 kB]
Пол:29 http://security.ubuntu.com/ubuntu noble-security/restricted amd64 Components [212 B]
Пол:30 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Packages [838 kB]
Пол:31 http://security.ubuntu.com/ubuntu noble-security/universe Translation-en [183 kB]
Пол:32 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Components [52,3 kB]
Пол:33 http://security.ubuntu.com/ubuntu noble-security/multiverse amd64 Components [212 B]
Получено 6 852 kB за 38с (181 kB/s)                                            
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Может быть обновлено 237 пакетов. Запустите «apt list --upgradable» для их показа.
N: Пропускается получение настроенного файла «main/binary-i386/Packages», так как репозиторий «https://packages.microsoft.com/repos/vscode stable InRelease» не поддерживает архитектуру «i386»
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ sudo apt install github-release
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
E: Невозможно найти пакет github-release
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ sudo apt install golang
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Следующий пакет устанавливался автоматически и больше не требуется:
  libllvm17t64
Для его удаления используйте «sudo apt autoremove».
Будут установлены следующие дополнительные пакеты:
  golang-1.22 golang-1.22-doc golang-doc
Следующие НОВЫЕ пакеты будут установлены:
  golang golang-1.22 golang-1.22-doc golang-doc
Обновлено 0 пакетов, установлено 4 новых пакетов, для удаления отмечено 0 пакетов, и 237 пакетов не обновлено.
Необходимо скачать 118 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 678 kB.
Хотите продолжить? [Д/н] Д
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 golang-1.22-doc all 1.22.2-2ubuntu0.3 [107 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 golang-1.22 all 1.22.2-2ubuntu0.3 [5 702 B]
Пол:3 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 golang-doc all 2:1.22~2build1 [2 788 B]
Пол:4 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 golang amd64 2:1.22~2build1 [2 736 B]
Получено 118 kB за 0с (1 245 kB/s)         
Выбор ранее не выбранного пакета golang-1.22-doc.
(Чтение базы данных … на данный момент установлено 264803 файла и каталога.)
Подготовка к распаковке …/golang-1.22-doc_1.22.2-2ubuntu0.3_all.deb …
Распаковывается golang-1.22-doc (1.22.2-2ubuntu0.3) …
Выбор ранее не выбранного пакета golang-1.22.
Подготовка к распаковке …/golang-1.22_1.22.2-2ubuntu0.3_all.deb …
Распаковывается golang-1.22 (1.22.2-2ubuntu0.3) …
Выбор ранее не выбранного пакета golang-doc.
Подготовка к распаковке …/golang-doc_2%3a1.22~2build1_all.deb …
Распаковывается golang-doc (2:1.22~2build1) …
Выбор ранее не выбранного пакета golang:amd64.
Подготовка к распаковке …/golang_2%3a1.22~2build1_amd64.deb …
Распаковывается golang:amd64 (2:1.22~2build1) …
Настраивается пакет golang-1.22-doc (1.22.2-2ubuntu0.3) …
Настраивается пакет golang-doc (2:1.22~2build1) …
Настраивается пакет golang-1.22 (1.22.2-2ubuntu0.3) …
Настраивается пакет golang:amd64 (2:1.22~2build1) …
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ go install github.com/aktau/github-release@latest
go: finding module for package github.com/dustin/go-humanize
go: finding module for package github.com/voxelbrain/goptions
go: finding module for package github.com/github-release/github-release/github
go: found github.com/dustin/go-humanize in github.com/dustin/go-humanize v1.0.1
go: found github.com/github-release/github-release/github in github.com/github-release/github-release v0.10.1
go: found github.com/voxelbrain/goptions in github.com/voxelbrain/goptions v0.0.0-20180630082107-58cddc247ea2
go: finding module for package github.com/tomnomnom/linkheader
go: finding module for package github.com/kevinburke/rest/restclient
go: found github.com/kevinburke/rest/restclient in github.com/kevinburke/rest v0.0.0-20240617045629-3ed0ad3487f0
go: found github.com/tomnomnom/linkheader in github.com/tomnomnom/linkheader v0.0.0-20180905144013-02ca5825eb80
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ echo 'export PATH="$PATH:$(go env GOPATH)/bin"' >> ~/.bashrc
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ source ~/.bashrc
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ github-release --version
github-release v0.10.1
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ github-release info -u ${GITHUB_USERNAME} -r lab09
tags:
- v0.1.0.0 (commit: https://api.github.com/repos/Mari-Mur-Meow/lab09/commits/cd0771df215b2660ddad45ecc4a00baad7024e00)
releases:
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ github-release release \
> --user ${GITHUB_USERNAME} \
    --repo lab09 \
    --tag v0.1.0.0 \
    --name "libprint" \
    --description "my first release"
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$  export PACKAGE_OS=`uname -s` PACKAGE_ARCH=`uname -m` 
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$  export PACKAGE_FILENAME=print-${PACKAGE_OS}-${PACKAGE_ARCH}.tar.gz
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ github-release upload \
>  --user ${GITHUB_USERNAME} \
    --repo lab09 \
    --tag v0.1.0.0 \
    --name "${PACKAGE_FILENAME}" \
    --file _build/*.tar.gz
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ github-release info -u ${GITHUB_USERNAME} -r lab09
tags:
- v0.1.0.0 (commit: https://api.github.com/repos/Mari-Mur-Meow/lab09/commits/cd0771df215b2660ddad45ecc4a00baad7024e00)
releases:
- v0.1.0.0, name: 'libprint', description: 'my first release', id: 218368513, tagged: 13/05/2025 at 18:00, published: 13/05/2025 at 18:50, draft: ✗, prerelease: ✗
  - artifact: print-Linux-x86_64.tar.gz, downloads: 0, state: uploaded, type: application/octet-stream, size: 5.9 kB, id: 254346779
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ wget https://github.com/${GITHUB_USERNAME}/lab09/releases/download/v0.1.0.0/${PACKAGE_FILENAME}
--2025-05-13 21:51:52--  https://github.com/Mari-Mur-Meow/lab09/releases/download/v0.1.0.0/print-Linux-x86_64.tar.gz
Распознаётся github.com (github.com)… 140.82.121.4
Подключение к github.com (github.com)|140.82.121.4|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://objects.githubusercontent.com/github-production-release-asset-2e65be/982968093/000a1659-61a3-40b1-b270-6ba826213e60?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20250513%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250513T185155Z&X-Amz-Expires=300&X-Amz-Signature=886d3f8413d1358b65d06e4dd39e4ad61219f06801a71fde5ba6c57fa0cfdbec&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dprint-Linux-x86_64.tar.gz&response-content-type=application%2Foctet-stream [переход]
--2025-05-13 21:51:56--  https://objects.githubusercontent.com/github-production-release-asset-2e65be/982968093/000a1659-61a3-40b1-b270-6ba826213e60?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=releaseassetproduction%2F20250513%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250513T185155Z&X-Amz-Expires=300&X-Amz-Signature=886d3f8413d1358b65d06e4dd39e4ad61219f06801a71fde5ba6c57fa0cfdbec&X-Amz-SignedHeaders=host&response-content-disposition=attachment%3B%20filename%3Dprint-Linux-x86_64.tar.gz&response-content-type=application%2Foctet-stream
Распознаётся objects.githubusercontent.com (objects.githubusercontent.com)… 185.199.111.133, 185.199.109.133, 185.199.110.133, ...
Подключение к objects.githubusercontent.com (objects.githubusercontent.com)|185.199.111.133|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 5868 (5,7K) [application/octet-stream]
Сохранение в: ‘print-Linux-x86_64.tar.gz’

print-Linux-x86_64.tar 100%[===========================>]   5,73K  --.-KB/s    за 0s      

2025-05-13 21:52:01 (33,0 MB/s) - ‘print-Linux-x86_64.tar.gz’ сохранён [5868/5868]

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ tar -ztf ${PACKAGE_FILENAME}
print-0.1.0.0-Linux/cmake/
print-0.1.0.0-Linux/cmake/print-config.cmake
print-0.1.0.0-Linux/cmake/print-config-noconfig.cmake
print-0.1.0.0-Linux/lib/
print-0.1.0.0-Linux/lib/libprint.a
print-0.1.0.0-Linux/include/
print-0.1.0.0-Linux/include/print.hpp
print-0.1.0.0-Linux/bin/
print-0.1.0.0-Linux/bin/demo
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git add .
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ git commit -m" final commit"
[master e6c9d7e]  final commit
 2 files changed, 95 insertions(+), 95 deletions(-)
 create mode 100644 print-Linux-x86_64.tar.gz
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$  git push origin master 
Username for 'https://github.com': Mari-Mur-Meow
Password for 'https://Mari-Mur-Meow@github.com': 
Перечисление объектов: 6, готово.
Подсчет объектов: 100% (6/6), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (4/4), готово.
Запись объектов: 100% (4/4), 6.63 КиБ | 6.63 МиБ/с, готово.
Всего 4 (изменений 2), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Mari-Mur-Meow/lab09
   cd0771d..e6c9d7e  master -> master
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab09$ 
