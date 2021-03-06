##  Example example of SQL Injection using Database.SQLQuery from GitHub (and idea for Cat.NET workflow) 

After posting [Another example why SATS technology needs custom rules (re: Detecting SQL Injection on .NET Entity framework)](http://blog.diniscruz.com/2013/07/another-example-why-sats-technology.html)  I did [this search on GitHub,](https://github.com/search?q=Database.SqlQuery&type=Code&ref=searchresults) and found an example of that dangerous **_Database.SqlQuery_** API in use:  

  * https://github.com/caioketo/QIERP/blob/master/QIERPDatabase/VerpContext.cs#L55 
   * **with default sa pwd**: https://github.com/caioketo/QIERP/blob/master/QIERPDatabase/VerpContext.cs#L18 
   * **use of Database.ExecuteSqlCommand:** https://github.com/caioketo/QIERP/blob/master/QIERPDatabase/VerpContext.cs#L59

These one allows callers to create SQL Injection (which means that whoever is consuming those APIs need to be VERY careful)  


* https://github.com/revolutionaryarts/wewillgather/blob/master/src/Libraries/Gather.Data/GatherObjectContext.cs#L69
* https://github.com/philpeace/PointyPointy/blob/master/PointyPointy.Web/Data/StoryContext.cs#L51
* https://github.com/samandmoore/GetRDoneWeb/blob/master/GetRDone/GetRDoneContext.cs#L25
* https://github.com/slask/MVCArchitectureTemplate/blob/master/Solution/DataAccess/Context/ScrabbleClubContext.cs#L106

  
This one look OK (on diagonal reading)  

  * https://github.com/JayBeavers/ChronoZoom/blob/exceptionalIo/Source/Chronozoom.Entities/Storage.cs#L122 (Ok, because timelinesMap.Keys are GUIDs). There are multiple other uses of Database.SqlQuery which look ok because either the parameters options were used, or the string concats where done on GUIDs)

**Idea for Cat.NET workflow**  

Now wouldn't it be great if we could automate an Cat.NET (or another SAST scanner) to do this type of analysis automatically?

For example an Bot ot TeamCity workflow that:

  1. cloned/pulled a repo
  2. compile it
  3. run cat.net on it (with default or custom rules)
  4. automatically package the issues discovered 
  5. send issues to repo owner
  6. allow rules to be customised (maybe as an XML file somewhere in the repo), for example, wrappers around **_Database.SQLQuery_** need to be marked as sinks)
  7. go back to 1

I also would like a mode to create UnitTests based on the vulns discovered (using SAST and DAST techniques), but that is a topic for another post :)  


Ideally all this would be linked to Developer friendly guidance (like [TeamMentor](https://teammentor.net/) or OWASP content) in order to help the developers to easily understand the issues and write the required fixes
