```c#
//užkomentuota eilutė

/* 
  užkomentuotas kodo blokas
*/

//paselectinus norimas eilutes ir CTRL + K + C jas visas užkomentuoja (windows)
//paselectinus norimas eilutes ir CTRL + K + U jas visas atkomentuoja (windows)
```

1. Parašyti programą, kuri nuskaito įvestą tekstą ir atspausdina jį ekrane. Atspausdintus duomenis rodyti, kol nepaspaudžiamas ENTER. 

```c#
//išvedame tekstą į Console
Console.WriteLine("Iveskite teksta:");

//nuskaitome tekstą iš Consolės ir pasidedame į kintamąjį
string tekstas = Console.ReadLine();

//išvedame tą, ką nuskaitėme ir pasidėjome į kintamąjį
Console.WriteLine(tekstas);

//čia programa sustoja ir laukia, kol kažką įvesime
//naudojame tam, kad nedingtų Console
Console.ReadLine();
```

2. Parašyti programą, kuri ATSKIRAI prašo įvesti vardą, pavardę, amžių ir atspausdina juos ekrane. Naudoti kintamuosius.

```c#
Console.WriteLine("Iveskite varda:");
string vardas = Console.ReadLine();

Console.WriteLine("Iveskite pavarde:");
string pavarde = Console.ReadLine();

Console.WriteLine("Iveskite amziu:");
string amzius = Console.ReadLine();

Console.WriteLine(vardas);
Console.WriteLine(pavarde);
Console.WriteLine(amzius);

Console.ReadLine();
```
3. Parašyti programą, kuri prašo įvesti apskritimo spindulį ir pagal jį suskaičiuoja jo ilgį ir plotą.

```c#
Console.WriteLine("Iveskite apskritimo spinduli:");
string spindulysTekstas = Console.ReadLine();

//pasiverciame nuskaitytą tekstą į skaičių, nes negalime teksto dauginti ir dalinti
double spindulys = double.Parse(spindulysTekstas);

double ilgis = 2 * Math.PI * spindulys;
double plotas = Math.PI * spindulys * spindulys;

Console.WriteLine("Apskritimo ilgis: " + ilgis);
Console.WriteLine("Apskritimo plotas: " + plotas);

Console.ReadLine();
```
4. Parašyti programą, kuri prašo įvesti atstumą (metrais) ir laiką (sekundėmis), o iš įvestų duomenų suskaičiuoja greitį km/h formatu.

```c#
Console.WriteLine("Iveskite atstuma metrais:");
string atstumasMetraisTekstas = Console.ReadLine();
double atstumasMetrais = double.Parse(atstumasTekstas);

Console.WriteLine("Iveskite laika sekundemis:");
string laikasSekundemisTekstas = Console.ReadLine();
double laikasSekundemis = double.Parse(laikasSekundemisTekstas);

double greitis = (atstumasMetrais / 1000) / (laikasSekundemis/3600);

Console.WriteLine("Greitis km/h: ", greitis);

Console.ReadLine();
```

5. Parašyti programą, kuri prašo įvesti vardą, pavardę ir gimimo vietą ir atspausdina juos ekrane tokiu formatu:

`Jonas Jonaitis deginasi Palangoje`

```c#
Console.WriteLine("Koks jusu vardas?");
string vardas = Console.ReadLine();

Console.WriteLine("Kokia jusu pavarde?");
string pavarde = Console.ReadLine();

Console.WriteLine("Kuriame mieste gimete?");
string miestas = Console.ReadLine();

Console.WriteLine(vardas + " " + pavarde + " deginasi " + miestas);

Console.ReadLine();
```
6. Parašyti programą, kuri prašo įvesti du skaičius ir patikrina ar jie lygūs. Rezultatą išvesti tokiu formatu: 

`skaičius1 ir skaičius2 yra lygūs/nelygūs`

```c#
Console.WriteLine("Iveskite pirma skaiciu:");
int skaicius1 = int.Parse(Console.ReadLine());

Console.WriteLine("Iveskite antra skaiciu:");
int skaicius2 = int.Parse(Console.ReadLine());

if(skaicius1 == skaicius2)
{
  Console.WriteLine("skaicius1 ir skaicius2 yra lygus.");
}
else 
{
  Console.WriteLine("skaicius1 ir skaicius2 yra nelygus.");
}

Console.ReadLine();
```
