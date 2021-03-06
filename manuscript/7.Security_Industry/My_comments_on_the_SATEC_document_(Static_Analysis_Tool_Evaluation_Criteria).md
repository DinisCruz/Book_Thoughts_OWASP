##  My comments on the SATEC document (Static Analysis Tool Evaluation Criteria) 

(submitted today to the wasc-satec@lists.webappsec.org list)

A bit late (deadline for submission is today) but are my notes on the version currently at [http://projects.webappsec.org/w/page/41188978/Static%20Analysis%20Tool%20Evaluation%20Criteria](http://projects.webappsec.org/w/page/41188978/Static%20Analysis%20Tool%20Evaluation%20Criteria)  

My comments/notes are marked as _Conted to add in underscore, bold and Italic_ or **_[content to be deleted in red]_**  

When I wanted to make a comment on particular change or deletion, I did it on a new line:

_DC Comment: ... a comment goes here in dark blue_

Of course that this is my opinion, and these notes are based on the notes I took in 'analogue mode' (i.e. on paper :)  )  


--------------------------------------------------------  

**Table of Contents:**

**Introduction:**

Static Code Analysis is the analysis of software code **_[without actually executing the binaries resulting from this code]_**. 

>_DC Comment: we don't need the extra definition, since it is possible to do static code analysis based on information/code/metadata obtained at run-time or via selective execution/simulation of the code/binaries. The key concept is that static analysis is about analysing and applying rules to a set of artefacts that have been extracted from the target application. From this point of view, we can do static analysis on an AST (extracted from source code), an intermediate representation (extracted from a .net or java binary) or run-time traces (extracted from a running application). We can also do static analysis on an application config files, on an application's authorisation model or even on application specific data (for example the security controls applied to a particular asset)_

  


Static code analysis aims at automating code analysis to find as many common **_[quality and]_** security software issues as possible. There are several open source and commercial analyzers available in the market for organizations to choose from. 

  


_DC Comment: it doesn't make sense to add 'quality' to mix (in fact the more I read this document the more I thought that the word 'security' should be part of the title of this document/criteria. Quality is a massive area in its own right, and apart form this small comment/reference, there is not a lot of 'software quality' on this document. This is a a document focused on Software security issues :) , and yes security is a sub-set of quality (which is ok if referenced like that)_

  


Static code analysis analyzers are rapidly becoming an essential part of every software organization's application security assurance program. Mainly because of the analyzers' ability to analyze large amounts of source code in considerably shorter amount of time than a human could, **__and the ability to automate security knowledge and workflows__**

**__  
__**

_DC Comment: The key advantage of static analysis is that it can codify an application security specialist knowledge and workflows.  By this, I mean that for the cases where it is possible to codify a particular type of analysis (and not all types of analysis can be automated), these tools can perform those **analysis in a repeatable, quantifiable and consistent way.** Scanning large code-bases is important, but more important is the ability to scale security knowledge, specially since I've seen cases where 'large code scans' where achieved by dropping results or skipping certain types of analysis-types (in fact most scanners will scan an app of any size if you delete all its rules :) )_

  


The goal of the SATEC project is to create a vendor-neutral document to help guide application security professionals during **__the creation of an __**source-code driven security **__programme__** **_[assessments]_**.  This document provides a comprehensive list of features that should be considered when **__evaluating__** **_[conducting] _** a security code **__Tool__** **_[review]_**. Different users will place varying levels of importance on each feature, and the SATEC provides the user with the flexibility to take this comprehensive list of potential analyzer features, narrow it down to a shorter list of features that are important to the user, assign weights to each feature, and conduct a formal evaluation to determine which scanning solution best meets the user's needs.

  


