---
title: Dart 语言中常见符号和语法详解
author: chatgpt
date: 2023-12-12 20:03:00 +0800
categories: [Learn]
tags: [dart]
pin: true
math: true
mermaid: true
---

Dart 是一种现代化的编程语言，广泛用于移动应用和 Web 开发。在 Dart 的开发中，你可能会遇到一些特殊的符号和语法，这些符号提供了便捷的方式来表达一些常见的操作。本文将深入解析一些常见的 Dart 符号和语法，帮助你更好地理解和编写 Dart 代码。

## 1. 两个点 `..`：级联操作符

级联操作符 `..` 允许对同一个对象执行一系列操作，而不需要重复引用该对象。这使得代码更加简洁，减少了对相同对象的重复引用。下面是一个简单的例子：

```dart
class Person {
  String name = '';
  int age = 0;
}

void main() {
  var person = Person()
    ..name = 'John'
    ..age = 30;

  print('${person.name} is ${person.age} years old.');
}
```

在这个例子中，级联操作符 `..` 允许我们在同一个对象 `person` 上执行多个操作，而不需要多次引用它。

## 2. 感叹号 `!`：非空断言

感叹号 `!` 用于告诉 Dart 编译器一个表达式的结果不会为空（null）。这在处理可能为空的变量时非常有用，同时避免了编译器的空值警告。以下是一个示例：

```dart
String? nullableString = 'Hello';
String nonNullableString = nullableString!; // 非空断言

print(nonNullableString.length);
```

在这个例子中，我们使用了非空断言 `!` 来告诉编译器 `nullableString` 不会为空。

## 3. 加叹号和加点 `!.`：非空调用
   - 用于在 Dart 空安全语法中调用可能为空的对象的属性或方法，同时告诉编译器在此处确保对象不为空。

   ```dart
   String? nullableText = 'Flutter';
   print(nullableText!.length); // 非空调用，告诉编译器对象不为空
   ```

## 4. 问号 `?`：空安全相关

问号 `?` 是 Dart 中空安全特性的一部分，主要用于处理可能为空的变量。它有多种用法，包括可空类型声明、非空断言、条件表达式等。以下是一些示例：

```dart
String? nullableText = 'Flutter';

// 空安全调用
print(nullableText?.length);

// 空合并运算符
String nonNullableText = nullableText ?? 'Default Value';
```

## 5. 问号加点 ?.
   - 使用 `?.` 可以安全地调用对象的属性或方法，如果对象为 `null`，则整个表达式的值为 `null`，而不会抛出空指针异常。

   ```dart
   String? possiblyNullString = someObject?.stringValue;
   ```

## 7. 美元符号 `$`：字符串插值

美元符号 `$` 在 Dart 中用于字符串插值，允许在字符串中引用变量或表达式的值。以下是一些示例：

```dart
String name = 'John';
print('Hello, $name!'); // 输出: Hello, John!

int x = 5;
int y = 10;
print('The sum of $x and $y is ${x + y}.');
```

美元符号 `$` 使得在字符串中引用变量或表达式的值变得更加简便，提高了代码的可读性。

通过深入理解这些 Dart 符号和语法，你将更好地掌握 Dart 语言的特性，提高在 Dart 中的编程效率。希望本文对你理解 Dart 语言中的常见符号有所帮助。如果有任何问题或需要进一步的解释，请随时提问。 Happy coding!


## Reference

* [Dart Operators](https://dart.dev/language/operators)
* [Dart Class](https://dart.dev/language/classes)