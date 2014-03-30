##  Is the TeamMentor's OWASP Library content released under an open License? 

Following the [FLOSSHack TeamMentor](http://diniscruz.blogspot.com/2012/11/flosshack-teammentor-and-sausage-making.html) thread,  Jerry Hoff asked _"Is the content in [http://owasp.teammentor.net/teamMentor](http://owasp.teammentor.net/teamMentor) creative commons?  Can we use it to freely fill out more of the cheat sheets and use in tutorial videos and so forth?"_

And the answer is: **YES**  

Here is the repository for the XML files: [https://github.com/TeamMentor-OWASP/Library_OWASP](https://github.com/TeamMentor-OWASP/Library_OWASP)

There are a bunch of (O2 based) tools to consume this content directly, or alternatively you can use the [TeamMentor CoreLib from NuGet](http://nuget.org/packages/TeamMentor.CoreLib) (which has all the classes and APIs needed)

Note that you can also link directly to the content (articles, libraries, folders or views) :

  * by title [https://owasp.teammentor.net/article/How_to_Protect_From_Injection_Attacks_in_ASP.NET](https://owasp.teammentor.net/article/How_to_Protect_From_Injection_Attacks_in_ASP.NET)
  * by title [https://owasp.teammentor.net/article/How_to_Encrypt_Configuration_Sections_in_ASP.NET_Using_DPAPI](https://owasp.teammentor.net/article/How_to_Encrypt_Configuration_Sections_in_ASP.NET_Using_DPAPI)
  * by title (on articles with the same title): 

  * [https://owasp.teammentor.net/article/All_Database_Input_Is_Validated](https://owasp.teammentor.net/article/All_Database_Input_Is_Validated)  (Asp.Net 3.5 version)
  * [https://owasp.teammentor.net/article/All_Database_Input_Is_Validated^OWASP^Java](https://owasp.teammentor.net/article/All_Database_Input_Is_Validated%5EOWASP%5EJava) (Java version)

* by GUID: [https://owasp.teammentor.net/article/56b0552d-2ceb-4714-a8f1-20a6a8609874](https://owasp.teammentor.net/article/56b0552d-2ceb-4714-a8f1-20a6a8609874)
* by View or folder: sometimes is more user friendly to only expose to the end user (for example) the articles in the [A08: Failure to Restrict URL Access](http://owasp.teammentor.net/teamMentor#load:e07b04c5-67f9-49a4-88fe-1b9ee8511da3&showFilters:false&showTree:false&centerGuidanceItems:true) view (instead of the whole TM GUI: [https://owasp.teammentor.net](https://owasp.teammentor.net/))

In addition to the 'article' pages (linked above) you can also see/consume the content using:

  * **raw**:[ https://owasp.teammentor.net/raw/All_Database_Input_Is_Validated](https://owasp.teammentor.net/raw/All_Database_Input_Is_Validated) (this is what the xml file stored in disk looks like)
  * **html**: [https://owasp.teammentor.net/html/56b0552d-2ceb-4714-a8f1-20a6a8609874](https://owasp.teammentor.net/html/56b0552d-2ceb-4714-a8f1-20a6a8609874) (direct html page with no AJAX loading or editing capabilities) - TM suports wikitext, xml and xsl content, but I think that all articles in this library are HTML based
  * **content**: [https://owasp.teammentor.net/content/56b0552d-2ceb-4714-a8f1-20a6a8609874](https://owasp.teammentor.net/content/56b0552d-2ceb-4714-a8f1-20a6a8609874) (the article's Html content with no TM Branding)
  * **jsonp**: [https://owasp.teammentor.net/jsonp/56b0552d-2ceb-4714-a8f1-20a6a8609874](https://owasp.teammentor.net/jsonp/56b0552d-2ceb-4714-a8f1-20a6a8609874) (to allow the easy consumption of TM content without worrying about that annoying _**same origin policy**_ security protection :) )
  * **wsdl**: [http://owasp.teammentor.net/aspx_pages/tm_Webservices.asmx](http://owasp.teammentor.net/aspx_pages/tm_Webservices.asmx)  - note: if you want to fuzz this, I can set-up a dedicated cloud version for you (on AppHarbor or Azure)

For reference the TM Documentation is at: [https://docs.teammentor.net](https://docs.teammentor.net/) 

The page [https://docs.teammentor.net/xml/Eval](https://docs.teammentor.net/xml/Eval) contains 4 videos and a download link (that points to the GitHub version) which allow you to run TM locally (btw look at the source code of that page and see some XML+XSL foo action :) )
