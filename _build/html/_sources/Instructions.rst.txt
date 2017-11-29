Instructions
============

#. Download macOS High Sierra from Itunes 

    `Download from Itunes <https://itunes.apple.com/us/app/macos-high-sierra/id1246284741?mt=12>`_ 

#. Run these commands in terminal one at a time

    .. code-block:: console

        hdiutil create -o /tmp/HighSierra.cdr -size 5200m -layout SPUD -fs HFS+J
        hdiutil attach /tmp/HighSierra.cdr.dmg -noverify -mountpoint /Volumes/install_build
        sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/install_build
        mv /tmp/HighSierra.cdr.dmg ~/Desktop/InstallSystem.dmg
        hdiutil detach /Volumes/Install\ macOS\ High\ Sierra
        hdiutil convert ~/Desktop/InstallSystem.dmg -format UDTO -o ~/Desktop/HighSierra.iso

    Sample result 1:

        .. image:: Pictures/SampleOutput1.png

    Sample result 2:

        .. image:: Pictures/SampleOutput2.png

    Resulting file:

        .. image:: Pictures/ResultFile.png

#. Rename the file by removing .cdr from the end and confirm using .iso

    .. image:: Pictures/RenameToISO.png

    Result File:

        .. image:: Pictures/FinalFile.PNG

Reference
---------

    `Link <https://tylermade.net/2017/10/05/how-to-create-a-bootable-iso-image-of-macos-10-13-high-sierra-installer/>`_ 
    
        

        
    
    

    


    