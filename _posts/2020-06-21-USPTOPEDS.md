---
title: USPTO PEDS Extraction Program
author: Ved
categories: software
layout: post
permalink: /software/USPTO_PEDS
---
# Introduction
This software extracts the data from USPTO PEDS API, this is used to get the current status and other details of US patent applications in bulk. This software gets inputs as only US patent application numbers. Further enhancements will include auto detection of Application numbers, Publications numbers and Granted numbers. 

# Background

USPTO Patent Examination Data System site provides data regarding ongoing patent examinations and examined US patent application's current status. This can be access via USPTO PAIR data base too. The PEDS data can be bulk downloaded or can be accessed via API given for free by USPTO. 
<br>
<br>
Accessing the data via PEDS is easier due to the fact that there is no Captcha associated with the search query site. As for the PAIR site it has Captcha associated with it, it takes a second more to get the status as we need to enter the captcha, but some times due to shared IP and other cases the captcha becomes a hectic hurdle to passthrough.
<br>
There comes PEDS to the rescue, it gives most of the current status like application status, Transaction History, Attorney Details, Patent term adjustment, Parent - Child applications, Foreign Priority, Assiginment details. As per my knowledge only data which it cant give is the Fees details and Fees details are not required in most cases. 
<br>
<br>
If you do want to have updated data and do not want to download the bulk data which is around 60GB( and growing) compressed in a zip folder format. Its a good vaible option to go for the API method to download the data.
<br>
<br>
The program described below is a creation of my own to extract multiple application current status details. The program is completly written in Web technologies such as HTML, CSS, javascript, Electron framework. It utlizes multiple already created libraries such as exceljs, Axios, electron-window-state etc.. I have made the program opensource so that any person can tweak it to their requirement.
<br>
<br>

# Software Working
<br>
You can find the software on [github](https://github.com/vedaprakashms/PEDS_USPTO/releases/download/V2/PEDS_extraction_app-V2.7z).

<br>
The working is quite simple:
<li> Download the software from the above link and extract using any Unzipping programs like 7zip.</li>
<li> In the extracted folder open the application file with the name "PEDS_extraction_app". You should be given with a screen such as below.
<img alt="First landing view" src="..\assets\Software_projects_images\USPTO_PEDS\Landing_view.png"></li>
<li>The program take input as a excel file with column A filled with US application numbers. Incase you are confused as to the format the tool it self provides a format to use. To use the tool given format, please click on the first icon named "Excel Template" as shown below.  
<img alt="Template Generate" src="..\assets\Software_projects_images\USPTO_PEDS\Template_genrate.png"></li>
<li>You should get a notification as shown below, sometimes if your system is controlled by an admin (like a corporate setup), you may not get the noitification. In any case you should be able to check the generated template on your desktop under the folder "PEDS_Templates". otherwise you can easily it up by Clicking the notification generated. The auto genrated files are named in a specific way with date and time included, so that you can find the applications numbers you have searched for later point of time. 
<img alt="Template Generate" src="..\assets\Software_projects_images\USPTO_PEDS\template_gen_notifcation.png"></li>
<li>Enter the application numbers from A2, Make sure the applications numbers are only in Column A, i.e. A2 till the end (A1048576 if needed ;)). Save the excel file and exit. 
<img alt="Template Generate" src="..\assets\Software_projects_images\USPTO_PEDS\Excel_filling.png"></li>
<li>If you have manually created then only follow this step, as a new auto genrated file shall be already been fed to the program. </li>
<li>Select the fields which you need to extract information from. we have total of 7 fields to choose from. once selected exit that selection by clicking the Red button on the lower right hand corner. 
<img alt="Template Generate" src="..\assets\Software_projects_images\USPTO_PEDS\Field_selection.png"></li>
<li>Click on the Start button and watch the program do the work for you.</li>
<li>Below Screen grab shows how the program works. Enjoy the program.
<img alt="Template Generate" src="..\assets\Software_projects_images\USPTO_PEDS\Working.gif"> </li>
<br>
<br>