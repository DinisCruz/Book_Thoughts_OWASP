##  CI is the Key for Application Security SDL integration 

The more time I spent with [CI](http://en.wikipedia.org/wiki/Continuous_integration) (namely with [TeamCity](http://blog.diniscruz.com/search/label/TeamCity)) the more my instinct is saying_ 'this is how we should be delivering and automating security knowledge!'_.  
  
CI environments (namely its scheduling capabilities) could be use to:  


  * Create scannable artifacts (i.e. projects, dlls, jars, etc...) for SAST engines
  * Create _'live versions'_ of the target site (in a clean and pre-populated-with-data states) for DAST engines (and pentest activities)
  * Automatically run SAST engines (like cat.net for example)
  * Run Unit-tests with further analysis
  * Trigger security actions (based on events like Git commits)
  * Trigger 'consolidation' analysis (for example of results from multiple tools) and publishing to results into other SDL tools (namely bug tracking systems)
  * Modify source-code (to automatically inject security guidance and fixes) -- see  [Fixing/Encoding .NET code in real time (in this case Response.Write)](http://o2platform.wordpress.com/2011/11/07/fixingencoding-net-code-in-real-time-in-this-case-response-write/) for a cool PoC
  * Inject security guidance into the application (maybe even exposing developers to it in the source code :) )
  * Create and sent reports to multiple stake-holders
  * Be the receiving end of security reports

Its the ability to create schedules and triggerable actions that is really getting me excited :)

So maybe what we (app security teams) should be doing is to start our engagements by setting up an CI environment (which would be integrated with the client's CI environment if they had one)

This also goes to the core of the idea that ["If we want to fix Security .... we have to fix Development"](http://blog.diniscruz.com/2012/10/amazing-presentation-on-integrating.html)

In a way that is why was so I interrested in the idea of integrating IBM's AppScan products with their [Rational Jazz](https://jazz.net/) tools (which have a number of CI/Collaboration capabilities). In fact that is exactly what I described in my [IBM AppScan 2011](http://blog.diniscruz.com/2009/11/part-i-ibm-application-security-related.html) post.

Isn't it amazing that IBM and HP have all the tools needed to create a real powerful (and effective) security remediation ecosystem, but just can't do it for cultural and political reasons?

And btw, OWASP is also completely MIA in the CI field 
