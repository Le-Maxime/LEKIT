# LEKIT - Набор утилит для Comfast WR632AX / Utility Kit for Comfast WR632AX

[Русский](#русский) | [English](#english)

---

## Русский

Интерактивный скрипт-меню для удобной установки, обновления и управления дополнительным программным обеспечением на Wi-Fi роутере **Comfast CF-WR632AX** под управлением OpenWrt.

### Возможности
1. **Выбор языка:** При первом запуске скрипт предлагает выбрать русский или английский язык.
2. **Интерактивное меню:** Быстрое управление установленными пакетами.
3. **Пакеты в комплекте:**
   - **LEBOOT** — Установка и прошивка безопасного загрузчика U-Boot с веб-интерфейсом восстановления (failsafe Web UI), создание резервной копии текущего раздела FIP (загрузчика) прямо из меню, а также автоматическое считывание текущей установленной версии из флеш-памяти роутера.
   - **uFan** — Автоматическое управление охлаждением (кулером) и интеграция мониторинга вентилятора в LuCI.
   - **Proton2025** — Установка и удаление современной темы LuCI Proton2025 (автоматически скачивает последние релизы и поддерживает пакетные менеджеры `opkg` / `apk`).
4. **Автоматическая установка:** При первом запуске скрипт сам копирует себя в систему для быстрого доступа.
5. **Сохранение при обновлении прошивки (sysupgrade):** Автоматически добавляется в конфигурацию sysupgrade, чтобы скрипт остался на роутере после обновления прошивки.
6. **Проверка обновлений:** Проверяет обновления самого LEKIT и установленных пакетов.

### Установка и запуск

Подключитесь к роутеру по SSH и выполните следующую команду:

```bash
wget --no-check-certificate -qO lekit "https://raw.githubusercontent.com/Le-Maxime/LEKIT/main/lekit" && chmod +x lekit && ./lekit
```

При первом запуске утилита автоматически скопирует себя в `/usr/sbin/lekit` и настроит автосохранение.

После этого для запуска меню из любого места достаточно просто ввести:

```bash
lekit
```

---

## English

Interactive menu-driven shell script for convenient installation, updates, and management of additional software on the **Comfast CF-WR632AX** Wi-Fi router running OpenWrt.

### Features
1. **Language Selection:** Prompts for Russian or English on the first run.
2. **Interactive Menu:** Convenient management of installed packages.
3. **Included Packages:**
   - **LEBOOT** — Safe installation and flashing of U-Boot bootloader with failsafe Web UI, backup of the current FIP partition directly from the menu, and automatic retrieval of the currently installed version from the router's flash memory.
   - **uFan** — Automatic fan (cooling) management and Fan monitoring integration for LuCI.
   - **Proton2025** — Installation and removal of the modern LuCI Proton2025 theme (automatically pulls latest releases and supports `opkg` / `apk` package managers).
4. **Automatic System Installation:** Copies itself to the system path on first run for quick access.
5. **sysupgrade Persistence:** Automatically adds itself to the sysupgrade configuration to persist across firmware upgrades.
6. **Update Verification:** Check for updates of LEKIT itself and the installed packages.

### Installation and Launch

Connect to your router via SSH and run the following command:

```bash
wget --no-check-certificate -qO lekit "https://raw.githubusercontent.com/Le-Maxime/LEKIT/main/lekit" && chmod +x lekit && ./lekit
```

On first run, the utility will automatically copy itself to `/usr/sbin/lekit` and configure system persistence.

Afterwards, to run the menu from anywhere, simply enter:

```bash
lekit
```