The aim of this document is not to define a list of _requirements_ that all static code analyzers must provide in order to be considered a "complete" analyzer, and evaluating specific products and providing the results of such an evaluation is outside the scope of the SATEC project.  Instead, this project provides the analyzers and documentation to enable anyone to evaluate static code analysis analyzers and choose the product that best fits their needs.  NIST Special Publication 500-283, "Source Code Security Analysis Analyzer Functional Specification Version 1.1", contains minimal functional specifications for static code analysis analyzers.  This document can be found at [http://samate.nist.gov/index.php/Source_Code_Security_Analysis.html](http://samate.nist.gov/index.php/Source_Code_Security_Analysis.html).

  


  


**Target Audience: **

The target audience of this document is the technical staff of software  organizations who are looking to automate parts of their source code driven security testing using one or more static code analyzers,**__and application security professionals (internal or external to the organisation) that responsible for performing application security reviews__**. The document will take into consideration those who would be evaluating the analyzer and those who would actually be using the analyzer. 

  


**Scope: **

The purpose of this document is to develop a set of criteria that should be taken into consideration while evaluating Static Code Analysis **_Tools_** **_[analyzers]_** for security testing. 

  


_DC Comment (and rant): OK, WTF is this 'Analysis Analyzers' stuff!!! This is about a **Tool** right? of course that a tool that does software analysis, is an analyzer, but saying that it we are talking about a code analysis analyzer sounds quite redundant :) There is TOOL in the name of the document, and we are talking about tools. In fact, these static analysis tools perform a bunch of analysis and more importantly (as multiple parts of this document cover), the **Analyzer **part of these analysis tools is just **one **of its required/desired features (for example enterprise integration and deployability are very important, and have nothing to do with __the 'Analyzer' part._

_  
_

_If I can't change your mind to change the redundant Analyzer, them you will need to rename this document to SAAEC (Static Analysis Analyzer Evaluation Criteria), actually what about the SAAEA (Static Analysis Analyzer Evaluation Analysis) :)_

  


Every software organization is unique in their environment. The goal is to help organizations achieve better application security in their own unique environment, the document will strictly stay away from evaluating or rating analyzers. However, it will aim to draw attention to the most important aspects of static analysis **_Tools_** **_[analyzers]_**  that would help the target audience identified above to choose the best **_Tool_** **_[analyzer]_**  for their environment and development needs. 

  


**Contributors:**

  


Aaron Weaver (Pearson Education)

Abraham Kang (HP Fortify)

Alec Shcherbakov (AsTech Consulting)

Alen Zukich  (Klocwork)

Arthur Hicken (Parasoft)

Amit Finegold (Checkmarx)

Benoit Guerette (Dejardins)

Chris Eng (Veracode)

Chris Wysopal (Veracode)

Dan Cornell (Denim Group)

Daniel Medianero (Buguroo Offensive Security)

Gamze Yurttutan

Henri Salo

Herman Stevens

Janos Drencsan

James McGovern (HP)

Joe Hemler (Gotham Digital Science)

Jojo Maalouf (Hydro Ottawa)

Laurent Levi  (Checkmarx)

Mushtaq Ahmed (Emirates Airlines)

Ory Segal (IBM)

Philipe Arteau 

Sherif Koussa (Software Secured) [Project Leader]

Srikanth Ramu (University of British Columbia)

Romain Gaucher  (Coverity)

Sneha  Phadke (eBay)

Wagner Elias (Conviso)

  


  


**Contact:**

Participation in the Web Application Security Scanner Evaluation Criteria project is open to all.  If you have any questions about the evaluation criteria, please contact Sherif Koussa ( sherif dot koussa at gmail dot com)

  


**Criteria:**

_  
_

_DC Comment: I think this criteria should be split into two separate parts:_

  * _**Operational Criteria **- These are generic items that are desired on any application that wants to be deployed on an enterprise (or to a large number of users). Anything that is not specific to analysing an application for security issues (see next point) should be here. For example installation, deployability, standards, licensing, etc.. (in fact this could be a common document/requirement across the multiple WASC/OWASP published criterias)_
  * _**Static Analysis Criteria - **Here is where all items that are relevant to an static analysis tool should exist. These items should be specific and non-generic. For example _

  * _**'the rules used by the engine should be exposed and consumable' **is an operational criteria (all tools should allow that)_
  * _**'the rules used by the engine should support taint-flow analysis'** is an static analysis criteria (since only these tools do taint-flow analysis)_

_Below I marked each topic with either [Operational Criteria] or [Static Analysis Criteria]_

  


**1. Deployment:**** **

Static code analyzers often represent a significant investment by software organizations looking to automate parts of their software security testing processes. Not only do these analyzers represent a monetary investment, but  they demand time and effort by staff members to setup, operate, and maintain the analyzer. In addition, staff members are required to check and act upon the results generated by the analyzer. Understanding the ideal deployment environment for the analyzer will maximize the derived value, help the organization uncover potential security flaws and will avoid unplanned hardware purchase cost. The following factors are essential to understanding the analyzer's capabilities and hence ensuring proper utilization of the analyzer which will reflect positively on the analyzer's utilization. 

  


**1.1 Analyzer Installation Support:****  **_[Operational Criteria]_

A static code analyzer should provide the following :

  * **Installation manual: **specific instructions on installing the analyzer and its subsystems if any (e.g. IDE plugins) including minimum hardware and software requirements.
  * **Operations manual: **specific and clear instructions on how to configure and operate that analyzer and its subsystems.
  * **SaaS Based Analyzers: **since there is no download or installation typically involved in using a SaaS based analyzer, the vendor should be able to provide the following:

  * Clear instructions on how to get started.
  * Estimated turn-around time since the code is submitted until the results are received.
  * What measures are being taken to keep the submitted code or binaries as well as to the reports confidential.

  


**1.2 Deployment Architecture:****  **_[Operational Criteria]_

Vendors provide various analyzer deployment options. Clear description of the different deployment options must be provided by the vendor to better utilize the analyzer within an organization. In addition, the vendor must specify the optimal operating conditions. At a minimum the vendor should be able to provide:

  * The type of deployment: server-side vs client-side as this might require permissions change or incur extra hardware purchase.
  * Ability to run simultaneous scans at the same time.
  * The analyzers capabilities of accelerating the scanning speed  (e.g. ability to multi-chain machines, ability to take advantage of multi-threaded/multi-core environments, etc)
  * The ability of the analyzer to scale to handle more applications if needed. 

  


**1.3 Setup and Runtime Dependencies:**** **_[Static Analysis Criteria]_

The vendor should be able to state whether the **_Tool_** **_[analyzer]_** uses a compilation based analysis or source code based analysis.

  * Compilation based analysis: where the **_Tool_** **_[analyzer]_** first compiles the code together with all dependencies, or the analyzer just analyses the binaries directly. Either ways, the analyzer requires all the application's dependencies to be available before conducting the scan, this enables the analyzer to scan the application as close to the production environment as possible.
  * Source code based analysis: does not require dependencies to be available for the scan to run. This could allow for quicker scans since the dependencies are not required at scan time.
  * **__Dynamic based analysis: where the tool analyzes data collected from real-time (or simulated) application/code execution (this could be achived with AOP, code instrumentation, debugging traces, profiling, etc..)__**

  


**2. Technology Support:**** **_[Static Analysis Criteria]_

Most organizations leverage more than one programming language within their applications portfolio. In addition, more software frameworks are becoming mature enough for development teams to leverage and use across the board as well as a score of 3rd party libraries, technologies, libraries which are used both on the server and client side. Once these technologies, frameworks and libraries are integrated into an application, they become part of it and the application inherits any vulnerability within these components. 

  


**2.1 Standard Languages Support:****  **_[Static Analysis Criteria]_

Most of the analyzers support more than one programming language. However, an organization looking to **_use_** **_[acquire]_** a static code analysis **_Tool_** **_[analyzer]_**  should make an inventory of all the programming languages, and their versions, used within the organizations as well as third party applications that will be scanned as well. After shortlisting all the programming languages and their versions, an organization should compare the list against the **_Tool's_** **_[analyzer's]_** supported list of programming languages and versions. Vendors provide several levels of support for the same language, understanding what level of support the vendor provides for each programming language is key to understanding the coverage and depth the analyzer provides for each language. One way of understanding the level of suppor**__t__** for a particular language is to inspect the **_Tool's_** **_[analyzer's] _**signatures (AKA Rules or Checkers) for that language.  

  


