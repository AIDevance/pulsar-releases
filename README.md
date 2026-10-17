# Pulsar VPN

VPN-клиент для **Windows, Linux и Android** от AIDevance. Работает поверх Xray-core.

**[Скачать последнюю версию](https://github.com/AIDevance/pulsar-releases/releases/latest)** · [Все выпуски и изменения](https://github.com/AIDevance/pulsar-releases/releases)

## Что скачать

| Система | Файл в выпуске |
| --- | --- |
| Windows 10/11, x64 | `Pulsar-VPN-windows-setup.exe` |
| Android 8 и новее, большинство телефонов | `Pulsar-VPN-arm64-v8a.apk` |
| Android, устройства и эмуляторы x86_64 | `Pulsar-VPN-x86_64.apk` |
| Arch Linux, x86_64 | `Pulsar-VPN-arch-x86_64.pkg.tar.zst` |
| Debian, Ubuntu и производные, amd64 | `Pulsar-VPN-debian-amd64.deb` |
| Другие дистрибутивы Linux, x86_64 | `Pulsar-VPN-linux-x86_64.tar.gz` |

На странице выпуска раскройте **Assets** и выберите файл для своей системы. В описании каждого выпуска — «Что нового».

## Установка

### Windows

Запустите установщик и следуйте его подсказкам. При обновлении установите новую версию поверх прежней. Режим TUN при первом включении запрашивает права администратора.

### Android

Скачайте APK, разрешите установку из выбранного браузера или файлового менеджера и откройте файл. При первом подключении подтвердите создание VPN-соединения. Для обновления установите новый APK поверх прежнего; проверка обновлений есть в Настройках приложения.

### Arch Linux

В каталоге со скачанным пакетом:

```sh
sudo pacman -U ./Pulsar-VPN-arch-x86_64.pkg.tar.zst
sudo systemctl enable --now pulsar@$USER
```

### Debian и Ubuntu

В каталоге со скачанным пакетом:

```sh
sudo apt install ./Pulsar-VPN-debian-amd64.deb
sudo systemctl enable --now pulsar@$USER
```

### Linux: архив tar.gz

Установите зависимости: `iproute2`, `glib2` (в Debian/Ubuntu — `libglib2.0-bin`), GTK 3, `wl-clipboard`, `xdg-utils` и systemd. Затем распакуйте архив в корень системы:

```sh
sudo tar -xzf Pulsar-VPN-linux-x86_64.tar.gz -C /
sudo systemctl daemon-reload
sudo systemctl enable --now pulsar@$USER
```

После установки на Linux откройте **Pulsar** из меню приложений. Командная строка также доступна: `pulsar status`, `pulsar up`, `pulsar down`.

## Первое подключение

Откройте приложение, добавьте ссылку на свою подписку или узел в разделе **Подписки**, затем включите VPN на **Главной**. Подписку предоставляет ваш VPN-провайдер; она не входит в приложение. В Настройках есть руководство «Как пользоваться Pulsar».

## Проверка файлов

В каждом выпуске есть `latest.json` с версией и SHA-256 опубликованных файлов. Сравните сумму скачанного файла с соответствующей записью:

```sh
sha256sum Pulsar-VPN-arm64-v8a.apk
```

В Windows PowerShell:

```powershell
Get-FileHash .\Pulsar-VPN-windows-setup.exe -Algorithm SHA256
```

Этот репозиторий содержит готовые сборки Pulsar. Разработчик — **AIDevance**.
