# Paul Campbell
## Ruby Ireland
### 23rd September 2014

---

# W-w-w-who?

^ Long time Rubyist
Last Ruby Ireland talk was 30th August 2011, 3 years ago, on Rails 3.1

---

# @paulca

^ Twitter and GitHub

---

# paul@tito.io

^ Anything I can do to help, just let me know

---

# Tito
## https://ti.to

^ Irish, not Tonganese!
The smoothest, slickest event registration platform on the planet.
Tell your friends!

---

# Úll
## http://ull.ie

^ Irish for Apple.
A conference about great products.
Next March. Add your email.

---

# RubyMotion

## A Bit of Background

^ Laurent Sansonetti
MacRuby
HipByte ... self-funded, bootstrapped company
left Apple, presumably because of Swift

---

# What is RubyMotion?

^ * Ruby, but Native
* LLVM
* Objective-C Runtime
* iOS
* OSX
* (beta) Android

---

# What does it look like?

---

# Ruby

---

# What does it act like?

---

# Ruby

---

# What does it feel like?

---

# Ruby

---

# But it's a web view, right?

---

# No

---

# Is it native?

---

# Yes

---

# But not proper native?

---

# Yes

---

# But Ruby is for web development, right?

---

# NO!

---

# But it's some kind of bridge, right?

---

# No

---

# But it’s slow, right?

---

# No

---

# But it’s cheating!

---

# YES!

---

# HOW MUCH?

---

# €99

---

# €99 (once off)

---

# €99 (once off)
## (plus another €99 per year for your Apple Developer Membership)

---

# But WHHHHHHHYYYYYYYYY?

^ Ruby is designed for programmer happiness and productivity. That hasn't changed.

---

```objectivec
//
//  ViewController.h
//  Yarrr
//
//  Created by Paul Campbell on 22/09/2014.
//  Copyright (c) 2014 Paul Campbell. All rights reserved.
//

#import <UIKit/UIKit.h>

@interface ViewController : UIViewController


@end


```

^ this is what Xcode starts you off with

---

```objectivec
//
//  ViewController.m
//  Yarrr
//
//  Created by Paul Campbell on 22/09/2014.
//  Copyright (c) 2014 Paul Campbell. All rights reserved.
//

#import "ViewController.h"

@interface ViewController ()

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
}

@end
```

^ That was just the header. Here's the implementation. I find it Objectionable!

---

# What about Swift?

^ It's not Ruby
Swift will never really do Android
It's almost like for like ... the beauty is the LLVM
Swift, Objective-C, Ruby ... all interchangeable

---

```swift
//
//  ViewController.swift
//  SwiftYarr
//
//  Created by Paul Campbell on 23/09/2014.
//  Copyright (c) 2014 Paul Campbell. All rights reserved.
//

import UIKit

class ViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }


}


```

^ Swift is super nice, but it's a bit like CoffeeScript and JavaScript
Ruby is a _very_ nice language!

--- 

# Can you make real apps?

---

# Yup.

---

