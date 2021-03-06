##  Is there a spreadsheet/template for Mapping WebServices Authorization Rules? 

What is the best way to map/document the Authorization Rules? (for example of WebServices)  

I'm looking for a spreadsheet/template that allows the business-rules (i.e. 'who has access to what') to be mapped, visualized and analyzed.

I looked at [owasp.org](http://owasp.org/) and this is what I found (did I missed something?)

  * [Guide to Authorization](https://www.owasp.org/index.php/Guide_to_Authorization) 
  * [Codereview-Authorization](https://www.owasp.org/index.php/Codereview-Authorization) 
  * [Testing for Authorization](https://www.owasp.org/index.php/Testing_for_Authorization) 
  * [Reviewing Code for Authorization Issues](https://www.owasp.org/index.php/Reviewing_Code_for_Authorization_Issues) 
  * [Cheat Sheets](https://www.owasp.org/index.php/Cheat_Sheets) (no Authorization one)

In the past I have created a couple of these (some even with O2 Automation), but NDAs prevented me from sharing. So today, since [I'm helping Arvind](http://diniscruz.blogspot.co.uk/2012/05/creating-spreadsheet-with-webservices.html) to create a set of Python scripts to test TeamMentor's WebServices, I took the time to create a model which I think came out quite well.

You can read about it here: [Creating a spreadsheet with WebService's Authorization Mappings](http://diniscruz.blogspot.co.uk/2012/05/creating-spreadsheet-with-webservices.html) and this is what it looks like:

[https://docs.google.com/a/owasp.org/spreadsheet/ccc?key=0AhHDFVmo550OdDZUcDU5eXpGVGFKWDZjS3VGUHdUTXc](https://docs.google.com/a/owasp.org/spreadsheet/ccc?key=0AhHDFVmo550OdDZUcDU5eXpGVGFKWDZjS3VGUHdUTXc)

![Inline images 1](images/Spreedsheet_with_autz_4.jpg) 

Since I'm going to integrate this with O2 next, it is better to change it into a better format/standard now (vs later).

I also think that we should have a couple of these templates in an easy to consume format on the OWASP WIki (I have lost count the amount of times that I have tried to explain the need for 'such authorization tables/mappings' without having good examples at hand).

Note that creating these mappings is just one part of the puzzle! Also as important is the ability to keep it well maintained, up-to-date and relevant.