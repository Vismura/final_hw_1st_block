# Итоговая работа 1 четверти

## Задача

---

### Написать программу, которая из имеющегося массива строк формирует массив из строк, длина которых меньше либо равна 3 символа. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решение не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами

---

## Описание алгоритма решения

---

### Сначала формируется два массива: первый и второй такой же длины. Потом метод, в котором цикл соразмерный длине массива, внутри цикла проверка условия ( <=3 ), если да, то элемент первого массива заносится в count, элемент второго массива. Переменная count чтобы поочередно закидывать из первого массива во второй. После присвоения увеличивается переменная count на 1 и возвращается к циклу for в котором i увеличивается на 1. И так проверяется до конца

---

### Графическое представление метода

![diagram](https://github.com/Vismura/final_hw_1st_block/blob/ec5194b0622e8c5c0cc1fdebeb9c29499baac50a/diagram.drawio.png?raw=true)

### Реализация алгоритма

```
internal class Program
{
    private static void Main(string[] args)
    {
        string[] array1 = new string[8] {"1234", "1567", "-2", "computer science", "hello", "2", "world", ":-)"};
        string[] array2 = new string[array1.Length];
        void SecondArrayWithIF(string[] array1, string[] array2)
        {
            int count = 0;
            for (int i = 0; i < array1.Length; i++)
            {
                if (array1[i].Length <= 3)
                {
                    array2[count] = array1[i];
                    count++;
                }
            }
        }
        void PrintArray(string[] array)
        {
            for (int i = 0; i < array.Length; i++)
            {
                Console.Write($"{array[i]} ");
            }
            Console.WriteLine();
        }
        SecondArrayWithIF(array1, array2);
        PrintArray(array2);
    }
}
```
