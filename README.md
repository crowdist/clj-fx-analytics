[![License](//img.shields.io/badge/license-LGPL-blue.svg?style=flat)](https://www.gnu.org/licenses/lgpl-3.0.en.html#content)

# ClojureFX

A Clojure extension to make working with [JavaFX](http://download.java.net/jdk8/jfxdocs/index.html) simpler and more idiomatic. It allows you to naturally work with stock JavaFX components through use of extended protocols. Should a feature be missing you can easily extend ClojureFX in your own codebase or just fall back to standard JavaFX methods.

## Features

This is in a very early state, so there isn't much yet. Take a look at the [ClojureFX wiki](https://bitbucket.org/zilti/clojurefx/wiki/Home).

* Declarative EDN GUI structure compilation
* FXML loading and scripting
* Simplified event binding (bind a Clojure function to an event trigger)
* Turn a scene graph into a flat id-node-map and/or get nodes by id out of a scene graph

### Declarative UI programming

```clojure
(def superbutton (compile [Button {:text "Close"
                                   :action #'close-handler}]))

(compile [VBox {:id "TopLevelVBox"
                :children [Label {:text "Hi!"}
                           Label {:text "I'm ClojureFX!"}
                           HBox {:id "HorizontalBox"
                           :children [Button {:text "OK"}
						              superbutton]}]}])
```
