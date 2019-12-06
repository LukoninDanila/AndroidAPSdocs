Component Overview 
==============================================
AndroidAPS is not just a (self-built) application, it is just one of serveral modules of your closed loop system. Before deciding for components, it would be a good idea to have a look at the `component setup <https://androidaps.readthedocs.io/en/dev/EN/index.html#component-setup>`_, too.
   
.. image:: ../images/modules.png
  :alt: Compontents overview

.. note:: 
   **VOOR JE EIGEN VEILIGHEID**

   De veiligheidsfuncties die in AndroidAPS zitten, maken gebruik van ingebouwde veiligheidsmaatregelen van de hardware componenten waaruit jouw systeem bestaat. Het is daarom van cruciaal belang dat je alleen een volledig functionerende FDA of CE goedgekeurde insulinepomp en CGM gebruikt voor het bouwen van jouw eigen closed loop. Gebruik alleen insulinepompen en CGMs die in deze handleiding beschreven staan, waarvoor de AndroidAPS software is geschreven en getest. Hardware of software wijzigingen aan deze componenten kunnen voor onverwachte uitkomsten zorgen (denk aan het ongewenst afgeven van insuline), waardoor de gebruiker een aanzienlijk risico loopt. Als je een insulinepomp of CGM-ontvanger vindt/koopt/krijgt die een defect heeft, zelfgemaakt is, of op welke manier dan ook veranderd is, GEBRUIK DEZE NIET voor het maken van een AndroidAPS-systeem.

   Daarnaast is het belangrijk om alleen originele verbruiksartikelen te gebruiken, zoals infuussets, inschiethulpen en reservoirs die door de fabrikant zijn goedgekeurd voor gebruik met jouw pomp of CGM. Door het gebruik van niet-originele, niet-geteste verbruiksmaterialen kunnen CGM metingen onnauwkeurig worden en/of fouten optreden in de insulinedosering. Insuline is zeer gevaarlijk wanneer het verkeerd wordt gedoseerd - speel alstublieft niet met je leven door jouw hulpmiddelen aan te passen.
   
   Tensotte een belangrijke opmerking: je mag géén SGLT-2 inhibitors (glifozines) gebruiken wanneer je loopt. Omdat deze medicatie ook de bloedsuiker verlaagt.  Deze medicatie in combinatie met een systeem dat de basale insuline verlaagt om BG te verhogen is bijzonder gevaarlijk, omdat deze stijging in BG mogelijk niet zal gebeuren en daardoor een gevaarlijk gebrek aan insuline kan ontstaan.

Necessary Modules
=====================
Good individual dosage algorithm for your diabetes therapy
------------------
Even though this is not something to create or buy, this is the 'module' which is probably underestimated the most but essential. When you let an algorithm help manage your diabetes, it needs to know the right settings to not make severe mistakes.
Even if you are still missing other modules, you can already verify and adapt your 'profile' in collaboration with your diabetes team. 
Most loopers use circadian BR, ISF and CR, which adapt hormonal insulin sensitivity during the day.

The profile includes

* BR (Basal rates)
* ISF (insulin sensitivity factor) is your blood glucose unit per one unit insulin
* CR (carb ratio) is gramms carbohydrate per one unit insulin
* DIA (duration of insulin acting).

No use of SGLT-2 inhibitors
-------
SGLT-2 inhibitors, also called gliflozins, inhibit reabsorption of glucose in the kidney. As they incalculably lower blood sugar levels, you MUST NOT take them while using a closed loop system like AndroidAPS! There would be a huge risk of a ketoacidosis or a hypoglycemia! The combination of this medication with a system that lowers basal rates in order to increase BG is especially dangerous as due to the gliflozin this rise in BG might not happen and a dangerous state of lack of insulin can happen.

Phone
-------
You need an Android smartphone with Google Android 6.0 or above. Users are creating a `list of tested phones and watches <https://docs.google.com/spreadsheets/d/1gZAsN6f0gv6tkgy9EBsYl0BQNhna0RDqA9QGycAqCQc/edit?usp=sharing>`_

To record a phone or watch that isn't already listed in the spreadsheet then please fill in the `form <https://docs.google.com/forms/d/e/1FAIpQLScvmuqLTZ7MizuFBoTyVCZXuDb__jnQawEvMYtnnT9RGY6QUw/viewform>`_.

