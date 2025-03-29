# Mushroom
Simple scripting programming language for unity 🍄

# Code examples

Basic
```OCaml
import msh.unity
import msh.io

// creating some script
class SomeClass {
  fun someFunction() {
    // full c# classes compability
    gameObject.transform.position = new Vector3(0, 0, 1)
  }
}

// on start
unity.onStart(fun {
  io.debug('unity start handle')
  s := new SomeClass()
  s.someFunction()
})

// on update
unity.onUpdate(fun {
  io.debug('unity update handle')
})
```
