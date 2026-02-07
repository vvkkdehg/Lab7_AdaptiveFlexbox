# Лабораторная работа №7

## Введение

Данная лабораторная работа посвящена освоению современных технологий CSS-разметки, в частности, модуля Flexbox. Адаптивная верстка — это подход к созданию веб-страниц, при котором дизайн и контент автоматически подстраиваются под размер экрана устройства. Flexbox представляет собой одномерную систему компоновки для размещения элементов в строку или столбец, что значительно упрощает создание гибких и адаптивных макетов.

## Описание проекта

В ходе выполнения лабораторной работы был создан проект, демонстрирующий практическое применение Flexbox для построения адаптивной веб-страницы "Магазин одежды". Проект включает основные компоненты современного веб-дизайна: заголовок с градиентным фоном, карточки товаров с кнопками действий, навигационное меню с индикацией активного состояния, информационный блок и футер с социальными ссылками. Все элементы реализованы исключительно с использованием свойств Flexbox, изученных в лабораторной работе.

## Создание рабочей директории

Создаем структуру проекта:

```bash
mkdir Lab7_Adaptive_FIO
cd Lab7_Adaptive_FIO
touch index.html styles.css README.md
mkdir img
```

## Создание базовой структуры HTML

```html
<!DOCTYPE html>
<html lang="ru-RU">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Адаптивная верстка: Flexbox и Grid</title>
    <link rel="stylesheet" href="styles.css" />
</head>
<body>
    <h1>Лабораторная работа №7</h1>
    <p>Изучаем Flexbox и Grid</p>
</body>
</html>
```

## Практика с Flexbox

#### Горизонтальное навигационное меню
HTML:
```html
<nav class="navbar">
    <a href="#">Главная</a>
    <a href="#">О нас</a>
    <a href="#">Услуги</a>
    <a href="#">Контакты</a>
</nav>
```
CSS:
```css
.navbar {
    display: flex;
    justify-content: space-around;
    background-color: #333;
    padding: 15px;
}
```

### Карточки товаров
HTML:
```html
<div class="cards">
    <div class="card">
        <h3>Товар 1</h3>
        <p>Описание товара</p>
        <button>Купить</button>
    </div>
</div>
```
CSS:
```css
.cards {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
}

.card {
    flex: 1 1 250px;
    display: flex;
    flex-direction: column;
}
```

### Центрирование элемента
HTML:
```html
<div class="center-container">
    <div class="centered-content">
        Я в центре!
    </div>
</div>
```
CSS:
```css
.flex-container {
    display: flex;
    gap: 10px;
}

.item {
    background-color: lightblue;
    padding: 20px;
    text-align: center;
}
```