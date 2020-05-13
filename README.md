# Документация

**GitHub Pages:**<br>
https://sadcat88.github.io/finStream/app/prod/index.html<br>

## Описание:

В проекте используется компонентная архитектура, <br>
а точней вольная интерпретация методологии БЭМ. <br>
Сборка проекта с помощью Gulp. <br>

<br>
Структура папок:<br>
app - корневая папка для сборки проекта<br>
∟ src - исходники pug + SCSS.<br>
∟ dev - собранные HTML + css + map. Без минификации. <br>
∟ prod - минификация, автопрефиксы, изъятие неиспользуемых стилей из вендорных файлов.<br>
сжатие картинок.<br>
<br>
<br>

**Кросбраузерность и поддержка старых версий** <br>
Для каждого начертания шрифта имеется 5 разных форматов (.ttf, .woff, .woff2, .eot, .svg)<br>
Все CSS файлы прогоняются через Autoprefix. <br>
<br>
Вендорные префиксы проставляются согласно следующему алгоритму:

- последние 10 версий всех браузеров
- 1% самых популярных версий всех браузеров
- IE 10, 9, 8
  <br>
  <br>

**Адаптивность** <br>
Bootstrap 4. <br>
Только сетка. <br>
<br>
<br>

**Сборка** <br>
Во время сборки в режиме development происходит автоматическая проверка HTML <br>
на валидность, а для css создаются map файлы, для удобства отладки, <br>
т.к. вся разработка велась в SCSS.
<br>
Переменные, для удобства кастомизации, вынесены в отдельный файл <br>
/assets/css/utils/\_vars.scss <br>
<br>
Шрифты подключены из папки /assets/fonts/ <br>
CDN не используется для повышения надежности, т.к. Роскомнадзор может <br>
их заблокировать за компанию с Телеграмом.
<br>
Во время сборки в режиме production все css файлы проходят через минификацию. <br>
К именам css файлов в строке подключения добавляются хэши для оптимизации загрузки <br>
на стороне клиента. Также все изображения проходят через автоматическое сжатие <br>
с заранее выбранным качеством <br>
<br>
