# TypeScript Basic Notes

<!-- TOC -->

- [TypeScript Basic Notes](#typescript-basic-notes)
  - [Installation](#installation)
    - [Config](#config)
    - [Webpack for TypeScript](#webpack-for-typescript)
    - [Intergration](#intergration)
  - [Modules](#modules)
    - [globals.d.ts](#globalsdts)
    - [lib.d.ts](#libdts)
  - [Basic Types](#basic-types)
  - [Enum Types](#enum-types)
    - [Number Enum](#number-enum)
    - [String Enum](#string-enum)
    - [Enum with Functions](#enum-with-functions)
    - [Enum as Flags](#enum-as-flags)
    - [Internal of Enum](#internal-of-enum)
  - [Function](#function)
    - [Function Interface](#function-interface)
    - [Arrow Function](#arrow-function)
    - [Weak Overload](#weak-overload)
  - [Type Assertion](#type-assertion)
  - [Interface](#interface)
    - [Extends Interface](#extends-interface)
    - [Implements Interface](#implements-interface)
  - [Index Signature](#index-signature)
    - [Select Index](#select-index)
  - [Alias Types](#alias-types)
  - [Literal Types](#literal-types)
  - [Moving Types](#moving-types)
  - [Access Modifiers](#access-modifiers)
    - [public/proteced/private](#publicprotecedprivate)
    - [readonly](#readonly)
  - [Generic Types](#generic-types)
    - [Generic Function](#generic-function)
    - [Generic Class](#generic-class)
    - [Specific Instances from Generic Types](#specific-instances-from-generic-types)
  - [Advanced Types](#advanced-types)
    - [Union Types](#union-types)
    - [Intersection Types](#intersection-types)
    - [Mapped Types](#mapped-types)
  - [Mixins](#mixins)
  - [Closure](#closure)
  - [Decorators](#decorators)
    - [Class Decorators](#class-decorators)
    - [Class Properties Decorators](#class-properties-decorators)
    - [Method Parameters Decorators](#method-parameters-decorators)
    - [Methods Decorators](#methods-decorators)
  - [React with TypeScript](#react-with-typescript)
    - [Props Types](#props-types)
    - [React Refs Types](#react-refs-types)
    - [Functional Component](#functional-component)
    - [Class Component](#class-component)
    - [Generic Component](#generic-component)
    - [Redux](#redux)
  - [Reference](#reference)

<!-- /TOC -->

## Installation

### Config

- [Types Defination](https://github.com/DefinitelyTyped/DefinitelyTyped)

```bash
npm i -D typescript awesome-typescript-loader source-map-loader
npm i -D react react-dom @types/react @types/react-dom
```

```json
{
  "compilerOptions": {
    /* 基本选项 */
    "target": "es5", // 'ES3', 'ES5', 'ES2015', 'ES2016', 'ES2017', or 'ESNEXT'
    "module": "es2015", // 指定使用模块: 'commonjs', 'amd', 'system', 'umd' or 'es2015'
    "lib": ["es6", "dom"], // 指定要包含在编译中的库文件
    "allowJs": true, // 允许编译 javascript 文件
    "checkJs": true, // 报告 javascript 文件中的错误
    "jsx": "react", // 'preserve', 'react-native', or 'react'
    "declaration": true, // 生成相应的 '.d.ts' 文件
    "sourceMap": true, // 生成相应的 '.map' 文件
    "outFile": "./", // 将输出文件合并为一个文件
    "outDir": "./build/", // 指定输出目录
    "rootDir": "./", // 用来控制输出目录结构 --outDir.
    "removeComments": true, // 删除编译后的所有的注释
    "noEmit": true, // 不生成输出文件
    "importHelpers": true, // 从 tslib 导入辅助工具函数
    "isolatedModules": true, // 将每个文件做为单独的模块 （与 'ts.transpileModule' 类似）

    /* 严格的类型检查选项 */
    "strict": true, // 启用所有严格类型检查选项
    "noImplicitAny": true, // 在表达式和声明上有隐含的 any类型时报错
    "strictNullChecks": true, // 启用严格的 null 检查
    "noImplicitThis": true, // 当 this 表达式值为 any 类型的时候，生成一个错误
    "alwaysStrict": true, // 以严格模式检查每个模块，并在每个文件里加入 'use strict'

    /* 额外的检查 */
    "noUnusedLocals": true, // 有未使用的变量时，抛出错误
    "noUnusedParameters": true, // 有未使用的参数时，抛出错误
    "noImplicitReturns": true, // 并不是所有函数里的代码都有返回值时，抛出错误
    "noFallthroughCasesInSwitch": true, // 报告 switch 语句的 fallthrough 错误

    /* 模块解析选项 */
    "moduleResolution": "node", // 选择模块解析策略： 'node' (Node.js) or 'classic'
    "baseUrl": "./", // 用于解析非相对模块名称的基目录
    "paths": {}, // 模块名到基于 baseUrl 的路径映射的列表
    "rootDirs": [], // 根文件夹列表，其组合内容表示项目运行时的结构内容
    "typeRoots": [], // 包含类型声明的文件列表
    "types": [], // 需要包含的类型声明文件名列表
    "allowSyntheticDefaultImports": true, // 允许从没有设置默认导出的模块中默认导入。

    /* Source Map Options */
    "sourceRoot": "./", // 指定调试器应该找到 TypeScript 文件而不是源文件的位置
    "mapRoot": "./", // 指定调试器应该找到映射文件而不是生成文件的位置
    "inlineSourceMap": true, // 生成单个 soucemaps 文件，而不是将 sourcemaps 生成不同的文件
    "inlineSources": true, // 将代码与 sourcemaps 生成到一个文件中

    /* 其他选项 */
    "experimentalDecorators": true, // 启用装饰器
    "emitDecoratorMetadata": true // 为装饰器提供元数据的支持
  },
  "include": ["./src/**/*"],
  "exclude": ["node_modules"]
}
```

### Webpack for TypeScript

```js
const path = require('path');

module.exports = {
  entry: './src/index.tsx',
  output: {
    filename: '[name].bundle.js',
    path: path.resolve(__dirname, 'dist')
  },
  devtool: 'source-map',
  resolve: {
    extensions: ['.js', '.json', '.ts', '.tsx']
  },
  module: {
    rules: [
      {
        test: /\.(ts|tsx)$/,
        loader: 'awesome-typescript-loader'
      },
      { enforce: 'pre', test: /\.js$/, loader: 'source-map-loader' }
    ]
  },
  externals: {
    react: 'React',
    'react-dom': 'ReactDOM'
  }
};
```

### Intergration

- [TSX-Boilerplate](@typescript-eslint/parser)
- [ESLint for TypeScript](https://github.com/typescript-eslint/typescript-eslint)
- [TSLint Config Airbnb](https://github.com/progre/tslint-config-airbnb)

## Modules

- [Types Search](https://microsoft.github.io/TypeSearch/)

### globals.d.ts

```js
declare module '*.css';
// import * as foo from './some/file.css';
```

```bash
npm i -D @types/react @types/react-dom
```

### lib.d.ts

```json
"compilerOptions": {
  "target": "es5",
  "lib": ["es6", "dom"]
}
```

```bash
tsc --target es5 --lib dom,es6
```

## Basic Types

```js
let num: number;
let str: string;
let bool: boolean;
let boolArray: boolean[];
let tuple: [string, number];
let power: any;

// 赋值任意类型
power = '123';
power = 123;

// 它也兼容任何类型
power = num;
num = power;

function log(message: string): void {
  console.log(message);
}
```

## Enum Types

### Number Enum

```js
enum CardSuit {
  Clubs = 1,
  Diamonds, // 2
  Hearts,   // 3
  Spades    // 4
}

// 简单的使用枚举类型
let Card = CardSuit.Clubs;

// 类型安全
Card = 'not a member of card suit'; // Error: string 不能赋值给 `CardSuit` 类型
```

### String Enum

```js
export enum EvidenceTypeEnum {
  UNKNOWN = '',
  PASSPORT_VISA = 'passport_visa',
  PASSPORT = 'passport',
  SIGHTED_STUDENT_CARD = 'sighted_tertiary_edu_id',
  SIGHTED_KEYPASS_CARD = 'sighted_keypass_card',
  SIGHTED_PROOF_OF_AGE_CARD = 'sighted_proof_of_age_card'
}
```

### Enum with Functions

```js
enum Weekday {
  Monday,
  Tuseday,
  Wednesday,
  Thursday,
  Friday,
  Saturday,
  Sunday
}

namespace Weekday {
  export function isBusinessDay(day: Weekday) {
    switch (day) {
      case Weekday.Saturday:
      case Weekday.Sunday:
        return false;
      default:
        return true;
    }
  }
}

const mon = Weekday.Monday;
const sun = Weekday.Sunday;

console.log(Weekday.isBusinessDay(mon)); // true
console.log(Weekday.isBusinessDay(sun));
```

### Enum as Flags

```js
enum AnimalFlags {
  None        = 0,
  HasClaws    = 1 << 0,
  CanFly      = 1 << 1,
  EatsFish    = 1 << 2,
  Endangered  = 1 << 3,
  EndangeredFlyingClawedFishEating = HasClaws | CanFly | EatsFish | Endangered
}

interface Animal {
  flags: AnimalFlags;
  [key: string]: any;
}

function printAnimalAbilities(animal: Animal) {
  var animalFlags = animal.flags;
  if (animalFlags & AnimalFlags.HasClaws) {
    console.log('animal has claws');
  }
  if (animalFlags & AnimalFlags.CanFly) {
    console.log('animal can fly');
  }
  if (animalFlags == AnimalFlags.None) {
    console.log('nothing');
  }
}

const animal = { flags: AnimalFlags.None };
printAnimalAbilities(animal); // nothing
animal.flags |= AnimalFlags.HasClaws;
printAnimalAbilities(animal); // animal has claws
animal.flags &= ~AnimalFlags.HasClaws;
printAnimalAbilities(animal); // nothing
animal.flags |= AnimalFlags.HasClaws | AnimalFlags.CanFly;
printAnimalAbilities(animal); // animal has claws, animal can fly
```

### Internal of Enum

```js
enum Tristate {
  False,
  True,
  Unknown
};

// compiles to
var Tristate;
(function(Tristate) {
  Tristate[(Tristate['False'] = 0)] = 'False';
  Tristate[(Tristate['True'] = 1)] = 'True';
  Tristate[(Tristate['Unknown'] = 2)] = 'Unknown';
})(Tristate || (Tristate = {}));

console.log(Tristate[0]); // 'False'
console.log(Tristate['False']); // 0
console.log(Tristate[Tristate.False]); // 'False' because `Tristate.False == 0`
```

## Function

### Function Interface

```js
interface ReturnString {
  (): string;
}

declare const foo: ReturnString;

const bar = foo(); // bar 被推断为一个字符串
```

```js
interface Complex {
  (foo: string, bar?: number, ...others: boolean[]): number;
}
```

```js
interface Overloaded {
  (foo: string): string;
  (foo: number): number;
}

// 实现接口的一个例子：
function stringOrNumber(foo: number): number;
function stringOrNumber(foo: string): string;
function stringOrNumber(foo: any): any {
  if (typeof foo === 'number') {
    return foo * foo;
  } else if (typeof foo === 'string') {
    return `hello ${foo}`;
  }
}

const overloaded: Overloaded = stringOrNumber;

// 使用
const str = overloaded(''); // str 被推断为 'string'
const num = overloaded(123); // num 被推断为 'number'
```

### Arrow Function

在一个以 number 类型为参数，以 string 类型为返回值的函数中:

```js
const simple: (foo: number) => string = foo => foo.toString();
```

### Weak Overload

```js
// 重载
function padding(all: number);
function padding(topAndBottom: number, leftAndRight: number);
function padding(top: number, right: number, bottom: number, left: number);
function padding(a: number, b?: number, c?: number, d?: number) {
  if (b === undefined && c === undefined && d === undefined) {
    b = c = d = a;
  } else if (c === undefined && d === undefined) {
    c = a;
    d = b;
  }
  return {
    top: a,
    right: b,
    bottom: c,
    left: d
  };
}

padding(1); // Okay: all
padding(1, 1); // Okay: topAndBottom, leftAndRight
padding(1, 1, 1, 1); // Okay: top, right, bottom, left
padding(1, 1, 1); // Error: Not a part of the available overloads
```

## Type Assertion

- `<type>`
- `as type`

> `as` is better in `.jsx`

```js
let foo: any;
let bar = <string>foo; // 现在 bar 的类型是 'string'
```

```js
function handler(event: Event) {
  const mouseEvent = event as MouseEvent;
}
```

## Interface

```js
interface Name {
  first: string;
  second: string;
}

let name: Name;
name = {
  first: 'John',
  second: 'Doe'
};

name = {
  // Error: 'Second is missing'
  first: 'John'
};

name = {
  // Error: 'Second is the wrong type'
  first: 'John',
  second: 1337
};
```

### Extends Interface

```js
// Lib a.d.ts
interface Point {
  x: number,
  y: number
}
declare const myPoint: Point

// Lib b.d.ts
interface Point {
  z: number
}

// Your code
let myPoint.z // Allowed!
```

### Implements Interface

```js
interface Crazy {
  new(): {
    hello: number
  };
}

class CrazyClass implements Crazy {
  constructor() {
    return { hello: 123 };
  }
}

// Because
const crazy = new CrazyClass(); // crazy would be { hello:123 }
```

## Index Signature

```js
let x: { foo: number, [x: string]: any };

x = { foo: 1, baz: 2 }; // ok, 'baz' 属性匹配于索引签名
```

当你声明一个索引签名时，所有明确的成员都必须符合索引签名

```js
// ok
interface Foo {
  [key: string]: number;
  x: number;
  y: number;
}

// Error
interface Bar {
  [key: string]: number;
  x: number;
  y: string; // Error: y 属性必须为 number 类型
}
```

使用交叉类型可以解决上述问题

```js
type FieldState = {
  value: string
};

type FormState = { isValid: boolean } & { [fieldName: string]: FieldState };
```

### Select Index

```js
type Index = 'a' | 'b' | 'c';
type FromIndex = { [k in Index]?: number };

const good: FromIndex = { b: 1, c: 2 };

// Error:
// `{ b: 1, c: 2, d: 3 }` 不能分配给 'FromIndex'
// 对象字面量只能指定已知类型，'d' 不存在 'FromIndex' 类型上
const bad: FromIndex = { b: 1, c: 2, d: 3 };
```

```js
type FromSomeIndex<K extends string> = { [key in K]: number };
```

## Alias Types

```js
type Text = string | { text: string };
type Coordinates = [number, number];
type Callback = (data: string) => void;
```

## Literal Types

```js
type CardinalDirection = 'North' | 'East' | 'South' | 'West';

function move(distance: number, direction: CardinalDirection) {
  // ...
}

move(1, 'North'); // ok
move(1, 'Nurth'); // Error

type OneToFive = 1 | 2 | 3 | 4 | 5;
type Bools = true | false;
```

## Moving Types

```js
// 捕获字符串的类型与值
const foo = 'Hello World';

// 使用一个捕获的类型
let bar: typeof foo;

// bar 仅能被赋值 'Hello World'
bar = 'Hello World'; // ok
bar = 'anything else'; // Error
```

```js
const colors = {
  red: 'red',
  blue: 'blue'
};

type Colors = keyof typeof colors;

let color: Colors; // color 的类型是 'red' | 'blue'
color = 'red'; // ok
color = 'blue'; // ok
color = 'anythingElse'; // Error
```

## Access Modifiers

### public/proteced/private

```js
class Singleton {
  private static instance: Singleton;
  private constructor() {
    // ..
  }

  public static getInstance() {
    if (!Singleton.instance) {
      Singleton.instance = new Singleton();
    }

    return Singleton.instance;
  }

  someMethod() {}
}

let someThing = new Singleton(); // Error: constructor of 'singleton' is private

let instacne = Singleton.getInstance(); // do some thing with the instance
```

### readonly

readonly type

```js
type Foo = {
  readonly bar: number;
  readonly bas: number;
};

// 初始化
const foo: Foo = { bar: 123, bas: 456 };

// 不能被改变
foo.bar = 456; // Error: foo.bar 为仅读属性
```

readonly indexable signature

```js
interface Foo {
  readonly [x: number]: number;
}

// 使用

const foo: Foo = { 0: 123, 2: 345 };
console.log(foo[0]); // ok（读取）
foo[0] = 456; // Error: 属性只读
```

readonly properties of class

```js
class Foo {
  readonly bar = 1; // OK
  readonly baz: string;
  constructor() {
    this.baz = 'hello'; // OK
  }
}
```

Readonly generic type

```js
type Foo = {
  bar: number,
  bas: number
};

type FooReadonly = Readonly<Foo>;

const foo: Foo = { bar: 123, bas: 456 };
const fooReadonly: FooReadonly = { bar: 123, bas: 456 };

foo.bar = 456; // ok
fooReadonly.bar = 456; // Error: bar 属性只读
```

in React

```js
class Something extends React.Component<{ foo: number }, { baz: number }> {
  someMethod() {
    this.props.foo = 123; // Error: props 是不可变的
    this.state.baz = 456; // Error: 你应该使用 this.setState()
  }
}
```

## Generic Types

### Generic Function

```js
function reverse<T>(items: T[]): T[] {
  const toreturn = [];
  for (let i = items.length - 1; i >= 0; i--) {
    toreturn.push(items[i]);
  }
  return toreturn;
}
```

### Generic Class

```js
// 创建一个泛型类
class Queue<T> {
  private data = [];
  push = (item: T) => this.data.push(item);
  pop = (): T => this.data.shift();
}

// 简单的使用
const queue = new Queue<number>();
queue.push(0);
queue.push('1'); // Error：不能推入一个 `string`，只有 number 类型被允许
```

```js
export interface Listener<T> {
  (event: T): any;
}

export interface Disposable {
  dispose(): any;
}

export class TypedEvent<T> {
  private listeners: Listener<T>[] = [];
  private listenersOncer: Listener<T>[] = [];

  public on = (listener: Listener<T>): Disposable => {
    this.listeners.push(listener);

    return {
      dispose: () => this.off(listener)
    };
  };

  public once = (listener: Listener<T>): void => {
    this.listenersOncer.push(listener);
  };

  public off = (listener: Listener<T>) => {
    const callbackIndex = this.listeners.indexOf(listener);
    if (callbackIndex > -1) this.listeners.splice(callbackIndex, 1);
  };

  public emit = (event: T) => {
    this.listeners.forEach(listener => listener(event));

    this.listenersOncer.forEach(listener => listener(event));

    this.listenersOncer = [];
  };

  public pipe = (te: TypedEvent<T>): Disposable => {
    return this.on(e => te.emit(e));
  };
}
```

### Specific Instances from Generic Types

```js
class Foo<T> {
  foo: T;
}

const FooNumber = Foo as { new (): Foo<number> }; // ref 1

function id<T>(x: T) {
  return x;
}

const idNum = id as { (x: number): number };
```

## Advanced Types

- [Advanced Types](https://www.typescriptlang.org/docs/handbook/advanced-types.html)

### Union Types

多种类型之一

```js
function formatCommandline(command: string[] | string) {
  let line = '';
  if (typeof command === 'string') {
    line = command.trim();
  } else {
    line = command.join(' ').trim();
  }

  // Do stuff with line: string
}
```

```js
interface Square {
  kind: 'square';
  size: number;
}

interface Rectangle {
  kind: 'rectangle';
  width: number;
  height: number;
}

// 有人仅仅是添加了 `Circle` 类型
// 我们可能希望 TypeScript 能在任何被需要的地方抛出错误
interface Circle {
  kind: 'circle';
  radius: number;
}

type Shape = Square | Rectangle | Circle;

function area(s: Shape) {
  switch (s.kind) {
    case 'square':
      return s.size * s.size;
    case 'rectangle':
      return s.width * s.height;
    case 'circle':
      return Math.PI * s.radius ** 2;
    default:
      const _exhaustiveCheck: never = s;
  }
}
```

### Intersection Types

extend 是一种非常常见的模式,
intersection type 具有所有类型的功能

```js
function extend<T, U>(first: T, second: U): T & U {
  const result = <T & U>{};
  for (let id in first) {
    (<T>result)[id] = first[id];
  }
  for (let id in second) {
    if (!result.hasOwnProperty(id)) {
      (<U>result)[id] = second[id];
    }
  }

  return result;
}

const x = extend({ a: 'hello' }, { b: 42 });

// 现在 x 拥有了 a 属性与 b 属性
const a = x.a;
const b = x.b;
```

`connect` in React

```js
import * as React from 'react'
import * as Redux from 'redux'

import { MyReduxState } from './my-root-reducer.ts'

export interface OwnProps {
  propFromParent: number
}

interface StateProps {
  propFromReduxStore: string
}

interface DispatchProps {
  onSomeEvent: () => void
}

type Props = StateProps & DispatchProps & OwnProps

interface State {
  internalComponentStateField: string
}

class MyComponent extends React.Component<Props, State> {
  ...
}

function mapStateToProps(state: MyReduxState, ownProps: OwnProps): StateProps {
  ...
}

function mapDispatchToProps(
  dispatch: Redux.Dispatch<any>,
  ownProps: OwnProps
): DispatchProps {
  ...
}

export default connect<StateProps, DispatchProps, OwnProps>
  (mapStateToProps, mapDispatchToProps)(MyComponent)
```

### Mapped Types

```js
type Readonly<T> = { readonly [P in keyof T]: T[P] }
type Partial<T> = { [P in keyof T]?: T[P] }
type ReadonlyPartial<T> = { readonly [P in keyof T]?: T[P] }
type Nullable<T> = { [P in keyof T]: T[P] | null }
type Required<T> = { [P in keyof T]-?: T[P] }
type Pick<T, K extends keyof T> = { [P in K]: T[P] }
type Extract<T, K extends keyof T> = { [P in K]: T[P] }
type Filter<T, U> = T extends U ? T : never
type Exclude<T, U> = T extends U ? never : T
type Record<T, K extends keyof any> = { [P in K]: T }
type Proxify<T> = { [P in keyof T]: Proxy<T[P]> }

type Proxy<T> = {
    get(): T;
    set(value: T): void;
}

```

## Mixins

```js
// 所有 mixins 都需要
type Constructor<T = {}> = new (...args: any[]) => T;

/////////////
// mixins 例子
////////////

// 添加属性的混合例子
function TimesTamped<TBase extends Constructor>(Base: TBase) {
  return class extends Base {
    timestamp = Date.now();
  };
}

// 添加属性和方法的混合例子
function Activatable<TBase extends Constructor>(Base: TBase) {
  return class extends Base {
    isActivated = false;

    activate() {
      this.isActivated = true;
    }

    deactivate() {
      this.isActivated = false;
    }
  };
}

///////////
// 组合类
///////////

// 简答的类
class User {
  name = '';
}

// 添加 TimesTamped 的 User
const TimestampedUser = TimesTamped(User);

// Tina TimesTamped 和 Activatable 的类
const TimestampedActivatableUser = TimesTamped(Activatable(User));

//////////
// 使用组合类
//////////

const timestampedUserExample = new TimestampedUser();
console.log(timestampedUserExample.timestamp);

const timestampedActivatableUserExample = new TimestampedActivatableUser();
console.log(timestampedActivatableUserExample.timestamp);
console.log(timestampedActivatableUserExample.isActivated);
```

## Closure

```js
const { called } = new class {
  count = 0;
  called = () => {
    this.count++;
    console.log(`Called : ${this.count}`);
  };
}();

called(); // Called : 1
called(); // Called : 2
```

## Decorators

- Attaching to a class:
  access to the class prototype and its member properties.
- Attaching to a class property:
  access to the name and value of that property,
  along with its class prototype `target`.
- Attaching to a class method parameter:
  access to that parameter’s index, name and value.
- Attaching to a class method:
  access to the method’s parameters, the metadata associated with the method object,
  along with its class prototype `target`.

```js
// class definitions
@decorator
class MyComponent extends React.Component<Props, State> {
  // class properties
  @decorator
  private static api_version: string;

  // class method parameters
  private handleFormSubmit(@decorator myParam: string) {
  }

  // class methods
  @decorator
  private handleFormSubmit() {
  }

  // accessors
  @decorator
  public myAccessor() {
    return this.privateProperty;
  }
}
```

### Class Decorators

```js
function classDecorator(options: any[]) {
  return target => {
    ...
  }
}

@classDecorator
class ...
```

```js
function inject(options: { api_version: string }) {
  // returns the class decorator implementation
  return target => {
    // `target` will give us access to the entire class prototype
    target.apiVersion = options.api_version;
  };
}

function deprecated(target) {
  console.log(`
    this class is deprecated and will be removed
    in a future version of the app
  `);
  console.log(`@: ${target}`);
}

@inject({
  api_version: '0.3.4'
})
@deprecated
class MyComponent extends React.Component<Props> {
  static apiVersion: string;
}
```

### Class Properties Decorators

first parameter `target` will be
`class prototype` for normal properties
and `class constructor` for static properties.

```js
function prop(target, name) {
  ...
}

function staticProp(constructor, name) {
  ...
}

class MyComponent extends React.Component<Props> {
  @prop
  public member: string

  @staticProp
  public static apiVersion: string;
}
```

### Method Parameters Decorators

`@uppercase`/`@lowercase` for string parameters,
`@rounded` for number parameters.

```js
function decorator(
  class,
  name: string,
  index: int,
) {
  ...
}
class MyComponent extends React.Component<Props> {
  private handleMethod(@decorator param1: string) {
    ...
  }
}
```

### Methods Decorators

- `target` parameter will class prototype
- `propertyKey` will be a string containing the name of the method.
- `propertyDescriptor` will provide with standard metadata associated with the object:
  configurable, enumerable, value and writable,
  as well as get and set.

```js
function methodDecorator(options: any[]) {
  return (
    target: MyComponent,
    propertyKey: string,
    propertyDescriptor: PropertyDescriptor
  ) => {
    ...
  }
}

class MyComponent extends React.Component {
  @methodDecorator
  handleSomething() {
    ...
  }
}
```

```js
function enumerable(enumerable: boolean) {
  return (
    target: MyComponent,
    propertyKey: string,
    propertyDescriptor: PropertyDescriptor
  ) => {
    propertyDescriptor.enumerable = enumerable;
  }
}

class MyComponent extends React.Component {
  @enumerable(false)
  handleSomething() {
    ...
  }
}
```

## React with TypeScript

- [React TypeScript Cheatsheet](https://github.com/fi3ework/blog/tree/master/react-typescript-cheatsheet-cn)

### Props Types

```js
export declare interface AppProps {
  children: React.ReactNode; // best
  style?: React.CSSProperties; // for style
  onChange?: (e: React.FormEvent<HTMLInputElement>) => void; // form events!
  props: Props & React.HTMLProps<HTMLButtonElement>
}
```

### React Refs Types

```js
class CssThemeProvider extends React.PureComponent<Props> {
  private rootRef: React.RefObject<HTMLDivElement> = React.createRef();

  render() {
    return <div ref={this.rootRef}>{this.props.children}</div>;
  }
}
```

### Functional Component

```js
type Props = {
  foo: string
};

const myComponent: React.FunctionComponent<Props> = props => {
  return <span>{props.foo}</span>;
};

<MyComponent foo="bar" />;
```

```js
import React, { MouseEvent, SFC } from 'react';

type Props = { onClick(e: MouseEvent<HTMLElement>): void };

const Button: SFC<Props> = ({ onClick: handleClick, children }) => (
  <button onClick={handleClick}>{children}</button>
);
```

### Class Component

read only state

```js
import React from 'react';
import Button from './Button';

const initialState = { clicksCount: 0 };
type State = Readonly<typeof initialState>;

class ButtonCounter extends React.Component<Props, State> {
  readonly state: State = initialState;

  render() {
    ...
  }
}
```

props and state types with `React.Component<>`

```js
type Props = {
  foo: string
};

class MyComponent extends React.Component<Props, {}> {
  render() {
    return <span>{this.props.foo}</span>;
  }
}

<MyComponent foo="bar" />;
```

```js
class FocusingInput extends React.Component<
  {
    value: string,
    onChange: (value: string) => any
  },
  {}
> {
  input: HTMLInputElement | null = null;

  render() {
    return (
      <input
        ref={input => (this.input = input)}
        value={this.props.value}
        onChange={e => {
          this.props.onChange(e.target.value);
        }}
      />
    );
  }
  focus() {
    if (this.input != null) {
      this.input.focus();
    }
  }
}
```

### Generic Component

```js
// 一个泛型组件
type SelectProps<T> = { items: T[] };
class Select<T> extends React.Component<SelectProps<T>, any> {}

// 使用
const Form = () => <Select<string> items={['a', 'b']} />;
```

### Redux

```typescript
const initialState = {
  name: '',
  points: 0,
  likesGames: true
};

type State = typeof initialState;
```

```typescript
export function updateName(name: string) {
  return <const>{
    type: 'UPDATE_NAME',
    name
  };
}

export function addPoints(points: number) {
  return <const>{
    type: 'ADD_POINTS',
    points
  };
}

export function setLikesGames(value: boolean) {
  return <const>{
    type: 'SET_LIKES_GAMES',
    value
  };
}

type Action = ReturnType<
  typeof updateName | typeof addPoints | typeof setLikesGames
>;

// =>
// type Action = {
//   readonly type: 'UPDATE_NAME';
//   readonly name: string;
// } | {
//   readonly type: 'ADD_POINTS';
//   readonly points: number;
// } | {
//   readonly type: 'SET_LIKES_GAMES';
//   readonly value: boolean;
// }
```

```js
const reducer = (state: State, action: Action): State => {
  switch (action.type) {
    case 'UPDATE_NAME':
      return { ...state, name: action.name }
    case 'ADD_POINTS':
      return { ...state, points: action.points }
    case 'SET_LIKES_GAMES':
      return { ...state, likesGames: action.value }
    default:
      return state
  }
};
```

## Reference

- [TypeScript Deep Dive](https://github.com/jkchao/typescript-book-chinese)
- [Clean TypeScript Code](https://github.com/labs42io/clean-code-typescript)
