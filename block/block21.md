GitHub

GitHub — это платформа, которая хранит Git-репозитории на своих множественных серверах. Как пользователь GitHub вы можете хранить свои удалённые репозитории на их серверах, а также вносить вклад в другие open-source репозитории. GitHub дополняет использование Git некоторыми новыми возможностями.

Например, вы можете сделать форк удалённого репозитория, то есть создать свою копию репозитория на севере GitHub. Это полезно в тех случаях, когда у вас нет прав на создание ветки в оригинальном репозитории. Когда вы воспользуетесь командой git clone, ваш локальный репозиторий будет отслеживать удалённый форк как origin, а оригинальный репозиторий как upstream.

После этого вам может понадобиться слить тематическую ветку вашего удалённого репозитория в основную ветку оригинального. Для этого вы можете создать новый Pull Request — запрос на внесение изменений, где GitHub проверяет наличие конфликтов прежде чем повзолить вам провести слияние. Зачастую существуют и другие проверки перед слиянием, например просмотр и одобрение кода или даже запуск тестов. В запросе можно обсудить код, а все коммиты, которые вы отправляете в удалённую тематическую ветку, будут автоматически добавлены в запрос, даже если он был создан до этих коммитов.