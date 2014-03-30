##  'Using the HTML5 Fullscreen API for Phishing Attacks', OWASP MIA and 'We need SAST technology for browsing the web safely' 

Really nice article from [Feross Aboukhadijeh](http://feross.org/about) on the Phishing potential of HTML5 FullScreen features:

You can read it at [Using the HTML5 Fullscreen API for Phishing Attacks](http://feross.org/html5-fullscreen-api-attack/)

Note that on Chrome in OSx it will show this alert

[![](images/Screen_shot_2012-10-12_at_10_51_33.png)](http://2.bp.blogspot.com/--RmQBWSarJw/UHfobSTfzPI/AAAAAAAAARg/5UPCRrACiIA/s1600/Screen+shot+2012-10-12+at+10.51.33.png)

  
... if you're not in Full Screen already. But in a lot of cases that will be easy to dismiss (specially with users used to click that 'Allow' button). See note below on using SAST technology to deal with this.

What is interesting about this story is that is also shows how developers DO care about security. There is a thread about it on [Hackers News](http://news.ycombinator.com/item?id=4629906) and on [Reddit](http://www.reddit.com/r/netsec/comments/116mdb/using_the_html5_fullscreen_api_for_phishing/) and I found this article via the CodeProject's Daily New email:

[![](images/Screen_shot_2012-10-12_at_11_04_24.png)](http://4.bp.blogspot.com/-sE2fCwLRIRM/UHfsQcYfNBI/AAAAAAAAAR4/xNsUgTp4PSI/s1600/Screen+shot+2012-10-12+at+11.04.24.png)

**OWASP MIA**

But where's OWASP on this thread?

  * both [Hackers News](http://news.ycombinator.com/item?id=4629906) and on [Reddit](http://www.reddit.com/r/netsec/comments/116mdb/using_the_html5_fullscreen_api_for_phishing/) have no mention for OWASP (just search the page)
  * [Feross article](http://feross.org/html5-fullscreen-api-attack/) also has no mention of OWASP
  * A quick search for Feross' name and OWASP didn't show anything 
  * Nothing on OWASP's website (which means that he has not presented at an OWASP conference or chapter)

  
So is Feross involved at all with OWASP? I can't find it.

As one of the guys who created one of the best ClickJacking examples [HOW TO: Spy on the Webcams of Your Website Visitors](http://feross.org/webcam-spy/) (and only 22 years old), he is clearly part of the new generation of AppSec Security experts.

But if OWASP is not able to attract him and create environments / ecosystems for Feross (and other new stars), that means that we (OWASP) are starting to be irrelevant for the new Generation :(

And that is a fundamental problem with OWASP. We should be measuring OWASP's success by its community and relevance. But it is much harder  to measure 'What could had happened' than 'what is happening'. This (amongst others) is why I proposed [a new model for OWASP](http://diniscruz.blogspot.com/2012/10/an-idea-of-new-model-for-owasp.html) so that OWASP can reinvent itself and find ways to add value to Feross (and its community).

**  
****We need SAST technology for browsing the web safely**

So how to do solve this? Unless we start to have SAST-like Technology on browsers (which allow us to write context-sensitive rules that know the difference between YouTube and Feross' website) I don't think we will find a good solution (it's just patches and hacks) 
