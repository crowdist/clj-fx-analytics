# ClojureFX

A Clojure wrapper to make working with [JavaFX](http://download.java.net/jdk8/jfxdocs/index.html) simpler and more idiomatic.

## Features

This is in a very early state, so there isn't much yet. Take a look at the [ClojureFX wiki](https://bitbucket.org/zilti/clojurefx/wiki/Home).

### Declarative UI programming

```clojure
(compile [VBox {:id "TopLevelVBox"
                :children [Label {:text "Hi!"}
                           Label {:text "I'm ClojureFX!"}
                           HBox {:id "HorizontalBox"
                                 :children [Button {:text "Alright."}]}]}])
```

## TODO

Everything.
