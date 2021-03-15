# Tutorial 
**Краткое описание**    
Все что трудно замомнить здесь! и на поминания всякие тоже есть
[Обратно](../Цель2021.md)

---
# NAV

- [Tutorial](#tutorial)
- [NAV](#nav)
- [CMD](#cmd)
- [Git and Git-Hab](#git-and-git-hab)
- [Gulp](#gulp)
  - [Install the gulp command line utility](#install-the-gulp-command-line-utility)
  - [Нужно сделать в начале каждого проэкта!](#нужно-сделать-в-начале-каждого-проэкта)
    - [1. **Create a `package.json` file in your project directory**](#1-create-a-packagejson-file-in-your-project-directory)
    - [2. **Install the gulp package in your devDependencies**](#2-install-the-gulp-package-in-your-devdependencies)
    - [3. **Create a `gulpfile.js` file in your project directory**](#3-create-a-gulpfilejs-file-in-your-project-directory)
    - [4. **Create consts**](#4-create-consts)
    - [5. **Add Plagins**](#5-add-plagins)
  - [Path](#path)
  - [Дальше делаем таски](#дальше-делаем-таски)
- [CSS](#css)
  - [Flex-Box](#flex-box)
    - [`justify-content`](#justify-content)
    - [`Align-items`](#align-items)
    - [`flex-direction`](#flex-direction)
  - [Text](#text)
    - [`Text-align`](#text-align)
- [LESS](#less)
  - [Переменные](#переменные)
  - [Oбявляем дополнительный .less](#oбявляем-дополнительный-less)
  - [functions](#functions)
    - [`darken()`](#darken)
    - [`lighten()`](#lighten)
    - [`when()`](#when)
  - [Так тож можно =>](#так-тож-можно-)
  - [Mixins](#mixins)
  - [Media](#media)
  - [EASY Less (_extantion VS Code_)](#easy-less-extantion-vs-code)
    - [Create a `settings.json` in `.vscode`](#create-a-settingsjson-in-vscode)


# CMD
<pre>
1. <kbd>Win</kbd>+<kbd>R</kbd> - Вызов окна "Выполнить"    
2. Далее вводим cmd и все!
</pre>
- Starting commands:
    - `cls` - очистка экрана интерпретатора
    - `dir` - отображение списка файлов и каталогов
    - `cd [/path]` - изменить директорию
    - `.` - текущая директория
    - `..` - предыдущая директория
    - `[f]:` - изменить диск

# Git and Git-Hab

- Starting commands:
  - `git --version`
  - `git --help`
  - `git init` - инициализирует директорию
- Commits:
  - `git status`
  - `git add [file]`
  - `git commit -m [name commit]` - новый комит
- Branchs: 
  - `git branch` - узнать ветку
  - `git branch -m [name]` - создает ветку или переименновывает
  - `git branch -d [name]` - удоляет ветку
  - `git checkout [name]` - переключает ветку
  - `git checkout -b [name]` - создает ветку и переходит на нее
  - `git merge [name]` - соединяет две ветки
- Additionally:
  - `created file .gitignore`
# Gulp
[**up**](#nav)
## Install the gulp command line utility
```
npm install --global gulp-cli
```
## Нужно сделать в начале каждого проэкта!
### 1. **Create a `package.json` file in your project directory**
```json
{
  "neme": "Gulp-web",
  "version": "1.0.0",
  "discription": "It is my first prodject on gulp",
  "aphtpr": "Pop-Locker"
}
```
### 2. **Install the gulp package in your devDependencies**
```
npm install --save-dev gulp
```
### 3. **Create a `gulpfile.js` file in your project directory**
Включаем `строгий режим`:
```
"use strict"
```

### 4. **Create consts**
- `src` - Отвечает за чтение файлов
- `dest` - Отвечает за запись файлов
```javaScript
const {src, dest} = require("gulp")
const gulp = require("gulp")
```
### 5. **Add Plagins**
- `Auto Prefixer`
  - Автоматически ставит превиксы в CSS
```
npm i gulp-autoprefixer --save-dev
```
```js
const autoprefixer = require("gulp-autoprefixer")
```
- `Css Beautify`
  - Автоматически форматирует ваш стиль чтобы можно было его последовательно и легко читать
```
npm i gulp-cssbeautify --save-dev
```
```js
const cssbeautify = require("gulp-cssbeautify")
```
- `Strip Css Comments`
  - Удаляет все коментарии
```
npm i gulp-strip-css-comments --save-dev
```
```js
const strip-css-comments = require("gulp-strip-css-comments")
```
- `Rename`
  - Меняет название файла
```
npm i gulp-rename --save-dev
```
```js
const rename = require("gulp-rename")
```
- `Sass`
  - Компилирует в Sass
```
npm i gulp-sass --save-dev
```
```js
const sass = require("gulp-sass")
```
- `Css Nano`
  - Сжимает Css файлы
```
npm install --save-dev cssnano
```
```js
const cssnano = require("cssnano")
```
- `Rigger`
  - Склеивает все js файлы
```
npm i gulp-rigger --save-dev
```
```js
const rigger = require("gulp-rigger")
```
- `Uglify`
  - Сжимает js файлы
```
npm i gulp-uglify --save-dev
```
```js
const uglify = require("gulp-uglify")
```
- `Plumber`
  -   Формирует вывод об ошибке, при этом работа Gulp не прерывается!
```
npm i gulp-plumber --save-dev
```
```js
const plumber = require("gulp-plumber")
```
- `Image Min`
  - Оптимизирует картинки
```
npm i gulp-imagemin --save-dev
```
```js
const imagemin = require("gulp-imagemin")
```
- `Del`
  - Оптимизирует папку сайта
```
npm i del --save-dev
```
```js
const dev = require("dev")
```
- `Panini`
  - Позволяем работать с HTML, создавать различные темплейты, шаблоны, различные фрагменты кода и подключать их в HTML. (Не шаблонизатор)
```
npm i panini --save-dev
```
```js
const panini = require("panini")
```
- `Browser Sync`
  - Local server
```
npm i browser-sync --save-dev
```
```js
const browsersync = require("browser-sync").create()
```
## Path
In `gulpfile.js`
```js
    // Сюда перемещаем исходники
var path = {
  build: {
    html: "dist/",
    js: "dist/assets/js/",
    css: "dist/assets/css/",
    image: "dist/assets/img/"
  },
    // Исходники
  src: {
    html: "src/*.html",
    js: "src/assets/js/*.js",
    css: "src/assets/sass/stule.scss",
    image: "src/assets/img/**/*.{jpg,png,svg,gif,ico}"
  },
    // Следим
  watch: {
    html: "src/**/*.html",
    js: "src/assets/js/**/*.js",
    css: "src/assets/sass/**/stule.scss",
    image: "src/assets/img/**/*.{jpg,png,svg,gif,ico}"
  },
  // Чистит папку
  clean: "./dist"
```
## Дальше делаем таски
In `gulpfile.js`
```js
function html() {
  return src(paht.src.html, {base: "src/"})
    .pipe(dist(paht.build.html))
}
exports.html = html;
```
# CSS
[**up**](#nav)
## Flex-Box
![flex-box](flex-box.png "Flex-Box")
```css
div {
  display: flex;
}
```
### `justify-content`

Определяет, как элементы flexbox выравниваются в соответствии с главной осью внутри контейнера (main-axis).
- `flex-start` - Элементы flexbox смещаются к началу главной оси контейнера
- `flex-end` - Элементы flexbox смещаются к концу главной оси контейнера
- `center` - Элементы flexbox центрированы вдоль главной оси контейнера
- `space-between` - Оставшееся пространство распределяется между элементами flexbox
- `space-around` - Оставшееся пространство распределяется вокруг элементов flexbox. Пустое пространство до первого и после последнего элемента равно половине пространства между каждым элементом
### `Align-items`
Свойство align-items контролирует выравнивание элементов по поперечной оси (cross axis).

- `flex-start` - Элементы flexbox выровнены в начале поперечной оси
- `flex-end` - Элементы flexbox выровнены в конце поперечной оси
- `center` Элементы flexbox выровнены в центре поперечной оси

### `flex-direction`

Определяет способ размещения элементов в контейнере flexbox, задает основную ось и задает направление элементов
- `row` - Выложит главную ось слева направо
- `row-reverse` - Выложит основную ось справа налево
- `column` - Выложит главную ось сверху вниз
- `column-reverse` - Выложит основную ось снизу вверх

---
## Text
### `Text-align`
Задает выравнивание текста.
- `left` - Выравнивание текста по левому краю
- `right` - Выравнивание текста по правому краю
- `center` - Выравнивание текста по центру
- `justify` - Выравнивание текста по левому и правому краям за исключением последней строки

# LESS 
[**up**](#nav)
## Переменные
```less
  @nameVar: #fff;
  @colormain: #000;
  @fw: 25px;
  @ff: Tarhoma;
```
Можно указывать путь в переменную:
```less
@img: "../img/";
```
```less
.post {
  background: url("@{img}bg.jpg") center no-repit;
}
```
Медиа запрос (~ убирает ковычки в css)
```less
@breakpoint-media: ~"(max-width: 575px)";
```

## Oбявляем дополнительный .less
```less
  @import "vars";
```

## functions

### `darken()`  
Делает цвет темнее (1 - цвет, 2 - значение)
  
```less
  div {
    background-color: darken(@colormain, 10%);
  }
```

### `lighten()`
Делает цвет светлее (1 - цвет, 2 - значение)

```less
  div {
    background-color: lighten(@colormain, 10%);
  }
```
### `when()`
Если цвет текста слишком светлый знасит цвет текста будет черный (у данном случее место белого)

```less
  .btn(@bg) {
  background-color: @bg;

   & when(lightness(@bg) > 50) {
     color: black;
   }
    &:hover,
    &:focus {
      background-color: lighten(@bg, 10%);
    }
}
```

## Так тож можно =>
```less
  & + & {
    margin: 10px;
  }
```

## Mixins
```less
.btn(@bg) {
  background-color: @bg;
    &:hover,
    &:focus {
      background-color: lighten(@bg, 10%);
    }
}
```

## Media
Пишем внутри:
```less
.title {
  font-size: @fs;
  color: @colmain;

  media (max-width: 575px) {
    font-weight: 10px;
  }
}
// или
.title {
  font-size: @fs;
  color: @colmain;

  media @breakpoint-mobile {
    font-weight: 10px;
  }
}
```

## EASY Less (_extantion VS Code_)

### Create a `settings.json` in `.vscode`
```json
{
  "less.compile": {
    "compress": true
  }

}
```
