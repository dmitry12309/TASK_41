## Коммиты

Так как коммиты являются основой истории версий, не будет лишним узнать о них немного больше.

Команда *git commit* откроет текстовый редактор для ввода сообщения коммита. Также эта команда принимает несколько распространённых аргументов:

- *m* позволяет написать сообщение вместе с командой, не открывая редактор. Например *git commit -m "Пофиксил баг"*;
- *a* переносит все отслеживаемые файлы в область подготовленных файлов и включает их в коммит (позволяет пропустить git add перед коммитом);
- *--amend* заменяет последний коммит новым изменённым коммитом, что бывает полезно, если вы неправильно набрали сообщение последнего коммита или забыли включить в него какие-то файлы.

Несколько советов, к которым стоит прислушаться:

- Коммитьте часто: вы не сможете откатить изменения, если откатывать не к чему.

- Одно изменение — один коммит: не помещайте все не связанные между собой изменения в один коммит, разделите их, чтобы было проще откатиться.

- Формат сообщений: заголовок должен быть в повелительном наклонении, меньше 50 символов в длину и должен логически дополнять фразу *this commit will ___(this commit will fix bugs — этот коммит исправит баги)*. Сообщение должно пояснять, почему был сделан коммит, а сам коммит показывает, что изменилось. Здесь подробно расписано, как писать сообщения для коммитов.
(Опционально) Не коммитьте незначительные изменения: в большом репозитории множество небольших коммитов могут засорить историю. Хорошим тоном считается делать такие коммиты при разработке, а при добавлении в большой репозиторий объединять их в один коммит.

[*Далее>>*](/block/block11.md)

[*<<Вернуться*](/block/block9.md)

[*<<На главную*](./readme.md)