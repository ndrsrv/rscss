# Другие источники

 * [ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss#49) ("CSS Перевёрнутый Треугольник") хорошее дополнение к любой rscss структуре.
 * [rsjs](http://ricostacruz.com/rsjs/) ("Понятный стандарт для структуры JavaScript") упорядочивание JavaScript для простых сайтов.

Другие решения
---------------

### БЭМ
[БЭМ] хорош, но иногда может раздражать необычным синтаксисом. RSCSS довольно много взял из БЭМ, только с другим синтаксисом.

```html
<!-- БЭМ -->
<form class='site-search site-search--full'>
  <input  class='site-search__field' type='text'>
  <button class='site-search__button'></button>
</form>
```

```html
<!-- rscss -->
<form class='site-search -full'>
  <input  class='field' type='text'>
  <button class='button'></button>
</form>
```

## Терминология

Некоторые концепты обладают похожей идеологией структурирования CSS.

| RSCSS     | БЭМ         | SMACSS        |
| ---       | ---         | ---           |
| Компонент | Блок        | Module        |
| Элемент   | Элемент     | Sub-Component |
| Слой      | ?           | Layout        |
| Вариант   | Модификатор | Sub-Module & State |

[БЭМ]: http://bem.info/
[Smacss]: https://smacss.com/
