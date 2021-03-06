# HTML

# 1. Анатомија на HTML елементи

> 💡 Термини што треба да ги знаеме: 
>  HTML element, HTML tag, opening tag, content, closing tag, self-closing tags

Секој HTML елемент се состои (најчесто) од два тагови меѓу кои се наоѓа текст или некаква друга содржина, како слика или видео.

```
<p>Hello World!</p>
```

## 1.1. HTML tag

Секој HTML tag има свое име коешто се наоѓа помеѓу две загради <>. На пример, во погорниот исечок можеме да го видиме тоа со HTML tag p што значи paragraph (параграф).
Името на тагот е p, и е заградено во <>, со тоа што на крајот добиваме:

```
<p>
```

## 1.2. HTML element структура

Секој HTML element се состои од:

- **Отварачки таг** (opening tag), со којшто започнуваме HTML element:
```
<p>
```
- **Содржина** (content), што се наоѓа помеѓу отварачкиот и затварачкиот таг:
  
```
<p>Hello World!
```
- **Затварачки таг** (closing tag), со кој што затвараме или завршуваме еден HTML element:

```
<p>Hello World!</p>
```

## 1.3. Само-затварачки тагови (self-closing)

Исто така постојат тагови што се затваарат сами. Тоа значи дека користиме само еден таг и тоа е opening tag (отварачки таг).

Тие HTML tags се викаат **self-closing tags** (само-затварачки тагови). Исто така можеме да ги наречеме **empty elements**.

### 1.3. листа на self-closing tags или empty elements

```
<br>

<embed>

<hr>

<img>

<input>

<link>

<meta>
```

# 2. Body елементот

> 💡 Термини што треба да ги знаеме: 
>  body елемент

Најосновен HTML tag e body тагот, затоа што тој се користи за да ги прикажеме сите други HTML елементи на една веб страна. Без body таг, не можеме да ги прикажеме елементите.

```
<body>

  <!-- СОДРЖИНА -->

</body>
```

> ⚠️ Ако заборавиме да напишиме body tag во HTML документот, пребарувачот сам ќе додаде body tag, но ние сепак треба секогаш да го додаваме.

# 3. Структура на HTML (parent — child hierarchy)

> 💡 Термини што треба да ги знаеме: 
>  parent-child relationship, nesting

Елементите во HTML се структурирани како во едно семејно дрво. Тоа значи дека во некои тагови можеме да внесуваме други тагови и тоа до бесконечност.

Хиерархирската врска помеѓу елементите е **родител (parent)** — **дете (child)**.

На пример, сите елементи што ќе ги додадеме во body тагот се деца или children на body тагот.

```
<!-- BODY е РОДИТЕЛ (PARENT) -->

<body>

	<!-- p, img, div се ВГНЕЗДЕНИ (NESTED) и се ДЕЦА (CHILDREN) -->

	<p>Hello World!</p>

	<img src="#" alt="Empty image"/>
	
	<!-- div е РОДИТЕЛ (PARENT) на p -->
	
	<div>

		<!-- ДЕТЕ на div и ВГНЕЗДЕН (NESTED) во div -->

		<p>Hello World!</p>

	</div>

</body>
```
> 💡 Исто така можеме да речеме дека сите елементи што се children на parent елементот се **вгнездени** или **nested**.
> Хиерархијата помеѓу елементите е битна затоа што некои одлики што ќе важат и ќе ги додадеме на parent елементот, ќе важат и за children елементите. 

# 4. Block vs. inline елементи

> 💡 Термини што треба да ги знаеме: 
>  block елемент, inline елемент

Постојат две категории на елементи во HTML: block и inline елементи.

## 4.1. Block елементи

Block елементите формираат **визибилен блок на страната** (тоа е заради основниот стил што го има секој пребарувач).

Block-level елементите секогаш се појавуваат на нова линија. И која било содржина што следи после block елемент е во нова линија.

Block елементите најчесто ја сочинуваат и прават структурата на една веб страна.

Пример за блок елементи се _p_, _ul_, _ol_, _nav_, _footer_, _div_.

```
<!-- ПРАВИЛНО -->

<body>

	<div>
	
		<p><em>Hello World!</em></p>
		
	</div>

</body>

<!-- НЕПРАВИЛНО -->

<body>

	<div>
	
		<em><p>Hello World!</p></em>
		
	</div>

</body>
```
## 4.1.1. Листа на block-level елементи

