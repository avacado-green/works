using System;

class Program
{
    static void Main()
    {
        //Ввод данных в консоль 
        Console.WriteLine("Введите строки, разделенные пробелами:");
        string input = Console.ReadLine();
        string[] array = input.Split(' ');
        //Преобразование массива
        string[] newArray = new string[array.Length];
        int newIndex = 0;
        //Условие действий при которых будет совершен цикл 
        for (int i = 0; i < array.Length; i++)
        {
            if (array[i].Length <= 100)
            {
                newArray[newIndex] = array[i];
                newIndex++;
            }
        }

        Array.Resize(ref newArray, newIndex);
        //Вывод данных
        Console.WriteLine("Новый массив строк, длина которых меньше или равна 100 символам:");
        foreach (string str in newArray)
        {
            Console.WriteLine(str);
        }
    }
}

