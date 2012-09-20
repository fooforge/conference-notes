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

### Off the tracks, [Nick Sutterer](url)

#### Topics

* 

#### Techniques

* 

### next_talk, [next_speaker](url)
