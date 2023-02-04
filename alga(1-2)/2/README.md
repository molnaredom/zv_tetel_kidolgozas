# Elemi adatszerkezetek, bináris keresőfák, hasító táblázatok, gráfok és fák számítógépes reprezentációja.

## Elemi adatszerkezetek
- ArrayList vs LinkedList
  - ArrayList: gyorsabb, kevesebb memória
  - LinkedList: módosító műveletekre jobb(UPDATE)
- SOR
- VEREM

## Bináris keresőfák

## Hasító táblázatok
![img.png](img.png)
- A tábla egy oszlop, ami eleinte üres és ebbe megpróbálunk számokat belehelyezni
- Kapunk egy szabáyt(képletet) és egy modulo értéket amikkel dolgozni fogunk:
- ![img_1.png](img_1.png)
  - Modulo = 10 = tábla hossza
  - Szabály = lineáris próba = (h(k) + i) mod N
    - Ahol i=iteráció_száma, N=modulo_érték, k=aktuális_szám
  
- Algoritmus:
  1. Kapunk egy számot (k) pl 46
  2. Lemodulózzuk (N számmal) 46 mod 10 = 6
  3. Megpróbáljuk beilleszteni a 6-os számú helyre
     - Ha sikerül(üres, nincs még szám beírva) --> continue; #Siker, ugrás a következő számra
     - Ha nem sikerül(már van szám beírva)
       - iv. A Szabályba behelyettesítünk
       - v. a kapott eredményt megpróbáljuk behelyettesítani 2. ponttól ismétlődik
         - Annyi iterációt megyünk ameddig nem lehet valahova betenni a számot a táblában.
  
- Pl:
  - 46, 34,42,23 bent van a táblában:
    - Modulo után 6, 4, 2, 3 helyek foglaltak
  - Megpróbáljuk az 52-t behelyezni
  - 52 mod 10 = 2
  - HOPPÁ a 2-es szám helyén már van szám a táblában
  - Jöjjön a szabály= (h(k) + i) mod N
  - h(k) = 2 , i=1 (mert a 1. iterációban vagyunk(0. az első)) N=10
  - (2 + 1) mod 10 = 3
  - Sajnos a 3 is foglalt :(, nézzük tovább
    - h(k) = 2 , i=2, N=10, (2 + 2) mod 10 = 4 --> Szintén foglalt
    - h(k) = 2 , i=3, N=10, (2 + 3) mod 10 = 5 --> Nem foglalt ---> betesszük az 5 ös helyre az 52-t

## Gráfok és fák számítógépes reprezentációja
- Fák
  - Alap infók: 
    - Fa = összefüggő, körmentes gráf
    - Gyökeres fa: van egy kitűntetett
      csúcsa, a gyökér
    - Bináris fa: gyökeres fa, ahol minden
      csúcsnak legfeljebb két gyereke van
  - Számítógépes reprezentáció: [261o]
    - **Csúcsokat és éleket reprezentálunk**
    - **Maga a fa egy mutató a gyökérre**