```
<address>

<article>

<aside>

<blockquote>

<canvas>

<dd>

<div>

<dl>

<dt>

<fieldset>

<figcaption>

<figure>

<footer>

<form>

<h1> - <h6>

<header>

<hr>

<li>

<main>

<nav>

<noscript>

<ol>

<p>

<pre>

<section>

<table>

<tfoot>

<ul>

<video>
```

## 4.2. Inline елементи

Inline елементите најчесто се наоѓаат во block елементи.

Тие не се појавуваат на нова линија како block елементите, ама се секогаш во линијата или блокот на некој од block елементите.

Пример за inline елементи се: _em_ (emphasis или _italics_) или **strong** (strong или **bold**).

Во примеров подолу, елементите ќе бидат во ист ред или иста линија без никаков простор помеѓу двата.

```
<!-- ПРИКАЖАНИ ВО ИСТ РЕД -->

<body>

<em>emphasis</em><strong>bold</strong>

</body>
```

Во овој пример подолу, секој од елементите ќе биде во нов ред, иако ги имаме напишано во HTML датотеката во еден ред:

```
<!-- ПРИКАЖАНИ ВО ДВА ПОСЕБНИ РЕДОВИ -->

<body>

	<p>emphasis</p><p>bold</p>

</body>
```

## 4.2.1. Листа на inline елементи

```
<a>

<abbr>

<acronym>

<b>

<bdo>

<big>

<br>

<button>

<cite>

<code>

<dfn>

<em>

<i>

<img>

<input>

<kbd>

<label>

<map>

<object>

<output>

<q>

<samp>

<script>

<select>

<small>

<span>

<strong>

<sub>

<sup>

<textarea>

<time>

<tt>

<var>
```

# 5. HTML attributes

> 💡 Термини што треба да ги знаеме: 
>  attribute

Атрибутите или attributes содржат дополнителни информации за HTML елементот што не се видливи во содржината. Тоа може да биде класа (class) на елементот што функционира како име за елементот и многу други различни информации.

Најчесто **шаблонот** за атрибути е следниов:

**име=”вредност”** односнo **name=”value”**

Конкретен пример:

```
<h1 class="title-of-article"></h1>
```

Можеме да заклучиме дека:
- Треба да оставиме простор помеѓу атрибутот и името на елементот. Ако имаме повеќе атрибути, треба да има простор помеѓу секој атрибут.
- После името на атрибутот има знак еднакво.
- После знакот еднакво ја внесуваме вредноста во наводници.

Друг пример на атрибут може да биде **href** во **a (anchor тагот)**, со којшто ја наведуваме адресата на веб страната.

```
<a href="/about.html">
```

## 5.2. Boolean attributes

Постојат attributes што не содржат вредност. Тоа е затоа што вредноста е иста како и името на атрибутот.

Пример за boolean attribute е **disabled** што се користи во **input** елементот. Овој attribute се користи за да му забраниме на корисникот да внесува било што во празното поле.

```
<form>

	<input type="text" disabled>

</form>

```

### 5.2.1. Листа на boolean attributes

```
allowfullscreen

allowpaymentrequest

async

autofocus

autoplay

checked

controls

default

defer

disabled

formnovalidate

hidden

ismap

itemscope

loop

multiple

muted

nomodule

novalidate

open

playsinline

readonly

required

reversed

selected

truespeed
```

# 6. Наводници во HTML

Најдобро е секогаш кога пишуваме attributes да користиме наводници. Ако не пишуваме наводници можеме да добиеме различни грешки што можеме многу лесно да ги избегнеме со следењето на едно лесно правило: **секогаш користи наводници**.

Се разбира, можеме да избереме слободно помеѓу двата типа на наводници:

- Single quotes (’’)
- Double quotes (””)

```
<!--- Може да функционира, но не го користиме -->

<a href=/about.html/>

<!--- ПРАВИЛНО -->

<a href="/about.html" />

<!--- ПРАВИЛНО -->

<a href='/about.html' />
```

> ❗Но, не смееме да мешаме single со double quotes и обратно.

```
<!--- ГРЕШНО -->

<a href="/about.html' />

<!--- ГРЕШНО -->

<a href='/about.html" />
```

# 7. Коментари во HTML

Користеме коментари за да го објасниме нашиот код и размислувањето зад истиот.

