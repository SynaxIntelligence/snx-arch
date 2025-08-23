# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Release Notes

### Unreleased [2.0.0] - 27-03-2025
**Новые возможности:**
- [+] добавлен скрипт `static-viewer.min.js` draw.io для поддержки просмотра, редактирования, экспорта xml схем.
  Источник: https://github.com/jgraph/drawio/blob/dev/src/main/webapp/js/viewer-static.min.js
- [+] добавлены стандартные таксономии `tags`, `categories`

### v1.2.0 (2024-07-11)

**Новые возможности:**
- [+] базовый плагин для поддержки просмотра, редактирования, экспорта `BPMN` схем.
- [+] функция сохранения диаграммы в `.svg` в каталоге проекта.
- [+] модуль интеграции с `SILA UNION` (получение `BPMN` схем в `.xml` и `.svg`).
- [+] объекты документации с атрибутами `sila.repository` `sila.object` для получения объектов диаграмм сервера `SILA`.
- [+] добавлены пример `BPMN` диаграмм для проекта `IID-1147`.
- [+] `docker-compose.yml` для развертывания серверов `SILA UNION` `sila/docker-compose.yml`.
- [+] ресурс с документацией `SILA UNION` `sila/docs`

**Улучшения:**
- Отсутствуют

**Исправленные ошибки:**
- Отсутствуют

### v1.1.0 (2024-05-31)

**Новые возможности:**
- [+] проект документации на `HUGO`.
- [+] собственная метамодель архитектуры проекта.
- [+] правила валидации модели.

**Улучшения:**
- [~] форма представления C4 слоев. Разработаны собственные шаблоны представлений на базе PlantUML.

**Исправленные ошибки:**
- Отсутствуют.

### v1.0.0 (2024-04-15)

**Первый выпуск:**
- Выпущена первая версия `IID-1147-Arch`:
    - [+] C4 Model для проекта `IID-1147` с использованием базовой метамодели `DOCHUB`.
