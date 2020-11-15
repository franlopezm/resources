# NodeJS
---

## Commands
- Get the version of v8 that runs on a specific version of node.
    `node -p process.versions.v8`

- List all the _in progress_ features available on each NodeJS release.
    `node --v8-options | grep "in progress"`


## NodeJS 14 - New features:
### Optional chaining
[More info MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)

```js
var person = {
  name: 'Ina',
  age: '23',
  father: {
    name: 'Dinah'
  }
}

console.log(person.mother?.lastname)
// Output: undefined

console.log(person.getAge?.())
// Output: undefined

console.log(person?.['mother_name'])
// Output: undefined
```

- Arrays

```js
const arr = [1,2,3,4,5]

console.log(arr?.[42])
// Output: undefined

console.log(arr?.[45]?.name)
// Output: undefined
```

### Nullish coalescing operator
[More info MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_Coalescing_Operator)

```js
console.log(null ?? 'default string')
// Output: default string

console.log(undefined ?? 'default string')
// Output: default string

console.log(0 ?? 'default string')
// Output: 0

console.log(false ?? 'default string')
// Output: false

console.log('' ?? 'default string')
// Output: ''

console.log('prueba' ?? 'default string')
// Output: prueba
```

### Intl.DisplayNames
[More info MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/DisplayNames/DisplayNames)

- Options:
  - types, one of this: language, script, region, currency
  - style, one of this: narrow, short, long

```js
const langToDisplay = ['fr', 'en-US', 'en', 'zh-TW', 'es', 'es-AR', 'zh-Hant', 'fr-CA']

function displayLang(locale) {
  const languagelong = new Intl.DisplayNames([locale], { type: 'language' })
  const languageNarrow = new Intl.DisplayNames([locale], { type: 'language', style: 'narrow' })
  const languageshort = new Intl.DisplayNames([locale], { type: 'language', style: 'short' })

  console.log('-- locale:', locale, '---')
  for(const lang of langToDisplay) {
    console.log(lang,
      '\n\tlong :', languagelong.of(lang),
      '\n\tnarrow :', languageNarrow.of(lang),
      '\n\tshort :', languageshort.of(lang)
    )
  }
}

// Display languages in English
displayLang('en')
// Display languages in Japanese
displayLang('jpn')
```

### Private fields and methods in Class
[More info v8.dev](https://v8.dev/features/class-fields)

```js
class Test {
  #private = 'Hello'
  name = ''

  constructor(name) {
    this.name = name
  }

  #getString() {
    return `${this.#private} ${this.name}`
  }

  sayHello() {
    return this.#getString()
  }
}

const person = new Test('Ina')

console.log(person.sayHello())
// Output: Hello Ina
```

### Try-catch-finally
[More info MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch)

- Unconditional catch-block
```js
try {
  throw "myException" // generates an exception
} catch (e) {
  // statements to handle any exceptions
  console.error(e) // pass exception object to error handler
}

// Output: myException
```

- The exception identifier
```js
function isValidJSON(text) {
  try {
    JSON.parse(text);
    return true;
  } catch {
    return false;
  }
}

console.log('isValidJSON', isValidJSON('hola'))
// Output: isValidJSON false
```

- The finally-block
```js
try {
  throw "myException" // generates an exception
} catch (e) {
  // statements to handle any exceptions
  console.error(e) // pass exception object to error handler
} finally {
  console.log('Finally')
}

// Output: myException
// Output: Finally
```

- Catch is optional with finally-block
```js
try {
  throw "myException" // generates an exception
} finally {
  console.log('Finally')
}

// Output: Finally
// Output: uncautch myException
```