Најчесто се користи за некој друг да може да разбере што сакаме да постигнеме или ако се вратиме на кодот многу подоцна да знаеме што сме сакале да постигнеме.

Коментарите не може да ги виде крајниот корисник и пребарувачот едноставно ги игнорира.

```
<!-- ПРИМЕР ЗА КОМЕНТАР -->
```

# 8. HTML Шаблон (Boilerplate)

## 8.1. index.html

За секоја веб апликација мораме да имаме index.html датотека, затоа што таа е првата датотека што ја бара секој веб сервер.

> 💡 Сите HTML документи завршуваат со .html

## 8.2. DOCTYPE

Секој HTML документ мора да започне со тагот !DOCTYPE html, затоа што тоа е начинот на кој што му кажуваме на пребарувачот (Google Chrome, Safari, Firefox) дека станува збор за HTML документ и која верзија на HTML е документот.

Моменталната верзија на HTML e **HTML5** и тоа можеме да му го кажеме на пребарувачот со следново:

```
<!DOCTYPE html>
```

Во претходната верзија на HTML (HTML4), тоа беше многу покомплицирано и подолго:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
```

## 8.3. HTML елемент

Откако ќе му кажеме на пребарувачот дека станува збор за HTML документ и која верзија на HTML ја користеме, треба да го напишеме html елементот, којшто е основниот или root елемент во секој HTML елемент и сите други елементи се негови children.

<!DOCTYPE html>
<html lang="en">


</html>

### 8.3.1. HTML lang

Во HTML елементот html секогаш треба да го напишеме (односно наведеме) јазикот којшто го користеме во HTML датотеката.

Тоа можеме да го направиме со атрибутот lang (attribute lang).

Многу е битно точно да го наведеме јазикот којшто го користеме во документот затоа што тоа им помага на сите направи кои им помагаат на лица со потешкотии да се адаптираат на точниот јазик и да ги читаат зборовите правилно.

```
<!DOCTYPE html>
<html lang="en">


</html>
```

## 8.4. Head елемент

Во **head** елементот ги ставаме сите **meta информации (metadata)** за нашата веб страна и други датотеки коишто ни требаат за да ги покажеме сите елементи правилно во пребарувачот.

Тие информации можат да бидат

- Kлучни зборови, опис за SEO
- Слика за различни социјални мрежи за SEO.
- CSS документи
- Character set (charset)
- Favicon
- Наслов на HTML документот

Во **head** елементот **не смееме** да ставаме елементи што треба да покажат некаква содржина на страната (тоа значи дека сите елементи што ги пишуваме во body елементот не смееме да ги пишуваме во head елементот).

```
<!DOCTYPE html>

<html lang="en">

	<head>

	</head>

</html>
```

### 8.4.1. Наслов на датотеката

Со HTML елементот title можеме да зададеме наслов на HTML датотеката.

>💡Се разбира, title елементот можеме да го искористиме само во head елементот како вгнезден внатре.

```
<!DOCTYPE html>

<html lang="en">

	<head>
	
		<title>Наслов</title>

	</head>

</html>
```

Ако пробаме да зачуваме една веб страна како Bookmark, насловот што го зададовме во head елементот ќе можеме да го видиме таму.

Исто така насловот од title елементот излегува во резултатите од пребарување на Google, на пример.

### 8.4.2. Мета информации

Мета информации или податоци се информации што ги опишуваат информациите. Во овој пример, мета информациите можат да го опишуваат авторот на HTML датотеката.

```
<!DOCTYPE html>

<html lang="en">

	<head>
	
		<title>Наслов</title>

		<meta></meta>

	</head>

</html>
```

### 8.4.3. Meta character set

Со атрибутот **charset** во HTML елементот <meta> можеме да го наместиме начинот на encoding. Ако го искористиме начинот на encoding **utf-8** корисникот ќе може да ги виде скоро сите знаци и симболи што ги користиме луѓето.

Иако некои пребарувачи како Google Chrome автоматски ги поправаат знаците што други пребарувачи не би ги препознале, најдобро е секогаш да напишеме **utf-8** како вредност во **charset**.

```
<!DOCTYPE html>

<html lang="en">

	<head>
	
		<title>Наслов</title>

		<meta charset="utf-8"></meta>

	</head>

