---
title: USPTO PEDS Extraction Program
author: Ved
categories: software
layout: post
permalink: /software/USPTO_PEDS
---

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
The program described below is a creation of my own to extract multiple application current status details. The program is completly written in Web technologies such as HTML, CSS, javascript, Electron framework. It utlizes multiple already created libraries such as exceljs, Axios, electron-window-state etc..
<br>
<br>

<br>
<br>
[USPTO PEDS](https://ped.uspto.gov/peds/)