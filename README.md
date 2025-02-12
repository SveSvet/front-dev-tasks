# front-dev-tasks
Some tasks for Frontend developer

## Задача 1. 
Необходимо преобразовать его в структуру, 
где данные будут сгруппированы по одному из полей(кроме id),
внутри сформированной группы должен лежать объект(или Map), 
ключами в котором должно быть поле id,
а значением объект из исходного массива с соответствующим полем id,
не включая само поле id.

```typescript
const data = [
  { id: 1, age: 20, name: "Иван", country: "Russia", registred: true },
  { id: 2, age: 30, name: "Дима", country: "USA", registred: true },
  { id: 3, age: 25, name: "Леха", country: "Russia", registred: false },
  { id: 4, age: 20, name: "Леха", country: "USA", registred: false },
  { id: 5, age: 30, name: "Иван", country: "Russia", registred: true },
  { id: 6, age: 50, name: "Леха", country: "Russia", registred: true },
  { id: 7, age: 20, name: "Дима", country: "USA", registred: false },
];

console.log(foo(data, "country"));
/*
{
  Russia: {
    '1': { age: 20, name: 'Иван', country: 'Russia', registred: true },
    '3': { age: 25, name: 'Леха', country: 'Russia', registred: false },
    '5': { age: 30, name: 'Иван', country: 'Russia', registred: true },
    '6': { age: 50, name: 'Леха', country: 'Russia', registred: true }
  },
  USA: {
    '2': { age: 30, name: 'Дима', country: 'USA', registred: true },
    '4': { age: 20, name: 'Леха', country: 'USA', registred: false },
    '7': { age: 20, name: 'Дима', country: 'USA', registred: false }
  }
}
*/
```

## Задача 2. 
Конвертация строки в разные стили написания

```typescript
Написать функцию convertCase, которая принимает два аргумента:

Строку (например, "Hello world, how are you?")
Формат ("camel", "snake", "kebab")
Функция должна возвращать строку в указанном формате.

Пример работы:

console.log(convertCase("Hello world, how are you?", "camel")); // "helloWorldHowAreYou"
console.log(convertCase("Hello world, how are you?", "snake")); // "hello_world_how_are_you"
console.log(convertCase("Hello world, how are you?", "kebab"));
```

Подсказки: 
- Регулярка, чтобы убрать все буквы и не цифры: `/[^a-zA-Z0-9\s]/g, ""`
- Регулярка, чтобы разбить по пробелам: `/\s+/`
