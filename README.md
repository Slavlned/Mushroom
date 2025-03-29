# Mushroom
Simple scripting programming language for unity 🍄

# Code examples

Basic
```Kotlin
import msh.unity
import msh.io

// creating some script
class SomeClass {
  fun someFunction() {
    // full c# classes compability
    gameObject.transform.position = Vector3(0, 0, 1)
  }
}

// on start
unity.onStart(fun {
  io.debug('unity start handle')
  s := SomeClass()
  s.someFunction()
})

// on update
unity.onUpdate(fun {
  io.debug('unity update handle')
})
```

Unity Coroutines Support
```msh
coroutine := unity.coroutineBuilder()
    .do(fun {
      io.debug('some code here')
    })
    .wait(3.5)
    .do(fun {
      io.debug('some wait here')
    })
    .build()

unity.coro(coroutine())
```
