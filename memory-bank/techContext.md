### Технический контекст

— Обновлено: автоматически из репозитория на момент генерации.

#### Платформа и язык
- **Платформа**: 1С:Предприятие 8.3.21.1895 (см. `tools/local-test/default.env`)
- **Язык**: BSL (1С)
- ** IDE/Инструменты разработки**: 1C:EDT 2023.3.5+10, Конфигуратор 1С

#### Состав репозитория и модули
- **Расширения 1С**:
  - `exts/yaxunit/src` — основной движок YAxUnit
  - `exts/smoke/src` — дымовой тест-движок на базе YAxUnit
- **Тесты**: `tests/src` — модульные тесты на YAxUnit
- **Демо-конфигурация для тестов**: `fixtures/demo-configuration`
- **Схема jUnit**: `fixtures/junit/JUnit.xsd`
- **Документация**: `documentation/` (Docusaurus, Node/Yarn), сборка — `documentation/build-full-doc.sh`

#### Локальная среда и инфраструктура
- **Локальный сервер 1С (Docker)**: `tools/local-test/onec-server/`
  - `docker-compose.yml`, `build/Dockerfile`, `build/conf.cfg`, `build/logcfg.xml`
  - Скрипты установки/обновления: `build/scripts/*.sh`
- **Переменные окружения**: `tools/local-test/default.env` (`ONEC_VERSION`, `EDT_VERSION`)

#### CI/CD и качество
- **GitHub Actions**: значки в `README.md` — анализ Sonar, тесты, сборка документации
- **SonarQube**: `openbsl` Quality Gate/метрики

#### Отчётность тестов
- Поддерживаемые форматы отчётов: **jUnit**, **Allure** (см. документацию в `documentation/docs/features/reports/` и API `documentation/api/ЮТАлюр.md`)
- Текущая задача ветки `feature/multiple-report-formats`: параллельная генерация нескольких форматов (см. `memory-bank/tasks.md`)

#### Стандарты и соглашения
- Отступы — табуляция
- Генерировать док-комментарии для экспортных методов (к тестам не применять)
- Проверка контекста исполнения — сначала `#Если Сервер Тогда ... #Иначе ... #КонецЕсли`
- Именование и структура модулей — согласно стандартам 1С (процедуры/функции, области, обработка ошибок через «Попытка-Исключение»)

#### Интеграции и коммуникации
- **Документация**: сайт на Docusaurus (см. значок в `README.md`)
- **Телеграм**: `t.me/BIAOpenTools/12` (ссылка в `README.md`)

#### Лицензирование
- Apache License 2.0 (см. `LICENSE` и `README.md`)


