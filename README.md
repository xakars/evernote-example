# Evernote

Проект позволяет взаимодействовать с API сайта [evernote.com](https://sandbox.evernote.com/).
Используется Python2.

### Установка
Создаем вирутальное окружение для Python2 с помощью библиотеки virtualenv:
```
virtualenv --python="/usr/bin/python2.7" "/path/to/new/virtualenv/
```
Активируем командой:
```
. ./env/bin/activate
```
Устанавливаем зависимости:
```
pip install -r requirements.txt
```
Перед использованием скриптов необходимо получить и положить в файл `.env` переменные виртуального окружения такие как:


`EVERNOTE_CONSUMER_KEY` и `EVERNOTE_CONSUMER_SECRET` получаем [тут](https://dev.evernote.com/#apikey) 

`EVERNOTE_PERSONAL_TOKEN` получаем [тут](https://sandbox.evernote.com/api/DeveloperToken.action)

`JOURNAL_NOTEBOOK_GUID` - GUID(идентификатор) блокнота

`JOURNAL_TEMPLATE_NOTE_GUID` - GUID(идентификатор) заметки

`INBOX_NOTEBOOK_GUID` - GUID блокнота 

## list_notebooks.py
Выводит все блокноты в формате "GUID блокнота - Название":
```console
$ python list_notebooks.py
909daf06-59c3-4dec-8bb1-0a67413f6c09 - GENERAL_Notebook
7f387978-163c-405a-947d-e054fdc7035a - SECOND_NOTEBOOK
```

## dump_inbox.py
Выводит заметки выбранного блокнота в текстовом ввиде.
```console
$ python dump_inbox.py

--------- 1 ---------


Note\n\npuper
```
## add_note2journal.py
Создает новую заметку.
```console
$ python add_note2journal.py
Title Context is:
{
    "date": "2022-10-02",
    "dow": "воскресенье"
}
Note created: SuperTitle
Done
```

