##  Secure coding (and Application Security) must be invisible to developers 

At OWASP a while back we come up with the idea that _'...Our [OWASP] mission is to make application security visible...' _and for a while I used to believe in the idea that if only everybody had full visibility into 'Application Security' then we would solve the problem.

But after a while I started to realize that what we need to create for developers, is for 'Application Security' / 'Secure Coding' to be INVISIBLE 99% of the time. It is only the decision makers (namely the buyers) that need visibility into an application secure state

We will never get secure applications at a large scale if we require ALL developers (or even most) to be experts at security domains like Crypo, Authentication, Authorization, Input validation/sanitation, etc...

  
Note that I didn't say that NOBODY should be responsible for an Application's security. Of course that there needs to be a small subset of the players involved that really cares and understands the security implications of what is being created (we can call these the security champions).

**The core idea is that developers should be using Frameworks, APIs and Languages that allow them to create secure applications by design **(where security is there but is invisible to developers).

**And when they **(the developers or architects) **create a security vulnerability, at that moment **(and only then)**, they should have visibility into what they created **(i.e. the side effects)** and be shown alternative ways to do the same thing in a secure way.**  
**  
**This is how we can scale, which is why it is critical that OWASP (and anybody who cares about solving the application security problem) needs to focus in improving our Framework's ability to create secure apps.

One key problem that we still have today (April 2012)  which is preventing the mass 'invisibilitycation of security'  at Framework level, is that we are still missing Security-focused  SAST/Static-Analysis rules  
**  
****How we fixed Buffer Overflows**

A very good and successfully example of making security 'invisible' for developers was the removal of 'buffer overflows' from C/C++ to .Net/Java (i.e. from unmanaged to managed code).

Do .NET/Java developers care about overflowing their buffers when handing strings? No, since that is handled by the Framework :)

THAT is how we make security (in this case Buffer Overflow protection) Invisible to developers

**The Cooking Analogy**  
**  
**If you are looking for an analogy, "a chef cooking food" is probably the better one.

Think of software developers that are cooking with a number of ingredients (i.e. APIs).

Do you really expect that chef to be an expert on how ALL those ingredients (and tools he is using) were created and behave?

It is impossible, the chef is focused on creating a meal!!!

Fortunately the chef can be confident that some/all of his ingredients+tools will behave in a consistent and well documented way (which is something we don't have in the software world).

I like the food analogy because, as with software, one bad ingredient is all it takes to ruin it.

  
**Related Posts:**  


  * ["Making Security Invisible by Becoming the Developer's Best Friends"](http://diniscruz.blogspot.co.uk/2012/04/making-security-invisible-by-becoming.html) presentation
  * [Security evolution into Engineering Productivity](http://diniscruz.blogspot.co.uk/2012/04/security-evolution-into-engineering.html)
