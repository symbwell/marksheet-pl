---
layout: post
title: "<strong>Składnia</strong> HTML"
subtitle: "Jak każdy język, również HTML ma swoje <strong>zasady</strong>"
section: html
---

HTML to nic innego jak **H**yper**T**ext **M**arkup **L**anguage:

* **HyperText** oznacza użycie protokołu HTTP
* **Markup** oznacza, że kod, który napisałeś został zawarty w słowach kluczowych (czyli tagach)
* **Language** oznacza, że Twój kod może zostać poprawnie zinterpretowany zarówno przez człowieka jak i komputer

Tak jak każdy język, HTML posiada zestaw **reguł**. Zasady te są relatywnie proste. Wyznaczają dolne **granice**, które mówią, gdzie coś się _zaczyna_, a gdzie _kończy_.

Spójrzmy na prosty paragraf, napisany w języku HTML:

{% highlight html %}
<p>Jeśli Tetris mnie czegoś nauczył, to tego, że problemy się piętrzą, a osiągnięcia znikają.</p>
{% endhighlight %}

<div class="result"><p>Jeśli Tetris mnie czegoś nauczył, to tego, że problemy się piętrzą, a osiągnięcia znikają.</p></div>

To, co widzisz w **nawiasach strzałkowych** `<`{:.language-html} i `<`{:.language-html} to **tagi** HTML. Definiują one _początek_ i _koniec_ elementu HTML.

Każdy z nich posiada swoją specyficzną **funkcję** w dokumencie HTML. W tym przypadku, `p`{:.language-html} oznacza **paragraf**.

Tagi HTML zazwyczaj występują w parach:

* tag _otwierający_ `<p>`{:.language-html} mówi przeglądarce, że w tym miejscu zaczyna się **paragraf**
* tag _zamykający_ `</p>`{:.language-html} oznacza **koniec** paragrafu

Jedyną różnicą, pomiędzy tagiem otwierającym i zamykającym jest **slash** `/`{:.language-html} poprzedzający nazwę znacznika.

Kombinacja tagu otwierającego i zamykającego wraz z zawartością pomiędzy nimi tworzy **element HTML**. Cała powyższa linijka kodu jest elementem HTML, wykorzystującym tagi HTML `<p>`{:.language-html} i `</p>`{:.language-html}.

If you [view this sample in your browser](/html/sample-paragraph.html), you'll notice that **HTML tags are not displayed** by the browser. They are only _read_ by the browser to know what _type_ of **content** you've written.

### Gdzie pisać HTML

Prawdopodobnie natknąłeś się na proste edytory plików, które posiadają rozszerzenie `.txt`.

Aby wspomniany plik tekstowy był intepretowany jako **dokument HTML** (zamiast dokumentu tekstowego), należy zmienić jego rozszerzenie z `.txt` na `.html`.

Otwórz swój **edytor tekstu**, a następnie skopiuj i wklej poniższy kod:

{% highlight html %}
<p>To moja pierwsza strona internetowa!</p>
{% endhighlight %}

Zapisz plik jako `moja-pierwsza-strona.html` a następnie otwórz go w swojej przeglądarce. Możesz to zrobić dwukrotnie klikając powstały plik lub przeciągając plik do pustej karty przeglądarki. Rezultat jaki zobaczysz to:

<div class="result"><p>To moja pierwsza strona internetowa!</p></div>

Remember:

* use a text editor like Notepad++ to **create** HTML documents
* use a browser like Firefox to **open** HTML documents

### Attributes

Attributes act like **extra** information tied to an HTML element. They are written _within_ an HTML _tag_. As such, they are not displayed by the browser either.

For example, the `href` attribute is used to define the target of a **link** (which uses an **a**nchor tag): 

{% highlight html %}
<a href="http://www.mozilla.com/firefox">Download Firefox</a>
{% endhighlight %}

<div class="result"><a href="http://www.mozilla.com/firefox">Download Firefox</a></div>

There are [16 HTML attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes) that can be used on _any_ HTML element. All of them are **optional**.

You'll mostly use `class` (which is used for CSS), and `title` (which is the tooltip that appears when hovering an item like this one).

Some HTML elements have **obligatory** attributes. For example, when inserting an image, you have to provide the location of the image, using the `src` (source) attribute:

{% highlight html %}
<img src="#" alt="Description of the image">
{% endhighlight %}

Considering that the purpose of the `<img>` element is to display an image, it makes sense for the path to the image to be **required**.

### Comments

If you write something in your code without disrupting how the browser will display your page, you can write **comments**. They will be _ignored_ by the browser, and are only useful for us humans who write the code.

A comment starts with `<!--` and ends with `-->`.

{% highlight html %}
<!-- This sentence will be ignored by the browser -->
<p>Hello World!</p>
{% endhighlight %}

<div class="result"><p>Hello World!</p></div>

### Self-enclosing elements

Some HTML elements only have an opening tag:

{% highlight html %}
<br> <!-- line-break -->
<img src="http://placehold.it/50x50" alt="Description"> <!-- image -->
<input type="text"> <!-- text input -->
{% endhighlight %}

Because they don't have a closing tag and consequently can't contain anything _inside_ them, self-enclosing elements usually carry a few attributes, to provide them with additional information.
