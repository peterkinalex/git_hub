stats.py - сохраняет стистику GitHub репозитория в xls(x) файл если находит библиотеку для работы с этим форматом. В противном случае результат сохраняется в формате CSV.

## Синтаксис
stats.py -u https://github.com/ink-ru/git_hub/ -s

-u - единственный обязательный параметр в котором передается полный HTTP(S) адрес GitHub репозитория.

-s - этот параметр отключает обработку даней без коммитов. Сохраняются только даты с коммитами.

Для вывода справки используйте ключ -h
> stats.py -h

# Windows
Python для Windows можно скачать [тут](https://www.python.org/downloads/windows/). Программа работает с Python версии 3 и выше. Поэтому рекомендуется устанавливать последнюю версию. Путь установки по умолчанию: `C:\Users\georg\AppData\Local\Programs\Python\Python36`

Если вы планируете запускать скрипт другой программой (планировщиком задач) то, для предотвращения появления окна командного процессора, можно использовать интерпретатор *python**w**.exe*. Если же вы хотите увидеть результат работы программы (включая ошибки), используйте классический интерпретатор *python.exe*

Для запуска программы необходимо указывать полные пути:
> C:\Users\georg\Documents>C:\Users\georg\AppData\Local\Programs\Python\Python36\python.exe C:\Users\georg\Documents\stats.py -u https://github.com/ink-ru/git_hub/ -s

Для того чтобы не указывать пути каждый раз можно прописать переменные окружения. Для этого перейдите в "Параметры" => "Дополнительные параметры системы" и на вкладке "Дополнительно" нажмите кнопку "Переменные среды". Далее необходимо в переменную PATH добавить путь к интерпретатору *Python*, например:
> %USERPROFILE%\AppData\Local\Programs\Python\Python36

Теперь, если перейти в директорию со скриптом, можно выполнить команду без указания полных путей:
> cd Documents

> python .\stats.py -u https://github.com/ink-ru/git_hub/ -s

# Linux
В современных дистрибутивах интерпретатор *Pytyon* установлен изначально. Для запуска программы используйте интерпретатор версии 3:

```python3 stats.py -u URL -s```

<!-- https://stackoverflow.com/questions/15587877/run-a-python-script-in-terminal-without-the-python-command -->

# Библиотеки Excel
Если скрипт не находит библиотеки для работы с Excel, то данные будут записаны в CSV формате.

<!-- > sudo apt-get install python-setuptools -->
Для работы с Excel необходимо предварительно установить необходимые модули. Если в системе установлены обе версии *Python*, то мы не можем использовать обычные команды для установки модулей:
> ```sudo easy_install xlsxwriter``` или ```pip install xlsxwriter```

для установки модулей для *Python* версии 3 необходимо использовать установщик `pip3`:
> sudo apt-get -y install python3-pip

> pip3 install xlsxwriter
<!-- > sudo pip3 install xlwt -->

## Ссылки

http://ghv.artzub.com/

https://developer.github.com/v3/repos/statistics/
http://pygithub.readthedocs.io/en/latest/github_objects.html
https://media.readthedocs.org/pdf/pygithub/stable/pygithub.pdf

<!-- get_stats_commit_activity

https://github.com/ink-ru/sublime-snippets/graphs/commit-activity
https://api.github.com/repos/PyGithub/PyGithub/stats/commit_activity -->


