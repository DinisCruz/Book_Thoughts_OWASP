##  FLOSSHack TeamMentor and the 'sausage making process' that is software/application development 

OWASP's [FLOSSHack](https://www.owasp.org/index.php/FLOSSHack) events are a really powerful initiative.

_"...Free/Libre Open Source Software Hacking (FLOSSHack) events are designed to bring together individuals interested in learning more about application security with open source projects and organizations in need of low cost or pro bono security auditing. FLOSSHack provides a friendly, but mildly competitive, workshop environment in which participants learn about and search for vulnerabilities in selected software. In turn, selected open source projects and qualified non-profit organizations benefit from additional quality assurance and security guidance...." _  
_  
_See [FLOSSHack_One](https://www.owasp.org/index.php/FLOSSHack_One) for the details (and vulnerabilities discovered) of the first event.

OWASP's [FLOSSHack](https://www.owasp.org/index.php/FLOSSHack) is one of those 'magical' spaces where the OWASP's community and its projects can come together and add a lot of value.  

In fact I remember the idea of doing something like this at the last Summit(s) but we couldn't find a FLOSS or commercial vendor that wanted to 'play the game' :)

  
And, just for record, I will be happy to help if an OWASP chapter (or University)  wants to do a similar FLOSSHack on [TeamMentor](http://owasp.teammentor.net/) 

Although TeamMentor (TM) is not OpenSource, it is very close, since the [source code is available](https://github.com/TeamMentor-OWASP/Master) and SI allowed me to 'open it' as much (if not more) as other OpenSource projects (note that TeamMentor uses O2 Platform's [FluentSharp APIs](https://nuget.org/packages?q=fluentsharp), and there has been significant changes/features in the [latest version of O2](http://diniscruz.blogspot.co.uk/p/owasp-o2-platform.html) which are a direct consequence of my TeamMentor development activities (for example the [O2 VisualStudio Extension](http://visualstudiogallery.msdn.microsoft.com/295fa0f6-37d1-49a3-b51d-ea4741905dc2) or the  [Real-Time Vulnerability Feedback in VisualStudio](http://diniscruz.blogspot.co.uk/p/real-time-vulnerability-feedback-in.html) PoC)).

I'm quite proud of the level of openness that TM has, and I hope that other commercial tools follow these ideas/activities. Here are a couple blog posts I wrote about TM's Security:

  * [TeamMentor Vulnerability Disclosures: CSRF , ClickJacking and Get Password Hash from Browser Memory](http://diniscruz.blogspot.co.uk/2012/10/teammentor-vulnerability-disclosures.html)  - checkout the emdeded pdfs with details of the vulnerabilities
  * [Couple XSS issues and XSS-By-Design (in TeamMentor)](http://diniscruz.blogspot.co.uk/2012/10/couple-xss-issues-and-xss-by-design-in.html)  - and why they were not fixed in the current 3.2 release
  * ['About' page broken due to ClickJacking protection](http://diniscruz.blogspot.co.uk/2012/10/about-page-broken-due-to-clickjacking.html)  - good example of the Security TAX that we (developers) have to pay due to security fixes
  * [Creating an TeamMentor Security Bounty Program](http://diniscruz.blogspot.co.uk/2012/10/creating-teammentor-security-bounty.html) - still need to publicly launch this, but for all practical purposes it is active
  * [Test and Hack TeamMentor server with 3.2 RC5 code and SI library](http://diniscruz.blogspot.co.uk/2012/09/test-and-hack-teammentor-server-with-32.html) - lastest 'please hack TM' invite
  * ["...O2 in Seattle..." and "...Please Hack TeamMentor (beta)..."](http://diniscruz.blogspot.co.uk/2011/12/o2-in-seattle-and-please-hack.html)  - first 'please hack TM' invite sent last year
  * On Testing TM WebServices

  * [Documenting how to test WebServices using scripts - the story so far](http://diniscruz.blogspot.co.uk/2012/05/documenting-how-to-test-webservices.html)  - see how hard it is to test WebServices in a real-world app
  * [Creating a spreadsheet with WebService's Authorization Mappings](http://diniscruz.blogspot.co.uk/2012/05/creating-spreadsheet-with-webservices.html) 
  * [Roadmap for Testing an WebService's Authorization Model](http://diniscruz.blogspot.co.uk/2012/05/roadmap-for-testing-webservices.html) 
  * [What is the formula for the WebServices Authentication mappings?](http://diniscruz.blogspot.co.uk/2012/05/what-is-formula-for-webservices.html) - spreadsheet template with Authorisation mappings 
  * [Testing TeamMentor 2.0 security using O2](http://diniscruz.blogspot.com/2012/04/testing-teammentor-20-security-using-o2.html) - how I used a mix of Static and Dynamic Analysis to test the security of the first TM WebService's refactoring

* [SecDDev - Security Driven Development](http://diniscruz.blogspot.co.uk/2012/10/secddev-security-driven-development.html) - an interesting idea :)

Note that we really embraced Git and GitHub as part of TeamMentor's development and workflow:

  * [Pretty cool visualisation of the 'GitHub based' TeamMentor Development+QA+Release workflow](http://diniscruz.blogspot.co.uk/2012/11/pretty-cool-visualisation-of-github.html) 
  * Master source code: [https://github.com/TeamMentor/master](https://github.com/TeamMentor/master)
  * Bugs and issues: [https://github.com/TeamMentor/master/issues](https://github.com/TeamMentor/master/issues)
  * Version with OWASP Top 10 Library ([https://github.com/TeamMentor-OWASP/Master](https://github.com/TeamMentor-OWASP/Master)) which you can see in action at [http://owasp.teammentor.net](http://owasp.teammentor.net/) (note that this is the full engine with the OWASP LIbrary content released under [a CC License](http://creativecommons.org/licenses/by/3.0/))
  * Bunch of misc code repositories: [https://github.com/TeamMentor](https://github.com/TeamMentor)

My objective is to create a super secure+powerful application, with maximum visibility+openness, while creating documentation on how it happened (which you can see by the current blog posts)

I think that TeamMentor is a good case study for the challenges of writing secure code, since it is a real-world app, with real-world complexity, real-world legacy stuff and real-world security compromises. This is a great learning opportunity to **look at the 'sausage making process' that is software/application developmen**t (with a bunch of  .Net, Asmx, jQuery, Javascript, and  xml files which can be easily deployed to the 'cloud'). We always talk how OWASP needs to engage with developers, work with them, help them to secure the app.... well here is a good opportunity to do just that. 

**I want/need help in securing TeamMentor, and Its not an easy task :)**

One area that I really want to move next, is the implementation of AppSensor-like-capabilities so that malicious activities can be detected and mitigated

Oh, and I could really do with a good layer of .NET ESAPI controls/capabilities :)
