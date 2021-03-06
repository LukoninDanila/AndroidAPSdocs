Neccessary checks after update to AndroidAPS 2.7
***********************************************************

The program code was changed significantly when switching to AAPS 2.7. Therefore it is important that you make some changes or check settings after the update.

Check BG source
-----------------------------------------------------------
* Check if BG source is correct after update.
* Especially when using `xDrip+ <../Configuration/xdrip.html>`_ it might happen, that BG source is changed to Dexcom app (patched).
* Open `Config builder <../Configuration/Config-Builder.html#bg-source>`_ (hamburger menu on top left side of home screen)
* Scroll down to "BG source".
* Select correct BG source if changes are neccessary.

.. image:: ../images/ConfBuild_BG.png
  :alt: BG source

Finish exam
-----------------------------------------------------------
* AAPS 2.7 contains new objective 11 for `automation <../Usage/Automation.html>`_.
* You have to finish exam (`objective 3 and 4 <../Usage/Objectives.html#objective-3-proof-your-knowledge>`_) in order to complete `objective 11 <../Usage/Objectives.html#objective-11-automation>`_.

Set master password
-----------------------------------------------------------
* Neccessary to be able to `export settings <../Usage/ExportImportSettings.html>`_ as they are encrypted as of version 2.7.
* Open Preferences (three-dot-menu on top right of home screen)
* Click triangle below "General"
* Click "Master-Password"
* Enter password, confirm password and click ok.

.. image:: ../images/MasterPW.png
  :alt: Set master password
  
Set Pump Password for Dana RS (if using Dana RS)
-----------------------------------------------------------
* Pump password for `Dana RS <../Configuration/DanaRS-Insulin-Pump.html>`_ was not checked in previous versions.
* Open Preferences (three-dot-menu on top right of screen)
* Scroll down and click triangle next to "Dana RS".
* Click "Pump password (v1 only)"
* Enter pump password (Default password is 1234) and click OK.

.. image:: ../images/DanaRSPW.png
  :alt: Set Dana RS password
  
To change password on Dana RS:

* Press OK button on pump
* In main menu select "OPTION" (move right by pressing arrow button several times)
* In options menu select "USER OPTION"
* Use arrow button to scroll down to "11. password"
* Enter old password (Default password is 1234)
* Set new password (Change numbers with + & - buttons / Move right with arrow button).
* Confirm with OK button.
* Save by pressing OK button again.
* Move down to "14. EXIT" and press OK button.
