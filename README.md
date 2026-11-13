

# ProcessKeyMapper

**Portable Windows keyboard mapping utility for selected applications.**

ProcessKeyMapper is a portable Windows utility designed to apply keyboard input mappings to selected applications. It consists of independent components responsible for launching, process monitoring, keyboard input handling, and graphical configuration.

---

## Язык / Language

- [Русский](#русский)
- [English](#english)

---

# Русский

## О проекте

**ProcessKeyMapper** — портативная утилита для Windows, предназначенная для переназначения клавиатурного ввода в выбранных приложениях.

Проект ориентирован на автономную работу: необходимые исполняемые файлы и конфигурация находятся в одной переносимой папке. Утилита не требует установки .NET или отдельного пакета Visual C++ Redistributable.

## Основные возможности

- Мониторинг запущенных процессов и автоматический запуск Backend при обнаружении целевого приложения.
- Переназначение клавиатурного ввода для выбранного активного процесса.
- Настройка правил для отдельных приложений.
- Выбор и переключение языка интерфейса.
- Графический интерфейс для настройки и диагностики.
- Поддержка нескольких языков интерфейса.
- Портативная структура файлов и настроек.
- Возможность настройки автоматического запуска.

## Архитектура

Проект состоит из четырёх независимых исполняемых компонентов:

| Компонент | Назначение |
|---|---|
| `ProcessKeyMapper.exe` | Главный Launcher. Проверяет наличие компонентов и запускает необходимые процессы. |
| `PKM_Watcher.exe` | Отслеживает появление целевых процессов и запускает Backend при необходимости. |
| `PKM_Backend.exe` | Обрабатывает клавиатурный ввод и применяет правила переназначения. |
| `PKM_GUI.exe` | Графический интерфейс настроек, справки и диагностики. |

Закрытие графического интерфейса само по себе не останавливает Backend.

## Портативность

ProcessKeyMapper разрабатывается как переносимое приложение.

- Основные файлы располагаются в папке программы.
- Конфигурация и языковые файлы хранятся рядом с приложением.
- Приложение не должно зависеть от путей, привязанных к конкретному компьютеру.
- Для сборок используется статическая версия C Runtime (`/MT`).
- Единственное предусмотренное исключение для системного реестра — необязательная настройка автозапуска через `HKCU Run`.

## Языки интерфейса

Базовые языки проекта:

- Русский — `RU_ru`
- Английский — `EN_en`
- Сербский — `SR_rs`

Языковые файлы располагаются в каталоге `locals`.

## Лицензирование

ProcessKeyMapper распространяется по собственной лицензии с доступным исходным кодом и ограничениями на коммерческое использование.

Наличие публичного исходного кода не означает разрешения на коммерческое использование.

Перед использованием, распространением или созданием производных проектов ознакомьтесь с файлом [`LICENSE.md`](LICENSE.md).

Правила предложений изменений, pull request и локализаций будут описаны в [`CONTRIBUTING.md`](CONTRIBUTING.md).

---

# English

## About

**ProcessKeyMapper** is a portable Windows utility designed to remap keyboard input for selected applications.

The project is built around independent components responsible for launching, process monitoring, keyboard input handling, and graphical configuration.

It is designed to run from a portable directory without requiring .NET or a separately installed Visual C++ Redistributable.

## Key Features

- Process monitoring and automatic Backend startup when a target application is detected.
- Keyboard input remapping for the selected foreground process.
- Per-application mapping rules.
- Graphical configuration and diagnostic interface.
- Multiple interface languages.
- Portable application and configuration structure.
- Optional automatic startup.

## Architecture

The project consists of four independent executable components:

| Component | Purpose |
|---|---|
| `ProcessKeyMapper.exe` | Main Launcher. Validates required components and starts the necessary processes. |
| `PKM_Watcher.exe` | Monitors target processes and starts the Backend when needed. |
| `PKM_Backend.exe` | Handles keyboard input and applies mapping rules. |
| `PKM_GUI.exe` | Provides settings, help, and diagnostic functionality. |

Closing the graphical interface does not stop the Backend.

## Portability

ProcessKeyMapper is designed as a portable application.

- Application files are stored in the program directory.
- Configuration and localization files are stored alongside the application.
- The application should not depend on machine-specific paths.
- Builds use the static C Runtime (`/MT`).
- The only planned registry exception is optional startup configuration through `HKCU Run`.

## Interface Languages

The project's base languages are:

- Russian — `RU_ru`
- English — `EN_en`
- Serbian — `SR_rs`

Localization files are stored in the `locals` directory.

## License

ProcessKeyMapper is distributed under a custom source-available license with restrictions on commercial use.

Public access to the source code does not grant permission for commercial use.

Before using, distributing, or creating derivative projects, read [`LICENSE.md`](LICENSE.md).

Contribution, pull request, and localization requirements will be documented in [`CONTRIBUTING.md`](CONTRIBUTING.md).

---

## Repository

The official repository is the primary source for the project.

Forks and derivative projects must comply with the conditions specified in the license.