_DC Comment: very important here is to also map/define if these rules are generic or framework/version specific. For example do all java rules apply to all java code, or are there rules that are specific to particular version of Java (for example 1.4 vs 1.7) or Framework (for example spring 1.4 vs 2.0)._

_  
_

_This is really important because there are certain vulnerabilities that only exist on certain versions of particular frameworks. For example, I __believe that the HttpResponse.Redirect in the version 1.1 of the .NET Framework was vulnerable to Header Injection, but that was fixed on a later release. Static code analysis should take this into account, and not flag all unvalidated uses of this Redirect method as Header Injection vulnerabilities._

  


**2.2 Programming Environment Support:****  **_[Static Analysis Criteria]_

Once an application is built on a top of a framework, the application inherits any vulnerability in that framework. In addition, depending on how the application leverages a framework or a library, it can add new attack vectors. _It is very important for the analyzer to be able to be able to trace tainted data through the framework as well as the custom modules built on top of it_.

  


_DC Comment: No, I don't agree with the underscored line above. **What is important is to understand HOW the frameworks work/behave**_

_  
_

_Also this comment doesn't make a lot of sense in the way most (if not all) current static analysis is done. There are two key issues here_

_  
_

_#1) what is the definition of a 'Framework'_

_#2) what does it mean to 'trace tainted data through the framework'_

_  
_

_On #1, unless we are talking about C/C++ (and even then) most code analysis is done on Frameworks. I.e. everything is a framework (from the point of view of the analysis engine). The analysis engine is 'told' that a particular method behaves in a particular way and it bases its analysis based on that_

_  
_

_From the point of view of a scanning engine, there is no difference between the way asp.net aspx works, vs the way the asp.net mvc framework behaves. Same thing for java, where from the scanning engine point of view there is no difference between the classes in a JRE (see _http://hocinegrine.com/wp-content/uploads/2010/03/jdk_jre.gif_) and Spring Framework classes_

_  
_

_In fact most static analysis is done based on:_

_  
_

_- **sources**: locations of the code that are known to have malicious data (which we call tainted data)_

_- **taint propagators** : methods that will pass tainted data to one of its parameters or return value_

_- **validators**: methods that will remove taint (ideally not blankly but based on a particular logic/vulnType)_

_- **reflection/hyper-jumps/glues**: cases where the application flow jumps around based on some (usually framework-driven) logic_

_- **sinks**: methods that are known to have a particular vulnerability (and should not be exposed to tainted data)_

_- **application control flows** : like **if** or **switch** statements which affect the exposure (or not) to malicious/taint data_

_- **application logic**: like mapping the authorization model and analysing its use_

_  
_

_The way most analysis is done, is to have rules that tell the engine how a particular method works. So in the .NET framework, the tools don't analyse Request.Querystring or Response.Write. They are 'told' that one is a source and the other is a sink. In fact, massive blind spots happen when there are wrappers around these methods that 'hide' their functionality from the code being analysed._

_  
_

_Even on C, there is usually a rule for _**strcpy**_ which is used to identify buffer overflows. Again most scanners will miss methods that have the exact same behaviour as _**strcpy **but are called something differently (in fact, I can write such methods C# that are vulnerable to buffer overflows which will missed by most (if not all) current tools :)  ). 

  


On the #2 point, yes ideally the scanners should be scanning the inside of these methods, but most scanners (if not all) would blow up if they did. 

  


And even if they did it, it wouldn't really work since each vulnerability has a particular set of patterns and context. 

  


So what does it mean _'to trace tainted data through frameworks'_? Are we talking about being able to follow taint over a sequence like this:

  


a) **request** **starts** on a **view** that is posting data to a

b) **controller** that sends the data to the

c) **business/db layer **which does something with it, and sends the result to a 

