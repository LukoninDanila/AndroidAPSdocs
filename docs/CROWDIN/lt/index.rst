Welcome to the AndroidAPS documentation
==============================================

AndroidAPS is an open source app for people living with insulin-dependent diabetes that acts as an artificial pancreas system (APS) on Google Android smartphones. Main components are different openAPS software algorithms which aim to do what a living pancreas does: keeping blood sugar levels within healthy limits by using automated insulin dosing (AID). Additionally, you need at least a supported and FDA/CE approved insulin pump and continuous glucose meter. 

The app does NOT use self-learning artificial intelligence. Instead, the calculations of AndroidAPS are based on the individual dosage algorithm and carbohydrate intake the user manually puts into his treatments profile, but they are verified by the system for safety reasons. 

The app is not provided in Google Play - you have to build it from source code by yourself for legal reasons.

Main components are:

.. image:: images/modules-female.png
  :alt: Components

For more details, please read on here.

Getting started
----------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Safety first <./Getting-Started/Safety-first.rst>
   What is a closed loop system <./Getting-Started/ClosedLoop.rst>
   What is a closed loop system with AndroidAPS <./Getting-Started/WhatisAndroidAPS.rst>  
   Wiki updates & changes <./Getting-Started/WikiUpdate.rst>
   
   
What do I need 
-----------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Module <./Module/module.rst>

   
How to Install AndroidAPS
------------
.. toctree::
   :maxdepth: 1
   :glob:

   Building the APK <./Installing-AndroidAPS/Building-APK.md>
   Update to a new version or branch <./Installing-AndroidAPS/Update-to-new-version.md>
   Install git <./Installing-AndroidAPS/git-install.rst>
   Troubleshooting Android Studio <./Installing-AndroidAPS/troubleshooting_androidstudio.rst>
   Release notes <./Installing-AndroidAPS/Releasenotes.rst>
   Dev branch <./Installing-AndroidAPS/Dev_branch.md>
   
   
Component Setup
---------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   CGM/FGM <./Configuration/BG-Source.rst>
   xDrip Settings <./Configuration/xdrip.md>
   Pumps <./Hardware/pumps.rst>
   Phones <./Hardware/Phoneconfig.rst>
   Nightscout setup <./Installing-AndroidAPS/Nightscout.md>
   Smartwatch  <./Hardware/Smartwatch.rst>
   

Configuration 
---------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Config builder <./Configuration/Config-Builder.md>
   Preferences <./Configuration/Preferences.md>
   
   
AndroidAPS Usage
------------
.. toctree::
   :maxdepth: 1
   :glob:
    
   AndroidAPS screens <./Getting-Started/Screenshots.md>
   Objectives <./Usage/Objectives.rst>
   OpenAPS features <./Usage/Open-APS-features.md>   
   COB calculation <./Usage/COB-calculation.rst>
   Sensitivity detection <./Configuration/Sensitivity-detection-and-COB.md>
   Profile switch <./Usage/Profiles.md>
   Temp-targets <./Usage/temptarget.md>   
   Extended carbs <./Usage/Extended-Carbs.rst>
   Automation <./Usage/Automation.rst>
  
 
General Hints 
---------------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Crossing timezones with pumps <./Usage/Timezone-traveling.md>
   Accessing logfiles <./Usage/Accessing-logfiles.md>
   Accu-Chek Combo tips for basic usage <./Usage/Accu-Chek-Combo-Tips-for-Basic-usage.md> 
   Export/Import Settings <./Usage/ExportImportSettings.rst>
   

AndroidAPS for children
------------------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Remote monitoring <./Children/Children.rst>
   SMS commands <./Children/SMS-Commands.rst>
   

Advanced 
----------
.. toctree::
   :maxdepth: 1
   :glob:
   
   Android auto <./Usage/Android-auto.md>
   Automation with 3rd party apps <./Usage/automationwithapp.md>
   

Troubleshooting
------------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
  
   Troubleshooting <./Usage/troubleshooting.rst>
   

FAQ 
------------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
  
   FAQ <./Getting-Started/FAQ.md>

   
Terminų žodynas
------------------------------------------
.. toctree::
   :maxdepth: 1
   :glob:
  
   Glossary <./Getting-Started/Glossary.md>
  

Where to go for help 
------------
.. toctree::
   :maxdepth: 1
   :glob:

   Useful resources to read before you start <./Where-To-Go-For-Help/Background-reading.md>
   Where to go for help <./Where-To-Go-For-Help/Connect-with-other-users.md>
   Wiki updates & changes <./Getting-Started/WikiUpdate.rst>

For Clinicians
------------
.. toctree::
   :maxdepth: 1
   :glob:
            
   For Clinicians <./Resources/clinician-guide-to-AndroidAPS>


How to help
------------
.. toctree::
   :maxdepth: 1
   :glob:

   How to help <./Getting-Started/How-can-I-help.md>
   How to translate the app and wiki <./translations.md>
   How to edit the wiki <./make-a-PR>


.. pastaba:: 
	**Atsakomybės Ir Įspėjimas**

	* Visa informacija, mintys ir šaltinio kodas yra skirti tik informaciniams ir moksliniams tikslams. Nightscout neatitinka jokių privatumo reikalavimų sveikatos priežiūros srityje. Savo rizika naudokite Nightscout ir AndroidAPS ir nenaudokite jų priimdami medicininius sprendimus.

	* Naudojant github.com šaltinio kodą, garantijos ir jokio oficialaus palaikymo nėra. Norėdami gauti daugiau informacijos, perskaitykite šios saugyklos LICENCIJĄ.

	* Visi gaminių ir gamintojų pavadinimai, prekės ženklai, paslaugų ženklai, prekių ženklai ir registruoti paslaugų ženklai yra atitinkamų savininkų nuosavybė ir naudojami tik informaciniais tikslais, o ne reklamai ar rinkodarai. Jie naudojami tik informaciniais tikslais ir nereiškia, kad AAPS priklauso jiems ir kad jie yra palaikomi.

	Please note - this project has no association with and is not endorsed by: `SOOIL <http://www.sooil.com/eng/>`_, `Dexcom <http://www.dexcom.com/>`_, `Accu-Chek, Roche Diabetes Care <http://www.accu-chek.com/>`_ or `Medtronic <http://www.medtronic.com/>`_
