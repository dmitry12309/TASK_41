Перемещение

Вместо совмещения двух ветвей коммитом слияния, перемещение заново воспроизводит коммиты тематической ветки в виде набора новых коммитов базовой ветки, что выливается в более чистую историю коммитов.

Для перемещения используется команда git rebase <основная ветка> <тематическая ветка>, которая воспроизводит изменения тематической ветки на основной; HEAD тематической ветки указывает на последний воспроизведённый коммит