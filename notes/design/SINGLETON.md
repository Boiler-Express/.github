[< back origin docs](https://github.com/Boiler-Express/.github/tree/main/notes/design)

# Singleton Pattern

> Singleton Pattern
>
> - Purpose : Restrict the generation of classes
> - When
>   - Only one instance of a class should be created
>       - Only one server application should be created.
>       - Only one env instance should be created.
> - Warning
>   - If you make Class to Singleton CLass, that class use memory in all process. <br> So, don't use 'Singleton' anywhere.

I usually create Express Instance, reference `Express Docs`.

1. Error, with Jest.
2. Guess, the cause of error.
3. Solution, `Singleton`

```javascript
// index.js
import Express from 'express';

const app = Express();
app.listen(4000, () => console.log(`Server is running in 4000`));
```

<hr>

### 1. Error, with Jest.

In _2022-04_, I got to know TDD, test-driven-development.

And I apply Test Code in my Application, with `jest-watch` options.


> `TDD` is Test Drive Development. <br>
> Before implementing a feature, you first type the code to prove stability of Logics. <br>

> `jest-watch`'s feature seems like **nodemon**. <br>
> If your test file will be changed, automatically run jest to testing.

And then I encounter this error.

```javascript
Error: That port is already in use.
```

<hr>

### 2. Guess, the cause of error.

Maybe, `undefined causes` to create 2 Express Instance.

So, I want to create 1 Express Instance.

<hr>

### 3. Solution, `Singleton`

I like to stability of logics.

So I apply these solution in logcis.

- 3.1. Hidden Arrow Function
- 3.2. Static variables in Class.

#### 3.1. Hidden Arrow Function

> This _arrow function_ runs only once. <br>
> More... [Boiler-Express/Base-Express ./src/index.js](https://github.com/Boiler-Express/Base-Express/blob/main/src/index.js)

```javascript
// index.js
(() => {
    console.log('hello');
})()
```

#### 3.2. Static variables in Class

> This _Express Instance_ only one can be created.
> More... [Boiler-Express/Base-Express ./src/server.js](https://github.com/Boiler-Express/Base-Express/blob/main/src/server.js)

```javascript
// server.js
import Express from 'express';

class App {

    static app;
    static getAppInstance() {
        this.app = Express();
        this.app.listen(4000, () => console.log('Server is running on 4000'));
    }

}
```
