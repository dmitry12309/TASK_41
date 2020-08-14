Удалённые серверы
Пока что мы обсуждали использование Git только на локальной машине. Однако мы можем хранить историю коммитов удалённых репозиториев, которую можно отслеживать и обновлять (считайте их удалёнными облачными бэкапами нашей истории коммитов).

Команда git remote -v выводит список удалённых репозиториев, которые мы отслеживаем, и имена, которые мы им присвоили.

При использовании команды git clone <url репозитория> мы не только загружаем себе копию репозитория, но и неявно отслеживаем удалённый сервер, который находится по указанному адресу и которому присваивается имя origin.

Наиболее употребляемые команды:

git remote add <имя> <url> — добавляет удалённый репозиторий с заданным именем;
git remote remove <имя> — удаляет удалённый репозиторий с заданным именем;
git remote rename <старое имя> <новое имя> — переименовывает удалённый репозиторий;
git remote set-url <имя> <url> — присваивает репозиторию с именем новый адрес;
git remote show <имя> — показывает информацию о репозитории.
Следующие команды работают с удалёнными ветками:

git fetch <имя> <ветка> — получает данные из ветки заданного репозитория, но не сливает изменения;
git pull <имя> <ветка> — сливает данные из ветки заданного репозитория;
git push <имя> <ветка> — отправляет изменения в ветку заданного репозитория. Если локальная ветка уже отслеживает удалённую, то можно использовать просто git push или git pull.
Таким образом несколько людей могут запрашивать изменения с сервера, делать изменения в локальных копиях и затем отправлять их на удалённый сервер, что позволяет взаимодействовать друг с другом в пределах одного репозитория.