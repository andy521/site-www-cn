---
title: 示例程序
description: 常用示例程序中包含详细示例说明链接。
---

{% comment %}

This collection is not exhaustive&mdash;it's just a brief
introduction to the language for people who like to learn by example.
You might also want to check out the language and library tours.

<div class="card-grid">
  <div class="card">
    <h3><a href="/guides/language/language-tour">Language tour</a></h3>
    <p>
      A comprehensive tour, with examples, of the Dart language.
      Most of the <em>read more</em> links in this page
      point to the language tour.
    </p>
  </div>
  <div class="card">
    <h3><a href="/guides/libraries/library-tour">Library tour</a></h3>
    <p>
      An example-based introduction to the Dart core libraries.
      See how to use the built-in types, collections,
      dates and times, streams, and more.
    </p>
  </div>
</div>

{% endcomment %}


这里的示例并不全面&mdash;它只是为那些喜欢通过示例了解语言的人提供一个语言的介绍。
你可能还希望阅读语言概览和库概览。

<div class="card-grid">
  <div class="card">
    <h3><a href="/guides/language/language-tour">语言概览</a></h3>
    <p>
      包含示例的 Dart 语言综合概览。
      文中多数的<em>阅读更多</em>会跳转到此概览。
    </p>
  </div>
  <div class="card">
    <h3><a href="/guides/libraries/library-tour">库概览</a></h3>
    <p>
      基于示例的 Dart 核心库简介。通过概览可以了解内置类型，
      集合，日期和时间，stream 等的使用方法。
    </p>
  </div>
</div>


{% comment %}

## Hello World

Every app has a `main()` function.
To display text on the console, you can use the top-level `print()` function:

<?code-excerpt "misc/test/samples_test.dart (hello-world)"?>
{% prettify dart %}
void main() {
  print('Hello, World!');
}
{% endprettify %}

{% endcomment %}


## Hello World

每个 app 都有一个 `main()` 函数。
使用顶级函数 `print()` 将文字输出到控制台。

<?code-excerpt "misc/test/samples_test.dart (hello-world)"?>
{% prettify dart %}
void main() {
  print('Hello, World!');
}
{% endprettify %}


{% comment %}

## Variables

Even in type-safe Dart code, most variables don't need explicit types,
thanks to type inference:

<?code-excerpt "misc/test/samples_test.dart (var)"?>
{% prettify dart %}
var name = 'Voyager I';
var year = 1977;
var antennaDiameter = 3.7;
var flybyObjects = ['Jupiter', 'Saturn', 'Uranus', 'Neptune'];
var image = {
  'tags': ['saturn'],
  'url': '//path/to/saturn.jpg'
};
{% endprettify %}

