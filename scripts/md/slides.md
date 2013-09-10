
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

- Maven
- Yeoman
- Grunt
- Bower
- TDD
- Repository workflow

---

title: DRCS/SCM workflow
subtitle: Doing it right?
class: Big nobackground fill

![Gitflow](images/gitflow-w.png)
 <footer class="source">source Vincent Driessen's branching model: http://nvie.com/posts/a-successful-git-branching-model/</footer>

---

title: Maven
subtitle:
class: segue dark nobackground

---

title:  Maven
subtitle:  Build manager for Java projects
content_class: flexbox vcenter

![maven](images/maven_cycle.jpg)

 <footer class="source">source http://books.sonatype.com/mvnref-book/reference/public-book.html</footer>

---

title:  Maven
subtitle:  Build manager for Java projects
class: columns-2
build_lists: true

Maven provides developers ways to manage :

- Builds
- Documentation
- Reporting
- Dependencies
- SCMs
- Releases
- Distribution
- mailing list

![Maven](images/maven_cycle2.png)

 <footer class="source">source http://books.sonatype.com/mvnref-book/reference/public-book.html</footer>

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
conten_class: smaller

<pre class="prettyprint" lang-java data-lang="XX.java">
public static final String DATE_PATTERN = "dd-mm-yyy";
....
final DateFormat format = new SimpleDateFormat(DATE_PATTERN);
</pre>

<pre class="prettyprint" lang-java data-lang="XXTest.java">
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

<pre class="prettyprint" lang-java data-lang="XX.java">
public static final String DATE_PATTERN = "dd-MM-yyy";
....
final DateFormat format = new SimpleDateFormat(DATE_PATTERN);
</pre>

<pre class="prettyprint" lang-java data-lang="XXTest.java">
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

content_class: flexbox vcenter

![TDD cycle](images/tdd_flow.gif)

<footer class="source">source: http://diogoosorio.com</footer>

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

- Installation
<pre class="prettyprint" lang-sh data-lang="$">
npm install -g yo
npm install -g generator-webapp
npm install -g generator-angular
</pre>
<br>
- Usage (with AngularJS generator):
<pre class="prettyprint" lang-sh data-lang="$">
yo angular
</pre>

![ Algo ](images/yeoman-logo.png)

Writes our Grunt configuration, pulling it in relevant Grunt tasks that we need for our build.

<footer class="source">source: http://yeoman.io</footer>

---

title: Grunt
subtitle: Build, preview and test your project
class: columns-2
content_class: smaller

<p>Basically; Grunt is a JavaScript task runner which you can think of as Ant for JavaScript.
 It has a <a href="http://gruntjs.com/plugins">vast</a> ecosystem of predefined tasks, <a href="https://github.com/gruntjs/grunt-contrib">some</a> of which are maintained by the core team and many contributed by the community.</p>
Installation
<pre class="prettyprint" lang-sh data-lang="$">
&#35; already installed with Yo
npm install -g grunt-cli
</pre>
Usage (with the AngularJS generator):
<pre class="prettyprint" lang-sh data-lang="$">
grunt test
grunt server
grunt
</pre>

![ Algo ](images/grunt.png)

<footer class="source">source: http://addyosmani.com/blog/making-maven-grunt/</footer>

---

title: Bower
subtitle: dependency management
class: columns-2 smaller
content_class: smaller

<pre class="prettyprint" lang-sh data-lang="$">
&#35; already installed with Yo
npm install -g bower
</pre>
<br>
Usage:
<pre class="prettyprint" lang-sh data-lang="$">
echo "alias bower='noglob bower'" >> ~/.zshrc
&#35; Using the dependencies listed in the current
&#35;  directory's bower.json
bower install
&#35; Using a local or remote package
bower install &lt;package&gt;
bower install angular-ui
&#35; Using a specific version of a package
bower install &lt;package&gt;#&lt;version&gt;
&#35; Using a different name and a specific version
&#35;  of a package
bower install &lt;name&gt;=&lt;package&gt;#&lt;version&gt;
</pre>

![ Algo ](images/bower-logo.png)
<footer class="source">source: http://bower.io</footer>

---

title: Demo Project
subtitle: part 2
class: center

Frontend dev. with Yeoman

![ Algo ](images/yeoman-workflow.jpg)

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

title: Protractor
subtitle: just for AngularJS
content_class: flexbox vcenter

![ Protractor ](images/protractor.png)

---

title: Protractor
content_class: flexbox vcenter

![ Protractor ](images/protractor2.png)

---

title: PhantomJS and SlimerJS
content_class: flexbox vcenter

![ Algo ](phantomjs.png)

---

title: Debugging AngularJS
subtitle:  Batarang
class: image

![Batarang](images/model-tree.png)

---

<iframe width="350" height="3500" src="//www.youtube.com/embed/wxWM4t68cR4?HD=1;rel=0;showinfo=0;controls=1" frameborder="0" allowfullscreen></iframe>

<footer class="source">source Bret Victor's Inventing on Principle (13'30) : https://www.youtube.com/watch?v=wxWM4t68cR4</footer>

---

