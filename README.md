demo-web
========

The M2SYS BioPlugin application suite allows you to integrate world-class biometric capabilities into your application, be it a traditional Windows-based application or a more modern web-based application. This is one in a series of repos that will display examples of these types of integrations, demonstrating the flexibility of this biometric solution.

This repo will cover using the BioPlugin Client through a web interface that is hosted on a remote server. The BioPlugin Server could be installed on that same server, or on a different server providing that the two can communicate properly. In this scenario the workstation with the BioPlugin Client installed on needs to be able to communicate with the server running BioPlugin Server over a TCP port, which by default is 1200. While its always recommended to secure the communication, the traffic between the BioPlugin Client and BioPlugin Server is encrypted using industry standard AES specification.

This type of deployment is useful for corporate networks, where network traffic is believed to be safe and secure through hardware devices and/or software solutions. The BioPlugin Client would be deployed using standard methods (GPO, SMS,Scripts, etc) to a selection of computer, the device is plugged in, and the user just opens Internet Explorer and browses to the provided URL.

The web server hosting these pages, the BioPlugin Server and it's database can all be located on different computers so configurations can achieve massive redundancy. Officially the BioPlugin Server supports Microsoft SQL (Including the free Express editions), MySQL, and Oracle database servers. However with enough elbow grease you can use several database technologies, and a great resource for that is connectionstrings.com.

For the web server we officially support Microsoft IIS, however you can run it with Apache using the right mods and settings. Other web servers haven't been tested, but could work if they support certain features/functions (Which is covered elsewhere).

Finally, the computer running the BioPlugin Server can be any standard workstation or server. Obviously the more enterprise-class servers will perform better than a quad core workstation, and with the right edition of the BioPlugin Server you can scale the number of processing threads relative the amount of cores available. Our most popular hardware/software solution is a 48 core 2U server, but recently we've been involved in some very dense blade scenarios that boggle the mind.

This example page was constructed using simple, standards compliant HTML and CSS, with a little bit of JavaScript and PHP. As you'll see in the code, most of is is for the interface's layout and visual appeal. The bioplugin.js file was made just for this example, in order to bundle the relevant code for learning purposes. In most cases you won't be exposing every single method we provide to the end user, so in practice you'll only be adding a few lines of code for most needs.