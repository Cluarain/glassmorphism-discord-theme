# Glassmorphism

## Предисловие  

Тема Glassmorphism, создана исключительно от нечего делать и будет (не будет) поддерживаться автором по мере возможностей.
В процессе написания пришла идея разделить тему на 2 вида: Glassmorphism Static и Glassmorphism Animated соответственно.  

### Glassmorphism Static  

Тема со статичным задним фоном. Можно установить любое изображение, gif, svg, видео и т.п. Нужно всего лишь... открыть файлик с темой и заменить `--bg-image: url(ссылка);`
Есть возможность использовать [фильтры css](https://cssgenerator.org/filter-css-generator.html) через переменную `--bg-filter: saturate(150%);`

### Glassmorphism Animated  

Тема с динамически меняющимся задним фоном. Можно установить любое изображение, gif, svg, видео и т.п. и любое их количество. 
Чтобы заменить текущие нужно всего лишь... открыть файлик с темой и заменить ссылку в `--bg-image-X: url(ссылка);`. 
Чтобы добавить новые изображения в карусель, нужно добавить новую переменную `--bg-image-X: url(ссылка);` в блок `:root {...}`
и переписать блок `@keyframes changeBg {...}`.

Если изображений будет 5, то соответственно 100% / 5 = 20% времени для каждого изображения

```css
  0%,
  19.99% {
    background: var(--bg-image-1);
  }
  20%,
  39.99% {
    background: var(--bg-image-2);
  }
  /* и т.д  */

```

Есть возможность использовать [фильтры css](https://cssgenerator.org/filter-css-generator.html), но тогда в каждом кадре надо будет выставлять свои фильтры или обнулять предыдущие через переменную `--bg-filter: none;`.  