</html>
```

> ❗Ако не напишеме utf-8, тогаш симболите и знаците ќе излезат како квадратчиња.

### 8.4.4. Meta и SEO

За подобра SEO оптимизација, односно за да може пребарувачот полесно да ја најде нашата страна кога некој пребарува клучни зборови, треба да ги внесеме тие клучни информации (наслов, клучни зборови, опис итн.) во секоја HTML датотека.

Атрибутите со **name** одат заедно во комбинација со **content** каде што ја внесуваме содржината за претходнонаведената вредност.

### 8.4.5. Автор 

За да го напишеме авторот на една HTML датотека го користеме meta елементот.

Битно е да се напомени дека името на авторот ќе биде видливо кога пребаруваме на Google.

```
<!DOCTYPE html>

<html lang="en">

	<head>
	
		<title>Наслов</title>

		<meta charset="utf-8"></meta>
		<meta name="author" content="Andrijan Tasevski"></meta>

	</head>

</html>
```

Исто така е корисно во CMS (Content Management Systems) за да знаеме кој е авторот на страната и кој ја пишувал содржината.

Исто така е добро да знаеме кој ја напишал HTML датотеката за да можеме да го исконтактираме.

### 8.4.6. Опис

За да напишеме опис за некојa HTML датотека, го користиме meta елементот.

Описот е многу битен затоа што тоа излегува под насловот на страната во пребарувањето на Google.

Исто така помага нашата страна да излезе повисоко во резултатите.

```
<!DOCTYPE html>

<html lang="en">

	<head>
	
		<title>Наслов</title>

		<meta charset="utf-8"></meta>
		<meta name="author" content="Andrijan Tasevski"></meta>
		<meta name="description" content="Weather application"></meta>
	</head>

</html>
```

### 8.4.7. Клучни зборови

Клучните зборови се многу битни за SEO затоа што со нив му кажуваме на пребарувачот за содржината што ја имаме во HTML датотеката.

Секогаш мораме да внесуваме клучни зборови затоа што тоа му помага на пребарувачото побрзо да ја каталогира нашата страна.

```
<!DOCTYPE html>

<html lang="en">

	<head>
	
		<title>Наслов</title>

		<meta charset="utf-8"></meta>
		<meta name="author" content="Andrijan Tasevski"></meta>
		<meta name="description" content="Weather application"></meta>
    <meta name=”keywords” content=”weather, vreme, meteo, prognoza”></meta>

	</head>

</html>
```

### 8.4.8. Други типови на мета информации (Facebook, Twitter)

**Facebook** има развиено свој metadata protocоl за да може полесно да дадеме мета информации за веб страни.

[Open Graph Protocol](https://ogp.me/)

```
<meta name=”og:title” content=”Наслов”> — Наслов на страната
<meta name=”og:type” content=”video.movie”> — Тип на содржина
<meta name=”og:image” content=”линк-до-сликата”> — Слика
<meta name=”og:url” content=”линк-до-страната”> — Линк за страната
```

**Twitter** исто така има развиено свој систем за metadata што се вика [Twitter cards](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/summary).

```
<meta name=”twitter:card” content=”summary” />
<meta name=”twitter:site” content=”@flickr” />
<meta name=”twitter:title” content=”Small Island Developing States” />
<meta name=”twitter:description” content=”View the album on Flickr.” />
<meta name=”twitter:image” content=”линк-до-сликата” />
```

### 8.4.9. Viewport

Viewport е местото од екранот каде што можеме да гледаме веб содржина.

Viewport најчесто нема иста големина како страната што ја гледаме на нашата направа. Тоа е затоа што помалите направи (мобилни телефони, таблети) генерираат веб страни во viewport или виртуелно прозорче што се поголеми од големината на екранот. Потоа ја земаат генерираната веб страна и ја намалуваат се додека не е усогласена со големината на екранот.

На пример, ако страната е генерирана во viewport со 980px, а нашата големина на екранот е 640px, таа ќе биде намалена на 640px за да може да ја собере на нашиот екран и да можеме да ја видиме (со zoom).

Ова најчесто се случува со страни кои што не се направени за помали направи.

Но, за да не треба да правиме zoom in на страните на помали направи, можеме да го искористиме атрибутот **viewport** во meta елементот.

Ако го напишеме следново:

```
<meta name=”viewport” content=”width=device-width”></meta>
```
тогаш нашата веб страна ќе биде исто толку широка колку што е широка нашата направа во CSS pixels (100% width).

Ако го додадеме следново:

```
<meta name=”viewport” content=”width=device-width, initial-scale=1”></meta>
```
тогаш кога страната ќе биде отворена и генерирана за корисникот, нивото на zoom ќе биде 100%.

```
<!DOCTYPE html>
<html>
	<head>

		<title>Наслов</title>

		<meta charset="utf-8"></meta>
		<meta name="author" content="Andrijan Tasevski"></meta>
		<meta name="description" content="Weather application"></meta>
		<meta name="viewport" content="width=device-width, initial-scale=1"></meta>"
	
	</head>
