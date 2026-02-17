# VLF Secure Connect

Windows VPN client with subscription support, flexible routing, deep-link import, and built-in auto-update.

- Windows Releases: https://github.com/skalover32-a11y/VLF-WIndows-VPN-client/releases
- Website: https://www.vlf-project.tech/

---

## EN

### What is it
**VLF Secure Connect** is a proprietary VPN client for Windows (and Android in the main ecosystem), designed for convenient subscription workflows, fast server selection, and predictable updates via GitHub Releases / Google Play.

This repository contains **release builds and documentation only**.  
The application source code is **private and not publicly available**.

### Key features
- Subscription and direct-link support.
- Fast import:
  - from clipboard,
  - via URL,
  - via QR,
  - via deep link `vlf://add/...`.
- Supported profile types:
  - `VLESS`,
  - `VMess`,
  - `Trojan`,
  - `Shadowsocks`,
  - `Hysteria2 / HY2`,
  - `TUIC`,
  - `WireGuard`.
- Routing modes:
  - **Route all traffic through VPN** (lists bypass),
  - **Route all traffic directly** (lists go through VPN).
- Exclusions:
  - websites/domains,
  - applications,
  - service presets (YouTube, Instagram, Facebook, X, TikTok, Telegram, WhatsApp, Discord, Google, Spotify, Netflix, Twitch),
  - country domains (TLD profiles).
- Ping tools:
  - bulk ping for a subscription group,
  - ping a specific server.
- Subscription auto-update:
  - on app start,
  - by interval `2/4/6/8/10/12` hours.
- Tunnel-level ad blocking:
  - `geosite:category-ads-all`.
- Logs:
  - built-in viewer,
  - on Windows: download / clear logs.
- Built-in update checks:
  - Android: Google Play In-App Update,
  - Windows: GitHub Releases.

### Deep link integration
Supported formats:
- `vlf://add/<urlencoded_payload>`
- `vlf://add?url=<urlencoded_payload>`
- `vlf://add#<urlencoded_payload>`

Examples:
- `vlf://add/https%3A%2F%2Fexample.com%2Fsub.txt`
- `vlf://add?url=...` (recommended)
- `vlf://add#vless%3A%2F%2F...`

On Windows the app uses single-instance logic: the link is forwarded to the already running application.

### Installation (Windows)
1. Open the Releases page.
2. Download the latest installer (`VLF_Setup_X.Y.Z.exe`).
3. Install the application.
4. Confirm Administrator privileges if required (needed for TUN mode).

---

## RU

### Что это
**VLF Secure Connect** — проприетарный VPN-клиент для Windows (и Android в экосистеме проекта), ориентированный на удобную работу с подписками, быстрый выбор серверов и предсказуемые обновления через GitHub Releases / Google Play.

Данный репозиторий содержит **только релизы и документацию**.  
Исходный код приложения является **закрытым и публично не распространяется**.

### Ключевые возможности
- Поддержка подписок и прямых ссылок.
- Быстрый импорт:
  - из буфера,
  - по ссылке,
  - через QR,
  - через deep link `vlf://add/...`.
- Поддерживаемые типы профилей:
  - `VLESS`,
  - `VMess`,
  - `Trojan`,
  - `Shadowsocks`,
  - `Hysteria2 / HY2`,
  - `TUIC`,
  - `WireGuard`.
- Режимы маршрутизации:
  - **Весь трафик через VPN** (списки идут в обход),
  - **Весь трафик напрямую** (списки идут через VPN).
- Исключения:
  - сайты/домены,
  - приложения,
  - пресеты сервисов,
  - домены по странам (TLD-профили).
- Пинг:
  - массовая проверка по группе подписки,
  - проверка конкретного сервера.
- Автообновление подписок:
  - при старте приложения,
  - по интервалу `2/4/6/8/10/12` часов.
- Блокировка рекламы в туннеле:
  - `geosite:category-ads-all`.
- Логи:
  - просмотр в приложении,
  - на Windows: скачать / очистить.
- Встроенная проверка обновлений:
  - Android: Google Play,
  - Windows: GitHub Releases.

### Deep link интеграция
Поддерживается формат:
- `vlf://add/<urlencoded_payload>`
- `vlf://add?url=<urlencoded_payload>`
- `vlf://add#<urlencoded_payload>`

### Установка (Windows)
1. Откройте страницу Releases.
2. Скачайте установщик (`VLF_Setup_X.Y.Z.exe`).
3. Установите приложение.
4. При необходимости подтвердите запуск с правами администратора.
