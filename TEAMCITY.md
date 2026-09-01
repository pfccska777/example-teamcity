# Домашнее задание «TeamCity»

Репозиторий проекта:

https://github.com/pfccska777/example-teamcity

## Выполнено

- поднят TeamCity Server;
- подключён и авторизован TeamCity Agent;
- поднят Nexus Repository Manager;
- настроена публикация Maven-артефактов в Nexus;
- создана Build Configuration в TeamCity;
- для default-ветки `master` выполняется `clean deploy`;
- для остальных веток выполняется `clean test`;
- включён автоматический запуск сборок при изменениях в Git;
- настройки TeamCity сохранены в репозитории через Versioned Settings в каталоге `.teamcity`;
- создана ветка `feature/add_reply`;
- добавлен новый метод `sayReply()`, содержащий слово `hunter`;
- добавлен отдельный unit-тест нового метода;
- сборка ветки `feature/add_reply` успешно прошла 6 тестов;
- `feature/add_reply` слита в `master`;
- сборка `master` успешно опубликована в Nexus;
- настроена публикация `.jar` в TeamCity Artifacts;
- артефакт `plaindoll-0.0.2.jar` успешно сформирован.

## Конфигурация TeamCity

Конфигурация хранится в:

`.teamcity/settings.kts`

Для feature-веток:

`clean test`

Для default-ветки:

`clean deploy`

Artifact rule:

`target/plaindoll-*.jar`

## Результат

CI/CD-процесс успешно настроен.

Сборки feature-веток запускают тестирование, сборки master выполняют deploy в Nexus.

Итоговый `.jar` также доступен в Artifacts TeamCity.
