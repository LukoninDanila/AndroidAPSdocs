# AndroidAPS ekranai

## Pradžios ekranas

![Pradžios ekranas V2.5](../images/Screenshot_Home_screen_V2_5_1.png)

Tai pradinis ekranas, kurį matysite paleidę AndroidAPS, ir kuriame yra visa svarbiausia informacija.

### Sritis A

* leidžia naviguoti tarp skirtingų AndroidAPS modulių braukiant į kairę arba dešinę

### Sritis B

* leidžia pakeisti ciklo būseną (atviras ciklas, uždaras ciklas, ciklo sustabdymas ir kt.)
* peržiūrėti dabartinį profilį ir atlikti [profilio perjungimą](../Usage/Profiles.md)
* peržiūrėti esamą glikemijos tikslą ir nustatyti [laikiną tikslą](../Usage/temptarget.md).

Palaikykite ilgai prispaudę bet kurį mygtuką, jei norite pakeisti nustatymus. Pvz.: palaikykite ilgai prispaudę tikslo laukelį (nuotraukoje "100"), jei norite nustatyti laikiną tikslą.

### Sritis C

* rodomi naujausi glikemijos duomenys, pateikti NGJ
* laikas nuo paskutinio duomenų gavimo
* pokyčiai per paskutines 15 ir 40 minučių
* dabartinė valandinė bazė, įskaitant visus sistemos nustatytos laikinos bazės (LB) duomenis
* aktyvus insulinas organizme (AIO)
* aktyvūs angliavandeniai organizme (AAO)

