# FunGeo

#### 14-04-25

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
