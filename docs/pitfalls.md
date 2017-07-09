# Ловушки

## Проблемы вложенных компонентов
Будьте осторожны со вложенными Компонентами, чьи Элементы имеют такие же названия, как Элементы в их общем контейнере.

```html
<article class='article-link'>
 <div class='vote-box'>
    <button class='up'></button>
    <button class='down'></button>
    <span class='count'>4</span>
  </div>

  <h3 class='title'>Article title</h3>
  <p class='count'>3 votes</p>
</article>
```

```scss
.article-link {
  > .title { /* ... */ }
  > .count { /* ... (!!!) */ }
}

.vote-box {
  > .up { /* ... */ }
  > .down { /* ... */ }
  > .count { /* ... */ }
}
```

В этом примере, если `.article-link > .count` не имело бы `>` селектора по потомку, это бы применилось к `.vote-box .count` Элементу. Это одна из причин, почему селекторы потомков предпочтительнее.
