
class: fill

![hipster ecosystem](images/frontend-eco1.png)
<footer class="source">Frontend Ecosystem source: http://decodize.com/</footer>

---

class: fill

![hipster ecosystem](images/frontend-eco2.png)
<footer class="source">Frontend Ecosystem source: http://decodize.com/</footer>

---

title: Agenda
class: big
build_lists: true

Things we'll (try to) cover;

- TDD
- Unit Testing
- E2E Testing
- CI

---

title: TDD
subtitle:
class: segue dark nobackground

---

title:  Brogramming TDD?
class: columns-2
build_lists: true

- Keep fixing your code until you can't see any bugs
- Test using alerts and console logs
- Hotswap variables directly to corner bugs
- Refresh the page as much as you can
- If I can't see the bug then it's not there
- Only bother testing with Chrome
- Wait for your boss to yell at you...
- Trace Driven Development

![Brogrammer](images/brogrammer.png)

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title:  Uncle Bob's TDD!
class: columns-2
build_lists: true

- Write your tests before or inline with during development
- Test using dump(), debugger and breakpoints
- Skip, focus and mock specific tests to corner certain bugs
- Autotest all your tests each time you update your code
- Existing tests keep track of previously-fixed bugs
- Test as many browsers and devices as you have access to
- Wait for your tests or CI server to yell at you...
- Test Driven Development

![UncleBob](images/unclebob.jpg)

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

content_class: flexbox vcenter

![TDD cycle](images/tdd_flow.gif)

<footer class="source">source: http://diogoosorio.com</footer>

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
        <td>karma/Testacular</td>
        <td>JSUnit</td>
        <td>EnhanceJS</td>
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
        <td>Protractor</td>
        <td>LBRTW UT</td>
</table>

<footer class="source">source: https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks#JavaScript</footer>

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
        <td class="highlight">karma/Testacular</td>
        <td>JSUnit</td>
        <td>EnhanceJS</td>
        <td>QUnit</td>
        <td>RhUnit</td>
        <td>Crosscheck</td>
    </tr>
    <tr>
        <td></td>
        <td>J3Unit</td>
        <td class="highlight">Mocha</td>
        <td>intern</td>
        <td>JSNUnit</td>
        <td>YUI Test</td>
        <td>JSSpec</td>
        <td>UnitTesting</td>
        <td>JSpec</td>
    </tr>
    <tr>
        <td></td>
        <td class="highlight">Jasmine</td>
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
        <td class="highlight">Protractor</td>
        <td>LBRTW UT</td>
</table>

<footer class="source">source: https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks#JavaScript</footer>

---

title: Unit Testing
subtitle:
class: segue dark nobackground

---

Unit Testing

The core units which make up features should be verified with accompanying unit tests. In JavaScript apps, the smallest units of code you can test are usually individual functions.

---

title: Controllers
subtitle:
class: big

<pre class="prettyprint" lang-js data-lang="Controller">
it('should have a working myController',
  inject(function($controller, $rootScope) {

  var ctrl = $controller('MyCtrl', {
    $scope : $rootScope
    //anything in here will act as a mock
  });
  expect($rootScope.data).toBe('something');
}));
</pre>

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title: Directives
subtitle: $compile and $digest
class: big

<pre class="prettyprint" lang-js data-lang="Directive">
it('should have a working myDirective',
  inject(function($compile, $rootScope, $document) {

  var body = angular.element($document[0].body);
  var element = angular.element('&lt;div my-directive&gt;&lt;/div&gt;');
  body.append(element);

  $compile(element)($rootScope);
  $rootScope.$digest();

  expect(element.children().length).toBe(10);
}));
</pre>

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title: Services/Factories
subtitle: Injecting the service...
class: big

<pre class="prettyprint" lang-js data-lang="Services">
it('should have a working myFactory',
  inject(function(urlPrefixer, $location) {

  urlPrefixer('/home');
  expect($location.path()).toBe('/public/home');
}));
</pre>

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title: Services/Factories
subtitle: Module to mock it!
class: big

<pre class="prettyprint" lang-js data-lang="Services">
it('should have a working myDirective',
  var interceptedPath;
  module(function($provider) {
    $provider.provide('$location', {
      path : function(p) {
        interceptedPath = p;
      }
    });
  });
  inject(function(urlCounter) {
    urlPrefixer('/home');
    expect(interceptedPath).toBe('/admin/home');
  })
);
</pre>

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title: Filters
subtitle: Like with services...
class: big

