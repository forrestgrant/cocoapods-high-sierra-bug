# Cocoapods & macOS High Sierra Incompatibility
## Environment
* macOS 10.13 High Sierra
* RubyMotion 5.2

## Steps to reproduce
1. `$ git clone git@github.com:forrestgrant/cocoapods-high-sierra-bug.git`
2. `$ cd cocoapods-high-sierra-bug`
3. `$ bundle install`
4. `$ rake pod:install`
5. `$ rake`

Following these steps will produce the error:
```
*** Terminating app due to uncaught exception 'NameError', reason: '/Users/fgrant/.rbenv/versions/2.2.5/lib/ruby/gems/2.2.0/gems/ProMotion-menu-1.1.0/lib/ProMotion/men: uninitialized constant ProMotion::Menu::Gestures::MMOpenDrawerGestureModePanningNavigationBar (NameError)
```

## Notes
* The app will run successfully by removing the 4 gems from the `Gemfile` (All gems except for `rake`)
* Other than the `Gemfile`, this is a boilerplate RubyMotion iOS app.
