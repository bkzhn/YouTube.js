[youtubei.js](../../../README.md) / [Utils](../README.md) / InnertubeError

# Class: InnertubeError

## Extends

- `Error`

## Extended by

- [`ParsingError`](ParsingError.md)
- [`MissingParamError`](MissingParamError.md)
- [`OAuth2Error`](OAuth2Error.md)

## Constructors

### new InnertubeError()

> **new InnertubeError**(`message`, `info`?): [`InnertubeError`](InnertubeError.md)

#### Parameters

• **message**: `string`

• **info?**: `any`

#### Returns

[`InnertubeError`](InnertubeError.md)

#### Overrides

`Error.constructor`

#### Defined in

[src/utils/Utils.ts:35](https://github.com/LuanRT/YouTube.js/blob/4ae0cc5c523a2080e68d6c0c1437c78fe318ea30/src/utils/Utils.ts#L35)

## Properties

### cause?

> `optional` **cause**: `unknown`

#### Inherited from

`Error.cause`

#### Defined in

node\_modules/typescript/lib/lib.es2022.error.d.ts:24

***

### date

> **date**: `Date`

#### Defined in

[src/utils/Utils.ts:31](https://github.com/LuanRT/YouTube.js/blob/4ae0cc5c523a2080e68d6c0c1437c78fe318ea30/src/utils/Utils.ts#L31)

***

### info?

> `optional` **info**: `any`

#### Defined in

[src/utils/Utils.ts:33](https://github.com/LuanRT/YouTube.js/blob/4ae0cc5c523a2080e68d6c0c1437c78fe318ea30/src/utils/Utils.ts#L33)

***

### message

> **message**: `string`

#### Inherited from

`Error.message`

#### Defined in

node\_modules/typescript/lib/lib.es5.d.ts:1077

***

### name

> **name**: `string`

#### Inherited from

`Error.name`

#### Defined in

node\_modules/typescript/lib/lib.es5.d.ts:1076

***

### stack?

> `optional` **stack**: `string`

#### Inherited from

`Error.stack`

#### Defined in

node\_modules/typescript/lib/lib.es5.d.ts:1078

***

### version

> **version**: `string`

#### Defined in

[src/utils/Utils.ts:32](https://github.com/LuanRT/YouTube.js/blob/4ae0cc5c523a2080e68d6c0c1437c78fe318ea30/src/utils/Utils.ts#L32)

***

### stackTraceLimit

> `static` **stackTraceLimit**: `number`

The `Error.stackTraceLimit` property specifies the number of stack frames
collected by a stack trace (whether generated by `new Error().stack` or
`Error.captureStackTrace(obj)`).

The default value is `10` but may be set to any valid JavaScript number. Changes
will affect any stack trace captured _after_ the value has been changed.

If set to a non-number value, or set to a negative number, stack traces will
not capture any frames.

#### Inherited from

`Error.stackTraceLimit`

#### Defined in

node\_modules/@types/node/globals.d.ts:162

## Methods

### captureStackTrace()

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Creates a `.stack` property on `targetObject`, which when accessed returns
a string representing the location in the code at which
`Error.captureStackTrace()` was called.

```js
const myObject = {};
Error.captureStackTrace(myObject);
myObject.stack;  // Similar to `new Error().stack`
```

The first line of the trace will be prefixed with
`${myObject.name}: ${myObject.message}`.

The optional `constructorOpt` argument accepts a function. If given, all frames
above `constructorOpt`, including `constructorOpt`, will be omitted from the
generated stack trace.

The `constructorOpt` argument is useful for hiding implementation
details of error generation from the user. For instance:

```js
function a() {
  b();
}

function b() {
  c();
}

function c() {
  // Create an error without stack trace to avoid calculating the stack trace twice.
  const { stackTraceLimit } = Error;
  Error.stackTraceLimit = 0;
  const error = new Error();
  Error.stackTraceLimit = stackTraceLimit;

  // Capture the stack trace above function b
  Error.captureStackTrace(error, b); // Neither function c, nor b is included in the stack trace
  throw error;
}

a();
```

#### Parameters

• **targetObject**: `object`

• **constructorOpt?**: `Function`

#### Returns

`void`

#### Inherited from

`Error.captureStackTrace`

#### Defined in

node\_modules/@types/node/globals.d.ts:146

***

### prepareStackTrace()

> `static` **prepareStackTrace**(`err`, `stackTraces`): `any`

#### Parameters

• **err**: `Error`

• **stackTraces**: `CallSite`[]

#### Returns

`any`

#### See

https://v8.dev/docs/stack-trace-api#customizing-stack-traces

#### Inherited from

`Error.prepareStackTrace`

#### Defined in

node\_modules/@types/node/globals.d.ts:150
