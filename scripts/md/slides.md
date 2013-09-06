
title: Frontend Ecosystem
subtitle:
content_class: image

![hipster ecosystem](images/frontend-eco1.png)
<footer class="source">source: http://decodize.com/</footer>

---

title: Frontend Ecosystem
subtitle:
content_class: image

![hipster ecosystem](images/frontend-eco2.png)
<footer class="source">source: http://decodize.com/</footer>

---

title: Backend (Java) Ecosystem
class: image

![java ecosystem](gitflow.png)

---

title: Agenda
class: big
build_lists: true

Things we'll (try to) cover;

- Maven
- Yeoman
- Grunt
- Bower
- TDD
- Repository workflow

---

title:  Demo Overview
class: image

---

title: DRCS/SCM workflow
subtitle: Doing it right?
content-class: image

![Gitflow](images/gitflow.png)

---

title: Maven
subtitle:
class: segue dark nobackground

---

title:  Maven
subtitle:  Build manager for Java projects
class:

---

title: Demo Project
subtitle: part 1
content_class: flexbox vcenter

Backend : Using maven archetypes!

---

content_class: vcenter

<iframe width="420" height="420" src="//www.youtube.com/embed/kljYH0b9NUc?HD=1;rel=0;showinfo=0;controls=0" frameborder="0" allowfullscreen></iframe>

<footer class="source">source: http://www.youtube.com/embed/kljYH0b9NUc</footer>
---
title: True story!

<pre class="prettyprint" data-lang="java">
public static final String DATE_PATTERN = "dd-mm-yyy";
....
final DateFormat format = new SimpleDateFormat(DATE_PATTERN);
</pre>

Test:
<pre class="prettyprint" data-lang="java">
@Before
public void setUp() throws Exception {
validDate = "10-04-2004";
}
@Test
public void testValidGregorianDate() throws Exception {
....
assertEquals(xmlGregorianCalendar.getDay(), 10);
}
</pre>

---

title: :-S

Class:
<pre class="prettyprint" data-lang="java">
public static final String DATE_PATTERN = "dd-MM-yyy";
....
final DateFormat format = new SimpleDateFormat(DATE_PATTERN);
</pre>

Test:
<pre class="prettyprint" data-lang="java">
@Before
public void setUp() throws Exception {
validDate = "10-04-2004";
}
@Test
public void testValidGregorianDate() throws Exception {
....
assertEquals(10, xmlGregorianCalendar.getDay());
assertEquals(4, xmlGregorianCalendar.getMonth());
assertEquals(2004, xmlGregorianCalendar.getYear());}
</pre>

---

title: TDD
subtitle: Java ecosystem
class: image

![demasiado](java_tdd.png)

---

title: Yeoman, Grunt and Bower
subtitle: Frontend Workflow
class: segue dark nobackground

---

title: Yeoman
subtitle: Scaffolds out a new application
class: image
build_lists: true

- generator angular
- generator
- generator
- generator
- generator

![ Algo ](images/yeoman-logo.png)

---

title: Grunt
subtitle: Build, preview and test your project
content-class: image

![ Algo ](images/grunt.png)

---

title: Demo Project
subtitle: part 2
class: title-slide

Backend : Frontend dev. with Yeoman!
![ Algo ](images/toolset.png)

---

class: nobackground fill
image: images/framvslib.png

<footer class="source white">http://merrickchristensen.com/articles/learn-js/mvstar-libraries-and-frameworks.html</footer>

---

title: TDD again!
subtitle: in JS..
content-class: image

![ Algo ](images/frontend-tdd.png)

---

title: Bower
subtitle: dependency management
content-class: image

![ Algo ](images/bower-logo.png)

---

title: Protractor
subtitle: just for AngularJS
class: image

![ Algo ](protractor.png)

---

title: PhantomJS and SlimerJS
class: image

![ Algo ](phantomjs.png)

---

title: Debugging AngularJS
subtitle: Hardcore vs Batarang
class: image

![Hardcore vs Batarang](image.png)
---

title: Current Web Tooling
subtitle: Bred Victor's dream
class: image

![web tooling](chrome-dev-tools.png)

---

title: Yeoman's dist
class: image

![web tooling](yeoman-dist.png)

---

title: Maven & Yeoman
class: segue dark nobackground

---

title: Releasing
class: maven-release-plugin ?
build_lists: true

- Bullet1
- Bullet2
- Bullet3

---

title: Shipping
class: image
![ Algo ](shipping.png)

---

title: Conclusions ??
class: generators
build_lists: true

- New web development Architecture demands a better back-end and front-end integration
- Future of yeoman looks promising!
- More generators in yeoman.

---

title: Today
class: nobackground fill

![Many kinds of devices.](image.png)

<footer class="source">source: place source info here</footer>

---

title: Big Title Slide
class: title-slide

---

title: Code Example

Media Queries are sweet:

<pre class="prettyprint" data-lang="css">
@media screen and (max-width: 640px) {
  #sidebar { display: none; }
}
</pre>

---

title: Once more, with JavaScript

<pre class="prettyprint" data-lang="java">
function isSmall() {
  return window.matchMedia("(min-device-width: ???)").matches;
}

function hasTouch() {
  return Modernizr.touch;
}

function detectFormFactor() {
  var device = DESKTOP;
  if (hasTouch()) {
    device = isSmall() ? PHONE : TABLET;
  }
  return device;
}
</pre>

---

title: Centered content
content_class: flexbox vcenter

This content should be centered!
