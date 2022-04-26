# Автоматизированная установка программ для windows 10 / 11

Первое что нужно сделать, для того что бы можно было воспользоваться автоматической установкой это:

* Откройте командную строку (power shell) от имени администратора
* Выполните одну из этих двух команд `Set-ExecutionPolicy AllSigned ` или `Set-ExecutionPolicy Bypass -Scope Process`
* Подвердите выполнение команды вписав `Y` а после одной из выполненых команд выполните следующую команду
* Следующим выполните эту команду
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Все вы готовы к автоматической установке программ. Для того что бы запустить установку программ. Кликните правой кнопокй мыши на файлы установки и запустите их  `от имени администратора` это <b>важно</b>!

## Возвращаем старое контекстное меню на Windows 11
Для возвращения старого конектсного меню нужно либо запустит файл `W11ClassicMenu.bat`
или же выполнить команду
```
reg.exe add “HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32” /f
taskkill /F /IM explorer.exe
start explorer.exe
```

## Установка других программ не входящих в списки файлов
Для того что бы установить программу которая не входит в основной список программа нужно выполнить такую команду в консоле от имени разработчика
```
choco install имя_программы -y --ignore-checksums
```

Все доступные программы вы можете нанйти на странице [Community Maintained Packages](https://community.chocolatey.org/packages)

Вы можете указывать основные параметры в команду
* `-y` - Подтвердить автоматически все соглашения
* `--ignore-checksums` - игнорировать проверку чексуммы, желательно всегда указывать
* `-v`, `--version`  - Указать версию программы, если не указывать скачаеться самая послежняя

Все доступные команды и параметры доступны на странице [Commands](https://docs.chocolatey.org/en-us/choco/commands/)

## Удалить программу
Для удаления каконибудь программы нужно выполнить команду
```
choco uninstall имя_программы
```

## Описание файлов
Описание всех файлов и устанавливающих программ

### Common.bat
Устанавливает все самые важные пакеты для windows такие как:
* [Klite Codec Pack - Все основные видео кодеки](https://codecguide.com/)
* [Microsoft Visual C++ Все версии](https://docs.microsoft.com/ru-ru/cpp/windows/latest-supported-vc-redist?view=msvc-170)
* [Google Chrome чистый](https://www.google.com/intl/ru_ru/chrome/)
* [Архиватор 7-zip](https://www.7-zip.org/)
* [AdwCleaner](https://ru.malwarebytes.com/adwcleaner/)
* [Dot Net пакеты всеx версий](https://dotnet.microsoft.com/en-us/)
* [Flameshot](https://flameshot.org/)

### GamingPrograms.bat
Устанавливает лаунчеры игр и другое
* [Discord](https://discord.com/download)
* [Steam](https://store.steampowered.com/about/Steam?l=russian)
* [EpicGames Launcher](https://store.epicgames.com/ru/download)
* [PicoTorrent - легковестный бесплатный торрент клиент](https://picotorrent.org/)

### NvidiaDrivers.bat
Для пользователе видеокарт Nvidia
* Актуальный игровой видеодрайвер
* [Geforce Expirience](https://www.nvidia.com/ru-ru/geforce/geforce-experience/)

### WebDev.bat
Программы для web разработчика php, js, python
* [Git](https://git-scm.com/)
* [Php version 7.4](https://www.php.net/downloads.php)
* [Composer](https://getcomposer.org/)
* [NodeJs ver 14.19.1](https://nodejs.org/en/)
* [Python2 и python3](https://www.python.org/downloads/)
* [Figma](https://www.figma.com/)
* [Vscode](https://code.visualstudio.com/)
* [Phpstorm](https://www.jetbrains.com/ru-ru/phpstorm/)
* [OpenSsh](https://www.openssh.com/)
* [Wget](https://www.gnu.org/software/wget/)
* [Curl](https://curl.se/)
* [Winscp](https://winscp.net/eng/docs/lang:ru)
* [Wsl 2](https://docs.microsoft.com/ru-ru/windows/wsl/about)
* [Docker Desktop](https://www.docker.com/products/docker-desktop/)
* [Docker Cli](https://docs.docker.com/engine/reference/run/)
* [Ruby](https://www.ruby-lang.org/ru/)
* [Yarn](https://yarnpkg.com/)