d) **view** that **displays** the **result** to user?

  


THIS is what I think it is important. I.e. we are able to analyze data based on the actual call-flow of the application. 

  


So in a way, we don't need to 'trace data' **_through_** the frameworks (as in **_'what is going on inside'_**) but on **top of the frameworks **(as in **_'what code is touched/executed_**)

  


This is actually where the new type of scanners which do a mix of static and dynamic analysis (like seeker, contrast, glass box stuff from IBM, etc...) have a big advantage (vs traditional AST or binary-based scanners), since they can actually 'see' what is going on, and know (for example) which view is actually used on a particular controller.

  


  


 At large, frameworks and libraries can be classified to three types:

  * **Server-side Frameworks:**frameworks/libraries that reside on the server, e.g. Spring, Struts, Rails, .NET etc
  * **Client-side Frameworks:**which are the frameworks/libraries that reside on browsers, e.g. JQuery, Prototype, etc
  * **__where is the 3rd type?__**

  


  


DC Comment: these 'types of framework' doesn't make sense here (i.e these are not really different 'types of frameworks', just different execution engines.

  


Now on the topic of **client-side and server-side code,** the real interesting questions are: 

  * Can the tool 'connect' traces from server-side code to traces on the client-side code?
  * Can the tool understand the context that the server-side code is used on the client side (for example the difference between a Response.Write/TagLib been used to output data into a an HTML element or an HTML attribute)

  


Understanding the relationship between the application and the frameworks/libraries is key in order to detect vulnerabilities resulting from the application's usage of the framework or the library, and the following in particular:

  


  * identify whether the application is using the framework in a insecure manner.
  * The analyzer would be able to follow tainted data between the application and the framework.
  * The analyzer's ability to identify security misconfiguration issues in the framework\library. 
  * Well-known vulnerability identified by the [Common Vulnerabilities and Exposures](http://cve.mitre.org/) (CVE)

  


  


DC Comment: see my point above about everything being a framework, and in fact, what happens is that most apps are made of:

  


a) language APIs

b) base class APIs

c) 3rd party frameworks that extend the base class APIs with new functionality

d) in-house APIS

  


Which all behave like 'frameworks'

  


Which means, that the first important question to ask is: **What is the level of Framework support that a particular tool has?**

  


The 2nd (and what I like about the items listed above) is the import question of: **Is the Framework(s) being used securely?**

**  
**

The 2nd point is very important, since even frameworks/apis that are designed to provide a security service (like an encoding/filtering/authentication api) can be used insecurely

  


In a way, what we should be asking/mapping here is: What are the known issues/vulnerabilities that the tool is able to detect?

  


Note: one of the areas that we (security industry) is still failing a lot, is in helping/pushing the framework vendors to 'codify how their frameworks' behaves, so that our tools/manual analysis know what to look for

  


  


**2.3 Industry Standards Aided Analysis:**** **