</html>
```

Вредностите за initial-scale можат да бидат различни (други вредности се можни, ова се само примери):
- 0.1 = 10% zoom
- 0.5 = 50% zoom
- 1.0 = 100% zoom
- 5.0 = 500% zoom

Кога користиме која било направа, на направата скроламе вертикално, и не хоризонтално, затоа треба да ги следиме следниве неколку правила:

1. Не користи **фиксирана ширина на елементи (fixed width for elements)**. На пример, ако ставиме еден div да има големина од 1500px, нема да може да се намали на помала направа и ќе треба да скроламе хоризонтално се да ја видиме содржината.

2. Содржината треба да биде прилагодена на различни viewports. Тоа е затоа што секоја направа има различен viewport.

3. Користи **CSS media queries** за да обликуваш веб страни за различни големини на екрани.

### 8.4.10. Додавање на favicon

За да го збогатиме дизајнот на нашата веб страна, можеме да додадеме икони (односно favicon што значи favorites icon) во мета информациите што ќе бидат видливи во одредени случаи.

Favicon е видлив во **browser tabs**, кога ќе направиме **bookmark** или кога ќе додадеме нашата страна во **favorites**.

Favicon можеме да додадеме во различни формати: .ico, .png или .gif

Најдобро е да биде форматот **.ico** затоа што е поддржан од најстарите пребарувачи, но сепак можеме да користеме и .png и .gif.
За да додадеме favicon, го пишуваме следново:

```
<!DOCTYPE html>
<html>
	<head>

		<title>Наслов</title>

		<meta charset="utf-8"></meta>
		<meta name="author" content="Andrijan Tasevski"></meta>
		<meta name="description" content="Weather application"></meta>
		<meta name="viewport" content="width=device-width, initial-scale=1"></meta>"
		<link rel="icon" type="image/x-icon" href="#" />	

	</head>
</html>
```

### 8.4.12. Додавање на CSS и JavaScript датотеки

CSS треба да биде секогаш во head елементот за да биде правилно обликуван HTML кодот што е напишан во body елементот.

Тоа можеме да го направиме со следниов код:

```
<link rel=”stylesheet” href=”my-css-file.css” />
```

Со rel=”stylesheet” му кажуваме на пребарувачот дека станува збор за документ што ќе го обликува HTML кодот и содржи код за стил/дизајн.

Со href=”#” ја посочуваме локацијата каде што се наоѓа датотеката.

```
<!DOCTYPE html>
<html>
	<head>

		<title>Наслов</title>

		<meta charset="utf-8"></meta>
		<meta name="author" content="Andrijan Tasevski"></meta>
		<meta name="description" content="Weather application"></meta>
		<meta name="generator" content="React and Next.js"></meta>
		<meta name="viewport" content="width=device-width, initial-scale=1"></meta>"
		<link rel="icon" type="image/x-icon" href="#" />
		<link rel="stylesheet" href="#" />

	</head>
</html>
```

Ако сакаме да додадеме **JavaScript** датотека во head елементот тогаш се користи следниов код:

```
<script src=”my-js-file.js” defer></script>
```

Во претходната линија на код, src е изворот или source каде што се наоѓа датотеката.

**Defer** па му кажува на пребарувачот дека треба да ја отвори и прочита JavaScript датотеката кога целосно ќе го прочита HTML кодот.

```
<!DOCTYPE html>
<html>
	<head>

		<title>Наслов</title>

		<meta charset="utf-8"></meta>
		<meta name="author" content="Andrijan Tasevski"></meta>
		<meta name="description" content="Weather application"></meta>
		<meta name="generator" content="React and Next.js"></meta>
		<meta name="viewport" content="width=device-width, initial-scale=1"></meta>"
		<link rel="icon" type="image/x-icon" href="#" />
		<link rel="stylesheet" href="#" />
		<script src="#" defer></script>

	</head>
