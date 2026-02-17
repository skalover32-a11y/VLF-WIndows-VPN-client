# VLF Secure Connect

Windows VPN client with subscription support, flexible routing, deep-link import, and built-in auto-update.

- Windows Releases: https://github.com/skalover32-a11y/VLF-WIndows-VPN-client/releases
- Source code (active development): https://github.com/skalover32-a11y/vlf_dart
- Website: https://www.vlf-project.tech/

---

## RU

### Что это
**VLF Secure Connect** — VPN-клиент для Windows (и Android в основном репозитории), ориентированный на удобную работу с подписками, быстрый выбор серверов и предсказуемые обновления через GitHub Releases / Google Play.

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
  - пресеты сервисов (YouTube, Instagram, Facebook, X, TikTok, Telegram, WhatsApp, Discord, Google, Spotify, Netflix, Twitch),
  - домены по странам (TLD-профили).
- Пинг:
  - массовая проверка по группе подписки,
  - проверка пинга конкретного сервера.
- Автообновление подписок:
  - при старте приложения,
  - по интервалу `2/4/6/8/10/12` часов.
- Блокировка рекламы в туннеле:
  - `geosite:category-ads-all`.
- Логи:
  - просмотр в приложении,
  - на Windows: скачать / очистить логи.
- Встроенная проверка обновлений:
  - Android: Google Play In-App Update,
  - Windows: GitHub Releases.

### Deep link интеграция
Поддерживается формат:
- `vlf://add/<urlencoded_payload>`
- `vlf://add?url=<urlencoded_payload>`
- `vlf://add#<urlencoded_payload>`

Примеры:
- `vlf://add/https%3A%2F%2Fexample.com%2Fsub.txt`
- `vlf://add?v=url` (рекомендуется `url=...`)
- `vlf://add#vless%3A%2F%2F...`

На Windows используется single-instance логика: ссылка передаётся в уже открытое приложение.

### Установка (Windows)
1. Откройте Releases.
2. Скачайте установщик вида `VLF_Setup_X.Y.Z.exe`.
3. Установите приложение.
4. При необходимости подтвердите запуск с правами администратора (для TUN-сценариев).

### Сборка из исходников (Windows)
Требования:
- Flutter SDK (актуальный stable),
- Visual Studio Build Tools (Desktop C++),
- Inno Setup 6 (для инсталлятора).

Команды:
```powershell
git clone https://github.com/skalover32-a11y/vlf_dart.git
cd vlf_dart
flutter pub get
pwsh tools/check_release_consistency.ps1 -ProjectRoot .
pwsh tools/build_and_package.ps1 -Installer
## EN
### What is it

VLF Secure Connect is a VPN client for Windows (and Android in the main repository), focused on convenient subscription workflows, fast server selection, and predictable updates via GitHub Releases / Google Play. :contentReference[oaicite:1]{index=1}

### Key features
- Subscription & direct-link support.
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
  - Route all traffic through VPN (lists are routed direct),
  - Route all traffic direct (lists are routed through VPN).
- Exclusions:
  - websites/domains,
  - apps,
  - service presets (YouTube, Instagram, Facebook, X, TikTok, Telegram, WhatsApp, Discord, Google, Spotify, Netflix, Twitch),
  - country-based domains (TLD profiles).
- Ping tools:
  - batch ping for a subscription group,
  - ping a specific server.
- Subscription auto-refresh:
  - on app start,
  - by interval `2/4/6/8/10/12` hours.
- Tunnel-level ad blocking:
  - `geosite:category-ads-all`.
- Logs:
  - built-in viewer,
  - on Windows: download / clear logs.
- Built-in update checks:
  - Android: Google Play In-App Update,
  - Windows: GitHub Releases. :contentReference[oaicite:2]{index=2}

### Deep link integration

Supported formats:
- `vlf://add/<urlencoded_payload>`
- `vlf://add?url=<urlencoded_payload>`
- `vlf://add#<urlencoded_payload>`

Examples:
- `vlf://add/https%3A%2F%2Fexample.com%2Fsub.txt`
- `vlf://add?url=...` (recommended)
- `vlf://add#vless%3A%2F%2F...`

On Windows the app uses single-instance logic: the link is forwarded to the already running instance. :contentReference[oaicite:3]{index=3}

### Install (Windows)

1. Open Releases.
2. Download an installer like `VLF_Setup_X.Y.Z.exe`.
3. Install the app.
4. If needed, confirm running as Administrator (required for TUN scenarios). :contentReference[oaicite:4]{index=4}

### Build from source (Windows)

Requirements:
- Flutter SDK (latest stable),
- Visual Studio Build Tools (Desktop C++),
- Inno Setup 6 (for the installer).

Commands:

```bash
git clone https://github.com/skalover32-a11y/vlf_dart.git
cd vlf_dart
flutter pub get
pwsh tools/check_release_consistency.ps1 -ProjectRoot .
pwsh tools/build_and_package.ps1 -Installer
``` :contentReference[oaicite:5]{index=5}


