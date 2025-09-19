# 🎓 Система учета успеваемости студентов

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/ru/docs/Web/JavaScript)
[![React](https://img.shields.io/badge/React-18.2+-61DAFB?logo=react&logoColor=black)](https://react.dev/)
[![Tauri](https://img.shields.io/badge/Tauri-1.0+-FFC131?logo=tauri&logoColor=black)](https://tauri.app/)
[![SQLite](https://img.shields.io/badge/SQLite-3.40+-003B57?logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Кроссплатформенное десктопное приложение** для учета академической успеваемости студентов в учебных группах. Разработано в качестве курсового проекта по дисциплине "Информационные системы".

![Главное окно приложения](screenshots/main-window.png) <!-- Замените на реальный скриншот -->

## ✨ Возможности

*   **👨‍🎓 Управление студентами и группами:** Добавление, редактирование, удаление студентов и учебных групп.
*   **📊 Ведение журнала успеваемости:** Внесение и изменение оценок по различным дисциплинам.
*   **📈 Аналитика и отчетность:** Построение графиков успеваемости, расчет среднего балла, экспорт данных.
*   **🔍 Умный поиск:** Быстрый поиск студентов, групп и дисциплин.
*   **💾 Локальное хранение данных:** Все данные хранятся локально в файле SQLite, не требуя подключения к интернету.
*   **🖥️ Кроссплатформенность:** Приложение работает на Windows, Linux и macOS.

## 🛠️ Стек технологий

*   **Фронтенд:** React, TypeScript, Vite
*   **Бэкенд:** Node.js (в рамках Tauri)
*   **UI Библиотека:** [название, например: MUI, Chakra UI]
*   **Фреймворк:** Tauri
*   **Язык:** Rust (для нативной части Tauri)
*   **База данных:** SQLite
*   **Инструменты сборки:** Vite, Cargo

## 📦 Установка и запуск

Для запуска проекта необходим предустановленный [Rust](https://www.rust-lang.org/tools/install) и [Node.js](https://nodejs.org/) (версия 18+).

1.  **Клонируйте репозиторий:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2.  **Установите зависимости для фронтенда:**
    ```bash
    npm install
    ```

3.  **Запустите приложение в режиме разработки:**
    ```bash
    npm run tauri dev
    ```

4.  **Для production-сборки:**
    ```bash
    npm run tauri build
    ```
    Собранные исполняемые файлы появятся в папке `src-tauri/target/release/`.

## 🏗️ Структура проекта

src/
├── components/ # React-компоненты (Table, Modal, Forms...)
├── pages/ # Страницы приложения
├── styles/ # Глобальные стили (CSS/SCSS)
├── assets/ # Статические assets (иконки, изображения)
└── ...
src-tauri/
├── src/ # Rust-код (команды Tauri, работа с БД)
├── Cargo.toml # Конфигурация Cargo
└── tauri.conf.json # Конфигурация Tauri
text


## 🗄️ Работа с данными

Приложение использует локальную базу данных SQLite. Файл БД по умолчанию создается в директории конфигурации операционной системы пользователя.

**Основные сущности:**
*   `groups` - Учебные группы
*   `students` - Студенты (связь с группами)
*   `subjects` - Дисциплины
*   `grades` - Оценки (связь со студентами и дисциплинами)

## 📄 Лицензия

Этот проект распространяется под лицензией MIT. Подробнее см. в файле [LICENSE](LICENSE).

## 🤝 Вклад в проект

Вклад в проект приветствуется! Если вы нашли баг или у вас есть предложение:
1. Создайте Issue с подробным описанием.
2. Форкните репозиторий и создайте ветку для вашей функции (`git checkout -b feature/AmazingFeature`).
3. Закоммитьте ваши изменения (`git commit -m 'Add some AmazingFeature'`).
4. Запушьте в ветку (`git push origin feature/AmazingFeature`).
5. Откройте Pull Request.

---

<div align="center">
    <sub>Разработано с ❤️ для курсового проекта</sub>
</div>

Как использовать:

    Скопируйте содержимое выше в файл README.md в корне вашего проекта.

    Обязательно замените placeholder'ы:

        https://github.com/your-username/your-repo-name.git на ссылку на ваш репозиторий.

        [название, например: MUI, Chakra UI] на ту UI-библиотеку, которую вы используете (или удалите, если не используете).

        Добавьте реальные скриншоты вашего приложения в папку screenshots/ и укажите на них путь (замените screenshots/main-window.png).

    Вы можете дополнить или изменить разделы (например, добавить более подробную инструкцию по установке, если есть специфичные шаги, или описать ключевые скрипты в package.json).
