# Тема 8. Основы объектно-ориентированного программирования
Отчет по Теме № 8 выполнила:
- Аликина Дарья Андреевна
- АИС-23-1

| Задание | Лаб_раб | Сам_раб |
| ------ |---------|---------|
| Задание 1 | +       | +       |
| Задание 2 | +       | +       |
| Задание 3 | +       | +       |
| Задание 4 | +       | +       |
| Задание 5 | +       | +       |

знак "+" - задание выполнено; знак "-" - задание не выполнено;



## Лабораторная работа №1
### Создайте класс “Car” с атрибутами производитель и модель. Создайте объект этого класса. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

my_car = Car("Toyota", "Corolla")
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/1.png)

### Выводы

Создаём класс “Car” с атрибутами производитель и модель

## Лабораторная работа №2
### Дополните код из первого задания, добавив в него атрибуты и методы класса, заставьте машину “поехать”. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car("Toyota", "Corolla")
my_car.drive()
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/2.png)

### Выводы

В код добавляем метод drive

## Лабораторная работа №3
### Создайте новый класс “ElectricCar” с методом “charge” и атрибутом емкость батареи. Реализуйте его наследование от класса, созданного в первом задании. Заставьте машину поехать, а потом заряжаться. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")
my_car = Car("Toyota", "Corolla")
my_car.drive()

class ElectricCar(Car):
    def __init__(self, make, model, battery_capacity):
        super().__init__(make, model)
        self.battery_capacity = battery_capacity

    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

my_electric_car = ElectricCar("Tesla", "Model S", 75)
my_electric_car.drive()
my_electric_car.charge()
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/3.png)

### Выводы

Создаём новый класс “ElectricCar” с методом “charge” и атрибутом ёмкость батареи
  
## Лабораторная работа №4
### Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поехать. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.


```python
class Car:
    def __init__(self, make, model):
        self._make = make
        self.__model = model

    def drive(self):
        print(f"Driving the {self._make} {self.__model}")

my_car = Car("Toyota", "Corolla")

print(my_car._make)
my_car.drive()
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/4.png)

### Выводы

В код добавляем инкапсуляцию, сделав атрибуты приватными

## Лабораторная работа №5
### Реализуйте полиморфизм создав основной (общий) класс “Shape”, а также еще два класса “Rectangle” и “Circle”. Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.

```python
class Shape:
    def area(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius


print(Rectangle(4, 5).area())
print(Circle(3).area())
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/5.png)

### Выводы

В код добавляем два класса наследника, применяем полиморфизм

## Самостоятельная работа №1
### Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Dog:  
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(f"{self.name} кушает!")


my_dog = Dog("Джессика", 2)

my_dog.bark()
print(f"Возраст: {my_dog.age} года")
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/11.png)

### Выводы

Данный код  создает собаку Джессика, её возраст и её действие
  
## Самостоятельная работа №2
### Самостоятельно создайте атрибуты и методы для ранее созданного класса. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Dog:
    def __init__(self, name, breed, weight):
        self.name = name
        self.breed = breed
        self.weight = weight
        self.is_hungry = True

    def eat(self):
        if self.is_hungry:
            print(f"{self.name} кушает")
            self.is_hungry = False
        else:
            print(f"{self.name} уже сыта")

    def play(self):  # Метод игры
        print(f"{self.name} играет с мячиком")
        self.is_hungry = True

my_dog = Dog("Джессика", "Пекинес", 1)

my_dog.eat()
my_dog.play()
print(f"Порода: {my_dog.breed}")
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/12.png)

### Выводы

Данный код создает собаку Джессика, кормит её, играет с ней и в итоге пишет породу собаки
  
## Самостоятельная работа №3
### Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Dog:
    def __init__(self, name, breed, weight):
        self.name = name
        self.breed = breed
        self.weight = weight
        self.is_hungry = True

    def eat(self):
        if self.is_hungry:
            print(f"{self.name} кушает")
            self.is_hungry = False
        else:
            print(f"{self.name} уже сыта")

    def play(self):
        print(f"{self.name} играет с мячиком")
        self.is_hungry = True


class Puppy(Dog):
    def __init__(self, name, breed, weight, favorite_toy):
        super().__init__(name, breed, weight)
        self.favorite_toy = favorite_toy

    def sleep(self):
        print(f"{self.name} крепко спет с {self.favorite_toy}")

    def play(self):
        print(f"{self.name} весело играет с {self.favorite_toy}")
        self.is_hungry = True


adult_dog = Dog("Джессика", "Пекинес", 2)
puppy = Puppy("Атос", "Дворняга", 5, "плюшевым мишкой")

adult_dog.play()
puppy.play()
puppy.sleep()
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/13.png)

### Выводы

Данный код создает взрослую собаку и щенка и заставляет их играть по-разному
  
## Самостоятельная работа №4
### Самостоятельно реализуйте инкапсуляцию, продолжая работать с ранее созданным классом. Она должна отличаться, от того, что указана в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Dog:
    def __init__(self, name, breed):
        self.name = name  
        self._breed = breed
        self.__age = 0

    def set_age(self, age):
        if age > 0:
            self.__age = age
        else:
            print("Возраст должен быть положительным")

    def get_age(self):
        return self.__age

    def _get_breed(self):
        return self._breed

my_dog = Dog("Джессика", "Пекинес")

my_dog.set_age(2)
print(f"Имя: {my_dog.name}")
print(f"Возраст: {my_dog.get_age()} года")
```
### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/14.png)

### Выводы

Данный код создает собаку Джессика, устанавливает ей возраст, выводит имя и возраст
  
## Самостоятельная работа №5
### Самостоятельно реализуйте полиморфизм. Он должен отличаться, от того, что указан в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python
class Dog:
    def sound(self):
        return "Гав-гав!"

class Cat:
    def sound(self):
        return "Мяу-мяу!"

class Cow:
    def sound(self):
        return "Му-у-у!"

def make_sound(animal):
    print(animal.sound())

animals = [Dog(), Cat(), Cow()]

for animal in animals:
    make_sound(animal)
```

### Результат.

![Меню](https://github.com/daryaalikina2005-arch/Tema8/blob/master/8/15.png)

### Выводы

Данный код создает разных животных и заставляет каждого издать свой характерный звук

## Общие выводы по теме
Я базово освоила тему ооп на языке программирования python. Также практика на python помогла закрепить изученный материал
