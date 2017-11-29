# PHP

## Пример 1

```php
Trait Debugger {
  public function __toString() {
    return $this->name;
  }
}

Class Person extends StdClass {
  use Debugger;
  protected $name = 'Nobody';
  public function __construct($name) {
    return $name;
  }
}

$pers1 = new Person('Ilya');
$pers2 = new Person('Anton');

printf('%s, %s', $pers1, $pers2);
// что будет выведено?
```

## Пример 2

```php
function foo() {
  static $x = 1;
  echo $x++ * 2;
}

foo();
foo();
foo();
// что будет выведено?
```

## Пример 3

```php
ob_start();
  echo "Test message";
  $output = ob_end_clean();
echo $output;
// что будет выведено?
```

# Javascript

```js
var user1 = {name: "Ilya", age: 32};
var user2 = user1;
user2.name = "Anton";
user2.age = 26;
console.log(user1['age'] - user2.age);
// что будет выведено?
```

# MySQL

## Пример 1

```
mysql> select * from data;
+------+
| val  |
+------+
|    0 |
|    1 |
|    2 |
| NULL |
+------+
4 rows in set (0,00 sec)

mysql> select avg(val) from data; -- что будет выведено?
```

## Пример 2

```
mysql> select  * from t_1;
+------+
| val  |
+------+
|    1 |
|    2 |
|   10 |
+------+
3 rows in set (0.00 sec)

mysql> select  * from t_2;
+------+
| val  |
+------+
|    1 |
|    2 |
+------+
2 rows in set (0.00 sec)

-- Как найти строки, отсутствующие в таблице t_2?
```

# Linux

1. Какой командой узнать, где находится php?
2. Как узнать, кто внес правку в определенную строку кода?
3. Как перезапустить сервер MySQL?


# Поболтать - из резюме

> Проектирование и создание БД (Postgresql/Mysql)

Какие сильные стороны Postgresql по сравнению с Mysql ты бы мог выделить?

> Разработка и документирование модульного проекта на Phalcon с нуля;

Для кого и как писалась документация?

> администрирование проектов, выкат релизов ... codereview

Каким способом принималась работа и делался кодревью?
