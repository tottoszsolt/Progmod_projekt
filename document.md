# Projektmunka dokumentáció
A program egy mátrixot generál, ahol minden cella értéke random módon generáltan 0, 1 vagy 2 lehet. A program feladata az, hogy a mátrixot bejárja úgy, hogy az első cellától (0, 0) indulva a lehető legkevesebb pontot gyűjtse össze a mátrix utolsó cellájáig (rows-1, columns-1).

A program az útvonal kiválasztásához a Greedy módszert alkalmazza. Minden lépésnél megvizsgálja, hogy jobbra és lefelé haladva melyik lépés adja a kisebb pontszámot. Ha jobbra vagy lefelé lehet lépni a mátrixon belül, akkor az a lépés választódik ki, amelyik a kisebb pontszámot eredményezi.

A program ezt addig folytatja, amíg el nem éri a mátrix utolsó celláját. A választott útvonalat kiírja a konzolra, valamint visszaadja a gyűjtött pontok összegét.

Ez a megoldás garantálja, hogy a program a lehető legkevesebb pontot gyűjti össze a mátrix megfelelő bejárásával.


 # A mátrix oszlopainak, és sorainak bekérése
<img width="631" alt="image" src="https://github.com/tottoszsolt/Progmod_projekt/assets/43206967/6b2e49ff-e386-44dc-bc3a-6d06282acb40"> <br />

Scanner segítségével bekértem a felhasználótól egy "oszlop" (column), és egy "sor" (row) adatot, amelyet egy változóban tároltam el.
Ezek után, létrehoztam egy mátrix változót, amely megkapta a fenti mezők értékét. Ez lényegében az üres mátrixom. 

 # A mátrix feltöltése elemekkel, a kész mátrix kiíratása, illetve a pontszám kiíratása
 <img width="649" alt="image" src="https://github.com/tottoszsolt/Progmod_projekt/assets/43206967/ef76ff8a-4b32-432d-bd0f-5b530063ec69"> <br />
Mint látható, egy egyszerű for ciklussal bejárom a tömböt, majd ezek után feltöltöm minden elemét véletlenszerűen egy egész integerrel, 0 és 3 között. 
Ezek mellett kiíratom a megszerzett pontokat, valamint a feltöltött mátrixot az elemeivel együtt.

# "Lépkedés" a mátrixon belül, pontok összeadása
<img width="888" alt="image" src="https://github.com/tottoszsolt/Progmod_projekt/assets/43206967/29bf2c26-dcc5-4e50-b303-ed71cd3ab9dc">
Egy while ciklussal bejárjuk a tömböt, egészen addig amíg nem értünk az oszlop vagy a sor utolsó eleméhez, tehát gyakorlatilag a mátrix jobb alsó sarkában a végéhez. 
Egy integer változóban tároltam a jobbra mozgást illetve vizsgálatot. Ugyan ez a séma a lefelé mozgásnál. Lényegében az algoritmus megnézi hogy az aktuális mezőtől jobbra nagyobb-e a szám mint ami alatta van, amennyiben igen, akkor lefelé megy, ha nem, akkor jobbra. Minden egyes lépésnél hozzáadja az adott mező értékét a "pont" változóhoz, így gyűjtve pontokat. 
