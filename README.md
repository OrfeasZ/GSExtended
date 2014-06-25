GSExtended
==========

A userscript to enhance Grooveshark experience.

Features
---------

* Song desktop notification
* Broadcast message notification on desktop based on configured keywords
* Larger Broadcast chatbox
* Timestamps on broadcast activities
* See who is friends with the current broadcaster
* See which songs are in the broadcast library / history
* See detailed votes for current song, suggestions and history
* New suggestion layout -> show song's album AND suggester's name separately
* Automatic upvote/downvote defined by the user.
* Better display of the player when the window is shrinked
* Spoiler tags, use [sp], [sp movie] or [spoiler movie] before a spoiler. Your message will be scrambled
* AutoLinkify web address and open media in a lightbox
* Can inline image linked in chat messages
* View fullscreen avatar of someone in the chat
* View full album art of the current track
* One hidden secret !

TODO
- Display the list of autovoted tracks
- fullscreen chat/ broadcast info 
- display broadcast statistics

It does not !
---------------------
* Make coffee or blueberry muffins
* Fix Grooveshark bugs ! If you see incoherent data, it may be because of the way GS refreshes its content. 
	Usually navigate away/back from BC page fixes this.

Instructions
------------


1. Firefox : You need [GreaseMonkey](https://addons.mozilla.org/fr/firefox/addon/greasemonkey/). ///  Chrome :  Install [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en) 
	or [NinjaKit](https://chrome.google.com/webstore/detail/gpbepnljaakggeobkclonlkhbdgccfek).


2. Once installed, visit this link : (https://github.com/Ramouch0/GSExtended/raw/master/Js/GSExtended.user.js)
3. Accept installation of the script.

For more information on how to install userscripts, please visit this page : http://userscripts.org/about/installing

If eveything is ok, you should see 4 GSX notifications when you visit grooveshark.

Settings
---------

Settings are on your profile preferences page. (http://grooveshark.com/#!/settings/preferences)
They are stored locally on your computer.
Some of them need a complete refresh of the page to be active.



FAQ
----
**Notifications are not shown**

Be sure to authorise notification for grooveshark. On your browser click on the icon on the left of the address bar.
You should see notification settings for the active site.

**Songs in broadcaster's collection are not shown with green border**

Large BC collection can take a while to be loaded, come back to this page later

**Some of broadcaster's friends are not highlighted in chat box**

Happens if the message is displayed before the script finished to laod data. It will be fixed if you navigate in GS.

**What are all this question marks in vote ?**

When you don't have data for one user loaded on your side, the script can't know the name of the voter. it will display a '?'.
By default GS only loads your friends and people you interact with. There is an option in the script preferences to force user data loading. BUT I strongly advise to not use it when you are in a big broadcast like Caleb's (>300 listeners).


**What 'Show real Votes' button does ?**

It show the number of vote from listener that are currently still listening.
It can be wrong because some listeners appear offline but they aren't... GS bug.

**What the vote tooltip means?**
```
/Number of voter still in BC/ : /Voters/ -> /Thoses who left/
```

**In history, I can't see who voted**

GS only gives vote number in history for songs that were played before you joined the BC. 
You can only see voters' names for songs that you listened.

**How to know which tracks are autovoted ?**

On songs listing you can see tracks that you marked as autovote. Currently there is now way to see a list of all autovoted songs.

**Suggester name is wrong !**

~~I know, it's a bug from GS. It appears when suggestion list is big (>30). It's also here when the script is not activated but less visible because suggesters are not always displayed.
Anyway, the tooltip info might always be right and updated :-)
I tried to find a fix for this but... (GS resuses songs views and does not update correclty the model binding)~~
This should be fixed by now. I'm forcing the first voter as suggester. This can be wrong if the suggester removed his vote, but this is also how GS shows it.

**Can I change notification duration ?**

On firefox it's handled by the browser and CANNOT be changed. 
On chrome it's setted to 3.5 sec. You can change it in preferences.
