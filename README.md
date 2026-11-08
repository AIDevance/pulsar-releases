# Pulsar VPN — VPN client for Windows, Linux and Android on Xray-core

**Pulsar VPN** is a VPN client by **AIDevance** for **Windows**, **Linux** and **Android**, built on [Xray-core](https://github.com/XTLS/Xray-core). Add your VPN subscription or a single link — VLESS (including Reality), VMess, Trojan or Shadowsocks — and Pulsar picks the fastest server by itself, proves that your traffic really goes through the VPN, and switches to another server when one slows down or fails.

**[Download the latest version](https://github.com/AIDevance/pulsar-releases/releases/latest)** · [All releases and what is new](https://github.com/AIDevance/pulsar-releases/releases) · [Download page](https://aidevance.github.io/pulsar-releases/) · [Русский ниже](#pulsar-vpn--vpn-клиент-для-windows-linux-и-android-на-xray-core)

## Features

- **Subscriptions and single links:** `vless://` (Reality too), `vmess://`, `trojan://`, `ss://`. Two tiers of servers — primary and reserve.
- **Automatic server choice.** The fastest primary server first; the reserve only when every primary is too slow or does not pass traffic; back to the primary by itself when it is fast again.
- **Honest status.** "Working" only after the external address through the VPN is checked and differs from the direct one; otherwise Pulsar says what is wrong.
- **Split tunneling.** Everything through the VPN, the local network directly, sites of your own country directly, your own lists "through VPN / direct / block", and chosen apps past the VPN or always through it.
- **Kill switch.** When the VPN is unavailable: either the direct internet, or no internet at all until the VPN is back; traffic can be held while the VPN starts.
- **System proxy or TUN** on Windows and Linux; the Android VPN service on phones.
- **Updates from this page.** Settings → Check for updates: the program downloads the new version, checks its SHA-256 against `latest.json` and installs it.
- **Tray and window** on Windows and Linux, the same window as the Android app; English and Russian. Command line `pulsar` everywhere.
- **Share.** A QR code in the program leads to the [download page](https://aidevance.github.io/pulsar-releases/), which offers the file for the scanning device.

A subscription comes from your VPN provider; it is not part of the app.

## Download

| System | File in the release |
| --- | --- |
| Windows 10/11, x64 | `Pulsar-VPN-windows-setup.exe` |
| Android 8 and newer, most phones | `Pulsar-VPN-arm64-v8a.apk` |
| Android, x86_64 devices and emulators | `Pulsar-VPN-x86_64.apk` |
| Arch Linux, x86_64 | `Pulsar-VPN-arch-x86_64.pkg.tar.zst` |
| Debian, Ubuntu and derivatives, amd64 | `Pulsar-VPN-debian-amd64.deb` |
| Other Linux distributions, x86_64 | `Pulsar-VPN-linux-x86_64.tar.gz` |

Direct links to the latest version:

- Windows: https://github.com/AIDevance/pulsar-releases/releases/latest/download/Pulsar-VPN-windows-setup.exe
- Android: https://github.com/AIDevance/pulsar-releases/releases/latest/download/Pulsar-VPN-arm64-v8a.apk
- Debian, Ubuntu: https://github.com/AIDevance/pulsar-releases/releases/latest/download/Pulsar-VPN-debian-amd64.deb

## Install

**Windows.** Run `Pulsar-VPN-windows-setup.exe`. Close other VPN clients first (exit them from the tray). To update, install the new version over the old one, or use Settings → Check for updates. TUN mode asks for administrator rights the first time.

**Android.** Open the APK on the phone and allow installing from this source if asked; confirm the VPN connection on the first connect.

**Linux.** `sudo pacman -U ./Pulsar-VPN-arch-x86_64.pkg.tar.zst` or `sudo apt install ./Pulsar-VPN-debian-amd64.deb`, then `sudo systemctl enable --now pulsar@$USER` and open **Pulsar** from the applications menu. The tar.gz archive and its dependencies are described in Russian below.

**First connection.** Open the app, add your subscription or server link in **Subscriptions**, then turn the VPN on at **Home**.

## Verify the files

Every release has `latest.json` with the version and the SHA-256 of each file: `sha256sum <file>` on Linux, `Get-FileHash <file> -Algorithm SHA256` in Windows PowerShell.

This repository holds the ready builds of Pulsar VPN; the source code is not published here. Developer — **AIDevance**.

---

# Pulsar VPN — VPN-клиент для Windows, Linux и Android на Xray-core

**Pulsar VPN** — VPN-клиент от **AIDevance** для **Windows, Linux и Android**, работает поверх Xray-core. Добавьте подписку своего VPN-провайдера или одну ссылку — VLESS (в том числе Reality), VMess, Trojan, Shadowsocks, — и Pulsar сам выберет самый быстрый сервер, проверит, что трафик действительно идёт через VPN, и перейдёт на другой сервер, если этот замедлится или откажет.

## Возможности

- **Подписки и одиночные ссылки** `vless://` (и Reality), `vmess://`, `trojan://`, `ss://`; два уровня серверов — основной и резервный.
- **Автоматический выбор сервера.** Сначала самый быстрый основной; резерв — только когда все основные слишком медленные или не пропускают трафик; на основной Pulsar возвращается сам.
- **Честный статус.** «Работает» — только после того, как внешний адрес через VPN проверен и отличается от прямого; иначе Pulsar говорит, что не так.
- **Маршрутизация.** Всё через VPN, локальная сеть напрямую, сайты своей страны напрямую, свои списки «через VPN / напрямую / не открывать», выбранные приложения мимо VPN или всегда через VPN.
- **Блокировка трафика (kill switch).** Когда VPN недоступен: прямой интернет или никакого, пока VPN не вернётся; удержание трафика на старте.
- **Системный прокси или TUN** на Windows и Linux; служба VPN Android на телефоне.
- **Обновление с этой страницы.** Настройки → «Проверить обновления»: программа скачает новую версию, сверит SHA-256 с `latest.json` и установит.
- **Трей и окно** на Windows и Linux — то же окно, что приложение на телефоне; русский и английский. Командная строка `pulsar` — везде.
- **Поделиться.** QR-код в программе ведёт на [страницу загрузки](https://aidevance.github.io/pulsar-releases/), которая предлагает файл для системы того, кто его отсканировал.

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
