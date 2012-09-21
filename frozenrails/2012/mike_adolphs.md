# Frozenrails

Quotes or merged quotes are highlighted **strongly**, comments made by myself *italic*

## 2012-09-20

### *What is a developer?* - [Jeff Casimir](https://twitter.com/j3), [Jumpstart Lab](http://jumpstartlab.com/)

#### Topics

* It's easy to look out for people who are like you
* Developer communities are mostly a monoculture
  * white, male, middle-class
* **Thank you for building the world, white man.**
* Being a developer is
  * profitable
  * great life
* Becoming a developer is
  * hard
  * scary
* We excel in building tools for people like us
* Fix the issue of
  * gender
  * race
  * class
* *Slight topic change:* Education
* **Understanding by design** (UBD)
* **ReadMe Driven Development** is beautiful
* Break down problems into fractals
* Analogy to Tennis: **How to become a Top 50 Women Tennis player?**
  * Break it down what to do:
    * Play faster
    * Smash harder
    * Become tougher
  * Playing more Tennis only won't get the job done
* **You can't just do more programming to become a good developer**
* *Coming back to developers*: .split example
  * Various levels of proficiency for using .split
    * Needs documentation
    * Can do white-space delimited split
    * Can do any character delimited split
    * Can do any character delimited split and limit
* **Let's write down the skills for being a great developer**
* Sets to evaluate candidates: Jumpstart S12
* Use those sets to
  * guide apprentices
  * categorize learning resources
  * build a stronger community
* **Are you in?** Then please help. If you're not do so as well.

#### Techniques

* no images, only text
* two rows, two colors
* *is this Comic Sans? No, but pretty close…*

### *Mind your metaphors* - [Amanda Wagener](https://twitter.com/a_wagener)

#### Topics

* Metaphors
  * The benefits
    * Make things easier
    * Simplify communicating with people
  * The dangers
    * Somehow shorthanded
    * Simplifies too much
    * Often includes unwanted dependencies
* An example:
  * Sprints should better be called strawls
  * *no more examples?*
* **Think about the metaphors you're using!**

#### Techniques

* Mostly text, centered
* Website/Wikipedia excerpt
* A couple quotes
* Images, full screen