Industry standard weaknesses classification, e.g. [OWASP Top 10](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project), [CWE/SANS Top 25](http://www.sans.org/top25-software-errors/), [WASC Threat Classification](http://projects.webappsec.org/w/page/13246970/Threat%20Classification%20Enumeration%20View), [DISA/STIG](http://www.disa.mil/) etc provide organizations with starting points to their software security gap analysis and in other cases these calssifications become metrics of minimum adherence to security standards. Providing industry standard aided analysis becomes a desirable feature for many reasons. 

  


_DC Comment:  I don't understand the relevance of this 2.3 item (in this context). These 'standards' are more relevant in the list of issues to find and in vulnerability discovery __repairing_

  


**2.4 Technology Configuration Support:**** **_[Static Analysis Criteria]_

Several tweaks provided by the analyzer could potentially uncover serious weaknesses.** **

  * ****Configuration Files Redefinition: **** configurations to other file types (e.g. *.ini, *.properties, *.xml, etc). It is a desirable and a beneficial feature to configure the analyzer to treat a non-standard extension as a configuration file. 
  * **Extension to Language Mapping: **the ability to extend the scope of the analyzer to include non-standard source code file extensions. For example, JSPF are JSP fragment files that should be treated just like JSP files. Also, HTC files are HTML fragment files that should be treated just like HTML files. PCK files are Oracle's package files which include PL/SQL script. While a analyzer does not necessarily have to understand every non-standard extension, it should include a feature to extend its understanding to these extensions.

  


_DC Comment:  The key issue here is for the Tool to understand how the target app/framework behaves. And that is only possible if the artefacts used by those frameworks are also analyzed. _

_  
_

_I would propose that we rename this section as 'Framework configuration support' and add more examples of the types of 'thing's that need to be looked at (for example the size of Models in MVC apps which could lead to Mass-Assignment/Auto-Binding vulnerabilities)_

  


**3. Scan, Command and Control Support:****  **_[Operational Criteria]_

The scan, command and control of static code analysis analyzers has a significant influence on the user's ability to configure, customize and integrate the analyzer into the organization's Software Development Lifecycle (SDLC). In addition, it affects both the speed and effectiveness of processing findings and remediating them.

  


**3.1 Command line support:****  **_[Operational Criteria]_

The user shouldbe able to perform scans using the command line which is a desirable feature for many reasons, e.g. avoiding unnecessary IDE licensing, build system integration, custom build script integration, etc. For SaaS based tools, the vendor should be able to indicate whether there are APIs to initiate the scan automatically, this becomes a desirable feature for scenarios involving large number of applications.

  


**3.2 IDE integration support:****  **_[Operational Criteria]_

The vendor should be able to enumerate which IDEs (and versions) are being supported by the analyzer being evaluated, as well as what the scans via the IDE will incorporate. For example, does an Eclipse plugin scan JavaScript files and configuration files, or does it only scan Java and JSP files.

  


_DC Comment:  the key question to ask here is __**WHO is doing the scan? **I.e is the scan actually done by the IDE's plugin (like on Cat.net case) or the plug-in is just a 'connector' into the main engine (running on another process or server). Most commercial scanners work in the later way, where the IDE plugins are mainly used for: scan triggers, issues view, issues triage and reporting_

  


**3.3 Build systems support: **_[Operational Criteria]_

The vendor should be able to enumerate the build systems supported and their versions (Ant, Make, Maven, etc). In addition, the vendor should be able to describe what gets scanned exactly in this context.

  


**3.4 Customization:**** **_[Static Analysis Criteria]_

The analyzer usually comes with a set of signatures (AKA as rules or checkers), this set is usually followed by the analyzer to uncover the different weaknesses in the source code. Static code analysis should offer a way to extend these signatures in order to customize the analyzer's capabilities of detecting new weaknesses, alter the way the analyzer detect weaknesses or stop the analyzer from detecting a specific pattern. The analyzer should allow users to:

  * **Add/delete/modify core signatures: **Core signatures come bundled with the analyzer by default. False positives is one of the inherit flaws in static code analysis analyzers in general. One way to minimize this problem is to optimize the analyzer's core signatures, e.g. mark a certain source as safe input. 
  * **Author custom signatures:** authoring custom signature are used to "educate" the analyzer of the existence of a custom cleansing module, custom tainted data sources and sinks as well as a way to enforce certain programming styles by developing custom signatures for these styles.
  * **Training: **the vendor should state whether writing new signatures require extra training.

_  
_

_DC Comment: customisation is (from my point of view) THE most important __differentiator of an engine (since out-of-the-box most, most commercial scanners are kind-of-equivaleant (i.e. they all work well in some areas and really struggle on others)._

_  
_

_Here are some important areas to take into account when talking about customization:_

  * _Ability to access (or even better, to manipulate) the internal-representations of the code/app being analysed_
  * _Ability to extend the current types of rules and findings (being able to for example add an app/framework specific authorization analysis)_
  * _Open (or even known/published) schemas for the tool's: rules, findings and intermediate representations_
  * _Ability for the client to publish their own rules in a license of their choice_
  * _REPL environment to test and develop those rules_
  * _Clearly define and expose the types of findings/analysis that the Tools rules/engine are NOT able to find (ideally this should be application specific)_
  * _Provide the existing 'out-of-the-box' rules in an editable format (the best way to create a custom rules is to modify an existing one that does a similar job). This is a very important point, since (ideally) ALL rules and logic applied by the scanning engine should be customizable _
  * _Ability to package rules, and to run selective sets of rules_
  * __Ability_ to (re)run an analysis for one 1 (one) type of issue_
  * __Ability_ to (re)run an analysis for one 1 (one) reported issue (or for a collection of the same issues)_
  * _Ability to create unit tests that validate the existence of those rules_
  * _Ability to create unit tests that validate the findings provided by the tools_

_The last points are very important since they fit into how developers work (focused on a particular issue which they want to 'fix' and move on into the next issue to 'fix')_

  


**3.5 Scan configuration capabilities:****  **_[Operational Criteria]_

This includes the following capabilities:

  * **Ability to schedule scans:** Scans are often scheduled after nightly builds, some other times they are scheduled when the CPU usage is at its minimum. Therefore, it might be important for the user to be able to schedule the scan to run at a particular time. For SaaS based analyzers, the vendor should indicate the allowed window of submitting code or binaries to scan.
  * **Ability to view real-time status of running scans: **some scans would take hours to finish, it would be beneficial and desirable for a user to be able to see the scan's progress and the weaknesses found thus far. For SaaS based analyzers, the vendor should be able to provide accurate estimate of the results delivery. 
  * **Ability to save configurations and re-use them as configuration templates: **Often a significant amount of time and effort is involved in optimally configuring a static code analyzer for a particular application.  A analyzer should provide the user with the ability to save a scan's configuration so that it can be re-used for later scans.
  * **Ability to run multiple scans simultaneously: **Organizations that have many applications to scan, will find the ability to run simultaneous scans to be a desirable feature.
  * **Ability to support multiple users: **this is important for organizations which are planning to rollout the analyzer to be used by developers checking their own code. It is also important for organizations which are planning to scan large applications that require more than one security analyst to assess applications concurrently.
  * **_[Static Analysis Criteria] _****Ability to perform incremental scans: **incremental scans proves helpful when scanning large applications multiple times, it could be desirable to scan only the changed portions of the code which will reduce the time needed to assess the results.

  


_DC Comment: the ability to perform incremental scans is not really a 'configuration' but it is a 'capability' _

_  
_

_DC Comment: On the topic of deployment I would also add a chapter/sections called:_

_  
_

_**"3.x Installation workflow **__[Operational Criteria]_

_**  
**_

_There should be detailed instructions of all the steps required to install the tool. Namely how to go from a _

  


_a) clean VM with XYZ operating system installed, to_

_b) tool ready to scan, to _

