## Sąlygos

4. Parašyti programą, kuri nuskaito įvestą skaičių ir patikrina ar jis yra lyginis ar nelyginis.

```c#
Console.WriteLine("Iveskite naturaluji skaiciu: ");
int skaicius = int.Parse(Console.ReadLine());

var lyginis = skaicius % 2 == 0;

if(lyginis)
{
    Console.WriteLine("Skaicius yra lyginis.");
}
else 
{
    Console.WriteLine("Skaicius yra nelyginis.");
}
```
galima ir šitaip, išnaudojant [trinarį operatorių](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/conditional-operator):

```c#
Console.WriteLine("Iveskite naturaluji skaiciu: ");
int skaicius = int.Parse(Console.ReadLine());

Console.WriteLine("Skaicius yra " + (skaicius % 2 == 0 ? "lyginis" : "nelyginis"));

Console.ReadLine();
```

5. Parašyti programą, kuri nuskaito savaitės dienos numerį ir atspausdina jos žodinį pavadinimą ekrane.

```c#
Console.WriteLine("Iveskite savaites dienos numeri: ");
int savDienosNr = int.Parse(Console.ReadLine());

switch(savDienosNr){
    case 1:
        Console.WriteLine("Pirmadienis");
        break;
    case 2:
        Console.WriteLine("Antradienis");
        break;
    case 3:
        Console.WriteLine("Treciadienis");
        break;
    case 4:
        Console.WriteLine("Ketvirtadienis");
        break;
    case 5:
        Console.WriteLine("Penktadienis");
        break;
    case 6:
        Console.WriteLine("Sestadienis");
        break;
    case 7:
        Console.WriteLine("Sekmadienis");
        break;
    default:
        Console.WriteLine("Savaiteje yra tik septynios dienos!!!");
        break;
}

Console.ReadLine();
```

6. Parašyti programą kalkuliatorių, kuri nuskaito 2 skaičius, nuskaito matematinį veiksmą, atlieka veiksmą ir atspausdina rezultatą ekrane tokiu formatu:
```c# 
{pirmas skaicius} {matematinis veiksmas} {antras skaičius} = {rezultatas}
```

```c# 
Console.WriteLine("Iveskite pirma skaiciu: ");
int skaicius1 = int.Parse(Console.ReadLine());

Console.WriteLine("Iveskite operacija:");
string operacija = Console.ReadLine();

Console.WriteLine("Iveskite antra skaiciu:");
int skaicius2 = int.Parse(Console.ReadLine());

switch(operacija){
    case "+":
        Console.WriteLine(skaicius1 + " + " + skaicius2 + " = " + (skaicius1 + skaicius2));
        break;
    case "-":
        Console.WriteLine(skaicius1 + " - " + skaicius2 + " = " + (skaicius1 + skaicius2));
        break;
    case "*":
        Console.WriteLine(skaicius1 + " * " + skaicius2 + " = " + (skaicius1 + skaicius2));
        break;
    case "/":
        Console.WriteLine(skaicius1 + " / " + skaicius2 + " = " + (skaicius1 + skaicius2));
        break;
    case "%":
        Console.WriteLine(skaicius1 + " % " + skaicius2 + " = " + (skaicius1 + skaicius2));
        break;
    case "^":
        Console.WriteLine(skaicius1 + " ^ " + skaicius2 + " = " + Math.Pow(skaicius1, skaicius2));
        break;
    default:
        Console.WriteLine("Nesuprantu tokios operacijos.");
        break;
}

Console.ReadLine();
```

galima ir taip, bet VS turėtų siūlyti paversti į `switch`:

```c# 
Console.WriteLine("Iveskite pirma skaiciu: ");
int skaicius1 = int.Parse(Console.ReadLine());

Console.WriteLine("Iveskite operacija:");
string operacija = Console.ReadLine();

Console.WriteLine("Iveskite antra skaiciu:");
int skaicius2 = int.Parse(Console.ReadLine());

double rezultatas = 0;

if(operacija == "+") 
{
    rezultatas = skaicius1 + skaicius2;
}
else if(operacija == "-") 
{
    rezultatas = skaicius1 - skaicius2;
}
else if (operacija == "*")
{
    rezultatas = skaicius1 * skaicius2;
}
else if (operacija == "/")
{
    rezultatas = skaicius1 / skaicius2;
}
else if (operacija == "%")
{
    rezultatas = skaicius1 % skaicius2;
}
else if (operacija == "^")
{
    rezultatas = Math.Pow(skaicius1, skaicius2);
}

Console.WriteLine(skaicius1 + " " + operacija + " " + skaicius2 + " = " + rezultatas);

Console.ReadLine();
```


## Ciklas ```while```

1. Parašykite programą naudojant while ciklą, kuri išvestų 10 pirmų natūraliųjų skaičių.

```c#
int i = 1;
while(i <= 10) 
{
  Console.WriteLine(i);
  i++;
}
Console.ReadLine();
```

2. Parašyti programą naudojant `while` ciklą, kuri nuskaitinėja įvestus skaičius tol, kol jų suma nėra daugiau 50.

```c#
int sum = 0;
while(sum < 50) 
{
  int number = int.Parse(Console.ReadLine());
  sum += number;
  Console.WriteLine($"suma: {sum} ");
}
Console.ReadLine();
```

