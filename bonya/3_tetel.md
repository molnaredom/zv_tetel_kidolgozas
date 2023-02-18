# Visszavezetés:
- hatékony visszavezetés akkor, ha Polinom időben történik
- Úgy kell átalakítani, hogy választartó legyen
  - Igen példányból igen példányt
  - Nem példányból nem példányt kell készíteni


- Algoritmusok
  - Megállás:
    - A program minden inputra megáll (tehát nem esik végtelen ciklusba)
  - Hamilton-út
    - Minden csúcsot pontosan egyszer érintek, úgy megyek végig a gráfon
  - SAT
    - Konjuktív normálformájú, ítélet-kalkulus beli formulák
      - Pl: (x1 V x2)  ∧(x3 V x2)  ∧(x1 V x4)
    - Típusai:
      - 2SAT
      - 3SAT
  - Klikk
    - Van e `k` db olyan csúcs amelyek páronként szomszédosak = **mindegyik csúcs össze van kötve mindegyikkel**
  - Csúcslefedés
    - Kiválasztom csúcsoknak egy halmazát( pl 1 es 4 es , 6 os csúcs nem muszaly hogy egymas mellett levo csucsok legyenek)
      - Egy csúcs lefedi a tőle 1 egységnyi távolságra lévő pontokat
  - Halmazlefedés
    - Ki tudok e választani/ meg tudok e adni `k` halmazt úgy hogy minden  pontot lefedjenek 
      - Nem lehet olyan pont ami nincs lefedve egy halmazzal sem
    - A halmazok már adottak, ezekbol kell kivalasztani(nem mi adjuk meg a halmazokat)
  - Halmazpakolás
  - 3 Színezés
    - Van egy grafod 3 szinre kell kiszinezni a szomszedok nem lehetnek ugyanolyan szinuek
  - Egész értékű programozás
  - Független csúcshelmaz
  - Domináns csúcshalmaz
  - Euler út:
    - Minden ponton pontosan egyszer mehetek végig a gráfon
  - Párosítás
    - Van 2 oszlop abban elemek, a bal oldalból minden elemhez talűlni kell egy párt a jobb oldalhoz
    - Pl a Fekete péter egy nem példány, a Memóriajáték egy Igen példány
  - Hármasítás
    - Hasonlít  a párosításhoz
    - 3 oszlpod van, olyan hármasokat kell találni, hogy ne használjunk fel kétszer egy elemet sem és mindenkit valahovaoszani kell


# Nemdeterminizmus
  - Def(adam): végtelen számú párhuzamosítás lehetséges idő romlás nélkül
- P osztály:
  - Összes polinom időben eldönthető problémák,
- NP osztály:
  - Nemdeterminisztikusan polinom időben eldönthető problémák
  - Nemdeterminisztikus modon polinom idoben eldol

