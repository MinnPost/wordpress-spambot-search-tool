Program : Spambot Search Tool
Version : 0.59
Released: Tuesday May 17th 2016
Licence : MIT Licence

	http://opensource.org/licenses/MIT

Author  : Steven Burn
Company : I.T. Mate
Website : http://support.it-mate.co.uk/?mode=Products&p=spambotsearchtool
Download: http://support.it-mate.co.uk/?mode=Products&act=DL&p=spambotsearchtool

Support : http://temerc.com/forums/viewforum.php?f=71
	  http://forum.hosts-file.net/viewforum.php?f=68

***********************************************************************
In this document
***********************************************************************

1. Overview
2. System Requirements
3. Known Issues
4. Updates
5. Updates Planned
6. Release Notes

	- Update notes + General Information

7. Installation
8. Installation Notes
9. Uninstallation
10. Conditions of use

***********************************************************************

1. Overview:

	Spambot Search Tool is a script that was originally posted to the StopForumSpam forums and written by Smurf Minions. 

	http://www.stopforumspam.com/forum/t37-Spambot-detector-%28with-this-API%29 

	Smurf Minions original only allowed you to query the StopForumSpam database, which is fine. However, I wanted something more, so decided to expand on it greatly, by enhancing the features to allow you to check the following databases; 

	1. fSpamlist*** - www.fspamlist.com
	2. StopForumSpam*** - www.stopforumspam.com
	3. Sorbs* - sorbs.net
	4. Spamhaus* - www.spamhaus.org
	5. SpamCop* - www.spamcop.net
	6. ProjectHoneyPot** - www.projecthoneypot.org
	7. Bot Scout*** - www.botscout.com
	8. DroneBL - www.dronebl.org
	10. Tor Project - torproject.org
	11. drone.abuse.ch - dnsbl.abuse.ch
	12. httpbl.abuse.ch - dnsbl.abuse.ch
	13. spam.abuse.ch - dnsbl.abuse.ch
	14. ZeusTracker.abuse.ch - zeustracker.abuse.ch
	15. Blocklist.de - blocklist.de

	There are two versions of the script available, the first is for use as a standalone "program" of sorts. You can see this in action at; 

	http://temerc.com/Check_Spammers 

	The second, is check_spammers_plain.php. This is a simplified version of the script that you can use for your forums, blogs, guestbooks or anything else that allows users to comment/post. It returns true or false, based on whether or not the user is listed in the database, and if listed, which one (e.g. fSpamlist, Spamhaus). 

	I've written an ASP function that ASP developers can use to query the script, and several PHP mods for the likes of WordPress, phpBB2 and phpBB3, SMF and more. These can be found at; 

	http://forum.hosts-file.net/viewtopic.php?f=69
	http://temerc.com/forums/viewforum.php?f=71 

	* IP queries only obviously 

	In the case of Spamhaus, this will also tell you which blacklist it is listed in (e.g. PBL, CBL, XBL) 

	** ProjectHoneyPot requires you have a valid API key before you can query their database 

	*** Bot Scout only allows a limited amount of queries for non-API key users. To remove this restriction, an API key is required.
	*** fSpamlist requires an API key.
	*** StopForumSpam requires an API key.

2. System Requirements

	NOTE: These are MINIMUM recommendations and should be taken as a guide ONLY.

	1. PHP 5.6 recommended* 
	2. Apache or IIS 
	3. allow_url_fopen MUST be enabled in php.ini 
	4. cURL (if file_get_contents is not available) 
	5. MySQL (if you ask it to save to DB) 
	6. IMAP (for viewing e-mail reports) 
	7. PHP Mail() (if you want e-mail reports sent to you) 

	* It should work just fine on PHP4, but will likely not work if you are using a version older than that.

	Note: If using an older version (prior to 5.6), the database functions will not work as of v0.59, unless mysqli_* is implemented.

	Tested on:

		Windows 7 Home Premium SP1
		Windows 7 Ultimate SP1
		Windows 8.1
		Windows Server 2008
		Windows Server 2008 R2
		Windows Server 2012
		Debian 7
		PHP 5.6, 7.0

3. Known Issues:

	None

4. Updates:

	See history.txt

5. Updates planned:

	None

6. Release Notes:

	None

7. Installation:

	Full install:

			n/a

	Basic install:

			n/a

	Update:

			Extract files to the check_spammers folder

	Manual (No-install):

			Copy or rename config.sample.php > config.php and counter.sample.txt > counter.txt

			Extract and upload check_spammers folder (including ALL of it's contents), to your web server

				- You can upload them to ANYWHERE on your server, it does not require a specific path

			Ensure you have inserted your ProjectHoneyPot and BotScout API keys into config.php

				- If the API keys are not present, it will notify you and simply ignore those 2 databases
				  until they are entered.

			Ensure the spambots folder and counter.txt are writable by your web server (the IUSR_ account on IIS)

			If using a database to store the spammer info, ensure you insert your DB connection info into config.php

8. Installation Notes:

	If you experience problems with the SBST not creating the database for you, please create it manually using the instructions at;

	http://forum.hosts-file.net/viewtopic.php?f=68&t=1607

9. Uninstallation:

	Full/Basic Install:

			n/a

	Manual (No-install):

			Delete Spambot Search Tool folder
			Delete SBST database (if you asked it to save info to DB)

10. Conditions of Use

See enclosed EULA.txt