![inline](https://dl.dropboxusercontent.com/s/uv9pu8hgaqx69k7/2014-09-23%20at%2002.00%202x%20%281%29.png?dl=0)

---

![inline](https://dl.dropboxusercontent.com/s/b4hcgavjpypijs1/2014-09-23%20at%2002.01%202x.png?dl=0)

---

![inline](https://dl.dropboxusercontent.com/s/enxrfy2x0vclyxi/2014-09-23%20at%2002.02%202x.png?dl=0)

--- 

# LET'S MAKE A THING!

---

# Ruby Ireland Schedule

---

```
$ motion create ruby-ireland-schedule-app
    Create ruby-ireland-schedule-app
    Create ruby-ireland-schedule-app/.gitignore
    Create ruby-ireland-schedule-app/app/app_delegate.rb
    Create ruby-ireland-schedule-app/Gemfile
    Create ruby-ireland-schedule-app/Rakefile
    Create ruby-ireland-schedule-app/resources/Default-568h@2x.png
    Create ruby-ireland-schedule-app/spec/main_spec.rb
```

---



```
$ cd ruby-ireland-schedule-app
$ rake
     Build ./build/iPhoneSimulator-8.0-Development
   Compile ./app/app_delegate.rb
    Create ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app
      Link ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app/ruby-ireland-schedule-app
    Create ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app/PkgInfo
    Create ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app/Info.plist
      Copy ./resources/Default-568h@2x.png
    Create ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.dSYM
  Simulate ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app
(nil)?  
```

---

# Whoops!

![inline](http://dl.dropboxusercontent.com/s/u7drhxc6dnsk9a2/2014-09-22%20at%2021.10%202x.png)

---

# Directory Structure

```
$ ls -1 *
Gemfile
Gemfile.lock
Rakefile

app:
app_delegate.rb

build:
iPhoneSimulator-8.0-Development

resources:
Default-568h@2x.png

spec:
main_spec.rb
```

---

# app/app_delegate.rb

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    true
  end
end

```

---

# app/app_delegate.rb

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    alert = UIAlertView.new
    alert.message = "Hello World!"
    alert.show
    true
  end
end
```

^ This is from the RubyMotion Tutorial

---

```
$ rake
     Build ./build/iPhoneSimulator-8.0-Development
   Compile ./app/app_delegate.rb
      Link ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app/ruby-ireland-schedule-app
    Create ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app/Info.plist
    Create ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.dSYM
  Simulate ./build/iPhoneSimulator-8.0-Development/ruby-ireland-schedule-app.app
(nil)?
```

---

# WHOOPS!

![inline](http://dl.dropboxusercontent.com/s/8m3g1aiopsl4mr5/2014-09-22%20at%2021.32%202x.png)

^ So, we have an alert. But let's make this nicer.

---

![inline](https://dl.dropboxusercontent.com/s/8q1el78us9wg8mj/2014-09-22%20at%2021.39%202x.png?dl=0)

---

# Gemfile

```
source 'https://rubygems.org'

gem 'rake'
# Add your dependencies here:

gem 'bubble-wrap', '~> 1.7.1'

```

^ BubbleWrap is awesome. Tons of helpers.

---

# app/app_delegate.rb

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    alert = UIAlertView.new
    alert.message = "Hello World!"
    alert.show
    true
  end
end
```

^ This is our very first Hello World app.
UIAlertView is a native app component.
You'll need to get used to Cocoa native components.

---

# app/app_delegate.rb

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    App.alert('Hello Ruby Ireland!')
    true
  end
end
```

^ RubyMotion contains lots of helpers.
This is an example of taking 3 lines and making it 1 line.
Loads of other helpers

---

![inline](https://dl.dropboxusercontent.com/s/rrbakyf4x23efe2/2014-09-22%20at%2021.44%202x.png?dl=0)

^ Here's what it looks like!
Let's do more than Hello World

---

# app/home\_view\_controller.rb

```ruby
class HomeViewController < UIViewController

  def loadView
    self.view = UIImageView.alloc.init
  end

  def viewDidLoad
    image = UIImage.imageNamed('belfast-ruby.png')
    view.image = image
  end
end
```

^ Again, we're using lots of Cocoa elements, and Cocoa callbacks.
RubyMotion and its helpers are gateways into the Cocoa world

---

# app/app_delegate.rb

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    @window = UIWindow.alloc.initWithFrame(UIScreen.mainScreen.bounds)
    @window.rootViewController = HomeViewController.alloc.init
    @window.rootViewController.wantsFullScreenLayout = true
    @window.makeKeyAndVisible
    true
  end
end

```

^ This is the standard way to initialize a fullscreen view on iOS

---

# WHOOPS!

![inline](https://dl.dropboxusercontent.com/s/zxfsylrkevxsc07/2014-09-22%20at%2021.59%202x.png?dl=0)

^ Yay!
But it's Ruby! Isn't there a neater way?
Yes!

---

# Motion Kit

![inline](https://dl.dropboxusercontent.com/s/pobex7bspqgiyee/2014-09-22%20at%2022.00%202x%20%281%29.png?dl=0)

^ Motion Kit, is like CSS for RubyMotion, lets you separate style from view

---

# Gemfile

```
source 'https://rubygems.org'

gem 'rake'
# Add your dependencies here:

gem "bubble-wrap", "~> 1.7.1"
gem 'motion-kit'
```

^ Add motion-kit to your Gemfile

---

# app/home\_view\_controller.rb

```ruby
class HomeViewController < UIViewController

  def loadView
    self.view = UIImageView.alloc.init
  end

  def viewDidLoad
    image = UIImage.imageNamed('belfast-ruby.png')
    view.image = image
  end
end
```

^ I used Belfast Ruby because Ruby Ireland doesn't have a logo anymore
Instead of this...

---

# app/home\_view\_controller.rb

```ruby
class HomeViewController < UIViewController

  def loadView
    @layout = HomeScreenLayout.new
    self.view = @layout.view
  end

end
```

^ ...we create a layout ... the layout is now responsible for arranging elements on the screen

---

# app/layouts/home\_screen\_layout.rb

```ruby
class HomeScreenLayout < MotionKit::Layout
  
end
```

^ create the layout...

---

# app/layouts/home\_screen\_layout.rb

```ruby
class HomeScreenLayout < MotionKit::Layout
  def layout
    
  end
end
```

^ add the layout method

---

# app/layouts/home\_screen\_layout.rb

```ruby
class HomeScreenLayout < MotionKit::Layout
  def layout
    add UIImageView, :logo
  end
end
```

^ ...add our UIImageView back

---

# app/layouts/home\_screen\_layout.rb

```ruby
class HomeScreenLayout < MotionKit::Layout
  def layout
    add UIImageView, :logo
  end

  def logo_style
    top 0
    left 0
    width '100%'
    height '100%'
    image UIImage.imageNamed('belfast-ruby')
  end
end
```

^ Use this CSS-like syntax, that interacts with Cocoa's frame layout API.
'belfast-ruby' is a .png in the resources/ folder

---

![inline](https://dl.dropboxusercontent.com/s/44i3cbmygv94mf9/2014-09-22%20at%2022.15%202x.png?dl=0)

^ ... and we get something very similar, but we've separated out our layout
Let's tidy it up.

---

# app/layouts/home\_screen\_layout.rb

```ruby
class HomeScreenLayout < MotionKit::Layout
  def layout
    add UIImageView, :logo
  end

  def logo_style
    top 0
    left 0
    width '289'
    height '234'
    image UIImage.imageNamed('belfast-ruby')
  end
end
```

^ we'll edit the dimensions of the image

---

# app/layouts/home\_screen\_layout.rb

```ruby
class HomeScreenLayout < MotionKit::Layout
  def layout
    root :home_screen_view do
      add UIImageView, :logo
    end
  end

  def logo_style
    top 0
    left 0
    width '289'
    height '234'
    image UIImage.imageNamed('belfast-ruby')
  end
end
```

^ and add a root view so that we can style the root view

---

# app/layouts/home\_screen\_layout.rb

```ruby
class HomeScreenLayout < MotionKit::Layout
  def layout
    root :home_screen_view do
      add UIImageView, :logo
    end
  end

  def home_screen_view_style
    background_color UIColor.whiteColor
  end

  def logo_style
    top 0
    left 0
    width '289'
    height '234'
    image UIImage.imageNamed('belfast-ruby')
  end
end
```

^ set the background color to white

---

![inline](https://dl.dropboxusercontent.com/s/drojrbvauiq2gpb/2014-09-22%20at%2022.24%202x.png?dl=0)

^ And it's looking a bit better, but let's center it up. For that we'll use Auto-Layout

---

```ruby
def logo_style
  top 0
  left 0
  width '289'
  height '234'
  image UIImage.imageNamed('belfast-ruby')
end
```

^ a bit about auto-layout ... it's like responsive design for Cocoa. Very powerful, very complicated, very confusing.

---

```ruby
def logo_style
  image UIImage.imageNamed('belfast-ruby')

  constraints do
    width.equals(289)
    height.equals(234)

    center.equals(:superview)
  end
end
```

^ Auto Layout is all about constraints, which are rules relative to other elements on the screen.

---

![inline](https://dl.dropboxusercontent.com/s/5pdb9coq386rf9l/2014-09-22%20at%2022.36%202x.png?dl=0)

^ And now we have our first not-shit version.
Let's add a label

---

# Dum, de, dum
## app/layotus/home\_screen\_layout.rb

```ruby
def layout
  ...
  add UILabel, :not
end
```

```ruby
def not_style
  text 'NOT!'
  color NSColor.whiteColor
  text_alignment NSTextAlignmentCenter
  constraints do
    width.equals(:logo)
    height 50
    top_left.equals(:logo)
  end
end
```

^ in our layout file, we add a label, with the same width and position as the logo, height of 50px

---

# Doo, de, doo

```ruby
class HomeScreenLayout < MotionKit::Layout
  view :lets_go_button
...
```

```ruby
def layout
  ...
  @lets_go_button = add UIButton, :lets_go_button
  ...
end
```

```ruby
...
def lets_go_button_style
  title 'Let’s Go!'
  title_color NSColor.blackColor
  constraints do
    width.equals(:superview)
    top.equals(:logo, :bottom)
    bottom.equals(:superview)
  end
end
...
```

^ Aaand we add a button, using the view method which is basically a fancy accessor.

---

# Whoopsie daisy!

![inline](https://dl.dropboxusercontent.com/s/hj33tkw9qdhmtke/2014-09-22%20at%2022.56%202x.png?dl=0)

^ And here's our layout, with a label and a button. We can do loads more if we want with frames and touch states etc. But for now this is good.

--- 

# app/home\_view\_controller.rb

```ruby
class HomeViewController < UIViewController

  def loadView
    @layout = HomeScreenLayout.new
    self.view = @layout.view
    @layout.build
  end

end
```

^ meanwhile back in our view controller, let's add some actions.

--- 

# app/home_view_controller.rb

```ruby
class HomeViewController < UIViewController

  def loadView
    @layout = HomeScreenLayout.new
    self.view = @layout.view
    @layout.build
  end

  def viewDidLoad
    @button = @layout.get(:lets_go_button)
    @button.when_tapped { open_meetups_list }
  end

  def open_meetups_list
    App.alert("What meetups?")
  end

end
```

^ the when_tapped is from BubbleWrap ... and we pass in a block for the action we want to take.

---

# OH NO!

![inline](https://dl.dropboxusercontent.com/s/v3u264b18omthox/2014-09-22%20at%2023.07%202x.png?dl=0)

^ Ok, the button works!
But now we need to actually do something.

---

# A Web API

![inline](https://dl.dropboxusercontent.com/s/fpmjlpgdfqynhi6/2014-09-23%20at%2017.52%202x.png)

^ We have a simple API, but we'll need to talk to it (async preferably)

---

# AFMotion

![inline](https://dl.dropboxusercontent.com/s/u6vgoyzd9hfkeiy/2014-09-22%20at%2023.11%202x.png?dl=0)

^ it's a RubyMotion wrapper for AFNetworking

---

# AFNetworking

![inline](https://dl.dropboxusercontent.com/s/a226hc5fchoc4a6/2014-09-22%20at%2023.11%202x%20%281%29.png?dl=0)

^ A modern, advanced, Cocoa-based, async HTTP library.

---

# Gemfile

```
source 'https://rubygems.org'

gem 'rake'
# Add your dependencies here:

gem 'afmotion'
gem "bubble-wrap", "~> 1.7.1"
gem 'motion-kit'
```

^ Add AFMotion to your Gemfile. AFMotion uses Cocoapods!

---

# CocoaPods!

![inline](https://dl.dropboxusercontent.com/s/x1fn81h1e2y5936/2014-09-22%20at%2023.16%202x.png?dl=0)

^ Cocoapods is like Rubygems, but for cocoa!
RubyMotion has native support.

---

# rake pod:install

---

# app/controllers/home\_view\_controller.rb

```ruby
def open_meetups_list
  AFMotion::JSON.get('http://ruby-ireland-schedule-api.herokuapp.com/meetups.json') do |result|
    if result.success?
      App.alert("Meetups: #{result.object}")
    else
      App.alert("Whoops!")
    end
  end
end
```

^ Let's replace the `open_meetups_list` method

---

![inline](https://dl.dropboxusercontent.com/s/2h9ck6krzsbzivp/2014-09-22%20at%2023.16%202x%20%281%29.png?dl=0)

^ So, we have some JSON. What's next. A TableView!

---

# The UITableView Docs

![inline](https://dl.dropboxusercontent.com/s/lz2yr4m4n4jhy9n/2014-09-22%20at%2023.35%202x.png?dl=0)

^ The UITableView docs
Apple's documentation is AWESOME. Use it. A lot.

---

# Xcode

![inline](https://dl.dropboxusercontent.com/s/rfbur2cm7ntfcom/2014-09-22%20at%2023.36%202x.png?dl=0)

^ So, Xcode is a beast. A friendly beast, but a beast nonetheless.

---

# The Hillegass Book

![inline](https://dl.dropboxusercontent.com/s/xr5aon9jm82gg2o/2014-09-22%20at%2023.38%202x.png?dl=0)

---

# HOWEVER

---

# RUBY

^ What if... instead of ...

---

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    @window = UIWindow.alloc.initWithFrame(UIScreen.mainScreen.bounds)
    @window.rootViewController = HomeViewController.alloc.init
    @window.rootViewController.wantsFullScreenLayout = true
    @window.makeKeyAndVisible
    true
  end
end

```

^ we could do...

---

```ruby
class AppDelegate < PM::Delegate
  def on_load(app, options)
    open HomeScreen.new
  end
end
```

^ what if, instead of actually learning what we're doing, 
we could just write some ruby, and MAGIC happens
Well, we CAN!

---

# ProMotion

![inline](https://dl.dropboxusercontent.com/s/swzst1a9zf0gokf/2014-09-22%20at%2023.43%202x.png?dl=0)

^ the worst name for a gem ever

---

# Gemfile

```
source 'https://rubygems.org'

gem 'rake'
# Add your dependencies here:

gem 'afmotion'
gem "bubble-wrap", "~> 1.7.1"
gem 'motion-kit'
gem 'ProMotion'
```

^ 

---

# app/home\_view\_controller.rb

```ruby
class HomeViewController < UIViewController

  def loadView
    @layout = HomeScreenLayout.new
    self.view = @layout.view
    @layout.build
  end

  def viewDidLoad
    @button = @layout.get(:lets_go_button)
    @button.when_tapped { open_meetups_list }
  end

  def open_meetups_list
    AFMotion::JSON.get('http://ruby-ireland-schedule-api.herokuapp.com/meetups.json') do |result|
      if result.success?
        App.alert("Meetups: #{result.object}")
      else
        App.alert("Whoops!")
      end
    end
  end
end
```

^ Here's what our home\_view\_controller was. 

---

```
mv app/home_view_controller.rb app/screens/home_screen.rb
```

^ ProMotion refers to screens as top level items. (Screens are superclassed from UIViewController ... they're still view controllers, but MAGIC view controllers)

---

# app/screens/home_screen.rb

```ruby
class HomeScreen < PM::Screen

  def load_view
    @layout = HomeScreenLayout.new
    self.view = @layout.view
    @layout.build
  end

  def on_load
    @button = @layout.get(:lets_go_button)
    @button.when_tapped { open_meetups_list }
  end

  def open_meetups_list
    open MeetupListScreen.new(nav_bar: true)
  end

end
```

^ ProMotion replaces the default Cocoa delegate methods with it's own more Rubyish ones. I'm on the fence. I like camelCasing when I'm in CocoaLand.
Now we need our TableView

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen
end
```

^ Just inherit from PM::Screen.

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen
  title "Meetups"
end
```

^ ProMotion includes a TON of convenience methods.

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen
  title "Meetups"

  def on_load
    load_async
  end
end
```

^ Let's build up our view

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen
  title "Meetups"

  def on_load
    load_async
  end

  def load_async
    AFMotion::JSON.get('http://ruby-ireland-schedule-api.herokuapp.com/meetups.json') do |result|
      if result.success?
        @meetups = result.object
      else
        @meetups = []
      end

      update_table_data
    end
  end
end
```

^ We'll push the JSON into a load_async method to populate an instance var

---

```ruby
class MeetupListScreen < PM::TableScreen

  title "Meetups"

  ...

  def table_data
    if !@meetups
      [{
        cells: [
          { title: "Loading..."}
        ]
      }]
    end
  end

  ...

end
```

^ ...and display a loading message

---

# Weeeeeeee!

![inline](https://dl.dropboxusercontent.com/s/yqve80wpnmwulmf/2014-09-23%20at%2000.06%202x.png?dl=0)

^ Yay!

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  title "Meetups"

  ...

  def table_data
    if !@meetups
      [{
        cells: [
          { title: "Loading..."}
        ]
      }]
    elsif @meetups.length == 0
      [{
        cells: [
          { title: "No meetups"}
        ]
      }]
    end
  end

  ...

end
```

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  title "Meetups"

  ...

  def table_data
    if !@meetups
      [{
        cells: [
          { title: "Loading..."}
        ]
      }]
    elsif @meetups.length == 0
      [{
        cells: [
          { title: "No meetups"}
        ]
      }]
    else
      [{
        cells: @meetups.map do |meetup|
          {
            title: meetup['title'],
            subtitle: "#{meetup['time']}"
          }
        end
      }]
    end
  end

  ...

end
```

^ Getting a bit hairy, but's pretty simple

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  title "Meetups"

  def on_load
    load_async
  end

  def table_data
    if !@meetups
      [{
        cells: [
          { title: "Loading..."}
        ]
      }]
    elsif @meetups.length == 0
      [{
        cells: [
          { title: "No meetups"}
        ]
      }]
    else
      [{
        cells: @meetups.map do |meetup|
          {
            title: meetup['title'],
            subtitle: "#{meetup['time']}"
          }
        end
      }]
    end
  end

  def load_async
    AFMotion::JSON.get('http://ruby-ireland-schedule-api.herokuapp.com/meetups.json') do |result|
      if result.success?
        @meetups = result.object
      else
        @meetups = []
      end

      update_table_data
    end
  end

end
```


^ The full thing: long, but simple

---

![inline](https://dl.dropboxusercontent.com/s/2vz36eertpzyhs6/2014-09-23%20at%2000.08%202x.png?dl=0)

^ Ok, here's where we're at.
We have our homeview

---

![inline](https://dl.dropboxusercontent.com/s/yqve80wpnmwulmf/2014-09-23%20at%2000.06%202x.png?dl=0)

^ Our loading view.

---

![inline](https://dl.dropboxusercontent.com/s/s7up1nxj4q6x3m3/2014-09-23%20at%2000.09%202x.png?dl=0)

^ And once we've fetched our meetups, we have our list!
ProMotion: ton of helpers. Want to add pull to refresh?

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  refreshable
  title "Meetups"

  ...

  def load_async
    AFMotion::JSON.get('http://ruby-ireland-schedule-api.herokuapp.com/meetups.json') do |result|

      end_refreshing

      if result.success?
        @meetups = result.object
      else
        @meetups = []
      end

      update_table_data
    end
  end

end
```

^ super easy to add pull to refresh ... two simple lines

---

![inline](https://dl.dropboxusercontent.com/s/s7up1nxj4q6x3m3/2014-09-23%20at%2000.09%202x.png?dl=0)

^ content before

---

![inline](https://dl.dropboxusercontent.com/s/ueu7vgt45csnvb7/2014-09-23%20at%2000.17%202x.png?dl=0)

^ aaand pull to refresh

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  refreshable
  title "Meetups"

  def on_refresh
    load_async
  end

  def on_load
    load_async
  end

  def table_data
    if !@meetups
      [{
        cells: [
          { title: "Loading..."}
        ]
      }]
    elsif @meetups.length == 0
      [{
        cells: [
          { title: "No meetups"}
        ]
      }]
    else
      [{
        cells: @meetups.map do |meetup|
          {
            title: meetup['title'],
            subtitle: "#{meetup['time']}"
          }
        end
      }]
    end
  end

  def load_async
    AFMotion::JSON.get('http://ruby-ireland-schedule-api.herokuapp.com/meetups.json') do |result|

      end_refreshing

      if result.success?
        @meetups = result.object
      else
        @meetups = []
      end

      update_table_data
    end
  end

end
```

^ Ok, here's where our code is at.
But it's long. It also has an online dependency.
Can we do better?

---

# Dreamcode

```ruby
class MeetupListScreen < PM::TableScreen

  title "Meetups"

  def on_load
    load_async
  end

  def table_data
    Meetup.table_data
  end

  def load_async
    Meetup.load_async do
      update_table_data
    end
  end

end
```

^ what if it could look like this AND work offline?
In order to work offline we'll need persistence.

---

# CDQ

![inline](https://dl.dropboxusercontent.com/s/act4egv096dsjmz/2014-09-23%20at%2000.25%202x.png?dl=0)

^ A bit about core data

---

# Gemfile

```
source 'https://rubygems.org'

gem 'rake'
# Add your dependencies here:

gem 'afmotion'
gem "bubble-wrap", "~> 1.7.1"
gem 'cdq'
gem 'motion-kit'
gem 'ProMotion'
```

^ add cdq to Gemfile

---

```
$ cdq init

     Creating init: 

  Δ  Creating directory: schemas
  Δ  Creating file: /Users/paulcampbell/Sites/ruby-ireland-schedule/ruby-ireland-schedule-app/schemas/0001_initial.rb
  Δ  Creating directory: spec/helpers
  Δ  Creating file: /Users/paulcampbell/Sites/ruby-ireland-schedule/ruby-ireland-schedule-app/spec/helpers/cdq.rb

     Done
  Δ  Checking bundle for cdq... /Users/paulcampbell/.rbenv/versions/2.0.0-p247/lib/ruby/gems/2.0.0/gems/cdq-0.1.9
  Δ  Adding schema:build hook to Rakefile... Done.

  Now edit schemas/0001_initial.rb to define your schema, and you're off and running.
```

^ initilize cdq. This added a schema:build rake task to Rakefile

---

# schemas/0001_initial.rb

```ruby
schema "0001 initial" do

  entity 'Meetup' do
    integer32 :id
    string    :title
    string    :presenter_name
    datetime  :time
    string    :venue

    datetime  :created_at
    datetime  :updated_at
  end
end
```

^ add the initial schema

---

# app/models/meetup.rb

```ruby
class Meetup < CDQManagedObject
end
```

^ It's a little bit like ActiveRecord.
But you need to tell your app you're using it

---

# app/app_delegate.rb

```ruby
class AppDelegate < PM::Delegate
  include CDQ

  def on_load(app, options)
    cdq.setup
    open HomeScreen.new
  end
end
```

^ Add CDQ to your app delegate, and set it up

---

```ruby
(main)> meetup = Meetup.create(
  title: 'A CDQ Primer',
  presenter_name: 'Paul Campbell', 
  venue: 'Engine Yard',
  time: Time.now
)
=> <Meetup: 0xbc7bad0> (entity: Meetup;
  id: 0xbc2e320
  <x-coredata:///Meetup/tA21D4133-6825-4BBE-A82E-03332EE90F772> ; 
  data: {
    "created_at" = nil;
    "presenter_name" = "Paul Campbell";
    time = "2014-09-22 23:37:00 +0000";
    title = "A CDQ Primer";
    "updated_at" = nil;
    venue = "Engine Yard";
})
```

^ within the console

---

```ruby
(nil)? Meetup.all
=> #<CDQ::CDQTargetedQuery:0xbda30b0
@entity_description=#<NSEntityDescription:0xbde5500>
@target_class=Meetup
@context=nil
@predicate=nil
@limit=nil
@offset=nil
@sort_descriptors=[]
@saved_key=nil>
```

^ within the console

---

```ruby
(nil)? Meetup.where(title: 'A CDQ Primer')
=> #<CDQ::CDQTargetedQuery:0xbc8c290
@entity_description=#<NSEntityDescription:0xbde5500>
@target_class=Meetup
@context=nil
@predicate=#<NSComparisonPredicate:0xbc7f0c0>
@limit=nil
@offset=nil
@sort_descriptors=[]
@saved_key=nil>
```

^ queries ... don't over use, but great for filtering.

---

```ruby
Meetup.first
Meetup.last
Meetup.sort_by(:time).limit(5).offset(3)
...
```

* scopes
* iCloud

^ it's backed by SQLite by default

---

# cdq.save

^ don't forget to persist ... Core Data isn't an ORM.

---

# app/models/meetup.rb

```ruby
class Meetup
  def self.load_async(&block)
    AFMotion::JSON.get('http://ruby-ireland-schedule-api.herokuapp.com/meetups.json') do |result|

      if result.success?
        App.delegate.cdq.reset!
        result.object.each do |meetup_json|
          meetup_json.delete(:url)
          meetup_json['time'] = NSDate.dateWithNaturalLanguageString(
            meetup_json['time']
          )
          Meetup.create(meetup_json)
        end
        App.delegate.cdq.save
      end

      block.call
    end
  end
end
```

^ Let's push our loading to our model, and create objects

---

# app/models/meetup.rb

```ruby
class Meetup
  def self.table_data
    return [{cells: [{ title: "No meetups"}]}] if none?
    [{
      cells: all.map do |meetup|
        {
          title: meetup.title,
          subtitle: "#{meetup.time}"
        }
      end
    }]
  end

  ...
end
```

^ let's implement a master view ... using cdq to pull out meetups

---

![inline](https://dl.dropboxusercontent.com/s/ve8de22jixdh7tz/2014-09-23%20at%2001.03%202x.png?dl=0)

^ It looks exactly the same, our code is cleaner
Let's implement a detail view

---

# app/screens/meetup\_show\_screen.rb

```ruby
class MeetupShowScreen < PM::TableScreen

  title 'Meetup'

  attr_accessor :meetup

  def table_data
    meetup.table_data
  end

end
```

^ keep it simple. No need to look up ... we can pass around objects... the app shares state, core data and RubyMotoin manage memory

---

# app/models/meetup.rb

```ruby
class Meetup < CDQManagedObject
  def self.table_data
    return [{cells: [{ title: "No meetups"}]}] if none?
    [{
      cells: sort_by(:time, order: :desc).map do |meetup|
        {
          title: meetup.title,
          subtitle: "#{meetup.time}",
          action: :show_meetup,
          arguments: meetup
        }
      end
    }]
  end

  ...
end
```

^ Let's add some actions

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  title "Meetups"
  refreshable

  def on_load
    load_async unless Meetup.any?
  end

  ...
end
```

^ Modify our list screen to work offline.

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  ...

  def table_data
    if @loading
      [{
        cells: [
          { title: "Loading..."}
        ]
      }]
    else
      Meetup.table_data
    end
  end

  ...

end
```

^ add a loading state

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  ...

  def load_async
    @loading = true
    Meetup.load_async do
      @loading = false
      end_refreshing
      update_table_data
    end
  end

  def show_meetup(meetup)
    open MeetupShowScreen.new(nav_bar: true, meetup: meetup)
  end

end
```

^ and implement the rest of our view. we're passing the meetup along... and keeping track of loading. not quite dreamcode, but almost.

---

# app/screens/meetup\_list\_screen.rb

```ruby
class MeetupListScreen < PM::TableScreen

  title "Meetups"
  refreshable

  def on_load
    load_async unless Meetup.any?
  end

  def on_refresh
    load_async
  end

  def table_data
    if @loading
      [{
        cells: [
          { title: "Loading..."}
        ]
      }]
    else
      Meetup.table_data
    end
  end

  def load_async
    @loading = true
    Meetup.load_async do
      @loading = false
      end_refreshing
      update_table_data
    end
  end

  def show_meetup(meetup)
    open MeetupShowScreen.new(nav_bar: true, meetup: meetup)
  end

end
```

^ our final view.

---

![inline](https://dl.dropboxusercontent.com/s/cfmz17sxj2wwkuz/2014-09-23%20at%2001.26%202x.png?dl=0)

^ the detail view.

---

# DEMO

---

# That's it! Yay!

---

# MORE STUFF

---

# Interface Builder

### https://github.com/rubymotion/ib

^ You can use Interface Builder, using the ib GEM
A lot of the Cocoa books and Apple samples teach IB, so it's really useful, particularly for OS X

---

# Samples

#### https://github.com/HipByte/RubyMotionSamples
#### https://github.com/motion-kit/motion-kit/tree/master/samples

^ Read all the sourcecode, download all the samples ...
... softens you to the way RubyMotion lets you use native Objective-C objects

---

# OS X

^ It just works and is great fun
CDQ works here too (watch out for rake schema:build)
Apex, web server ... cool

---

# Android

^ Compiles to native JVM bytecode

---

# People to Follow

* @lrz Laurent Sansonetti (MacRuby, RubyMotion)
* @twerth Todd Worth (Ruby Dispatch, RMQ)
* @seriousken Ken Miller (CDQ)
* @jamonholmgren Jamon Holmgren (ProMotion)
* @FluffyJack (Motion in Motion)

^ Compiles to native JVM bytecode

---

# Tutorials

* Getting started with Motion Kit and ProMotion: http://jamonholmgren.com/getting-started-with-motionkit-and-promotion
* Building iOS forms the ProMotion way with ProMotion-form http://jamonholmgren.com/building-ios-forms-the-promotion-way-with-promotion-form

---

# Screencasts

* Motion in Motion https://motioninmotion.tv
* AUD$9 per month

---

# Email Weekly

* http://rubymotiondispatch.com

---

# Books

- Cocoa Programming for Mac OS X
- Big Nerd Ranch iOS Programming
- Loads more

^ there are actually so many books

---

# end

---

# Made with Deckset
## http://www.decksetapp.com

---

# Slides

#### https://github.com/paulca/ruby-ireland-23-sept-2014

---

# API

#### https://github.com/paulca/ruby-ireland-schedule-api

---

# App

#### https://github.com/paulca/ruby-ireland-schedule-app