
gulp                    -- Запуск gulp в консоли
Кнопки: Ctrl + C        -- Остановить выполнение команды gulp

*****************************************************************************************

СТАРТ НОВОГО ПРОЕКТА

1. Создать папку проекта
2. Из старого проекта скопировать и вставить в корень нового проекта (или стянуть сборку с Github https://github.com/E-Kot/front_gulp):
- src
- gulpfile.js
- package.json
3. открыть новый проект в редакторе
4. Открыть терминал
5. Выполнить команду: npm i
6. Выполнить команду: gulp

-----------------------------

После СТАРТА проекта, возможно нужно будет подкорректировать плагин Fonter

Как настроить fonter plugin в Gulp?

1. открываем node_modules/gulp-fonter/dist/index.js,
2. находим строку:
newFont.path = source.dirname + '\\' + source.stem + '.' + type;
3. меняем '\\' на '/'

*****************************************************************************************


Чтобы собрать спрайт из набора иконок выполни:
==============================================

1.  gulp

2.  Открыть второй терминал и выполни:

gulp svgSprite

3.  Примеры использования спрайта (код) смотри здесь: 
dist/img/stack/sprite.stack.html 
 
Готовый спрайт (Картинки) тут:
http://localhost:3000/img/stack/sprite.stack.html


*****************************************************************************************


Чтобы преобразовать шрифт otf в ttf выполни:
==============================================
gulp otf2ttf


Заполнение файла src/scss/fonts.scss
==============================================
Чтобы функция срабатывала, файл fonts.scss должен быть абсолютно пустой (даже без пробелов или отступов).
------------------------------------------------------------------------------------

После того, как автоматически заполнился файл src/scss/fonts.scss, 
нужно его подкорректировать в ручную например БЫЛО так:

@include font("ProximaNova-Black", "ProximaNova-Black", "400", "normal");
@include font("ProximaNova-Bold", "ProximaNova-Bold", "400", "normal");
@include font("ProximaNova-BoldIt", "ProximaNova-BoldIt", "400", "normal");
@include font("ProximaNova-Light", "ProximaNova-Light", "400", "normal");
@include font("ProximaNova-LightIt", "ProximaNova-LightIt", "400", "normal");

Вносим ИЗМЕНЕНИЯ:

@include font("ProximaNova", "ProximaNova-Black", "900", "normal");
@include font("ProximaNova", "ProximaNova-Bold", "700", "normal");
@include font("ProximaNova", "ProximaNova-BoldIt", "700", "italic");
@include font("ProximaNova", "ProximaNova-Light", "300", "normal");
@include font("ProximaNova", "ProximaNova-LightIt", "300", "italic");


