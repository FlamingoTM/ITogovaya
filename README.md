# ITogovaya
Задача: написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Решение представляет собой консольное приложение на языке C#. Для запуска приложения необходимо открыть проект в среде разработки Visual Studio и нажать кнопку "Start". В файле README.md находится более подробное описание задачи и инструкции по запуску программы.


using System;

class Program {
  static void Main(string[] args) {
    Console.WriteLine("Введите элементы массива, разделяя их пробелом:");
    string[] input = Console.ReadLine().Split();

    int count = 0;
    for (int i = 0; i < input.Length; i++) {
      if (input[i].Length <= 3) count++;
    }

    string[] output = new string[count];
    int j = 0;
    for (int i = 0; i < input.Length; i++) {
      if (input[i].Length <= 3) output[j++] = input[i];
    }

    Console.WriteLine("Результирующий массив: [" + string.Join(", ", output) + "]");
  }
}