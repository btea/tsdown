## foo.js

```js
//#region utils/foo.ts
const foo$1 = (a) => {
	console.log("utils/foo:" + a);
};

//#endregion
//#region foo.ts
const foo = (a) => {
	console.log("foo:" + a);
};

//#endregion
export { foo, foo$1 };
```
## index.js

```js
import { foo as foo$1, foo$1 as foo } from "./foo.js";

export { foo$1 as foo, foo as utilsFoo };
```
## run.js

```js
import { foo, foo$1 } from "./foo.js";

//#region run.ts
foo("hello world");
foo$1("hello world");

//#endregion
```