_c) scan completed"_

_  
_

_**"3.x Scanning requirements **_**_[Static Analysis Criteria] _**

_**  
**_

_There should be detailed examples of what is required to be provided in order for a (or THE optimal) scan to be triggered. For example some scanners can handle a stand-alone dll/jar , while others need all dependencies to be provided. Also the scanners that do compilation tend to be quite temperamental when the scanning server is not the same as the normal compilation/CI server"_

_  
_

  


**3.6 Testing Capabilities:****  **_[Static Analysis Criteria]_

**  
**

_DC Comment: In my view this whole section (3.6) should be restructured to match the types of analysis that can be done with static analysis tools._

_  
_

_For example XSS, SQLi, File transversal, Command Injection, etc... are all '__source to sink' vulnerabilities. Where what matters is the tools ability to follow tainted data across the application (and the ability to add new sources and sinks)_

_  
_

_What I really feel we should be doing here is to map out the capabilities that are important for a static analysis tool, for example:_

  * _**Taint propagation** (not all do this, like FxCop) _

  * _Intra-procedue_
  * _Inter-procedue_

* _**Handing of Collections, setters/getters, Hashmaps **(for example is the whole object tainted or just the exact key (and for how long))_
* _**Reflection**_
* _**Event driven flows **(like the ones provided by ASP.NET HttpModules, ASP.NET MVC, Spring MVC, etc...)_
* _**Memory/objects manipulations** (important for buffer overflows)_
* _**String Format** analysis (i.e. what actually happens in there, and what is being propagated)_
* _**String** Analysis (for regex and other string manipulations)_
* _**Interfaces** (and how they are mapped/used)_
* _**Mapping views to controllers **, and more importantly, mapping tainted data inserted in model objects used in views_
* _**Views nesting **(when a view uses another view)_
* _**Views use of non-view APIs** (or custom view controls/taglibs)_
* _**Mapping of Authorization and Authentication** models and strategies_
* _**Mapping of internal methods** that are exposed to the outside world (namely via WEB and REST services)_
* _**Join traces** (this is a massive topic and one that when supported will allow the post-scan handling of a lot of the issues listed here)_
* _**Modelling/Visualization of the real size of Models** used in MVC apps (to deal with Mass-Assignment/Auto-binding), and connecting them with the views used_
* _**Mapping of multi-step data-flows** (for example data in and out of the database, or multi-step forms/worflows). Think reflected SQLi or XSS_
* _**Dependency injection** _
* _**AoP code** (namely cross cuttings)_
* _**Validation/Sanitisation** **code** which can be applied by config changed, metadata or direct invocation_
* _**Convention-based behaviours** , where the app will behave on a particular way based on how (for example) a class is named_
* _**Ability to consume data from other tools **(namely black-box scanners, Thread modelling tools, Risk assessment, CI, bug tracking, etc..), including other static analysis tools_
* _**List the type of coding techniques that are 'scanner friendly' **, for example an app that uses hashmaps (to _move data around) _or has a strong event-driven architecture (with no direct connection between source and sink) is not very static analysis friendly_
* _....there are more, but hopefully this makes my point...._

_As you can see, the list above is focused on the **capabilities of static analysis tool,** not on the type of issues that are 'claimed' that can be found._

_  
_

_All tools say they will detect SQL injection, but __what is VERY IMPORTANT (and what matters) is **the ability to map/rate all this 'capabilities' to the application being tested** (i.e asked the question of '**can vuln xyz be found in the target application given that it uses Framework XYZ and is coded using Technique XYZ' **)_

_  
_

_This last point is key, since most (if not all tools) today only **provide results/information about what they found and not what they analyzed.**_

_**  
**_

_I.e if there are no findings of vuln XYZ? does that mean that there are no XYZ vulns on the app? or the tool was not able to find them?_

_  
_

_In a way what we need is for tools to also report back the **level of assurance that they have on their results** (i.e based on the code analysed, its coverage and current set of rules, **how sure is the tool that it found all issues?**)_

_  
_

Scanning an application for weaknesses is an important functionality of the analyzer. It is essential for the analyzer to be able to understand, accurately identify and report the following attacks and security weaknesses.

  * API Abuse
  * Application Misconfiguration
  * Auto-complete Not Disabled on Password Parameters 
  * Buffer Overflow
  * Command Injection 
  * Credential/Session Prediction
  * Cross-site Scripting 
  * Denial of Service
  * Escalation of Privileges 
  * Insecure Cryptography 
  * Format String
  * Hardcoded Credentials 
  * HTTP Response Splitting
  * Improper Input Handling
  * Improper Output Encoding
  * Information Leakage
  * Insecure Data Caching 
  * Insecure File Upload  
  * Insufficient Account Lockout 
  * Insufficient Authentication
  * Insufficient Authorization
  * Insufficient/Insecure Logging 
  * Insufficient Password Complexity Requirements
  * Insufficient Password History Requirements 
  * Insufficient Session Expiration
  * Integer Overflows
  * LDAP Injection
  * Mail Command Injection
  * Null Byte Injection
  * Open Redirect Attacks 
  * OS Command Injection
  * Path Traversal
  * Race Conditions 
  * Remote File Inclusion
  * Second Order Injection 
  * Session Fixation
  * SQL Injection
  * URL Redirection Abuse
  * XPATH Injection
  * XML External Entities
  * XML Entity Expansion
  * XML Injection Attacks 
  * XPATH Injection

  


  


