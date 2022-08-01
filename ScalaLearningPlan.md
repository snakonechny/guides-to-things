## How I went about learning Scala

### 0. Motivation - why Scala?

* for Spark, the API seems to be richer, especially the low-level functionality. See [here](https://www.youtube.com/watch?v=LBoSgiLV_NQ)

* serious data engineering seems to be done in Scala; Spark is to blame here, I think - [video](https://www.youtube.com/watch?v=MG1XMUWG1oM)

* a lot of really smart people thinking really smart thoughts about things I don't understand - [blog](https://blog.softwaremill.com/why-scala-a6ac8c98c541)

* this new Dotty compiler is fascinating - [video](https://www.youtube.com/watch?v=Nv-BzYOMiWY&t=922s). Heads up, Dotty will become Scala 3 eventually, and since this video was published the compiler has moved even further along

* turns out people can explain complicated technical concepts without going full academic on you - [video](https://www.youtube.com/watch?v=IayQ7lxPUP4)

### 1. Setup

* don't use Intellij as your IDE; everyone and their mother uses Intellij, and I think it makes starting very easy but doing anything more complicated - too difficult for a Scala novice. I think Scala should be learned in the least obstructed way possible, and VSCode/Metals is the way to go IMO

* I committed to VSCode and wanted to pull my hair out for a few weeks, but eventually you get the hang of things. This is a good motivation for VSCode as [your IDE of choice](https://www.youtube.com/watch?v=MRQMylDxBJ8&t=1412s)

* this helped enormously - [video](https://www.youtube.com/watch?v=kc2jrTEs5ug&t=641s)

* in general, if nothing works and `sbt` doesn't start and you miss `IPython`, just clone a repo from Github that has a working Scala project. Load it up and start modifying the `build.sbt` file to get all the packages you need, etc.

### 2. Classes/videos/guides
*(in the order I took them, mostly)*

* this [playlist](https://www.youtube.com/watch?v=pq4MneSnZDc&list=PLJGDHERh23x-YBJ8LmYU_IGBFflvsKfLu)

* sections 2, 3, and 4 of this [class](https://www.udemy.com/course/rock-the-jvm-scala-for-beginners/)

* then this [class](https://www.udemy.com/course/advanced-scala/)

* then depending on your interests:
    
    - for [Akka and distributed actor system](https://www.udemy.com/course/akka-essentials), followed by his recommended course sequence
    - for [Spark intro](https://www.udemy.com/course/apache-spark-with-scala-hands-on-with-big-data) or [intro v2](https://www.udemy.com/course/spark-essentials)
    . I did both and like the second course a little better
    - for Spark Streaming [(I really like this stuff)](https://www.udemy.com/course/spark-streaming)

* for more pedantic style and philosophy learning - [Scala Basic and Intro to Functional Programming](https://rockthejvm.com/p/scala) and [Advanced FP](https://rockthejvm.com/p/advanced-scala)

* the fine folks of [Lightbend](https://academy.lightbend.com/) made all of their basic and some premium trainings available for free as long as you log in with your organization's email. @deloitte.com works just fine

_Heads up, if you're a Deloitte employee, [Udemy is free for you](https://deloittedevelopment.udemy.com/); if you aren't a Daddy D employee, $20 a course is pretty affordable nonetheless_

### 3. Books
*(I keep them around for reference, but I wouldn't read a book and consider that being "learning Scala")*

* _Programming Scala_ by Wampler & Payne; Scala operational manual

* _Functional Programming in Scala_ by Chiusano & Bjarnason; how all topical books should be written. What -> Why -> How -> Upsides/Downsides -> Alternatives

* _Hands-On Scala Programming_ by Li Haoyi; practical, driven by use cases. Is it worth $60? I don't know, but if someone else is paying...

* _Spark: The Definitive Guide_ by Chambers & Zaharia; DON'T BUY THE HARDCOPY PLEASE - THE EBOOK OFFERS FREE UPDATES EVERY TIME THERE IS A MAJOR SPARK RELEASE

; _Learning Spark_ by Damji, Wenig & Das; [Available for free, maintained and updated](https://pages.databricks.com/rs/094-YMS-629/images/LearningSpark2.0.pdf)

* [Zaharia's dissertation](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2014/EECS-2014-12.pdf)

### 4. Theoretical stuff
*(Personally, I find this really interesting and difficult and elaborate; I don't think watching/reading this is required, but who knows, maybe it'll come up in an interview)*

* primer for category theory - [video](https://www.youtube.com/watch?v=Ss149MsZluI&t=2856s)

* functional paradigms - [video](https://www.youtube.com/watch?v=L0aYcq1tqMo)

* why would you do this to yourself/why functional programming is useful  - [video](https://www.youtube.com/watch?v=m40YOZr1nxQ&t=1728s)

* mathematical definitions of these concepts/how a person with more math than me might think about their code - [blog](https://typista.org/categories-in-dotty/)

### 5. Don't's

* I don't recommend the Scala sequence on Coursera. They took a high caliber university course tailored for advanced CS majors and threw it up as a MOOC. It's very pedantic, very theoretical, and there are no facilities for getting help since the homeworks are the exact opposite of theoretical. Roughly equivalent to "let's learn about fluid dynamics and aerodynamic design of large bodies; now go fly a Boeing 737 MAX"

* same goes for the edX, even if you pay for the certificate

* don't watch any of Odersky's videos or read any of his papers. He is a genius, but he is an awful lecturer. It's very discouraging

### 6. Community

* I don't do enough of this, but I highly recommend joining the [Gitter channel for Scala](https://gitter.im/scala/scala). People are generally very helpful, aren't rude, and even if you just scroll through the messages, it's a fantastic way to see how Scala code lives in the wild

* there is a DC meetup for Scala; haven't done any of the events