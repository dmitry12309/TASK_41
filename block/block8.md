Просмотр изменений в файловых системах

Команда git status отображает все файлы, которые различаются между тремя разделами. У файлов есть 4 состояния:

Неотслеживаемый (untracked) — находится в рабочей директории, но нет ни одной версии в HEAD или в области подготовленных файлов (Git не знает о файле).
Изменён (modified) — в рабочей директории есть более новая версия по сравнению с хранящейся в HEAD или в области подготовленных файлов (изменения не находятся в следующем коммите).
Подготовлен (staged) — в рабочей директории и области подготовленных файлов есть более новая версия по сравнению с хранящейся в HEAD (готов к коммиту).
Без изменений — одна версия файла во всех разделах, т. е. в последнем коммите содержится актуальная версия.

Примечание Файл может быть одновременно в состоянии «изменён» и «подготовлен», если версия в рабочей директории новее, чем в области подготовленных файлов, которая в свою очередь новее версии в HEAD.

Мы можем использовать опцию -s для команды git status, чтобы получить более компактный вывод (по строке на файл). Если файл не отслеживается, то будет выведено ??; если он был изменён, то его имя будет красным, а если подготовлен — зелёным.

Чтобы посмотреть сами изменения, а не изменённые файлы, можно использовать следующие команды:

git diff — сравнение рабочей директории с областью подготовленных файлов;
git diff --staged — сравнение области подготовленных файлов с HEAD.
Если использовать аргумент <файл/папка>, то diff покажет изменения только для указанных файлов/папок, например git diff src/.

Обновление файловых систем
Команда git add <файл/папка> обновляет область подготовленных файлов версиями файлов/папок из рабочей директории.

Команда git commit обновляет HEAD новым коммитом, который делает снимки файлов в области подготовленных файлов.

Действие команды git reset <коммит> состоит из трёх потенциальных шагов:

Переместить указатель HEAD на <коммит> (например, при откате коммита в рабочей директории и области подготовленных файлов будут более новые версии файлов, чем в HEAD). Также указатель HEAD ветки будет перемещён на этот коммит.
Обновить область подготовленных файлов содержимым коммита. В таком случае только в рабочей директории будут новейшие версии файлов.
Обновить рабочую директорию содержимым области подготовленных файлов. С этим нужно быть осторожнее, поскольку в итоге будут уничтожены изменения файлов.
По умолчанию команда git reset выполняет только шаги 1 и 2, однако её поведение можно изменить с помощью опций --soft (только 1 шаг) и --hard (все шаги).

Если передать путь к файлу/папке, то команда будет выполнена только для них, например git reset --soft HEAD~1 src/.

Команда git checkout HEAD <файл> приводит к тому же результату, что и git reset --hard HEAD <файл> — перезаписывает версию файла в области подготовленных файлов и в рабочей директорией версией из HEAD, то есть отменяет изменения после последнего коммита.

С другой стороны, git checkout <файл> (уже без HEAD) перезаписывает версию файла в рабочей директории версией в области подготовленных файлов, то есть отменяет изменения с момента последней подготовленной версии.

Наконец, git rm <файл> отменяет отслеживание файла и удаляет его из рабочей директории, опция --cached позволит сохранить файл.