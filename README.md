#Ülesanne 1: Binaarpuu Implementatsioon
Ei osanud koodi kirjutada. 
Ülesanne 2: Kuhja (Heap) Struktuuri Teoreetiline Analüüs 
● Kirjelda min-kuhja ja max-kuhja struktuuride teoreetilisi omadusi. 
Min-kuhi:
Iga tasand on täiendatud vasakult paremale ja sõlmede võtmed on väiksed või võrdsed oma laste võimetega
Max-kuhi:
Täielik binaarne puu struktuur, iga sõlme võti on suurem või võrdne lastega.

● Analüüsi nende struktuuride aja- ja ruumikomplekssust. 
Nad on sarnased, kus mõlemal viisil on (n on kuhja suurus).
Sisestamine: O(log n);
Eemaldamine: O(log n);
Ehitamine: O(n);
Otsing: O(n).

● Aruta, kuidas kuhja struktuurid sobivad andmete sorteerimiseks ja prioriteetjärjekordade haldamiseks. 

Min-kuhi:
Kuhja iga sõlme väiksem element asub puu juures ning kui eemaldatakse min-kuhi juur, saab kõige väiksema elemendi, mis sobib sorteerimiseks. Sobib hästi Heapsort algoritmi jaoks. Min kuhi otsib väiksemat elementi ja max kuhi suurimat. Dijkstra kasutab min-kuhja.

Max-kuhi:
Kuhja iga suurem element asub puu juures ining eemaldatakse max-kuhja juur, saab kõige suurema elemendi, mis sobib sorteerimiseks.
Ülesanne 3: Binaarse Otsingupuu (Binary Search Tree, BST) Teoreetiline Analüüs 
● Kirjelda binaarse otsingupuu (BST) andmestruktuuri ja selle põhielemente. 
Kasutatakse kui andmed tuleb salvestada sorteeritud kujul või kui on vaja kiiret otsingut, sisestamist ja kustutamist. Sõlmedel võib olla rohkem kui kaks last.
Põhielemendid on Sõlm, Juur, Lehed, Vasak ja Parem alampuu, Vanem.
● Arutle, kuidas tasakaalustamata puud mõjutavad BST tõhusust ja kuidas seda saab teoreetiliselt optimeerida. 
Tasakaalustamata puud muudavad BST ebaefektiivseks. Puu on ebatasakaalus, mis võib tähendada seda, et see tekitab halvema otsimis ja lisaaega. Seda saab optimeerida, kui kasutada AVL või Pun-Must puu otsingupuud, mis säilitavad tasakaalu tagamiseks kindlaid reegleid. AVL puu tagab, et iga sõlme tasakaalu (vasaku ja parema alampuu kõrguste erinevus) erinevus on maksimaalselt kõrgemal kui 1. Pun-must puu kasutab värve, et tagada puu tasakaalustus.
Ülesanne 4: Punase-Musta Puu (Red-Black Tree) Teoreetiline Ülevaade 
● Kirjelda punase-musta puu andmestruktuuri ja selle peamisi omadusi. 
Punase - musta puu andmestruktuur on tasakaalustatud binaarne otsingupuu, kus igal sõlmel on värv (peale selle, et need on seotud ka informatsiooniga).  Algoritm säilitab tasakaalu nii, et puu jääb tasakaalu ka pärast lisamist või kustutamist, kehtestades teatud reeglid värvidele ja seeläbi orienteerudes.
Omadused:
Sõlmede värvimine Punasteks ja Mustadeks sõlmedeks.
Juursõlm on must.
Lehed on mustad.
Kui sõlm on punane, siis kõik lapsed on mustad.
Et tasakaalustada lisatakse ja eemaldatakse sõlmi.
● Võrdle teoreetiliselt punase-musta puu ja binaarse otsingupuu tõhusust. 
Punane-must puu on tõhusam, siis kui tegu pole väga suute andmehulgaga. BST on aga tõhusam suurte andmemahtudega aga tasakaal sõltub sisestatud andmetest. Samas Punane-must tagab lühemad otsinguteed ehk üleüldiselt kiirem ning värvireeglite jälgimisel on võimalik neid ka taastada.

● Aruta, kuidas punase-musta puu tasakaalustamine ja värvireeglid aitavad kaasa andmestruktuuri tõhususele.
Värvireeglid aitavad teha pöördeid ja muudatusi, et taastada mingi sõlme lisamisel tasakaal. Need võimaldavad kiireid otsinguid ja tõhusaid lisamise/kustutamise operatsioone isegi suurte andmemahtude korral, samas säilitavad sügavust ja tagavad optimaalse otsinguaja. Tagab andmetervikluse.

Ülesanne 5: AVL Puu vs. Punase-Musta Puu Teoreetiline Võrdlus 
● Kirjelda AVL puu andmestruktuuri ja selle peamisi omadusi. 
Omadused:
AVL puu andmestruktuuril peab olema sõlmede kõrguste erinevus maksimaaslet 1, tagades nii tasakaalu. Operatsioonid võtavad aega O(log n).
● Võrdle teoreetiliselt AVL puu ja punase-musta puu tõhusust. 
Mõlemad struktuurid tagavad tasakaalu ja kiireid otsinguid. Punase-musta puul võib olla vähem tasakaalustamisoperatsioone, sest on AVL puuga võrreldes reeglite kohapealt lihtsam ja efektiivsem. AVL on tasakaalustamisel rangem kuid võib nõuda rohkem mäluruumi.

● Analüüsi, millistes rakendustes oleks üks struktuur teisele eelistatav ja põhjenda oma valikuid. 
Otsingupõhistes rakendustes oleks hea kasutada mõlemat, sest tagavad kiire otsingu. Kui mängu tuleb sagdane lisamine või kustutamine, siis sobiks Punane-Must rohkem, sest nõuab vähem tasakaalustamisoperatsioone (värvireeglid tagavad selle). Mälukasutuses võiks eelistada Punane_Must puud, sest värve saab tõlgendada baitites. AVL peab aga salvestama tasakaalustamise info iga sõlme kohta.
Boonusülesanne (2 punkti): 
● Analüüsi ja võrdle erinevaid binaarpuude tasakaalustamise algoritme (näiteks AVL, punase-musta, Splay puud, B-tree) teoreetiliselt. Selgita, kuidas need algoritmid aitavad optimeerida andmestruktuuride jõudlust erinevates rakendustes.
AVL:
      Tasakaalustatkase nii, et kõik alampuude kõrguste vahe on kõige rohkem. Miinuseks, et pidev tasakaalustamine võib mõjutada lisamise ja kustutamise kiirust. Sobib hästi sinna, kus otsingud on sagedased ja soovitakse kindlat ajakulu  otsinguoperatsioonidele.

Punane-Must:
Tasakaalustab puud kasutades värve (must ja punane), kehtesdaes reeglid, et nende järgi toimida. Ajamahukuselt on halvem kui AVL. Sobib rakendustesse, kus tehakse rohkem lisamist ja kustutamist, kui otsinguid (nt andmebaasides).
Splay:
Tasakaalustamine käib tuues viimati kasutatud sõlmed puu juurde lähedale. Sobib dünaamilistele rakendustele. On kiire sisestamisel ja eemaldamisel.
B-puu:
Tasakaalustab, hoides kindlat hulka võtmeid igas sõlmes. Keerukam implementeerida võrreldes AVL-ga. Sobib suurematele andmemahtudele või andmebaasidele, kus on vaja tasakaalustada suurt hulka võtmeid.