title: Yeoman's dist
class: image
build_lists: true

- Recompiling all CoffeeScript and SASS files for production
- Using r.js to compile and optimize any AMD modules
- Concatenation and minification of scripts and stylesheets
- Compressing your images using OptiPNG for PNG files and JPEGtran-turbo for JPEGs
- Creating an Application Cache manifest via Confess.js
- Using revision filenames or oldernames

<footer class="source">source https://github.com/yeoman/yeoman/wiki/yeoman-build</footer>

---

title: Maven & Yeoman
class: segue dark nobackground

---

class: dark
content_class: quote smaller flexbox vleft auto-fadein
build_lists: true

What are the options?

- <q>We don’t know how to integrate Grunt tooling into our Maven workflow. Even after setting up Node on our dev. box, there’s no documentation about using Maven with Grunt and everyone seems to want it but there are no blessed solutions out there.</q>
 - Consider your backend and front-end code as completely separate entities
 - Ignore modern tooling altogether.
 - Use the Maven-exec plugin to call out to Grunt from your existing build process


<footer class="source">source is Osmani of course!: http://addyosmani.com/blog/making-maven-grunt/</footer>

---

title: Maven and Yo/Grunt :  yeoman-maven-plugin

Declare the plugin:

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;plugin&gt;
      &lt;groupId&gt;com.github.trecloux&lt;/groupId&gt;
      &lt;artifactId&gt;yeoman-maven-plugin&lt;/artifactId&gt;
      &lt;version&gt;0.1&lt;/version&gt;
      &lt;executions&gt;
          &lt;execution&gt;
              &lt;goals&gt;
                  &lt;goal&gt;build&lt;/goal&gt;
              &lt;/goals&gt;
          &lt;/execution&gt;
      &lt;/executions&gt;
  &lt;/plugin&gt;
</pre>

<footer class="source">source: https://raw.github.com/trecloux/yeoman-maven-plugin/master/src/main/java/com/github/trecloux/yeoman/YeomanMojo.java</footer>

---

title: Maven and Yo : maven-war-plugin

Add the yeoman dist directory to our WAR file:

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;plugin&gt;
    &lt;artifactId&gt;maven-war-plugin&lt;/artifactId&gt;
    &lt;version&gt;2.4&lt;/version&gt;
            &lt;configuration&gt;
        &lt;webResources&gt;
            &lt;resource&gt;
                &lt;directory&gt;yo/dist&lt;/directory&gt;
            &lt;/resource&gt;
        &lt;/webResources&gt;
    &lt;/configuration&gt;
&lt;/plugin&gt;
</pre>

---

title: Maven and Yo : maven-clean-plugin
content_class: smaller

And clean the generated directories:

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;plugin&gt;
    &lt;artifactId&gt;maven-clean-plugin&lt;/artifactId&gt;
    &lt;version&gt;2.5&lt;/version&gt;
    &lt;configuration&gt;
        &lt;filesets&gt;
            &lt;fileset&gt;
                &lt;directory&gt;yo/dist&lt;/directory&gt;
            &lt;/fileset&gt;
            &lt;fileset&gt;
                &lt;directory&gt;yo/.tmp&lt;/directory&gt;
            &lt;/fileset&gt;
            &lt;fileset&gt;
                &lt;directory&gt;yo/app/components&lt;/directory&gt;
            &lt;/fileset&gt;
            &lt;fileset&gt;
              &lt;directory&gt;yo/node_modules&lt;/directory&gt;
            &lt;/fileset&gt;
        &lt;/filesets&gt;
    &lt;/configuration&gt;
&lt;/plugin&gt;
</pre>

---

title: Maven and Bower : exec-maven-plugin
content_class: smaller

Gerbrand van Dieijen's Bower-maven Dependency management :

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;plugin&gt;
   &lt;groupId&gt;org.codehaus.mojo&lt;/groupId&gt;
   &lt;artifactId&gt;exec-maven-plugin&lt;/artifactId&gt;
   &lt;executions&gt;
     &lt;execution&gt;
     &lt;phase&gt;generate-sources&lt;/phase&gt;
     &lt;goals&gt;
      &lt;goal&gt;exec&lt;/goal&gt;
     &lt;/goals&gt;
     &lt;/execution&gt;
   &lt;/executions&gt;
   &lt;configuration&gt;
     &lt;executable&gt;bower&lt;/executable&gt;
     &lt;arguments&gt;
      &lt;argument&gt;install&lt;/argument&gt;
     &lt;/arguments&gt;
     &lt;workingDirectory&gt;${basedir}/src/main/webapp&lt;/workingDirectory&gt;
   &lt;/configuration&gt;
 &lt;/plugin&gt;
</pre>

<footer class="source">source Xebia: http://blog.xebia.com/2013/06/15/maven-user-starting-with-javascript-package-management/</footer>

---

title: What about Jetty? jetty-maven-plugin
content_class: smaller