</html>
```

# 9. Работа со текст во HTML

## 9.1. Наслови

Постојат 6 елементи со коишто можеме да направиме наслов во HTML:

```
<!-- НАСЛОВИТЕ ЌЕ БИДАТ ВО РАЗЛИЧНА ГОЛЕМИНА КОГА ЌЕ ГИ НАПИШЕМЕ ВО .html ДАТОТЕКА -- >

<h1>Наслов 1</h1>
<h2>Наслов 2</h2>
<h3>Наслов 3</h3>
<h4>Наслов 4</h4>
<h5>Наслов 5</h5>
<h6>Наслов 6</h6>
```

Големината на секој од HTML насловите е претходно дефинирана во default стиловите на секој пребарувач (Chrome, Firefox, Safari).

### 9.1.1 Хиерархија со HTML наслови

Иако можеме да ги наместиме насловите како што сакаме, хиерархијата на насловите во документот треба да има смисла. Ако започнеме со h2, на пример, тогаш нема да го искористиме h1.

Пример, како би требало да изгледа хиерархијата со наслови:

```
<h1>Главен наслов на страната</h1>

<p>Некој текст</p>

<h2>Поднаслов</h2>

<p>Некој текст</p>

<h2>Нов поднаслов</h2>

<p>Повторно текст</p>
```

**Неколку правила за HTML хиерахија**

- Најдобро е да имаме еден h1 елемент во целата датотека и сите други наслови да бидат под него.
- Ги користиме насловите во правилен редослед (h1 - h2 - h3 - h4 - h5 - h6). Под h3 елемент не смееме да имаме h1.
- Идеално не треба да користиме повеќе од три различни наслови во една датотека. На пример, би искористиле наслови само од h1 до h3.

## 9.2. Параграф

Елементот p што значи параграф (paragraph), се користи за да пишуваме текст со нормална големина. Исто и тој има веќе дефинирана големина во стиловите на пребарувачот.

```
<p>Параграф</p>
```

## 9.3. Span

За разлика од насловите h1 или параграфите p, елементот span не е семантички обележан.

Ако сакаме да напишеме некој текст без да има некакви семантички одлики, го користиме span елементот.

```
<span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</span>
```

span најчесто се користи кога сакаме да вгнездиме некој текст во наслов или параграф и да му дадеме различен стилски одлики со CSS.

Тоа е можно затоа што span е **inline element**, а h1 - h6 и p се **block elements**.

```
<!-- Го вгнездуваме <span> во <h1> -->

<h1>Купете го новиот <span>компјутер</span> од нашата линија.</h1>

<!-- Додаваме стил со CSS: зборот компјутер ќе биде обоен во црвено -->

<style>

  h1 span {
  color: red;
  }

</style>
```

## 9.4. Break

Елементот **br** или break се користи за да почнеме да пишуваме текст во нова линија.

Тој се состои само од **еден** таг (само br и без /br).

```
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. <br> Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
```

>💡br се користи како вгнезден елемент во друг елемент. 

>❗br *не се користи* за правење простор помеѓу два елементи (за тоа постои margin во CSS).

## 9.5. Horizontal rule

Елементот hr се користи за правење пауза помеѓу тематски елементи и содржини.

Најчесто стои помеѓу два <p> елементи.

```
<p>Еден параграф</p>

<hr>

