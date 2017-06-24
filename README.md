# Related Link
![version](https://img.shields.io/badge/version-1.0-green.svg?style=flat-square "Version")
![DLE](https://img.shields.io/badge/DLE-10.2_--_11.x_(UTF--8)-red.svg?style=flat-square "DLE Version")
[![CC BY-NC-SA License](https://img.shields.io/badge/license-CC_BY--NC--SA_3.0-blue.svg?style=flat-square)](https://github.com/Gameerr/Ene-Pm/blob/master/LICENSE)

**Модуль DLE Related Link** предназначен для создания релевантой кольцевой переликовки новостей по категории в полной новости. Страницы, связанные в кольцо, будут иметь намного больший статистический вес. А релевантные данные повышат кликабельность и заинтересованость пользователей вашего сайта.
# Требования к системе
* Версия DLE: 10.2 и выше
* Поддерживаемая кодировка: UTF-8
* Версия php: 5.3 и выше
# Установка
1. Залить все файлы к себе на сервер по папкам, предварительно изменив название папки **Default** в **templates** на название своего шаблона.
2. Открыть **fullstory.tpl** и в нужном вам месте вставить подключение<pre><code>{include file="engine/modules/related_link.php?news_id={news-id}"}</code></pre>
# TPL файлы
1. **related_link.tpl** - отвечает за вывод новостей, имеет все те же теги что и краткая новость.
2. **related_block.tpl** - отвечает за показ новостей если они имееються. В файле есть 3 тега:<br/>
  2.1 **{content}** - выводит оформленные новости по шаблону из **related_link.tpl**.<br/>
  2.2 **[content] текст [/content]** - выводит текст внутри тегов если есть похожие новости.<br/>
  2.3 **[not-content] текст [/not-content]** - выводит текст внутри тегов если похожих новостей нет.
# Дополнительно
Стандартно выводиться 5 похожих новостей, для кольцевой перелинковки нужно как минимум 4. По-этому если вам требуеться изменить на 4 или другое число, то вам поможет следующее подключение<pre><code>{include file="engine/modules/related_link.php?news_id={news-id}&limit=4"}</code></pre>Где число 4 и есть количество выводимых новостей.