[Read more](/guides/language/language-tour#variables) about variables in Dart, including default values, the `final` and `const` keywords, and static types.

{% endcomment %}


## 变量

虽然 Dart 代码是类型安全的，但是由于支持类型推断，大多数变量是不需要显式指定类型的：

<?code-excerpt "misc/test/samples_test.dart (var)"?>
{% prettify dart %}
var name = 'Voyager I';
var year = 1977;
var antennaDiameter = 3.7;
var flybyObjects = ['Jupiter', 'Saturn', 'Uranus', 'Neptune'];
var image = {
  'tags': ['saturn'],
  'url': '//path/to/saturn.jpg'
};
{% endprettify %}

[阅读更多](/guides/language/language-tour#变量)  Dart 中关于变量的内容，
包含默认值， `final` 和 `const` 关键字，以及静态类型。


{% comment %}
## Control flow statements

Dart supports the usual control flow statements:

<?code-excerpt "misc/test/samples_test.dart (control-flow)"?>
{% prettify dart %}
if (year >= 2001) {
  print('21st century');
} else if (year >= 1901) {
  print('20th century');
}

for (var object in flybyObjects) {
  print(object);
}

for (int month = 1; month <= 12; month++) {
  print(month);
}

while (year < 2016) {
  year += 1;
}
{% endprettify %}

[Read more](/guides/language/language-tour#control-flow-statements) about control flow statements in Dart,
including `break` and `continue`, `switch` and `case`, and `assert`.
{% endcomment %}


## 控制流程语句

Dart 支持常用的控制流语句：

<?code-excerpt "misc/test/samples_test.dart (control-flow)"?>
{% prettify dart %}
if (year >= 2001) {
  print('21st century');
} else if (year >= 1901) {
  print('20th century');
}

for (var object in flybyObjects) {
  print(object);
}

for (int month = 1; month <= 12; month++) {
  print(month);
}

while (year < 2016) {
  year += 1;
}
{% endprettify %}

[阅读更多](/guides/language/language-tour#控制流程语句)  Dart 中关于控制流程语句的内容，
包括 `break` 和 `continue` ， `switch` 和 `case` ， 以及 `assert` 。


{% comment %}
## Functions

[We recommend](/guides/language/effective-dart/design#types)
specifying the types of each function's arguments and return value:

<?code-excerpt "misc/test/samples_test.dart (functions)"?>
{% prettify dart %}
int fibonacci(int n) {
  if (n == 0 || n == 1) return n;
  return fibonacci(n - 1) + fibonacci(n - 2);
}

var result = fibonacci(20);
{% endprettify %}

A shorthand `=>` (_arrow_) syntax is handy for functions that
contain a single statement.
This syntax is especially useful when passing anonymous functions as arguments:

<?code-excerpt "misc/test/samples_test.dart (arrow)"?>
{% prettify dart %}
flybyObjects.where((name) => name.contains('turn')).forEach(print);
{% endprettify %}

Besides showing an anonymous function (the argument to `where()`),
this code shows that you can use a function as an argument:
the top-level `print()` function is an argument to `forEach()`.

[Read more](/guides/language/language-tour#functions) about functions in Dart,
including optional parameters, default parameter values, and lexical scope.
{% endcomment %}


## 函数

[我们建议](/guides/language/effective-dart/design#类型)
指定每个函数的参数类型和返回值：

<?code-excerpt "misc/test/samples_test.dart (functions)"?>
{% prettify dart %}
int fibonacci(int n) {
  if (n == 0 || n == 1) return n;
  return fibonacci(n - 1) + fibonacci(n - 2);
}

var result = fibonacci(20);
{% endprettify %}

`=>`（箭头）语法用于仅包含一条语句的函数。该语法在匿名函数作为函数参数情况中
非常有用。

<?code-excerpt "misc/test/samples_test.dart (arrow)"?>
{% prettify dart %}
flybyObjects.where((name) => name.contains('turn')).forEach(print);
{% endprettify %}

上例除了演示匿名函数（匿名函数作为 `where()` 的参数），同时也演示了函数作为
参数的使用：顶级函数 `print()` 是传入 `forEach()` 方法的一个参数。

[阅读更多](/guides/language/language-tour#函数) Dart 中关于函数的内容,
包括可选参数，默认参数值，以及词法作用于。


{% comment %}
## Comments

Dart comments usually start with `//`.

{% prettify dart %}
// This is a normal, one-line comment.

/// This is a documentation comment, used to document libraries,
/// classes, and their members. Tools like IDEs and dartdoc treat
/// doc comments specially.

/* Comments like these are also supported. */
{% endprettify %}

[Read more](/guides/language/language-tour#comments) about comments in Dart,
including how the documentation tooling works.
{% endcomment %}


## 注释

Dart 通常使用 `//` 作为注释的开始。

{% prettify dart %}
// 这是一个标准的单行注释。

/// 这是一个文档注释，用来为库，类，以及它们的成员提供文档。
/// 像 IDEs 和 dartdoc 的工具会专门处理这些注释来生成文档。

/* 也支持类似的注释 */
{% endprettify %}

[阅读更多](/guides/language/language-tour#注释) 在 Dart 中关于注释的内容，
包括文档工具的工作原理。


{% comment %}
## Imports

To access APIs defined in other libraries, use `import`.

<?code-excerpt "misc/test/samples_test.dart (import)" plaster="none"?>
{% prettify dart %}
// Importing core libraries
import 'dart:math';

// Importing libraries from external packages
import 'package:test/test.dart';

// Importing files
import 'path/to/my_other_file.dart';
{% endprettify %}

[Read more](/guides/language/language-tour#libraries-and-visibility) about libraries and visibility in Dart,
including library prefixes, `show` and `hide`, and lazy loading through the `deferred` keyword.
{% endcomment %}


## Import

使用 `import` 来访问其他库中的 API 。

<?code-excerpt "misc/test/samples_test.dart (import)" plaster="none"?>
{% prettify dart %}
// 导入核心库
import 'dart:math';

// 从外部包导入库
import 'package:test/test.dart';

// 导入文件
import 'path/to/my_other_file.dart';
{% endprettify %}

[阅读更多](/guides/language/language-tour#库和可见性) Dart 中关于库和可见性的内容,
包括库前缀，`show` 和 `hide` ，以及通过 `deferred` 关键字的懒加载。


{% comment %}
## Classes

Here's an example of a class with three properties, two constructors,
and a method. One of the properties can't be set directly, so it's
defined using a getter method (instead of a variable).

{% comment %}
The linter rule sort_constructors_first made us put the getter below
the constructors: https://github.com/dart-lang/linter/issues/859.
{% endcomment %}

<?code-excerpt "misc/lib/samples/spacecraft.dart (class)"?>
{% prettify dart %}
class Spacecraft {
  String name;
  DateTime launchDate;

  // Constructor, with syntactic sugar for assignment to members.
  Spacecraft(this.name, this.launchDate) {
    // Initialization code goes here.
  }

  // Named constructor that forwards to the default one.
  Spacecraft.unlaunched(String name) : this(name, null);

  int get launchYear =>
      launchDate?.year; // read-only non-final property

  // Method.
  void describe() {
    print('Spacecraft: $name');
    if (launchDate != null) {
      int years =
          DateTime.now().difference(launchDate).inDays ~/
              365;
      print('Launched: $launchYear ($years years ago)');
    } else {
      print('Unlaunched');
    }
  }
}
{% endprettify %}

You might use the `Spacecraft` class like this:

<?code-excerpt "misc/test/samples_test.dart (use class)" plaster="none"?>
{% prettify dart %}
var voyager = Spacecraft('Voyager I', DateTime(1977, 9, 5));
voyager.describe();

var voyager3 = Spacecraft.unlaunched('Voyager III');
voyager3.describe();
{% endprettify %}

[Read more](/guides/language/language-tour#classes) about classes in Dart,
including initializer lists, optional `new` and `const`, redirecting constructors,
`factory` constructors, getters, setters, and much more.
{% endcomment %}


## 类

下面是一个关于类的示例，这个类包含三个属性，两个构造函数，以及一个方法。
其中一个属性不能被直接赋值，因此它被定义为一个 getter 方法（而不是变量）。

{% comment %}
The linter rule sort_constructors_first made us put the getter below
the constructors: https://github.com/dart-lang/linter/issues/859.
{% endcomment %}

<?code-excerpt "misc/lib/samples/spacecraft.dart (class)"?>
{% prettify dart %}
class Spacecraft {
  String name;
  DateTime launchDate;

  // 构造函数，使用语法糖设置成员变量。
  Spacecraft(this.name, this.launchDate) {
    // 这里编写初始化代码。
  }

  // 命名构造函数，最终调用默认构造函数。
  Spacecraft.unlaunched(String name) : this(name, null);

  int get launchYear =>
      launchDate?.year; // read-only non-final 属性

  // 方法。
  void describe() {
    print('Spacecraft: $name');
    if (launchDate != null) {
      int years =
          DateTime.now().difference(launchDate).inDays ~/
              365;
      print('Launched: $launchYear ($years years ago)');
    } else {
      print('Unlaunched');
    }
  }
}
{% endprettify %}

可以像下面这样使用 `Spacecraft` 这个类：

<?code-excerpt "misc/test/samples_test.dart (use class)" plaster="none"?>
{% prettify dart %}
var voyager = Spacecraft('Voyager I', DateTime(1977, 9, 5));
voyager.describe();

var voyager3 = Spacecraft.unlaunched('Voyager III');
voyager3.describe();
{% endprettify %}

[阅读更多](/guides/language/language-tour#类)  Dart 中关于类的内容,
包括初始化列表，可选关键字 `new` 和 `const` ，重定向构造函数， `factory` 
构造函数， getter 方法， setter 方法，以及更多类似部分。


{% comment %}
## Inheritance

Dart has single inheritance.

<?code-excerpt "misc/lib/samples/spacecraft.dart (extends)"?>
{% prettify dart %}
class Orbiter extends Spacecraft {
  num altitude;
  Orbiter(String name, DateTime launchDate, this.altitude)
      : super(name, launchDate);
}
{% endprettify %}

[Read more](/guides/language/language-tour#extending-a-class) about extending classes, the optional `@override` annotation, and more.
{% endcomment %}


## 扩展类（继承）

Dart 支持单继承。

<?code-excerpt "misc/lib/samples/spacecraft.dart (extends)"?>
{% prettify dart %}
class Orbiter extends Spacecraft {
  num altitude;
  Orbiter(String name, DateTime launchDate, this.altitude)
      : super(name, launchDate);
}
{% endprettify %}

[阅读更多](/guides/language/language-tour#扩展类继承) 关于类继承，可选的 `@override` 注解，以及其他内容。


{% comment %}
## Mixins

Mixins are a way of reusing code in multiple class hierarchies. The following class can act as a mixin:

<?code-excerpt "misc/lib/samples/spacecraft.dart (mixin)"?>
{% prettify dart %}
class Piloted {
  int astronauts = 1;
  void describeCrew() {
    print('Number of astronauts: $astronauts');
  }
}
{% endprettify %}

To add a mixin's capabilities to a class, just extend the class with the mixin.

<?code-excerpt "misc/lib/samples/spacecraft.dart (mixin use)" replace="/with/[!$&!]/g"?>
{% prettify dart %}
class PilotedCraft extends Spacecraft [!with!] Piloted {
  // ···
}
{% endprettify %}

`PilotedCraft` now has the `astronauts` field as well as the `describeCrew()` method.

[Read more](/guides/language/language-tour#adding-features-to-a-class-mixins) about mixins.
{% endcomment %}


## Mixin

Mixin 是一种在多个类层次结构中重用代码的方法。下面的类可以作为一个 mixin ：

<?code-excerpt "misc/lib/samples/spacecraft.dart (mixin)"?>
{% prettify dart %}
class Piloted {
  int astronauts = 1;
  void describeCrew() {
    print('Number of astronauts: $astronauts');
  }
}
{% endprettify %}

将 mixin 的功能添加到一个类中，只需要继承这个类并 with 这个 mixin 。

<?code-excerpt "misc/lib/samples/spacecraft.dart (mixin use)" replace="/with/[!$&!]/g"?>
{% prettify dart %}
class PilotedCraft extends Spacecraft [!with!] Piloted {
  // ···
}
{% endprettify %}

现在 `飞行器` 有了 `astronauts` 字段以及 `describeCrew()` 方法。

[阅读更多](/guides/language/language-tour#为类添加功能-mixins) 关于 mixin 的内容.


{% comment %}
## Interfaces and abstract classes

Dart has no `interface` keyword. Instead, all classes implicitly define an interface. Therefore, you can implement any class.

<?code-excerpt "misc/lib/samples/spacecraft.dart (implements)"?>
{% prettify dart %}
class MockSpaceship implements Spacecraft {
  // ···
}
{% endprettify %}

[Read more](/guides/language/language-tour#implicit-interfaces) about implicit interfaces.

You can create an abstract class to be extended (or implemented) by a concrete class. Abstract classes can contain abstract methods (with empty bodies).

<?code-excerpt "misc/lib/samples/spacecraft.dart (abstract)" replace="/abstract/[!$&!]/g"?>
{% prettify dart %}
[!abstract!] class Describable {
  void describe();

  void describeWithEmphasis() {
    print('=========');
    describe();
    print('=========');
  }
}
{% endprettify %}

Any class extending `Describable` has the `describeWithEmphasis()` method, which calls the extender's implementation of `describe()`.

[Read more](/guides/language/language-tour#abstract-classes) about abstract classes and methods.
{% endcomment %}


## 接口和抽象类

Dart 没有 `interface` 关键字。相反，所有的类都隐式定义了一个接口，因此，任意类都可以作为接口被实现。

<?code-excerpt "misc/lib/samples/spacecraft.dart (implements)"?>
{% prettify dart %}
class MockSpaceship implements Spacecraft {
  // ···
}
{% endprettify %}

[阅读更多](/guides/language/language-tour#隐式接口) 关于隐式接口的内容。

创建一个抽象类，这个类可以被一个具体的类去扩展（或实现）。抽象类可以包含抽象方法（只声明未实现）。

<?code-excerpt "misc/lib/samples/spacecraft.dart (abstract)" replace="/abstract/[!$&!]/g"?>
{% prettify dart %}
[!abstract!] class Describable {
  void describe();

  void describeWithEmphasis() {
    print('=========');
    describe();
    print('=========');
  }
}
{% endprettify %}

任意一个扩展了 `Describable` 的具体类都拥有 `describeWithEmphasis()` 方法，这个方法调用了具体类中实现的 `describe()` 。

[阅读更多](/guides/language/language-tour#抽象类) 关于抽象类和方法的内容。


{% comment %}

## Async

Avoid callback hell and make your code much more readable by
using `async` and `await`.

<?code-excerpt "misc/test/samples_test.dart (async)" replace="/async/[!$&!]/g"?>
{% prettify dart %}
const oneSecond = Duration(seconds: 1);
// ···
Future<void> printWithDelay(String message) [!async!] {
  await Future.delayed(oneSecond);
  print(message);
}
{% endprettify %}

The method above is equivalent to:

<?code-excerpt "misc/test/samples_test.dart (Future.then)"?>
{% prettify dart %}
Future<void> printWithDelay(String message) {
  return Future.delayed(oneSecond).then((_) {
    print(message);
  });
}
{% endprettify %}

As the next example shows, `async` and `await` help make asynchronous code
easy to read.

<?code-excerpt "misc/test/samples_test.dart (await)"?>
{% prettify dart %}
Future<void> createDescriptions(Iterable<String> objects) async {
  for (var object in objects) {
    try {
      var file = File('$object.txt');
      if (await file.exists()) {
        var modified = await file.lastModified();
        print(
            'File for $object already exists. It was modified on $modified.');
        continue;
      }
      await file.create();
      await file.writeAsString('Start describing $object in this file.');
    } on IOException catch (e) {
      print('Cannot create description for $object: $e');
    }
  }
}
{% endprettify %}

You can also use `async*`, which gives you a nice, readable way to build streams.

<?code-excerpt "misc/test/samples_test.dart (async*)"?>
{% prettify dart %}
Stream<String> report(Spacecraft craft, Iterable<String> objects) async* {
  for (var object in objects) {
    await Future.delayed(oneSecond);
    yield '${craft.name} flies by $object';
  }
}
{% endprettify %}

[Read more](/guides/language/language-tour#asynchrony-support) about
asynchrony support, including async functions, `Future`, `Stream`,
and the asynchronous loop (`await for`).

{% endcomment %}


## Async

避免回调地狱（callback hell），使用 `async` 和 `await` 使代码更具可读性。

<?code-excerpt "misc/test/samples_test.dart (async)" replace="/async/[!$&!]/g"?>
{% prettify dart %}
const oneSecond = Duration(seconds: 1);
// ···
Future<void> printWithDelay(String message) [!async!] {
  await Future.delayed(oneSecond);
  print(message);
}
{% endprettify %}

上面的方法相当于:

<?code-excerpt "misc/test/samples_test.dart (Future.then)"?>
{% prettify dart %}
Future<void> printWithDelay(String message) {
  return Future.delayed(oneSecond).then((_) {
    print(message);
  });
}
{% endprettify %}

如下一个示例所示，`async` 和 `await` 有助于使异步代码变的易于阅读。

<?code-excerpt "misc/test/samples_test.dart (await)"?>
{% prettify dart %}
Future<void> createDescriptions(Iterable<String> objects) async {
  for (var object in objects) {
    try {
      var file = File('$object.txt');
      if (await file.exists()) {
        var modified = await file.lastModified();
        print(
            'File for $object already exists. It was modified on $modified.');
        continue;
      }
      await file.create();
      await file.writeAsString('Start describing $object in this file.');
    } on IOException catch (e) {
      print('Cannot create description for $object: $e');
    }
  }
}
{% endprettify %}

同样 `async*` 能够提供一个很棒的，可读的方式去构造 stream 。

<?code-excerpt "misc/test/samples_test.dart (async*)"?>
{% prettify dart %}
Stream<String> report(Spacecraft craft, Iterable<String> objects) async* {
  for (var object in objects) {
    await Future.delayed(oneSecond);
    yield '${craft.name} flies by $object';
  }
}
{% endprettify %}

[阅读更多](/guides/language/language-tour#异步支持) 关于异步支持的内容，
包括异步函数， `Future` ， `Stream` ， 以及异步循环 （ `await for` ）。


{% comment %}

## Exceptions

To raise an exception, use `throw`:

<?code-excerpt "misc/test/samples_test.dart (throw)"?>
{% prettify dart %}
if (astronauts == 0) {
  throw StateError('No astronauts.');
}
{% endprettify %}

To catch an exception, use a `try` statement with `on` or `catch` (or both):

<?code-excerpt "misc/test/samples_test.dart (try)"?>
{% prettify dart %}
try {
  for (var object in flybyObjects) {
    var description = await File('$object.txt').readAsString();
    print(description);
  }
} on IOException catch (e) {
  print('Could not describe object: $e');
} finally {
  flybyObjects.clear();
}
{% endprettify %}

Note that the code above is asynchronous;
`try` works for both synchronous code and code in an async function.

[Read more](/guides/language/language-tour#exceptions) about exceptions, including stack traces, `rethrow`, and the difference between
Error and Exception.

{% endcomment %}


## 异常

使用 `throw` 抛出一个异常：

<?code-excerpt "misc/test/samples_test.dart (throw)"?>
{% prettify dart %}
if (astronauts == 0) {
  throw StateError('No astronauts.');
}
{% endprettify %}

使用 `try` 语句以及 `on` 和 `catch`（或者两者），捕获一个异常。

<?code-excerpt "misc/test/samples_test.dart (try)"?>
{% prettify dart %}
try {
  for (var object in flybyObjects) {
    var description = await File('$object.txt').readAsString();
    print(description);
  }
} on IOException catch (e) {
  print('Could not describe object: $e');
} finally {
  flybyObjects.clear();
}
{% endprettify %}

请注意，上面的代码是异步的; 
同步代码以及异步函数代码中都能够使用 `try` 捕获异常。

[阅读更多](/guides/language/language-tour#异常) 关于异常的内容，
包括栈跟踪（ stack traces ）， `rethrow` ，以及 Error 和 Exception的区别。


{% comment %}

## Other topics

Many more code samples are in the
[language tour](/guides/language/language-tour) and the
[library tour](/guides/libraries/library-tour).
Also see the [Dart API reference,]({{site.dart_api}})
which often contains examples.

{% endcomment %}


## 其他主题

更多示例程序在
[语言概览](/guides/language/language-tour) 和
[库概览](/guides/libraries/library-tour) 中。
另请参阅 [Dart API reference,]({{site.dart_api}})，
其中通常包含示例程序。
