1. Apibrėžti ir priskirti reikšmes dvimačiam bool masyvui, kuris turi 4 eilutes ir 7 stulpelius ir atspausdinti jį ekrane. (Jei elemento reikšmė true - tai *, jei false, tai -).

```
---*---
--*-*--
-*-*-*-
*-*-*-*
```
```c#
bool[,] manoMasyvas = new bool[4, 7] 
{
    { false, false, false, true, false, false, false },
    { false, false, true, false, true, false, false },
    { false, true, false, true, false, true, false },
    { true, false, true, false, true, false, true}
};

for (int i = 0; i < 4; i++){
    for (int j = 0; j < 7; j++)
    {
        Console.Write($"{(manoMasyvas[i,j] ? "*": "-")}");
    }
    Console.WriteLine();
}

Console.ReadLine();
```
##Kartojam

###level 1

1. Deklaruokite sveikų skaičių masyvą kuriame bus 10 skaičių. Įdėkite po vieną į masyvą skaičius, šitaip: ```c# masyvas[indeksas] = 10;```

```c#
int[] skaiciai = new int[10];
skaiciai[0] = 7;
skaiciai[1] = 8;
skaiciai[2] = 19;
skaiciai[3] = 7;
skaiciai[4] = 8;
skaiciai[5] = 19;
skaiciai[6] = 7;
skaiciai[7] = 8;
skaiciai[8] = 19;
skaiciai[9] = 19;
```

2. Deklaruokite tekstų masyvą, kuriame bus 5 tekstai (string). Deklaruojant iš karto ir nurodykite šių tekstų reikšmes (tarp riestinių skliaustų).

```c#
string[] tekstai = { "viens", "du", "trys", "keturi", "penki" };
```

3. Atspausdinkite kiekvieną tekstų masyvo elementą naudojantis for ciklu.

```c#
for (int i = 0; i < tekstai.Length; i++)
{
    Console.WriteLine(tekstai[i]);
}
```

4. Atspausdinkite kiekvieną skaičių masyvo elementą pakeltą kvadratų, t.y. Jei masyve turite skaičius 1, 2 , 3 ir t.t., tai atspausdini turite 1, 4, 9 ir t.t.

```c#
for (int i = 0; i < skaiciai.Length; i++)
{
    Console.WriteLine(skaiciai[i] * skaiciai[i]);
}
```

###level 2

1. Deklaruokite skaičių masyvą, kuriame bus 15-a skaičių - neigiamų ir teigiamų.

```c#
int[] skaiciai = { 1, 0, -10, -4, 19, 4, 5, -4, -3, 9, 10, -5, -3, 1, 2 };

for (int i = 0; i < skaiciai.Length; i++)
{
    Console.Write(skaiciai[i] + " ");
}
Console.WriteLine();
```

2. Atspausdinkite masyvą vienoje eilutėje palikdami tarpus tarp skaičių.

```c#
for (int i = 0; i < skaiciai.Length; i++)
{
    Console.Write(skaiciai[i] + " ");
}
Console.WriteLine();
```

3. Raskite masyve didžiausią skaičių ir atspausdinkite jo indeksą.

```c#
int maxI = 0;

for (int i = 0; i < skaiciai.Length; i++)
{
    if (skaiciai[i] > skaiciai[maxI])
    {
        maxI = i;
    }
}
```

4. Suskaičiuokite, kiek masyve yra neigiamų skaičių.

```c#
int neigiamuSk = 0;

for (int i = 0; i < skaiciai.Length; i++)
{
    if (skaiciai[i] < 0)
    {
        neigiamuSk++;
    }
}
```

5. Paverskite masyve visus neigiamus skaičius teigiamais, o teigiamus - neigiamais ir atspausdinkite masyvą iš naujo.

```c#
for (int i = 0; i < skaiciai.Length; i++)
{
    skaiciai[i] = skaiciai[i] * -1;
}
```