### *ZeroMQ: Scriptable sockets* - [Lourens Naude](https://twitter.com/methodmissing)
Slides available on [Speakerdeck](https://speakerdeck.com/u/methodmissing/p/zeromq-sockets-on-steroids-1)

#### Topics

* Why?
  * Because even in 2012 it's still too expensive to maintain integration points
* Socket I/O problems:
  * Strong developer profile required
  * Lack of portability
* What's a ZeroMQ socket?
  * Super (scriptable) socket
  * Asynchronous connect
  * Socket types:
    * Request <-> Reply
    * Push <-> Subscribe
    * Push <-> Pull (Pipeline)
* *pretty fast, can't keep up taking notes. He mainly shows ZeroMQ features*
* *Code dive with Ruby bindings on socket creation and more. Sorry, the pace left me stranded.*

#### Techniques

* Mostly text, lots of diagrams
* No colorized source code

### *Designing Hypermedia APIs*, [Steve Klabnik](https://twitter.com/steveklabnik)

#### Topics

* Most people think short-term
* Flexibility and stability needs to be balanced the right way
* Adapters
  * fog as middleware
* **Something's coupled when it breaks if you change it**
* Solution: **Radical decoupling**
  * Media type as the backbone of decoupling
  * *Example with microblogging JSON*
* **REST Fans call this 'independent evolution'**
* Server and client software can evolve apart from the media type
* Examples:
  * GitHub pagination `"rel":"next"`
  * ID->URI
* More information on [Designing Hypermedia APIs](http://designinghypermediaapis.com)

#### Techniques

* Header/Content separation
* Couple diagrams, almost no colorized code
* Pretty neat though

### *Fighting code smells* - Ruby code analysis tools, [Dennis Ushakov](http://twitter.com/en_Dal)

#### Topics

* **Pareto principle** (20% new code, 80% modifications)
* Code that smells:
  * Runtime errors/warnings
  * Dead code
  * Copy/paste'd code
  * Complex method bodies
  * Code style violations
  * Framework pattern violations
* Code quality tools:
  * Static tools
    * inspect code without launching
    * 100% no side effects, but hard to implement and not Rails compliant
    * Existing tools: Reek, flog, flay, Roodi, metrics_fu
    * Metrics foo provides aggregate resulrs for flay, flog, reek, roodi
  * Runtime tools
    * Inspect code by launching
    * Cope well with DSL magic
    * may have side effects
    * Existing tools:
      * Code testing:
        * Test::Unit
        * rspec/Cucumber
      * Code coverage
        * rcov, simplecov
        * heckle
        * RubyMine
* Morale: **Use static analysis tools, test and try RubyMine**

#### Techniques

* *The usual suspects* **and CAT CONTENT (only on last slide though)!**

### The tale of a server infrastructure, [Ville Lautanala](http://twitter.com/lautis)

#### Topics

* *quiet guy, can hardly understand what's going on*
* Explaining server infrastructure issues by example of [flowdock](https://flowdock.com/)
* *showing off various application layer diagrams of how their infrastructure evolved*
* Chef at Flowdock:
  * Used for:
    * Firewall
    * User setup/SSH key roll-out
    * *and more*
  * *couple knife command examples*
  * Testing chef recipes
    * Use environments to isolate changes
    * use temporary VMs
    * cucumber-chef gem
    * *no information about [test-kitchen](http://github.com/opscode/test-kitchen)? :(*
* Zookeeper is being used for distributed coordination
  * eg. for **redis failover**
* Chef vs. Zookeeper
  * Chef is for bootstrapping and configuration files
  * Zookeeper for automatic failover
* Mesh-based VPN between boxes
* SSL endpoints in AWS
* Learnings
  * Make it crash when someone's there to fix it
  * *and probably more, but I wasn't able to understand what he's saying :(*

#### Techniques

* Simple background, few words
* Colored diagrams, colorized source code
* Internet meme pictures (yay!)

### Off the tracks, [Nick Sutterer](https://twitter.com/apotonick)

#### Topics

* *Off the tracks literally: Nick begins his talk with telling a story and Elton John in the back*
* Nick wants more object orientation in Rails
* Example: A model with having a send_sms method in the user model
* **"Fat model, skinny controller"**
* *I think the morale is: Don't be afraid of making use of more classes, right? Right.*
* *Pretty lengthy example. Unable to follow since the talk's pretty weird, I'm sorry.*

#### Techniques

* Music, campfire on screen
* Mostly Google Image search images

### Post-Rails? Composable apps with a first-class API, [Brandur Leach](https://brandur.org)

#### Topics

* Keep your core application small and agile
* `BUTC` (Break up the core) is a learning from Salesforce splitting their Perl monolith into smaller pieces
* Split huge rails apps into smaller ones
* Let them talk via APIs to each other
* Examples from Heroku
  * Dashboard
  * Manager (Manager Web -> Manager API -> Core API)
* Take care of reusability
* **A good API is a reusable API**
* Favour Service Orientied Architecture (SOA) to ease the scaling pain
* APIs are important at least as the corresponding web application
* Benefits
  * More people are able to maintain different parts of the platform
  * Maintenance is easier, implementation of new features as well (Increasing happiness)
* **Lessons learned:**
  * Testing becomes harder, more stubs needed
  * Yehuda Katz's [artifice](http://rubygems.org/gems/artifice) or [excon-artifice](http://rubygems.org/gems/artifice-excon) for routing requests to a Rack application

#### Techniques

* First `impress.js` talk this year :)

### Deploy, scale and sleep at night with JRuby, [Joe Kutner](https://twitter.com/codefinger)

Slides on [Slideshare](http://www.slideshare.net/jkutner/deploy-scale-and-sleep-at-night-with-jruby)

#### Topics

* *He's the writer of 'Deploying with JRuby'*
* **Sysadmin is the worst job in the industry**
* Deploying to a JVM is about making life for sysadmins easier
* The current application infrastructure is cumbersome to scale
* **Passenger or Unicorn are not solving the underlying problem they just ease the pain.**
* It comes down to: Ruby Thread -> [GIL](http://en.wikipedia.org/wiki/Global_Interpreter_Lock) -> Kernel Thread
* **Steve Klabnik: 'Will Ruby ever get rid of GIL?', Matz: 'No' at RubyConf last year**
* Deploying to a JVM solves the problem
  * No thread managing anymore, only processes
* *showing benchmarks from [TorqueBox](http://torquebox.org/)*
* To know what needs to be changed in order to use JRuby use the [jruby-lint](https://github.com/jruby/jruby-lint) gem
* Various JVM solutions
  * [Warbler](http://kenai.com/projects/warbler/pages/Home)
    * Advantages
      * Creates warfile which then can be served by Tomcat/Jetty/WebLogic/JBoss
      * Warfiles can be signed
      * Deployment is fast
      * Makes `bundle install` obsolete
    * Disadvantages
      * Need to generate a warfile for each change
  * [Triniad](http://rubygems.org/gems/trinidad) (lightweight Ruby webserver)
    * Runs RoR application in an embedded Apache Tomcat container
    * Deployment still capistrano based
    * Brings a couple of extensions like a job scheduler (Quartz), worker (Resque) with it
  * [TorqueBox](http://torquebox.org)
    * `torquebox run`, then `torquebox deploy`
    * **The real power of torquebox comes from its subsystems**
    * Includes clustering, load-balancing and high availability out-of-the-box
  * A couple other solutions: Mizuno, Puma, torquebox-lite
  * Cloud companies provide a wide range of solutions
* Morale: *read his [book](http://pragprog.com/book/jkdepj/deploying-with-jruby)* and use `JRubyFrozenKutner` for a discount

#### Techniques

* White slides, lego images
* nice introduction

### Sleep!, [Alex Koppel]()

*got replaces with a surprise talk by Jeff Casimir, but somehow missed the talk :(*

### Advanched caching in Rails, [Adam Hawkins](https://twitter.com/adman65)

Slides available on [Speakerdeck](https://speakerdeck.com/u/twinturbo/p/advance)

#### Topics

* Based on experience while building an ERP at Radium
* Showing various Rack methods and their actions on the HTTP header
* Presenting various methods of caching
  * HTTP caching in Rails
    * Should be used pretty much everywhere
  * Action caching `caches_action`
  * Fragment caching
    * Should be used for HTML
  * Rails.cache
    * Should be used for arbitrary computations
* Cache expiration techniques
  * Dependency graphs
    * **The most complex thing that could possibly work**
  * Manual expiration
    * **Waste of time, don't do it**
  * Auto-expiring keys
    * **The eastiest thing that could possibly work**
  * **Russian Doll Caching**
    * **Cache one thing that caches another**
    * Comes with Rails 4
  * JSON APIs with ActiveModel::Serializers
* Wrap-up
  * Use HTTP caching everywhere
  * Use auto-expiring keys everywhere
  * Don't use sweepers, page or action caching
  * Beware of things that happen outside the HTTP Request

#### Techniques

* Simple slides, but pretty
* Short comic video, Stallman analogy
* nice pace

### Sponsored talk by Deveo, [Jerry Jaeppinen](http://www.deveo.com/)

#### Topics

* Talking about best practices and lessons learned during development within the last year
* *no sales show, nice!*
* Deveo has been built with Rails and Sinatra
* Use JS for frontend
* *Some neat javascript foo for changing the URL, woot!*

#### Techniques

* Simple slides, two columns

### I know Kung Fu! (Neo4j on Rails without JRuby), [Rogelio J. Samour](https://twitter.com/therubymug)

#### Topics

* Graph database explanation and differentiation to more popular database types
* Showing the advantages of graph databases by example of relationships
* Graph databases focus on the relationship of data, not the actual result set
* *neat Matrix example to explain graphs*
* Rails implementation
  * For JRuby: `Neo4j.rb gem`
  * Rubygems that wrap the Neo4J REST API:
    * Neography
    * Architect4r
    * [Keymaker](https://github.com/therubymug/keymaker)

#### Techniques

* Simple, clean slides
* Nice diagrams

### Hungry Academy: Learning to be a developer in five months, [Melanie Gilman](https://twitter.com/melanieeeg) & [Mary Cutrali](https://twitter.com/marycutrali)

#### Topics

* Steps at [Hungry Academy](http://hungryacademy.com/)
  * Week 1-2: Ruby introduction
  * Week 3-4: Ruby systems (testing with rspec), Project: 'Sales engine'
  * Week 5-7: Ruby essentials (discovered twitter-bootstrap)
  * Week 8-9: Rails under load, Project: 'Son of Store Engine'
  * Week 10-12: Providing and consuming APIs, Project: 'Feed Engine'
  * Week 13-15: Coordinating services, Project: 'Chat'
  * Week 16-18: ? *Lost focus, talk was too entertaining*
  * Week 19-21: 'Donor Choose' aka VC funding simulation (?)
* Almost all apps got hosted on heroku
* Mary's [GitHub profile](https://github.com/maryelizbeth) and Melanie's [GitHub profile](https://github.com/mrgilman)
* Melanie's [`omniauth-tripit`](https://rubygems.org/gems/omniauth-tripit) gem
* All their Hungry Academy projects available in this [gist](https://gist.github.com/3717847)

#### Techniques

* Fullscreen images, screenshots
* Very entertaining

### Γυβψ community, [Danish Khan](https://github.com/danishkhan)

#### Topics

* Title change: **Don't be an a\*\*hole!**
* Talking about Ruby/Rails community pros and cons
* Politeness, respectfulness and being kind is the currency of Open Source
* Get rid of things like [http://rubydramas.com/](http://rubydramas.com/), spend your energy in a more positive way
* If you're a project maintainer **maintain** your project. If you're not able to, don't be a maintainer and find another
* Spend efforts also on documentation, provide examples
* Act as a mentor if possible
* * **The one exclusive sign of thorough knowledge is the power of teaching** - Aristoteles
* **Respect each other, be nice to people**
* **Always have a README and a CONTRIBUTING file!**
* Make use of GitHub issue labels to define the needed skill level to fix the issue
* Don't just complain, send a pull request
* **Don't fight fire with fire!**

#### Techniques

* Fullscreen images, small Flickr badge with the user's name
  * *awesome way to give credit to flickr users!*
* Nyan-Octocat mutant!

### How to be a more productive developer, [Jeremy Walker](https://twitter.com/iHiD)

#### Topics

* **Developers tend to share traits**
* **Let's talk about me!** - *funny guy*
* Jeremy uses [gitshots](http://coderwall.com/p/xlatfq) and isn't proud of his photos at 4:30am
* **Make sure that you don't work too hard**
* **Creativity is a crucially important part of the job**
* "What gets me out of bed", Jeremy asks
  * Money? **Nope**
  * Career progression? **Nope**
  * Writing software? **Yes**
  * Learn something? **Yes**
  * Achieving something? **Yes**
  * Making the world better? **Yes**
* **Being good under pressure doesn not mean being under pressure is good**
* Highest quality productivity tip: **Turn off the Internet**
* What to do during your tests run
  * Get shit done. Over your entire career you might spend 2 full years of waiting for test results
* **Live a healthy life**

#### Techniques

* Single line, mostly quotes
* Funny slides, this guy's hilarious

### Rescuing Resque, [Terence Lee](https://twitter.com/hone02)

#### Topics

* What's Resque
  * Basically a job queue library
* Resque 1.x only gets bugfixes
* Resque 2 is being developed almost fulltime
  * Contributors very welcome
* *Presentation contained a lot of code examples, therefore hard to describe.*

#### Techniques

* A lot of code, well presented
* Finally source code covered in colors

### Therapeutic Refactoring, [Katrina Owen](https://twitter.com/kytrinyx)

And the [full talk](http://confreaks.com/videos/1071-cascadiaruby2012-therapeutic-refactoring)  (on the big screen)  
Code samples on [GitHub](https://github.com/kytrinyx/therapeutic-refactoring)

#### Topics

* *I've seen this talk already at Nordic Ruby 2012 and I enjoyed it a lot*
* **Guilt driven development**
* **More refactoring is an optimization.**
* **Refactoring is not rehacktoring!**
* Katrina shows by lots of lines of well structured code how to refactor a non documented, quite complex method 
* *Best see it for yourself when you get the chance*
* **Replace method with method object**
* Don't name methods by how things get done
* For a start copy existing code into new methods and scan for local variables
* **First quarantine the method, than extract stuff and/or delete it**
* Codejunk Top 10
  * Bad comments
  * Trailing whitespace
  * Commented-out code
  * Needless parantheses
  * Powerless code
  * Unnecessary `require`'s
  * The booleanest boolean
  * Too much hard work
  * Duplicated tests
  * Combine all the codejunk
* **Happiness leads to good design**

#### Techniques

* Clean slides, mostly white
* Lots of code, well structured and highlighted
* Internet meme pictures, yay!

### When not to use object-oriented techniques, [Mike Burns](https://twitter.com/mikeburns)

#### Topics

* Showing various programming paradigms
  * Aspect-oriented programming
    * facets gem
    * Conecpt was conceived by [Karl Lieberherr](http://en.wikipedia.org/wiki/Karl_Lieberherr)
  * Functional programming
    * Focusing behavior of something
    * Filter and operate on structures of data
    * Add new behavior to a static set of data
  * Structured programming
    * Use language keywords to define the structure of your program
*I'm sorry, but that's too much theory for me to keep up at the end of the day*
* Wrap-up: When to use OOP
  * Quickly add new data
  * Encapsulate state
  * Simplify conditionals
  * *(?)*
* 20% discount for [learn.thoughtbot.com](http://learn.thoughtbot.com/): FROZENRAILS

#### Techniques

* Lots of code, simple slides
* Nice presentation style, live example **on Linux!**

### Keynote: Y-NOT, Adventures in functional programming, [Jim Weirich](http://twitter.com/jimweirich)

#### Topics

* Talk's highly technical, extremely pointless and contains the worst ruby code ever
* But it'll be fun, he says. *I've seen enough Weirich to see where this is going…*
* *OMG.*

#### Techniques

* Emacs.

EOF