**4. Product Signature Update:  **** **_[Operational Criteria]_

Product signatures (AKA rules or checkers) are what the static code analysis analyzer use to identify security weaknesses. When making a choice of a static analysis analyzers, one should take into consideration the following:

  


**4.1 Frequency of signature update:**** **

Providing frequent signature update to a static code analysis **_Tool_** **_[analyzer]_**  ensure the analyzer's relevance to threat landscape.Hence, it is important to understand the following about a analyzer's signature update:

  * Frequency of signature update: whether it is periodically, on-demand, or with special subscription, etc.
  * Relevance of signatures to evolving threats:  Information must be provided by the vendor on how the products signatures maintain their relevance to the newly evolving threats.

  


**4.2 User signature feedback:**** **

The analyzers must provide a way for users to submit feedback on bugs, flawed rules, rule enhancement, etc.

  


**5. Triage and Remediation Support:****  **_[Static Analysis Criteria]_

A crucial factor in a static code analysis **_Tool_** **_[analyzer]_** is the support provided in the triage process and the accuracy, effectiveness of the remediation advice. This is vital to the speed in which the finding is assessed and remediated by the development team.

  


**5.1 Finding Meta-Data: **** **

Finding meta-data is the information provided by the analyzer around the finding. Good finding meta-data helps the auditor or the developer to understand the weakness and decide whether it is a false positive quicker. The analyzer should provide the following with each finding:

  * Finding Severity: the severity of the finding with a way to change it if required.
  * Summary: explanation of the finding and the risk it poses on exploit.
  * Location: the source code file location and the line number of the finding.
  * Data Flow: the ability to trace tainted data from a source to a sink and vise versa.

  


_DC Comment: The tool should provide as much as possible (if not all) data that it created (for each issue reported, and the issues NOT reported). There should be a mode that allows the use of the internal representations of the analysis performed, and all the rules that were triggered/used_

_  
_

**5.2 Meta-Data Management:**** **

  * The analyzer should provide the ability to mark a finding as false positive.
  * Ability to categorize false positives. This enforces careful consideration before marking a finding as false positive, it also allows the opportunity to understand common sources for false positives issues, this could help in optimizing the results. 
  * Findings marked as false positives should not appear in subsequent scans. This is helps avoid repeating the same effort on subsequent scans.
  * The analyzer should be able to merge\diff scan results. This becomes a desirable feature if\when the application is re-scanned, the analyzer should be able to append results of the second scan to the first one.
  * The vendor should be able to indicate whether the analyzer support the ability to define policies that incorporate flaw types, severity levels, frequency of scans, and grace periods for remediation.  

  


**5.3 Remediation Support:**

  * The analyzer should provide accurate and customizable remediation advice.
  * Remediation advise should be illustrated with examples written in the same programming language as the finding's.

  


  _DC Comment: Ability to extend the reports and Join traces is also very __important_

_  
_

**6. Reporting Capabilities:****  **_[Operational Criteria]_

The analyzer's reporting capability is one of its most visible functionalities to stakeholders. An analyzer should provide different ways to represent the results based on the target audience. For example, developers will need as much details as possible in able to remediate the weakness properly in a timely fashion. However, upper management might need to focus on the analysis's high level summary, or the risk involved more so than the details of every weakness. 

  


**6.1 Support for Role-based Reports: **** **

The analyzer should be able to provide the following types of reports with the ability to mix and match:

  * Executive Summary: provides high-level summary of the scan results.
  * Technical Detail Reports: provides all the technical information required for developers to understand the issue and effectively remediate it. This should include:

  * Summary of the issue that includes the weakness category.
  * Location of the issue including file name and line of code number.
  * Remediation advice which must be customized per issue and includes code samples in the language of choice.
  * Flow Details which indicates the tainted data flow from the source to the sink.   

  * Compliance Reports:Scanners should provide a report format that allows organizations to quickly determine whether they are in violation of regulatory requirements or other standards.  These reporting capabilities should be considered if certain regulations are important to the organization.  The following list provides some potentially applicable standards:

  * OWASP Top 10
  * WASC Threat Classification
  * CWE/SANS Top 25
  * Sarbanes-Oxley (SOX)
  * Payment Card Industry Data Security Standard (PCI DSS)
  * Health Insurance Portability and Accountability Act (HIPAA)
  * Gramm-Leach-Bliley Act (GLBA)
  * NIST 800-53
  * Federal Information Security Management Act (FISMA)
  * Personal Information Protection and Electronic Documents Act (PIPEDA)
  * Basel II

  


**6.2 Report Customization:**** **

The analyzer should be able to support report customization. At a minimum, the analyzer should be able to provide the following:

  * Ability to include the auditor's findings notes in the report.
  * Ability to mark findings as false positives, and remove them from the report.
  * Ability to change the report's template to include the organization's logo, header, footer, report cover,etc. 

  


**6.3 Report Formats:**** **

The vendor should be able to enumerate the report formats they support (PDF, XML, HTML, etc)

  

