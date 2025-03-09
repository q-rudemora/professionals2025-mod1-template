# Профессионалы веб разрабокта модуль А (Описание недоделано!)

В первые 1:30 полностью разрабатывался собственный css-framework и реализовывалась html разметка главной страницы

css-framework разрабатывался в том же файле, что и остальные стили

```css
/* /assets/app.css */
/* Заготовки для стилей */
/* ФЛЕКСЫ */
.flex {
  display: flex;
}
.aic {
  align-items: center;
}
.aifs {
  align-items: flex-start;
}
.jcc {
  justify-content: center;
}
.jcfe {
  justify-content: flex-end;
}
.jcsb {
  justify-content: space-between;
}
.jic {
  justify-items: center;
}
.col {
  flex-direction: column;
}
.dotted {
  text-decoration: underline;
}
/* ГРИДЫ */
.grid {
  display: grid;
}
.gtc-3 {
  grid-template-columns: repeat(3, 1fr);
  @media (max-width: 960px) {
    grid-template-columns: repeat(2, 1fr);
  }
  @media (max-width: 768px) {
    grid-template-columns: repeat(1, 1fr);
  }
}
.gtc-2 {
  grid-template-columns: repeat(2, 1fr);
  @media (max-width: 768px) {
    grid-template-columns: repeat(1, 1fr);
  }
}

.container {
  padding: 0 var(--padding-cont);
}
.block,
.form-block {
  padding: var(--padding-block);
}
.block img,
.block .content,
.form-block img,
.form-block .content {
  width: 40%;
}

.tac {
  text-align: center;
}

/* Маленькие плашки которые определяют категории или статус питомцев */
.tag {
  padding: 0.6rem 1.7rem;
  background-color: #893476;
  color: #f4f4f4;
  border-radius: 999rem;
  font-weight: bold;
  text-transform: uppercase;
}

/* Стилизация точек для слайдена в блоке main.hero */
.dot {
  --size: 1rem;
  height: var(--size);
  width: var(--size);
  background-color: #ddd;
  border-radius: 100%;
  &.active {
    background-color: #777;
  }
}

/* Стили для кнопок */
.button {
  padding: 0.7rem 2rem;
  background-color: rgb(66, 152, 116);
  border: 1px solid #429874;
  color: #f4f4f4;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s;
}
.button.small {
  padding: 0.3rem;
}
.button.red {
  background-color: #d55252dd;
  border-color: #b90808;
}
.button:hover {
  background-color: inherit;
  color: #429874;
}

/* Поля для ввода */
.c-input {
  border-radius: 1rem;
  padding: 0.6rem 1rem;
  border: 2px solid #0003;
  background-color: #fff3;
}

/* Отступы */
.g-1 {
  gap: 1.25rem;
}
.g-2 {
  gap: 2rem;
}
.g-3 {
  gap: 3rem;
}

.info-user {
  padding: 2rem;
  border: 1px solid #0003;
}
.card {
  background-color: #f4f4f4;
  width: 100%;
  padding: 2rem;
  border: 1px solid #0003;
  border-radius: 1rem;
  box-shadow: 0 0 5px #0000;
  transition: all 0.3s;
}
.card h2 {
  font-size: 2rem;
}
.card:hover {
  box-shadow: 0 0 5px #0005;
}
.card p.grey {
  color: #999;
}

/* Бэкграунд для архива */
.arch {
  background-color: #eee;
}
```

### Шапка (header)

html код -

```html
<header class="header flex jcsb aic container" id="header">
  <a href="./index.html" class="logo"
    ><img src="./assets/iamges/logo.png" alt="Новая жизнь"
  /></a>
  <nav class="navigation flex g-2">
    <li><a href="./search.html">Поиск</a></li>
    <li><a href="./register.html">Регистрация</a></li>
    <li><a href="./login.html">Личный кабинет</a></li>
    <li><a href="#">Добавить в избранное</a></li>
    <li><a href="./index.html#reviews">Отзывы</a></li>
  </nav>
  <a class="burger"><img src="./assets/iamges/burger.png" alt="" /></a>
</header>
```

css -

```css
/* Шапка сайта */
.header {
  height: 80px;
}
```

### Подвал (footer)

Далее разрабатывался подвал сайта

html -

```html
<footer class="footer flex jcsb block">
  <a href="./index.html#header" class="logo"
    ><img src="./assets/iamges/logo-light.png" alt="Новая жизнь"
  /></a>

  <div class="flex col g-2">
    <p><strong>Номер телефона:</strong> 8 (800)123-45-67</p>
    <p><strong>e-mail:</strong> mail@newlife.ru</p>
  </div>

  <nav class="flex col g-2">
    <li><a href="./index.html#header">Главная</a></li>
    <li><a href="./register.html">Регистрация</a></li>
    <li><a href="./login.html">Авторизация</a></li>
    <li><a href="./profile.html">Личный кабинет</a></li>
  </nav>
</footer>
```
css - 
```css
/* Подвал сайта */
.footer {
    background-color: #444;
}
.footer * {
    color: #f4f4f4;
}
.footer img {
    width: 100% !important;
}
```
