files: https://antidote.cloud/d/710601b28c4a4710a23a/

Before use, the .zip file must NOT be unzipped.

Please do not try to copy the image to your SD card. Images must be burned to the SD card. 

Download Balena Etcher for this purpose: https://www.balena.io/etcher/

After NOT unpacking the zip file and installing Balena Etcher, you need to follow the steps of the application. This will completely overwrite your existing SD card. 

After finishing the steps in Balena Etcher:

Mount your SD-Card again
Open the "Boot" Folder and edit the following files:

	Open the "hostname" file:
    	Change the name from "cupyracer1" to anything you want, all lower case + no special charakters are
        allowed. Also it can not start with a number!
        
    Open the "wpa_supplicant.conf.txt" file in a code (NOT a TEXT-EDITOR!!!) 
        (use Visual Studio CODE for that)
    	Rename to wpa_supplicant.conf
        In the given scheeme add your credentials
        If you want to priorise a network over another add:
        	priority=9 
            
            
To connect to your car over SSH:

    open a shell or powershell/cmd on your computer and type:
    
        ssh pi@yourhostname.local 
        (replace yourhostname with the name you put in the "hostname" file earlier)
        
    when asked for a password it is:
    raspberry
    
    your shell will look as if you aint type that is a security feature and expected
    just type the password and press enter
    
To edit the code of the car on your computer:

	go to the nework section of your file explorer/finder and:
    	if on Mac/Linux: 
        	right click on the icon that is named after your hostname and chose:
            	Connect as.
                
        
		if on Microsoft:
        	type:
            \\yourhostname.local
            (replace yourhostname with the name you put in the "hostname" file earlier)
            
     when asked for credentials the:
     user is: Code
     pwd is: 1234
