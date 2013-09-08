
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

<iframe width="420" height="420" src="//www.youtube.com/embed/2tRo4jVCnIM?HD=1;rel=0;showinfo=0;controls=0" frameborder="0" allowfullscreen></iframe>

<footer class="source">source: https://www.youtube.com/watch?v=2tRo4jVCnIM</footer>

---

title: True story!
class: smaller

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
content-class: smaller

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
content-class: smaller

<table>
    <tr>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
    </tr>
    <tr>
        <td></td>
        <td>JMockit</td>
        <td>JTiger</td>
        <td>SpryTest</td>
        <td>Jtest</td>
        <td class="highlight">JUnit</td>
        <td>JWalk</td>
        <td class="highlight">TestNG</td>
        <td>Needle</td>
    </tr>
    <tr>
        <td></td>
        <td>NUTester</td>
        <td>Concordion</td>
        <td>JExample</td>
        <td>DbUnit</td>
        <td>JUnitEE</td>
        <td>Cactus</td>
        <td>JSST</td>
        <td>GroboUtils</td>
    </tr>
    <tr>
        <td></td>
        <td>Mockrunner</td>
        <td>Unitils</td>
        <td>JBehave</td>
        <td>Instinct</td>
        <td>JDave</td>
        <td>beanSpec</td>
        <td>Cucumber-JVM</td>
        <td>XMLUnit</td>
    </tr>
    <tr>
        <td></td>
        <td>EasyMock</td>
        <td>JMock</td>
        <td class="highlight">Mockito</td>
        <td>Concutest</td>
        <td>SureAssert</td>
        <td>PowerMock</td>
        <td>Jukito</td>
        <td>GrandTestAuto</td>
    </tr>
</table>

<footer class="source">source: https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks#Java</footer>

---

title: Yeoman, Grunt and Bower
subtitle: Frontend Workflow
class: segue dark nobackground

![ Algo ](images/toolset.png)

---

title: Yeoman
subtitle: Scaffolds out a new application
class: columns-2
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
class: columns-2

![ Algo ](images/grunt.png)

---

title: Demo Project
subtitle: part 2
class: center

Backend : Frontend dev. with Yeoman!
![ Algo ](images/yeoman.webp)

---

class: nobackground fill
image: images/framvslib.png

<footer class="source white">http://merrickchristensen.com/articles/learn-js/mvstar-libraries-and-frameworks.html</footer>

---

title: TDD again!
subtitle: Ecosystem in JS..
class: smaller

<table>
    <tr>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
        <th></th>
    </tr>
    <tr>
        <td></td>
        <td>Suitest</td>
        <td>DOH</td>
        <td>LBRTW UT</td>
        <td>JSUnit</td>
        <td>Enhance JS</td>
        <td>QUnit</td>
        <td>RhUnit</td>
        <td>Crosscheck</td>
    </tr>
    <tr>
        <td></td>
        <td>J3Unit</td>
        <td>Mocha</td>
        <td>intern</td>
        <td>JSNUnit</td>
        <td>YUI Test</td>
        <td>JSSpec</td>
        <td>UnitTesting</td>
        <td>JSpec</td>
    </tr>
    <tr>
        <td></td>
        <td>Jasmine</td>
        <td>screw-unit</td>
        <td>Test.Simple</td>
        <td>Test.More</td>
        <td>TestCase</td>
        <td>TestIt</td>
        <td>jsUnitTest</td>
        <td>JSTest</td>
    </tr>
    <tr>
        <td></td>
        <td>JSTest.NET</td>
        <td>jsUnity</td>
        <td>RhinoUnit</td>
        <td>JasUnit</td>
        <td>FireUnit</td>
        <td>Js-test-driver</td>
        <td>Js-test-runner</td>
        <td>Sinon.js</td>
    </tr>
    <tr>
        <td></td>
        <td>SOAtest</td>
        <td>Vows</td>
        <td>Nodeunit</td>
        <td>Tyrtle</td>
        <td>wru</td>
        <td>Buster.JS</td>
</table>

<footer class="source">source: https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks#JavaScript</footer>


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

title: yeoman-maven-plugin
class: yeoman-maven-plugin
build_lists: true

- Bullet1 github
- Bullet2
- Bullet3

------

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
- Other Conclusions? you gotta be kidding me!
- JS-Java live in perpetual work in progress

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
