# LDAP-credentials-collector-backdoor-generator

Idea About This script
-----------------------
Last year, during external network VAPT of a client i got inside the network using vulnerable web application. Once i was inside, i observed there is an intranet appication which was accessible only if user is having LDAP credentials. 

I got helpdesk LDAP user account and logged into the intranet (its a long story how i managed to get it), also i was having web shell on one server where i got LDAP database dump for organization and started for hash cracking. After my best i could get plain text for only 60% password hashes and my target BIG FISH was still out of my reach (server admin's LDAP account).

After that i made my mind to try something different and simple. Server was not rootable but i was having web shell access on the intranet web portal and included my script to get visitors passwords.

How actually it work
--------------------
This script generate backdoor code which log username password of an user who have passed HTTP basic auth using LDAP credentials. 

If attacker is having web shell access of the website where users are landing after successful HTTP basic authentication via LDAP account, it extract user's username and password from request header (Authorization). 

Attacker need to include the backdoor generated by this script in the website and script will start logging username, password of visitors.

How to use
----------
This script generate one file which we need to upload on target server, include the backdoor file in the webportal (which is getting used by users). Backdoor code will extract username password of the user from Authorization header and will log them in a file.

Step 1. Access script and click "start process" button

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/1.png">

Step 2. Chose any name with which you want to generate backdoor, in my case i am going for "beautiful.css". Credential collector file name is the name of the file which will save credeantials on target server. Backdoor will generate this file on target server to store the stolen credentials, attacker just need to download credential collector file to get stolen credenatials. In my case credeantial collector file name is "collector.jpg"

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/2.png">

Step 3. once you click "create backdoor file" button, you will prompted with "download backdoor" button screen, just click the button to download the backdoor.

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/4.png">

Step 4. Upload backdoor to target server

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/5.png">

Step 5. Include backdoor file in the website file which is getting used frequestly by users.
code to include backdoor is 

include('beautiful.css');

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/6.png">

Step 6. Wait for users to login or to visit the website having our backdoor. Let's say one user is logging in using his LDAP account.

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/7.png">

Step 7. As user will visit the page after successful authentication, backdoor file will generate collector.jpg file for credential storage.

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/8.png">

Step 8. To get stolen credentials, attacker need to download credential file (collector.jpg)

<img src="https://raw.githubusercontent.com/incredibleindishell/LDAP-credentials-collector-backdoor-generator/master/images/10.png">

Step 9. save the file and open it in any text editor and get your credentials.


--==[[ With Love from Team IndiShell ]]==--

--==[[ Greetz To ]]==--

Zero cool, code breaker ICA, root_devil, google_warrior, INX_r0ot, Darkwolf indishell, Baba, Silent poison India, Magnum sniper, ethicalnoob Indishell, Local root indishell, Irfninja indishell, Reborn India,L0rd Crus4d3r,cool toad, Hackuin, Alicks,Gujjar PCP,Bikash,Di nelson Amine,Th3 D3str0yer, SKSking, rad paul,Godzila,mike waals,zoo zoo,cyber warrior,shafoon, Rehan manzoor, cyber gladiator,7he Cre4t0r,Cyber Ace, Golden boy INDIA,Ketan Singh, D2 Yash, Aneesh Dogra, AR AR, saad abbasi, hero, Minhal Mehdi, Raj bhai ji, Hacking queen, lovetherisk, D3. 

--==[[ Love to To ]]==--

My Father, my Ex Teacher, cold fire hacker, Mannu, ViKi, Ashu bhai ji, Soldier Of God, Bhuppi, Rafay Baloch, Mohit, Ffe, Ashish, Shardhanand, Budhaoo, Jagriti, Salty, Hacker fantastic, Jennifer Arcuri and Don(Deepika kaushik), Govind
