# FunGeo

#### 15-04-25

- support d = C(q, P(150,150))
- support making circle given center point and point at circle.
- change function call to use (): R
- support making rectangle from 2 Points.
- when to reset this lastType? in the caller for expression().
- global variable lastType for type checking in compiler
- check type of argument of L, must be numbers.
- don't support expression statement
- overload L. Accept 2 points arguments.
- change kind in LObj to use Kind enum
- change function call to use (): P
- change function call to use (): L
- move cursor to the end when going through repl history (bug fix)
- add Token Comma
- make test.html
- make fungeo-test.js

#### 14-04-25

- create closed shape object GeoShape
- method S to make closed shape object
- change length property to end in token because we always do
    slice(token.start, token.start + token.length);
- add optional property error for token error
- add C command to make circle
  c = C 100 100 50
- add circle support
- add stroke command
- make fill fail when the argument doesn't have fillStyle property
- change fillStyle to strokeStyle in GeoLine
- change stroke property to strokeStyle
- change color property to fillStyle
- change color command to fill
- use const enum for kind property in GObj (or in all Obj??)

#### 13-04-25

- don't fire enter when repl is empty
- don't compiler empty string
- use try catch in compiler.
- give error when trying to draw non GObj.

#### 12-04-25

- add lineop_obj as bindable
- make syntax L 100 100 100 100
- create repl object
- create default canvas 300x300
- separate files
- create a scanner object
- print input text in console
- add input field
- make simple html without css