<pre class="prettyprint" lang-js data-lang="Filters">
it('should have a working even filter',
  inject(function(evenFilter, $filter) {

  expect(evenFilter([1,2,3,4])).toBe([2,4]);
  expect($filter('even')([1,2,3,4])).toBe([2,4]);
}));
</pre>

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title: Routes
subtitle: $location
class: big

<pre class="prettyprint" lang-js data-lang="Routes">
it('should have a working /home route', inject(function($location, $rootScope) {
  $location.path('/home');
  $rootScope.$digest();

  expect($location.path()).toBe('/home');
  expect($route.current.controller).toBe('HomeCtrl');
}));
</pre>

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title:Skipping and Filtering Tests
subtitle:
content_class: flexbox vcenter

![ Compatibility ](images/jasmine_mocha.png)

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>

---

title: Test Coverage
subtitle: karma-coverage
class: big
build_lists: true

- Comes bundled into Karma via karma-coverage
- Gives you a full breakdown of what tests were captured and what tests were not
- Run using "grunt coverage".

 <footer class="source">source http://www.yearofmoo.com/2013/09/advanced-testing-and-debugging-in-angularjs.html</footer>


---





---

 title: E2E Testing
 subtitle:
 class: segue dark nobackground

---

title: Promises
subtitle: ... or futures, deferreds
class: big

Promises are objects which represent the pending result of an asynchronous operation. You can use these to schedule further activity after the asynchronous operation has completed by supplying a callback.
<br>
Providing a clear interface to schedule activity with asynchronous tasks, they also compose.

<footer class="source">source: http://martinfowler.com/bliki/JavascriptPromise.html and http://net.tutsplus.com/tutorials/javascript-ajax/wrangle-async-tasks-with-jquery-promises/</footer>

---

title: Promises
subtitle: ... or futures, deferreds
class: big

<pre class="prettyprint" lang-js data-lang="Promise">
<br>
aPromise = someAsyncOperation();
aPromise.done(function() {
// runs if all went well
});
aPromise.fail(function() {
// runs if something went wrong
});
aPromise.always(function() {
// runs either way
});
</pre>

<footer class="source">source: http://martinfowler.com/bliki/JavascriptPromise.html and http://net.tutsplus.com/tutorials/javascript-ajax/wrangle-async-tasks-with-jquery-promises/</footer>

---

title: Protractor
subtitle: just for AngularJS
content_class: flexbox vcenter

![ Protractor ](images/protractor.png)

---

 title: Protractor
 subtitle:
 class: big
 build_lists: true

- An AngularJS E2E Testing Framework
- Introduced during AngularJS 1.2 and Beyond presentation
- A new replacement of the existing E2E Testing framework

  <footer class="source">source: An Introduction to AngularJS End to End Testing with Protractor http://www.youtube.com/watch?v=idb6hOxlyb8</footer>

---

 title: Protractor
 subtitle:
 class: big
 build_lists: true

- Built on WebdriverJS and Selenium Server
- New syntax when writing tests
- Allows running tests targeting remote addresses, No longer need to have test files on the server being tested
- Can take advantage of Selenium Grid to run multiple browsers at once; ie Sauce Labs
- Has it’s own runner, no need for Karma
- Can use Jasmine or Mocha to write test suites



  <footer class="source">source: An Introduction to AngularJS End to End Testing with Protractor http://www.youtube.com/watch?v=idb6hOxlyb8</footer>

---

 title: Protractor
 subtitle:
 class: big

- Installed via Node Package Manager
<pre class="prettyprint" lang-sh data-lang="$">
<br>
npm install protractor
</pre>

- Install Selenium Standalone Server
<pre class="prettyprint" lang-sh data-lang="$">
<br>
node_modules/protractor/bin/install_selenium_standalone
</pre>

- Note: The Standalone Server is not needed if you are going to run against an existing Selenium Grid or Installation
- Note: Windows users need to execute second command from node

  <footer class="source">source: An Introduction to AngularJS End to End Testing with Protractor http://www.youtube.com/watch?v=idb6hOxlyb8</footer>