<p>Втор параграф</p>
```

## 9.6. Emphasis (Italics)

За нешто да _нагласиме_ најчесто користиме italics.

Тоа можеме да го направиме во HTML со _em_ (кратко за emphasis) или со _i_ (italics).

Пример со em:

```
<p>Lorem ipsum <em>dolor sit amet</em>, consectetur adipiscing elit</p>
```

Пример со i:

```
<p>Lorem ipsum <i>dolor sit amet</i>, consectetur adipiscing elit</p>
```

>💡em или i се користат како вгнездени елементи во параграф или наслов.

Најдобро е да користиме em затоа што софтверот различно го чита тој елемент за лицата со оштетен вид. Исто така има други семантички предности.

## 9.7. Strong (Bold)

За да кажеме дека нешто е битно користиме **bold**.

Тоа можеме да го направиме во HTML со **strong** или со **b** (bold).

Пример со strong:

```
<p>Lorem ipsum <strong>dolor sit amet</strong>, consectetur adipiscing elit</p>
```

Пример со b:

```
<p>Lorem ipsum <b>dolor sit amet</b>, consectetur adipiscing elit</p>
```

>💡strong или b се користат како вгнездени елементи во параграф или наслов.

Најдобро е да користиме strong затоа што софтверот различно го чита тој елемент за лицата со оштетен вид. Исто така има други семантички предности.

## 9.8. Цитати

Ако цитираме текст, го користиме елементот **blockquote**. За да го наведиме изворот, го користиме атрибутот **cite**.

```
<blockquote cite="извор-на-цитатот">Цитат</blockquote>
```

>💡<blockquote> елементот има веќе preset browser style и е секогаш индентиран.

## 9.9. Unordered list

Кога сакаме да направиме листа на работи каде што редоследот не е битен, користиме **ul (unordered list)**.

За секој елемент во листата мораме да вгнездиме посебен HTML елемент во **ul**, и тој е: **li (list item)**.

```
<ul>
  <li>Млеко</li>
  <li>Јајца</li>
  <li>Вода</li>
</ul>
```

### 9.9.1. Вгнездување на други елементи

Можеме да вгнездуваме други елементи во секој li.

```
<!-- Вгнездуваме <a> во <li> -->

<ul>
  <li>
    <a>Млеко</a>
  </li>
  <li>Јајца</li>
  <li>Вода</li>
</ul>
```

### 9.9.2. Промена на симболот пред секој елемент

Симболот пред секој елемент во листата можеме да го менуваме преку атрибутот type во ul елементот.

**Типови на елементи**:

- none
- circle
- square
- disc

```
<!-- Без симбол пред секој елемент -->

<ul type="none">
  <li>Млеко</li>
  <li>Јајца</li>
  <li>Вода</li>
</ul>

<!-- Квадратче пред секој елемент -->

<ul type="square">
  <li>Млеко</li>
  <li>Јајца</li>
  <li>Вода</li>
</ul>
```

## 9.10. Ordered list

Ако сакаме да направиме листа на елементи и работи каде што редоследот е битен, тогаш го користиме елементот **ol**. Во ol елементот мораме да вгнездиме **li** за секој елемент од листата.

```
<ol>
  <li>Млеко</li>
  <li>Јајца</li>
  <li>Вода</li>
</ol>
```
### 9.10.1. Промена на симболот пред секој елемент

Симболот пред секој елемент во листата можеме да го менуваме преку **атрибутот type** во **ol** елементот.

**Типови на елементи**:

- 1 (со броеви)
- A (со големи букви)
- a (со мали букви)
- I (со римски броеви)
- i

```
<!-- Број пред секој елемент -->

<ol type="1">
  <li>Млеко</li>
  <li>Јајца</li>
  <li>Вода</li>
</ol>

<!-- Голема буква по азбучен ред пред секој елемент -->

<ol type="A">
  <li>Млеко</li>
  <li>Јајца</li>
  <li>Вода</li>
</ol>

<!-- Римски број пред секој елемент -->

<ol type="I">
  <li>Млеко</li>
  <li>Јајца</li>
  <li>Вода</li>
</ol>
```

## 9.11. Description list

Description list или описна листа се користи кога сакаме да направиме листа со елементи и нивен опис.

Структурата се состои од следниве елементи:

- dl (description list)
- dt (description term)
- dd (description definition)

```
<!-- Во <dt> ги вгнездуваме <dt> и <dd> -->

<dl>
  <dt>цинк</dt>
  <dd>Цинк е хемиски елемент со знак Zn и атомски број 30.</dd>
</dl>
```

Најчесто не се користи затоа што истото (хиерархијата) можеме да го постигнеме со наслови и параграфи.

## 9.12. Superscript и subscript

**Superscript (надзнак)** и **subscript (подзнак)** се користат за датуми, хемиски формули, математика итн.

**Superscript** се пишува со HTML елементот **sup**. Тој е секогаш вгнезден елемент (inline element) во некој друг елемент како наслов или параграф.

```
<p>Моменталната температура е 25<sup>C</sup></p>
```

**Subscript** се пишува со HTML елементот sub. Тој е секогаш вгнезден елемент (inline element) во некој друг елемент како наслов или параграф.

```
<p>Кафеин: C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub></p>
```
