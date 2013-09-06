title: Frontend Ecosystem
class: image
![hipster ecosystem](gitflow.png)


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
title: Maven & Yeoman
subtitle:
class: segue dark nobackground

---
title: DRCS/SCM workflow
subtitle: Doing it right?
class: image

![Mobile vs desktop users](gitflow.png)
---
title:  Maven
subtitle:  Build manager for Java projects
class:

---

title: Demo Project,
content_class: flexbox vcenter

Backend : Using maven archetypes!

---
title: True story!

Class:
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
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---
title:
subtitle:
class:

---


title: Slide Title
subtitle: Subtitle
class: image

![Mobile vs desktop users](image.png)

---

title: Segue Slide
subtitle: Subtitle
class: segue dark nobackground

---

title: Agenda
class: big
build_lists: true

Things we'll cover (list should build):

- Bullet1
- Bullet2
- Bullet3

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
