---
title: Python Using Pip
localeTitle: Python, использующий Pip
---
Мы видели, как использовать `import` заявления для `import` различных модулей и использования их в наших программах. Сам Python поставляется с несколькими встроенными модулями, но сообщество Python может предложить больше.

> Это модули, которые делают python настолько мощным!

Модули сторонних разработчиков добавляют к Python гораздо больше функциональности. Теперь мы узнаем, как установить эти модули, чтобы мы могли использовать их в наших программах.

Самый простой способ - использовать `pip`
```
pip install <module_name> 
```

Если вы использовали `npm` , вы можете подумать об этом как о _npm_ Python.

Замечание: разница в том, что с npm, `npm install` по умолчанию устанавливает локальные пакеты в проект, тогда как `pip install` по умолчанию устанавливается по умолчанию. Чтобы локально установить модули, вам необходимо создать и активировать так называемую [виртуальную среду](http://docs.python-guide.org/en/latest/dev/virtualenvs/) , поэтому `pip install` устанавливается в папку, в которой находится эта виртуальная среда, а не глобально (для чего могут потребоваться права администратора).

В прошлый раз, в вики `import-statements` указателях, мы использовали пример модуля `requests` . Поскольку это сторонний модуль, мы должны установить его отдельно после установки python.

Установка его будет такой же простой, как `pip install requests` . Вы можете даже передать различные аргументы вместе с ним. То, что вы столкнетесь чаще всего, - `--upgrade` . Вы можете обновить модуль python с помощью:
```
pip install <module_name> --upgrade 
```

Например, чтобы обновить модуль запросов до его последней версии, будет так же просто, как и `pip install requests --upgrade` .

Прежде чем использовать `pip` , вам нужно будет установить его (это довольно просто). Вы можете установить его [здесь](https://bootstrap.pypa.io/get-pip.py)

Просто нажмите на ссылку. И сохраните файл как `get-pip.py` _Не забывайте расширение `.py` ._ И запустите его.

Альтернативой использованию pip было бы попробовать [`easy_install`](https://bootstrap.pypa.io/ez_setup.py) .

Использование `easy_install` также прост. Синтаксис:
```
easy_install <module_name> 
```

Тем не менее, `pip` более популярен, чем использование `easy_install` .

**Примечание.** В некоторых системах, где установлены оба Python 2 и Python 3, `pip` и `pip3` будут делать разные вещи. `pip` устанавливает версию пакета Python 2, а `pip3` будет устанавливать версию пакета Python 3. Для получения дополнительной информации о различии между Python 2 и 3 см. [Это](https://guide.freecodecamp.org/python/python-2-vs-python-3) руководство. Вы можете проверить версию `pip` , выполнив `pip --version` и / или `pip3 --version` :
```
pip3 --version 
 pip 18.0 from /usr/local/lib/python3.5/dist-packages/pip (python 3.5) 
```

Мы также можем создать txt-файл, содержащий список модулей, которые должны быть установлены с помощью pip. Например, мы могли бы создать файл `requirements.txt` и его содержимое:
```
Kivy-Garden==0.1.4 
 macholib==1.5.1 
 idna==2.6 
 geoip2nation==0.1.2 
 docutils>=0.14 
 Cython 
```

В этом файле мы также можем установить версию для установки. После этого, вызывая pip с помощью:
```
 pip install -r <FILE CONTAINING MODULES> 
 
          OR IN OUR CASE 
 
 pip install -r requirements.txt 
```

Необходимо установить все модули, перечисленные в файле.