Any problems with the spreadsheet please send an email to `hardware@androidaps.org <mailto:hardware@androidaps.org>`_, any donations of phone/watch models that still need testing please send an email to `donations@androidaps.org <mailto:hardware@androidaps.org>`_.

Insulin pump
--------
AndroidAPS **currently** works with 

- `Accu-Chek Combo <../Configuration/Accu-Chek-Combo-Pump.html>`_ (additionally needed: Ruffy app, LineageOS or Android 8.1 on your phone)
- `Accu-Chek Insight <../Configuration/Accu-Chek-Insight-Pump.html>`_ 
- `DanaR <../Configuration/DanaR-Insulin-Pump.html>`_ 
- `DanaRS <../Configuration/DanaRS-Insulin-Pump.html>`_  
- `some old Medtronic pumps <../Configuration/MedtronicPump.html>`_ from upcoming version 2.4 (additionally needed: RileyLink/Gnarl hardware, Android Phone with bluetooth low energy / BLE-chipset)

**Other pumps** that may have the potential to work with AndroidAPS are listed on the `Future (possible) Pumps <../Getting-Started/Future-possible-Pump-Drivers.html>`_ page.

If you need to **privately buy** a pump then you can find various distributors is in `this spreadsheet <https://drive.google.com/open?id=1CRfmmjA-0h_9nkRViP3J9FyflT9eu-a8HeMrhrKzKz0>`_, please share the details of yours if not already listed.

**So what's the best pump for looping with AndroidAPS?**

The Combo, the Insight and the older Medtronics are solid pumps, and loopable. The Combo has the advantage of many more infusion set types to choose from as it has a standard luer lock. And the battery is a default one you can buy at any gas station, 24 hour convenience store and if you really need one, you can steal/borrow it from the remote control in the hotel room ;-).

The advantages of the DanaR/RS vs. the Combo as the pump of choice however are:

- The Dana*R/RS connects to almost any phone with Android >= 5.1 without the need to flash lineage. If your phone breaks you usually can find easily any phone that works with the Dana*R/RS pumps as quick replacement... Met de Combo is dat minder makkelijk. (Dit kan veranderen in de toekomst, als Android 8.1 populairder wordt)
- Initial pairing is simpler with the Dana* RS. Maar dit doe je meestal eenmalig.
- So far the Combo works with screen parsing. In het algemeen werkt dit prima, maar het is traag. Bij het loopen merk je dit vaak niet eens omdat alles op de achtergrond werkt. Still there is much more time you need to be connected so more time where the BT connection might break, which isn't so easy if you walk away from your phone whilst bolusing & cooking. 
- The Combo vibrates on the end of TBRs, the Dana* R vibrates (or beeps) on SMB. Waarschijnlijk gebruikt de loop 's nachts vaker een TBR dan SMB.  De DanaRS kun je zo instellen dat de pomp niet piept of trilt wanneer een TBR of SMB wordt gegeven.
- Reading the history on the RS in a few seconds with carbs makes it possible to switch phones easily while offline and continue looping as soon a soon as some CGM values are in.
- All pumps AndroidAPS can talk with are waterproof on delivery. Alleen de Dana pompen zijn ook gegarandeerd waterdicht tijdens gebruik, doordat de ruimtes voor batterij en reservoir volledig afgesealed zijn. 

BG bron
------------
This is just a short overview of all compatible CGMs/FGM with AndroidAPS. For further details, look `here <../Configuration/BG-Source.html>`_. Just a short hint: if you can display your glucose data in xDrip+ app or Nightscout website, you can choose xDrip+ (or Nightscout with web connection) as BG source in AAPS.

* `Dexcom G6 <../Hardware/DexcomG6.html>`_: It works with xDrip+ app or patched Dexcom app
* `Dexcom G5 <../Hardware/DexcomG5.html>`_: It works with xDrip+ app or patched Dexcom app
* `Dexcom G4 <../Hardware/DexcomG4.html>`_: These sensors are quite old, but you can find instructions on how to use them with xDrip+ app
* `Libre 2 <../Hardware/Libre2.html>`_: It works with xDrip+ (no transmitter needed), but you have to build your own patched app.
* `Libre 1 <../Hardware/Libre1.html>`_: You need a transmitter like Bluecon or MiaoMiao for it (build or buy) and xDrip+ app
* `Eversense <../Hardware/Eversense.html>`_: It works so far only in combination with ESEL app and a patched Eversense-App (works not with Dana RS and LineageOS, but DanaRS and Android or Combo and Lineage OS work fine)
* `Enlite <../Hardware/MM640g.html>`_: quite complicated with a lot of extra stuff