---

 title: Protractor
 subtitle:
 class: big

<pre class="prettyprint" lang-js data-lang="Basic Test Structure">
var util = require('util');

describe('Adjunct List', function () {
    var ptor;

    beforeEach(function () {
        ptor = protractor.getInstance();
        ptor.get('#/');
    });

    it('should do something', function () {
        ptor = protractor.getInstance();
        ptor.findElement(protractor.By.className('brand')).click();
        expect(ptor.getCurrentUrl()).toContain('#/');
    }, 10000);
});
</pre>


  <footer class="source">source: An Introduction to AngularJS End to End Testing with Protractor http://www.youtube.com/watch?v=idb6hOxlyb8</footer>

---

 title: Protractor
 subtitle:
 class: big
 build_lists: true

- Use Selenium WebdriverJS Syntax:
<pre class="prettyprint" lang-js data-lang="Locators">
<br>
	ptor.findElement(protractor.By.x(‘...’));
or
	ptor.findElements(protractor.By.x(‘...’));
</pre>
- findElement returns a single element, findElements returns an array of elements.
- Both will throw an exception if the locator cannot find the element on the page



  <footer class="source">source: An Introduction to AngularJS End to End Testing with Protractor http://www.youtube.com/watch?v=idb6hOxlyb8</footer>

---

 title: Protractor
 subtitle:
 class: big

<pre class="prettyprint" lang-js data-lang="Locators">
protractor.By.className('redBtn')
protractor.By.css('.redBtn')
protractor.By.id('loginButton')
protractor.By.linkText('Go Home')
protractor.By.partialLinktext('Home')
protractor.By.name('email')
protractor.By.tagName('h2')
protractor.By.xpath('')
</pre>

---

 title: Protractor
 subtitle:
 class: big

<pre class="prettyprint" lang-js data-lang="Locators">
protractor.By.binding('{{status}}')
protractor.By.select("user")
protractor.By.selectedOption("red")
protractor.By.input("user")
protractor.By.repeater("cat in pets")
protractor.By.repeater("cat in pets").row(1).column("{{cat.name}}"))
</pre>

---

 title: WebElement
 subtitle: Methods
 class: big

<pre class="prettyprint" lang-js data-lang="WebElement Methods">
<br>
clear() //If this element is a text entry element, this will clear the value.
click() //Click this element.
getAttribute(name) //Get the value of a the given attribute of the element.
getCssValue(propertyName) //Get the value of a given CSS property.
getLocation() //Where on the page is the top left-hand corner of the rendered element?
getSize() //What is the width and height of the rendered element?
getTagName() //Get the tag name of this element.
</pre>

---

 title: WebElement
 subtitle: Methods
 class: big

<pre class="prettyprint" lang-js data-lang="WebElement Methods">
<br>
getText() // Get the visible (i.e. not hidden by CSS) innerText of this element,
          //including sub-elements, without any leading or trailing whitespace.
isDisplayed() // Is this element displayed or not? This method avoids the problem
              //of having to parse an element's "style" attribute.
isEnabled() // Is the element currently enabled or not? This will generally return
            //true for everything but disabled input elements.
isSelected() // Determine whether or not this element is selected or not.
sendKeys(keysToSend) //Use this method to simulate typing into an element,
                     //which may set its value.
</pre>

---

 title: CI
 subtitle:
 class: segue dark nobackground

 ---

 title: Continuous Integration
 subtitle:
 class: segue nobackground

 Continuous Integration is a software development practice where members of a team integrate their work frequently, usually each person integrates at least daily - leading to multiple integrations per day. Each integration is verified by an automated build (including test) to detect integration errors as quickly as possible. Many teams find that this approach leads to significantly reduced integration problems and allows a team to develop cohesive software more rapidly.

 <footer class="source">source http://martinfowler.com/articles/continuousIntegration.html</footer>

---

title:  Travis
class: columns-2
build_lists: true

- Sidebar
- Build in progress [yellow]
- Build failed [red]
- Build passed [green]
- Project name and links
- Types of build
- Build activity

![Travis](images/travis-interface.png)

 <footer class="source">source http://net.tutsplus.com/tutorials/tools-and-tips/travis-ci-what-why-how/</footer>

---