**7. Enterprise Level Support: ****  **_[Operational Criteria]_

When making a choice on a static analysis analyzer in the Enterprise, one should take into consideration the ability to integrate the analyzer into various enterprise systems, such as bug tracking, reporting, risk management and data mining.

  


**7.1 Integration into Bug Tracking Systems:**** **

Vendors should be able to enumerate the supported bug tracking applications, in addition to how are they being supported (direct API calls, CSV export, etc)

  


_DC Comment: More importantly: **HOW is that that integration done?**_

_**  
**_

_For example, if there are 657 vulnerabilities found, are there going to be 657 new bug tracking issues? or 1 bug? or 45 bugs (based on some XYZ criteria)?_

  


**7.2   Integration into Enterprise Level Risk Management Systems:**** **

Information security teams and organizations need to present an accurate view of the risk posture of their applications and systems at all times. Hence, the analyzer should provide integration into enterprise level risk management systems. 

  


_DC Comment: same as above, what is important here is to ask 'how is it done?'_

_  
_

_And for the vendors that also sell those other products, they should provide details on how that integration actually happens (which ironically, in a lot of cases, they don't really have a good integration story/capabilities)_

  


**7.3   Ability to Aggregate Projects:**** **

This pertains to the ability to add meta-data to a new scan. This data could be used to aggregate and classify projects, which could be used to drive intelligence to management. For example, this can help in identifying programming languages that seem to genere more findings thus better utilizing training budge for example. 

  


_DC Comment: And how to integrate with aggregator  tools like ThreadFix_

  


Another example, is to mark certain applications as "External Facing" which triggers the analyzer to perform a more stringent predefined scan template.

  


_DC Comment: this last paragraph should not be here (Enterprise support) and would make more sense in the 'Customization section'_

_  
_

Projects in organizations are built using a certain set of technologies and/or frameworks. These can be commercial, open source or built in-house. Certain projects may tend to have more security flaws as compared to others based on a technology or framework used or based on the how the technology\framework is used within a given business context. Static analysis analyzers could be used to configure similar projects with additional metadata to detect these patterns. This will build intelligence around them that lends to being able to detect which application components have more security weaknesses and why.

_  
_

_DC Comment: this last paragraph is important, but also feels out of place here_

  


  


**7.4   Licensing Scheme:**** **

Static Code Analysis analyzers varies in their licensing schemes. Usually, the following factors decide on the analyzer's total cost of ownership.

  * Licensing Scheme Factors:

  * Metered scan (pay-per-line) license: licensing fees depends on how many lines of code needs to be scanned.
  * Pay-per-application license : a license would issued for a specific application and can't be used for any other applications.
  * Time-based Subscriptions: one or more applications could be scanned unlimited number of times before the expiration of the license. 
  * Per-user licenses: a user-based license that is usually combined with one or more of the other schemes.
  * Unlimited/perpetual Licenses: for scanning unlimited applications by unlimited users. 
  * Server costs: for client\server models.

* Licensing Scheme Enforcement: 

  * License Server: dedicated server where licenses are stored and can be accessed by users on the network.
  * Local/node-locked: License is tied to a specific OS type, machine and named user.
  * User locked: license is tied to a specific username.
  * Floating: a number of licenses are shared among a larger number of users over time.
  * Trust or contract based: the licensing scheme mentioned in the contract is assumed to be honoured by the user with no extra enforcement.

_  
_

_DC Comment:  __add question about 'Open schemas' (i.e. do they exist?), and the multiple evaluation options_

  


**Index A: Static Code Analysis Preparation Cheat Sheet:**** **

Taking a decision about the correct static code analysis analyzer to acquire could be a daunting, however, preparation for such a task could be very helpful. Every analyzer is unique so as your corporate environment. The following is a set of information you need to gather which could make the decision much easier to take:

  * A list of the programming languages used in the organization.
  * A list of the frameworks and libraries used in the organization.
  * Who will be tasked to perform the scan
  * How the analyzer will be integrated into the Software Development Lifecycle
  * How will the developers see the scan results
  * Budget allocated to the analyzer purchase including the hardware to run the machine (if any)
  * A decision on whether the code (or the binaries) is allowed to be scanned outside the organization.

  


**Index B: References **

  * WASC Threat Classifications ([http://projects.webappsec.org/w/page/13246978/Threat%20Classification](http://projects.webappsec.org/w/page/13246978/Threat%20Classification))
  * Web Applications Security Scanner Evaluation Criteria ([http://projects.webappsec.org/w/page/13246986/Web%20Application%20Security%20Scanner%20Evaluation%20Criteria](http://projects.webappsec.org/w/page/13246986/Web%20Application%20Security%20Scanner%20Evaluation%20Criteria)) 
  * NIST Source Code Security Analysis Analyzer Functional Specifications Version 1.1 ([http://samate.nist.gov/docs/source_code_security_analysis_spec_SP500-268_v1.1.pdf](http://samate.nist.gov/docs/source_code_security_analysis_spec_SP500-268_v1.1.pdf)) 
  * Static Program Analysis ([http://en.wikipedia.org/wiki/Static_program_analysis](http://en.wikipedia.org/wiki/Static_program_analysis))
  * List of Analyzers For Static Code Analysis ([http://en.wikipedia.org/wiki/List_of_analyzers_for_static_code_analysis](http://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)) 

  


  