Nightscout
------------
Nightscout is a open source web application that can log and display your CGM data and AndroidAPS data and creates reports. You can find more information on the `website of the Nightscout project <http://www.nightscout.info/>`_. You can create your own Nightscout website `using Heroko <http://www.nightscout.info/wiki/welcome/set-up-nightscout-using-heroku>`_, use the semi-automated Nightscout setup on `zehn.be <https://ns.10be.de/en/index.html>`_ or host it on your own server (this is for IT experts).

Nightscout is independent of the other modules. You will need it to fulfill Objective 1.

Additional information on how to configure Nightscout for use with AndroidAPS can be found `here <../Installing-AndroidAPS/Nightscout.html>`_.

AAPS-.apk file
---------------
The basic component of the system. Before installing the app, you have to build the apk-file (which is the filename extension for an Android App) first. Instructions are  `here <../Installing-AndroidAPS/Building-APK.html>`_.  

Optional Modules
==================
Smartwatch
---------------
You can choose any smartwatch with Android Wear 1.x and above. Most loopers wear a Sony Smartwatch 3 (SWR50) as it is the only watch that can get readings from Dexcom G5/G5 when phone is out of range. Some other watches can be patched to work as a standalone receiver as well (see `this documentation <https://github.com/NightscoutFoundation/xDrip/wiki/Patching-Android-Wear-devices-for-use-with-the-G5>`_ for more details).

Users are creating a `list of tested phones and watches <https://docs.google.com/spreadsheets/d/1gZAsN6f0gv6tkgy9EBsYl0BQNhna0RDqA9QGycAqCQc/edit?usp=sharing>`_. There are different watchfaces for use with AndroidAPS, which you can find `here <../Configuration/Watchfaces.html>`_.

To record a phone or watch that isn't already listed in the spreadsheet then please fill in the `form <https://docs.google.com/forms/d/e/1FAIpQLScvmuqLTZ7MizuFBoTyVCZXuDb__jnQawEvMYtnnT9RGY6QUw/viewform>`_.

Any problems with the spreadsheet please send an email to `hardware@androidaps.org <mailto:hardware@androidaps.org>`_, any donations of phone/watch models that still need testing please send an email to `donations@androidaps.org <mailto:hardware@androidaps.org>`_.

xDrip+
-------
Even if you don't need to have the xDrip+ App as BG Source, you can still use it for i.e. alarms or a good blood glucose display. You can have as many as alarms as you want, specify the time when the alarm should be active, if it can override silent mode, etc. Some xDrip+ information can be found `here <../Configuration/xdrip.html>`_. Please be aware that the documentations to this app are not always up to date as its progress is quite fast.

Gebruiksvoorbeeld
============
If you want to get a step by step example, you might want to look at a sample setup. The first sample setup is quite old, but should be still up-to-date.

.. toctree::
   :maxdepth: 1
   :glob:
   
   Sample Setup <../Getting-Started/Sample-Setup.rst>
 
  
What to do while waiting for modules
============================================
It sometimes takes a while to get all modules for closing the loop. But no worries, there are a lot of things you can do while waiting. It is NECESSARY to check and (where approporiate) adapt basal rates (BR), insulin-carbration (IC), insulin-sensitivity-factors (ISF) etc. And maybe open loop can be a good way to test the system and get familiar with AndroidAPS. Using this mode, AndroidAPS gives treatment advices you can manually execute.

You can keep on reading through the docs here, get in touch with other loopers online or offline, `read <https://androidaps.readthedocs.io/en/dev/EN/Where-To-Go-For-Help/Background-reading.html>`_ documentations or what other loopers write (even if you have to be careful, not everything is correct or good for you to reproduce).

**Done?**
If you have your AAPS components all together (congrats!) or at least enough to start in open loop mode, you should first read through the `Objective description <../Usage/Objectives.html>`_ before each new Objective and setup up your `hardware <../index.html#component-setup>`_.