Pasirinktiniai [spalvoti indikatoriai](../Configuration/Preferences#overview) (KAT | INS | REZ | SEN | BAT) suteikia vizualinę informaciją ir perspėjimus apie kateterio ir insulino naudojimo laiką, senkantį rezervuarą, sensoriaus ar baterijos naudojimo trukmę.

Aktyvaus insulino organizme kiekis yra nulis, jei naudojama tik standartinė bazė ir nėra bolusų insulino. Skaičiai laužtiniuose skliaustuose rodo, kiek aktyvaus insulino yra iš buvusių bolusų ir kiek - iš bazės pakeitimų, kuriuose atliko AAPS. Antras skaičius gali būti su minuso ženklu, jei kurį laiką sistema bazę mažino arba buvo išjungusi.

### Sritis D

Paspauskite mažą rodyklę D srities dešinėje pusėje ir pasirinkite, kokią informaciją matysite grafikuose žemiau.

### Sritis E

Rodoma Jūsų sensoriaus (NGJ) pateikiama kraujo gliukozės kiekio (KG) kreivė bei Nightscout perspėjimai, pvz.: kalibracijos ar įvesti angliavandeniai.

Ilgai paspaudę ant grafiko, galite pakeisti laiko skalę. Galite matyti 6, 8, 12, 18 ar 24 val. duomenis.

Jei pasirinkote, taip pat matysite gliukozės kitimo prognozės kreives.

* **Oranžinė** linija: [AAO](../Usage/COB-calculation.rst) (oranžinė spalva dažniausiai naudojama angliavandeniams vaizduoti)
* **Mėlyna** linija: AIO (ši spalva įprastai žymi insuliną)
* **Žydra** linija: glikemijos kitimo prognozė, jei būtų nustatyta nulinė bazė
* **Geltona** linija: [NDM](../Configuration/Sensitivity-detection-and-COB#sensitivity-oref1) (nedeklaruotas maistas)

Šios kreivės rodo skirtingas gliukozės kitimo prognozes, atsižvelgiant į įvairius parametrus: aktyvių angliavandenių absorbciją; aktyvaus insulino veikimą; laiką, per kurį gliukozė galėtų peržengti žemą arba aukštą ribą, jei staiga pradėtų kristi labiau, nei numatyta ir reikėtų nulinės bazės, arba kilti labiau, nei numatyta dėl nedeklaruoto maisto.

**Ištisinė mėlyna** linija rodo bazės tiekimą. **Punktyrinė mėlyna** linija rodo bazę, kuri suprogramuota pompoje ir kuri būtų leidžiama, jei programa nieko nekeistų. Ištisinė linija yra reali bazė su visais pokyčiais (LB).

**Plona geltona** linija rodo insulino aktyvumą. Ji remiasi tikėtinu insulino poveikiu glikemijai, kai neveikia kiti veiksniai (pvz.: angliavandeniai).

### Sritis F

Šią sritį galite keisti naudodamiesi D srities pasirinkimais.

* **Aktyvus insulinas organizme** (mėlynas grafikas): rodo, kiek aktyvaus organizmo yra Jūsų organizme. Jei nebuvo laikinų bazių, SMB ir bolusų, AIO yra lygus nuliui. AIO nykimas priklauso nuo IVT ir insulino profilio nustatymų. 
* **Aktyvūs angliavandeniai organizme** (oranžinis grafikas): rodo, kiek Jūsų organizme yra dar aktyvių angliavandenių. Jų nykimas priklauso nuo algoritmo apskaičiuotų nuokrypių (deviacijų). Kai nustatoma didesnė angliavandenių įtaka, nei tikėtasi, sistema suleis daugiau insulino ir AIO padidės (kaip labai padidės priklauso nuo Jūsų saugumo nustatymų). 
* **Nuokrypiai**: 
   * **PILKI** stulpeliai rodo glikemijos svyravimus (nuokrypius arba deviacijas), kuriuos sukelia angliavandeniai. 
   * **ŽALI** stulpeliai rodo, kad glikemija yra didesnė, nei algoritmas apskaičiavo. 
   * **RAUDONI** stulpeliai rodo, kad glikemija yra mažesnė, nei algoritmas apskaičiavo.
* **Jautrumas** (balta linija): tai jautrumas insulinui, kurį apskaičiavo Autosense funkcija. Tai jautrumo insulinui faktoriaus pokyčiai dėl fizinio aktyvumo, hormonų ir pan.
* **Aktyvumas** (geltona linija): tai insulino aktyvumas, apskaičiuotas pagal insulino profilio nustatymus (jis nėra išskaičiuotas iš AIO). Kreivė tuo aukštesnė, kuo insulino aktyvumo pikas arčiau. AIO mažėjant, aktyvumas gali tapti neigiamas. 

### Sritis G

Čia galite suleisti bolusą (įprastai tam naudosite Skaičiuotuvo mygtuką) ir įvesti kalibracijas. Čia taip pat bus matomas Greitojo vedlio mygtukas, jei jis sukonfigūruotas [Konfigūracijoje](../Configuration/Config-Builder#quickwizard-settings).

## Skaičiuotuvas

![Skaičiuotuvas](../images/Screenshot_Bolus_calculator.png)

Įprastai jis naudojamas maisto bolusams suleisti.

### Sritis A

vieta, kur įvedate informaciją apie norimą bolusą. KG (kraujo gliukozės) langelyje matosi paskutinis sensoriaus rodmuo. Jei sensorius neveikia, šis langelis bus tuščias. AV langelyje turite įvesti maisto, kurį valgysite, angliavandenių ar jų atitikmens kiekį. KOREKCIJOS langelyje galite pakeisti pasiūlytą insulino dozę, AV LAIKO langelyje galite nurodyti sistemai, kad valgysite tik po kažkurio laiko, todėl ir bolusas bus atidėtas. Šiame langelyje galite įvesti ir laiką su minuso ženklu, jei angliavandenius jau suvalgėte anksčiau.

Jei pažymėsite SUPER BOLUSO laukelį, bus suleistas papildomas insulinas, kurio kiekis lygus ateinančių 2 valandų bazei, o bazė taps nulinė. Tai galbūt padės išvengti didelio glikemijos pakilimo po maisto, nes papildomai "pasiskolinama" insulino iš bazės.

### Sritis B

rodo apskaičiuotą bolusą. Jei aktyvaus, anksčiau suleisto insulino kiekis viršija apskaičiuotą boluso kiekį, bus parodytas tik papildomai reikalingų angliavandenių kiekis.

### Sritis C

rodo įvairius elementus, kurie naudojami apskaičiuojant bolusą. Jūs galite nuimti žymes nuo bet kurių iš jų, tačiau normaliai neturėtumėte to daryti.

### AAO ir AIO kombinacijos ir jų reikšmė

<ul>
    <li>Jei pažymėsite ir AAO, ir AIO, į skaičiavimus bus įtraukti visi dar aktyvūs angliavandeniai ir visas aktyvus insulinas (suleistas kaip laikina bazė ar SMB)</li>
    <li>Jei pažymėsite tik AAO, bet ne AIO, anksčiau suleistas ir dar aktyvus insulinas nebus įskaičiuotas, todėl rizikuojate perdozuoti. </li>
    <li>Jei pažymėsite tik AIO be AAO, AAPS skaičiavimuose atsižvelgs į anksčiau suleistą ir aktyvų insuliną, tačiau ne į angliavandenius. Todėl matysite pranešimą 'trūksta angliavandenių'.
</ul>

Jei norite suleisti bolusą papildomam maistui, kurį valgėte tuoj po jau įvesto maisto (pvz.: užsimanėte deserto), naudinga nuimti žymes nuo visų laukelių. Tokiu būdu bus įskaičiuojami tik nauji angliavandeniai, o ne tie, kurie buvo įvesti anksčiau, nes jie nebūtinai tiksliai absorbuoti ir AIO nebūtinai juos tiksliai atitinka.

### Neteisingo AAO kiekio nustatymas

![Lėtas angliavandenių įsisavinimas](../images/Calculator_SlowCarbAbsorbtion.png)

Jei pasinaudoję skaičiuotuvu matote tokį perspėjimą, reiškia sistema nustatė galimai klaidingą AAO kiekį. Todėl suleisdami papildomą bolusą rizikuojate perdozuoti! Išsamesnės informacijos ieškokite [AAO apskaičiavimo puslapyje](../Usage/COB-calculation#detection-of-wrong-cob-values).

## Insulino profilis

![Insulino profilis](../images/Screenshot_insulin_profile.png)

Čia rodomas Jūsų pasirinkto insulino aktyvumo profilis. VIOLETINĖ kreivė rodo, kiek insulino lieka laikui bėgant po injekcijos, nes jis pamažu ardomas, o MĖLYNA kreivė rodo, kaip kinta jo aktyvumas.

Turėtumėte naudoti vieną iš Oref profilių, kuriuose insulino veikimas turi ilgą "uodegą". Įprastai naudodami pompą Jūs tikriausiai skaičiuodavote, kad insulinas išnyksta po maždaug 3.5 val. Tačiau uždarame cikle "uodegos" yra labai reikšmingos, nes skaičiavimai yra žymiai preciziškesni, todėl net mažiausi insulino likučiai turi būti įskaičiuojami.

Išsamiau apie skirtingus insulino tipus, aktyvumo profilius ir kam viso to reikia, galite paskaityti čia: [Understanding the New IOB Curves Based on Exponential Activity Curves](https://openaps.readthedocs.io/en/latest/docs/While%20You%20Wait%20For%20Gear/understanding-insulin-on-board-calculations.html#understanding-the-new-iob-curves-based-on-exponential-activity-curves)

Jūs taip pat galite perskaityti puikų blogo straipsnį čia: [Why we are regularly wrong in the duration of insulin action (DIA) times we use, and why it matters…](http://www.diabettech.com/insulin/why-we-are-regularly-wrong-in-the-duration-of-insulin-action-dia-times-we-use-and-why-it-matters/)

Ir dar daugiau čia: [Exponential Insulin Curves + Fiasp](http://seemycgm.com/2017/10/21/exponential-insulin-curves-fiasp/)

## Pompos statusas

![Pompos statusas](../images/Screenshot_pump_Combo.png)

Čia matome insulino pompos (pavyzdyje Accu-Chek Combo) statusą. Informacija aiški savaime. Jei ilgai prispausite ISTORIJOS mygtuką, sistema nuskaitys Jūsų pompos istoriją, taip pat ir bazės profilį. Prisiminkite, kad Combo pompoje galimas tik vienas bazės profilis.

## Priežiūra

![Priežiūra](../images/Screenshot_care_portal.png)

Čia rasite tas pačias funkcijas, kaip Jūsų Nightscout puslapyje po "+" simboliu, ir galėsite pridėti pastabų prie savo duomenų. Pavyzdžiui, galėsite pažymėti, kada keitėte kateterį ar insulino rezervuarą. DĖMESIO - tai tik įrašai, ne komandos pompai! Taigi, jei čia įrašysite bolusą, tai bus tik įrašas Nightscout ataskaitoje, tačiau pompa jokio boluso nesuleis.

## LOOP, MA, AMA, SMB

Įprastai Jums nereikėtų rūpintis šių langų įrašais - tai tik OpenAPS algoritmo skaičiavimų rezultatai, besikeičiantys kaskart atsinaujinus sensoriaus duomenims. Jie aptariami kitose instrukcijose.

## Profilis

![Profilis](../images/Screenshot_profile.png)

AndroidAPS gali veikti įvairių profilių nustatymų pagrindu. Dažnai (kaip parodyta pavyzdyje) naudojamas Nightscout profilis, kuris įkeliamas per Nightscout client įskiepį ir čia tik rodomas, bet negali būti keičiamas. Jei norite atlikti pakeitimus, darykite tai savo Nightscout puslapyje ir tada AndroidAPS atlikite [profilio perjungimą](../Usage/Profiles.md), kad aktyvuotumėte pakeitimus. Tokie duomenys, kaip bazės pakeitimas ir pan., po to bus automatiškai nukopijuoti į pompą.

**IVT:** insulino veikimo trukmė, kaip aprašyta skyrelyje "Insulino profilis".

**IA:** insulino ir angliavandenių santykis. Gali būti nustatomi skirtingi IA skirtingu paros metu.

**JIF:** jautrumo insulinui faktorius - tai skaičius, kuris parodo, kiek mmol/l sumažina kraujo gliukozę suleistas 1 V insulino.

**Valandinė bazė:** tai bazės profilis Jūsų pompoje.

**Tikslas:** tai glikemijos vertė, kurios algoritmas sieks visą laiką. Jūs galite nustatyti skirtingus tikslus skirtingiems paros laikotarpiams. Jūs taip pat galite nustatyti tikslinį diapazoną, tačiau tada algoritmas atliks pakeitimus tik tada, kai prognozė rodys, kad glikemija "išeis" iš numatytų ribų. Tokiu atveju sistema reaguos žymiai vangiau ir Jums bus sunkiau pasiekti stabilią glikemiją.

## Terapija, xDrip, NSClient

Čia rasite paprastus įrašus apie terapiją (bolusus ir angliavandenius), xDrip žinutes ir pranešimus, nusiųstus į Nightscout per įdiegtą Nightscout Client. Įprastai Jūs neturėtumėte rūpintis šiais įrašais, nebent iškyla nenumatyta problema.

## Konfigūracija

![Konfigūracija](../images/Screenshot_config_builder.png)

Čia Jūs konfigūruosite savo AndroidAPS. Pavyzdyje matote įprastą derinį, kai naudojama Combo pompa, Dexcom G5 su xDrip+, NovoRapid insulinas su Oref profiliu ir duomenų perdavimas į Nightscout debesijos serverį.

Pažymėti laukeliai dešinėje reiškia, kad tam tikras modulis bus rodomas viršutinėje meniu eilutėje (žr. Pradžios ekrano A sritis), o dantračio simbolis leidžia patekti į konkretaus modulio nustatymus, jei tokie yra.

## Parametrai ir Nustatymai

Dešiniajame viršutiniame kampe rasite tris vertikalius taškus. Paspaudę pateksite į programos parametrų, istorijos peržiūros, sąrankos vedlio, programos informacijos pasirinkimus bei rasite mygtuką "išeiti", kuris uždaro AAPS programą.