# Frozenrails

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
* Sets to evaluate candidates: Jumpstart S12/Thoughtbot S0912
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
* It comes down to: Ruby Thread -> GIL -> Kernel Thread
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

### I know Kung Fu! (Neo4j on Rails without JRuby), [Rogelio J. Samour]()

#### Topics

* asdf

#### Techniques

* asdf

### Hungry Academy: Learning to be a developer in five months

#### Topics

* asdf

#### Techniques

* asdf

### Γυβψ community, [Danish Khan]()

#### Topics

* asdf

#### Techniques

* asdf

### How to be a more productive developer, [Jeremy Walker]()

#### Topics

* asdf

#### Techniques

* asdf

### Rescuing Resque, [Terence Lee]()

#### Topics

* asdf

#### Techniques

* asdf

### Therapeutic Refactoring, [Katrina Owen]()

#### Topics

* asdf

#### Techniques

* asdf

### When not to use object-oriented techniques, [Mike Burns]()

#### Topics

* asdf

#### Techniques

* asdf


### Keynote: Y-NOT, Adventures in functional programming, [Jim Weirich]()

#### Topics

* asdf

#### Techniques

* asdf

EOF