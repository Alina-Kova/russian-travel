# Путешествия по России
------------------------------------------------------------
## Проект создан для закрепления навыков адаптивной верстки HTML и CSS c использованием медиазапросов с применением таких свойств как Grid Layout и Flex.
 
 В основе проекта содержится структурированный и семантически корректный код с использованием семантических тэгов **header, main, section, footer, nav**. 
 Код написан по правилам **методологии БЭМ**. Файлы и пути к файлам в проекте также организованы по **БЭМ Nested**.
 
Данный проект был содержит секции с элементами *анимации* при наведении мыши. 
Для всех ссылок используется анимация - при наведении мыши такст ссылок становится полупрозрачным. Для этого было использовано свойство **transition**, a также свойство **opacity** c псевдоклассом **:hover**: 

    ```css
    .header__lang-link {
      font-size: 18px;
      line-height: 20px;
      text-decoration: none;
      color: #ffffff;
      margin: 0;
      transition: opacity .5s ease-in forwards;
    }

    .header__lang-link:hover {
      opacity: 0.8;
    }
    ``` 

Код написан под различные разрешения экрана от менее 320 px до более 1280px с помощью медиазапросов. Просмотр станицы возможен как на мобильных экранах, так и на широкоформатном дисплее. 

При построении секций были применены **grid layout** и **flex**:

```css
.photo-grid {
  display: grid;
  max-width: 288px;
  grid-template-columns: 1, 1fr;
  grid-template-rows: repeat(12, 216px);
  flex-wrap: wrap;
  row-gap: 12px;
  margin: 0 auto 64px;
}
``` 

В блоке *cover* был применён overlay под текстом с помощью псевдокласса **:before** с ещё большим затеменением при наведении курсора мыши при помощи псевдокласса **:hover** :


```css
.cover::before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: #2A2C2F;
    opacity: 0.3;
}

.cover:hover::before {
    background: #2A2C2F;
    opacity: 0.8;
}
``` 

С проектом можно ознакомиться на GitHub Pages по ссылке: https://alina-kova.github.io/russian-travel/index.html