We can integrate <a href="http://www.eclipse.org/jetty/">Jetty</a> as well:

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;plugin&gt;
    &lt;groupId&gt;org.mortbay.jetty&lt;/groupId&gt;
    &lt;artifactId&gt;jetty-maven-plugin&lt;/artifactId&gt;
    &lt;version&gt;8.1.4.v20120524&lt;/version&gt;
    &lt;configuration&gt;
        &lt;stopKey&gt;foo&lt;/stopKey&gt;
        &lt;stopPort&gt;8000&lt;/stopPort&gt;
        &lt;reload&gt;manual&lt;/reload&gt;
        &lt;webAppConfig&gt;
            &lt;contextPath&gt;/${project.name}&lt;/contextPath&gt;
            &lt;baseResource implementation=&quot;org.eclipse.jetty.util.resource.ResourceCollection&quot;&gt;
                &lt;resourcesAsCSV&gt;src/main/webapp,yo/dist&lt;/resourcesAsCSV&gt;
            &lt;/baseResource&gt;
        &lt;/webAppConfig&gt;
    &lt;/configuration&gt;
&lt;/plugin&gt;
</pre>

<footer class="source">source: http://jpgmr.wordpress.com/2013/06/12/jetty-and-the-yeoman-maven-plugin/</footer>

---

title: Releasing
content_class: smaller

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;plugin&gt;
        &lt;groupId&gt;org.apache.maven.plugins&lt;/groupId&gt;
        &lt;artifactId&gt;maven-release-plugin&lt;/artifactId&gt;
        &lt;version&gt;${maven-release-plugin.version}&lt;/version&gt;
        &lt;configuration&gt;
          &lt;autoVersionSubmodules&gt;true&lt;/autoVersionSubmodules&gt;
          &lt;goals&gt;deploy&lt;/goals&gt;
          &lt;pushChanges&gt;false&lt;/pushChanges&gt;
          &lt;localCheckout&gt;true&lt;/localCheckout&gt;
          &lt;tagNameFormat&gt;v@{project.version}&lt;/tagNameFormat&gt;
        &lt;/configuration&gt;
&lt;/plugin&gt;
</pre>

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;scm&gt;
&#160;&#160;&lt;connection&gt;scm:git:https://xxx/xxx.git&lt;/connection&gt;
&#160;&#160;&lt;developerConnection&gt;scm:git:https://xxx/xxx.git&lt;/developerConnection&gt;
&#160;&#160;&lt;url&gt;https://xxx/xxx.git&lt;/url&gt;
&lt;/scm&gt;
</pre>

---

title: Releasing
subtitle: With pure git (git flow)
class: smaller
content_class: smaller

<pre class="prettyprint" lang-sh data-lang="$">
git checkout develop
git branch Version_1.0
git checkout Version_1.0
mvn release:prepare -B
mvn release:clean
mvn release:prepare release:perform -B
git tag -d v-1.0
git checkout master
git fetch origin master
git merge –no-ff Version_1.0
git tag -a Version_1.0
git push origin master
git checkout develop
git fetch origin develop
git merge –no-ff Version_1.0
git push origin develop
git branch –d Version_1.0
</pre>

---

title: Releasing
subtitle: With git-flow

<pre class="prettyprint" lang-sh data-lang="$">
git checkout develop
git flow release start v-1.0
mvn release:prepare -B
mvn release:clean
mvn release:prepare release:perform -B
git tag -d v-1.0
git flow release finish -p 1.0
</pre>

---

title: Releasing
subtitle: With jgitflow

<pre class="prettyprint" lang-sh data-lang="$">
git checkout develop
mvn clean jgitflow:release-start
mvn jgitflow:release-finish
</pre>

<pre class="prettyprint" lang-xml data-lang="pom.xml">
&lt;build&gt;
    &lt;plugins&gt;
        &lt;plugin&gt;
            &lt;groupId&gt;com.atlassian.maven.plugins&lt;/groupId&gt;
            &lt;artifactId&gt;maven-jgitflow-plugin&lt;/artifactId&gt;
            &lt;version&gt;1.0-alpha20&lt;/version&gt;
            &lt;configuration&gt;
                &lt;!-- see goals wiki page for configuration options --&gt;
            &lt;/configuration&gt;
        &lt;/plugin&gt;
    &lt;/plugins&gt;
&lt;/build&gt;
</pre>

<footer class="source">source: https://blogs.atlassian.com/2013/05/maven-git-flow-plugin-for-better-releases/</footer>

---

title: What about Gradle??
class: columns-2

The quick and dirty way of doing it would just be to either hard code some grunt.execute().text ...
<pre class="prettyprint" data-lang="groovy">
task requirejs(type: Exec) {
    commandLine 'grunt', 'requirejs'
}
</pre>

![ Gradle ](images/gradle-icon-512x512.png)

<footer class="source">source: http://naleid.com/blog/2013/01/24/calling-gruntjs-tasks-from-gradle/</footer>

---

title: Conclusions ??
class: generators
build_lists: true

- The new web development Architecture demands a better back-end and front-end integration.
- On projects where the front-end and back-end are somewhat coupled, using Maven as our primary build system with binaries like Grunt and Bower called out as needed is completely feasible.
- For new projects, keeping these two pieces distinctly separate comes with the flexibility to use whatever tooling chain you want, including just using Grunt for your front-end.