3. Sukurkite programą naudojant while ciklą, kuri apskaičiuotų dvejeto laipsnį 2n, kuris yra ne didesnis už teigiamą sveikąjį skaičių a. 
Pvz.: Jei a = 20, tai turi būti išvesta 16. Jei a = 1024, tai turi būti išvesta 1024.

```c#
Console.WriteLine("Iveskite skaiciu: ");
int sk = int.Parse(Console.ReadLine());

int laipsnis = 0;
while(sk > 1) 
{
  sk = sk / 2; //arba sk/=2;
  laipsnis++;
}

Console.WriteLine(Math.Pow(2, laipsnis));
Console.ReadLine();
```

## Ciklas ```do while```

1. Parašykite programą naudojant do while ciklą, kuri išvestų 10 pirmų natūraliųjų skaičių.

```c#
int i = 1;
do 
{
    Console.WriteLine(i);
    i++;
} 
while (i <= 10);
```

2. Parašykite programą naudojant do while ciklą, kuri suskaičiuotų, kiek skaitmenų turi duotas skaičius a.

```c#
Console.WriteLine("Iveskite skaiciu:");
int sk = int.Parse(Console.ReadLine());

int skaitmenuSkaicius = 0;

do 
{
   sk = sk / 10;
   skaitmenuSkaicius++;
} 
while(sk != 0);

Console.WriteLine($"Skaicius turi {skaitmenuSkaicius} skaitmenu.");
```

## Ciklas ```for```

1. Parašyti programą naudojant `for` ciklą, kuri suskaičiuoja pirmų 10 natūraliųjų skaičių sumą.

```c#
int sum = 0;
for (var i = 1; i <= 10; i++)
{
  sum += i;
}
Console.WriteLine($"suma: {sum}");
```

2. Parašyti programą naudojant for ciklą, kuri prašo įvesti natūralųjį skaičių ir atspausdina visus žemesnius natūraliuosius skaičius mažėjančia tvarka.

```c#
Console.WriteLine("Iveskite skaiciu:");
int sk = int.Parse(Console.ReadLine());

for (int i = sk - 1; i > 0; i--) 
{
    Console.WriteLine(i);
}
```

3. Parašyti programą naudojant for ciklą, kuri prašo įvesti skaičių ir atspausdina jo daugybos lentelę.

```c#
Console.WriteLine("Iveskite skaiciu:");
int sk = int.Parse(Console.ReadLine());

for (int i = 1; i <= 10; i++) 
{
    Console.WriteLine($"{sk} * {i} = {sk*i}");
}
```
4. Parašyti programą naudojant for ciklą, kuri prašo įvesti piramidės aukštį ir atspausdina skaičių piramidę tokiu formatu:

```
1 
2 3 
4 5 6 
7 8 9 10 
```

```c#
Console.Write("Iveskite eiluciu skaiciu: ");
var eiluciuSk = int.Parse(Console.ReadLine());
int isvedamasSkaicius = 1;

//einame per eilutes ir spausdiname skaicius
for (var i = 1; i <= eiluciuSk; i++)
{
    //eiluteje esanciu skaiciu turi buti ne daugiau nei eilutes nr (i)
    for (var j = 1; j <= i; j++)
    {
        Console.Write($"{isvedamasSkaicius} ");
        //kaskarta isvede skaiciu, ji padidiname
        isvedamasSkaicius++;
    }

    Console.Write("\n");
}

Console.ReadLine();
```

## ```break``` ir ```continue```

1. Parašykite programą, kuri iteruoja per pirmus 20 natūraliųjų skaičių, skaičiuoja jų sumą ir išeina iš ciklo, kai suma tampa didesnė už 15. (break)

```c#
int suma = 0;

for (int i = 1; i <= 20; i++)
{
    suma += i;
    Console.WriteLine($"{i}. suma = {suma}");

    if (suma > 15)
        break;
}
```

2. Parašykite programą, kuri išves visus skaičius nuo 1 iki 17, išskyrus 7 ir 13. (continue)

```c#
for (int i = 1; i <= 17; i++)
{
    if(i == 7 || i == 13)
        continue;
    Console.WriteLine(i);
}
```

## masyvai

1. Parašyti programą, kuri nuskaito 10 elementų į masyvą ir jį atspausdina.

```c#
int[] skaiciai = new int[10];

for (int i = 0; i < skaiciai.Length; i++)
{
    Console.WriteLine("Iveskite skaiciu:");
    int sk = int.Parse(Console.ReadLine());
    skaiciai[i] = sk;
}

for (int i = 0; i < skaiciai.Length; i++)
{
    Console.Write($"{skaiciai[i]} ");
}
```

2. Parašyti programą, kuri prašo įvesti masyvo dydį ir tada nuskaito n elementų į masyvą ir atspausdina jį atvirkščiai.

```c#
 Console.WriteLine("Iveskite masyvo dydi:");
int n = int.Parse(Console.ReadLine());

int[] elementai = new int[n];

for (int i = 0; i < elementai.Length; i++)
{
    Console.WriteLine("Iveskite skaiciu:");
    int sk = int.Parse(Console.ReadLine());
    elementai[i] = sk;
}

for (int i = n - 1; i >= 0; i--)
{
    Console.Write($"{elementai[i]} ");
}
```

