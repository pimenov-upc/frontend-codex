# Правила іменування

Цей документ містить стандарти іменування для різних елементів коду в проекті. Дотримання цих правил забезпечує консистентність та покращує читабельність коду.

## camelCase

- Назви змінних
- Назви констант (не глобальних)
- Назви функцій
- Назви подій
- Назви методів та атрибутів класів
- Атрибути інтерфейсів
- GraphQL поля

## PascalCase

- Імена класів
- Імена інтерфейсів
- Типи, аліаси типів
- Компоненти Vue
- Файли компонентів Vue
- GraphQL типи
- Vuetify компоненти (наприклад, `VBtn`, `VCard`, `VTextField`)
- Custom wrapper компоненти навколо Vuetify (наприклад, `CustomVBtn`, `AppVCard`)

## kebab-case

- URL шляхи
- Імена властивостей JSON
- HTML атрибути
- CSS класи та ідентифікатори
- CSS змінні
- API ендпоінти
- Props у Vue template (наприклад, `:button-color`, `:is-loading`)
- Vuetify props у template (наприклад, `:append-icon`, `:max-width`)
- Назви директорій

## snake_case

- Константи (наприклад, `api_url`, `max_retries`)
- Ключі та ідентифікатори в базах даних (наприклад, `user_id`, `created_at`)
- Назви таблиць в базах даних (наприклад, `user_profiles`, `order_items`)
- Імена файлів

## UPPER_SNAKE_CASE

- Глобальні константи (наприклад, `DEFAULT_TIMEOUT`, `API_KEY`)
- Перемінні середовища (наприклад, `NODE_ENV`, `DATABASE_URL`)
- Імена файлів описів (наприклад, `README`, `LICENSE`, `CHANGELOG`, `CONFIG_FILE`, `SETTINGS_JSON`)
- Імена ключів в enum (наприклад, `STATUS_ACTIVE`, `ROLE_ADMIN`)

## Train-Case

- Властивості HTTP headers (наприклад, `Get-User-Info`, `Update-User-Settings`)
- Може застосовуватися для спеціальних випадків, наприклад, для назв певних файлів або ресурсів, які мають бути легко читабельними (наприклад, `User-Profile-Settings`, `Order-Details-Page`)


