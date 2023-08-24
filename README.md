# typescript-protected-access-modifier

### Protected Keyword

Protected acts like Private. Only as we saw before in the video, private does not lend it's attributes to children of a class. Private variables/attributes can only be accessed by the class. Where as, Protected Keyword, tells Typescript that the attribute can be accessed by children of a class. In our case below, Admin, being a child of User, can change it's own name because of the setter function within itself, and the Protected status of name:

```Typescript
class User {
  protected _name: string

  constructor(name: string) {
    this._name = name
  }

  get name(): string {
    return this._name
  }
}

class Admin extends User {
  set name(n: string){
    this._name = n
  }
}

const admin = new Admin('robin')
admin.name = 'azeaze'
```
