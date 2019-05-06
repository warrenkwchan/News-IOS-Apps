# News-IOS-Apps
It is to test how to grab articles using third party API and populate them on users' view

Purpose:

This is the first IOS project I started and I just want to simply make a news api and fetch the data from a third party api 
news.org (this is a very awesome website that give you different types of news). Their json format is simple and make it 
easy to make a model to transform/ parse the json data. The archecture is just API -> ArticleModel -> ViewController -> DetailViewController.

What I learned:

- solidify the best practice following MVC architectural pattern

- understanding important concepts of protocol and delegates. 
  -Protocol are just like Java Interface that specify a set of methods
  that other classes need to implement them if these will use the protocol.
  -Delegate took me a while to wrap my head around. Delegate in a general sense are to implements/handled protocol methods when 
   this delegate conform to the procotol and the delegate implementation of the protocols methods will be triggered when a class
   referencing this delegate has called to methods listed in protocol. The class doesn't care about how the delegate implements
   the protocol methods as long it trusts the delegate will give what is expected. 
   
- learn how to request an api call to fetch and parse the data. steps: url -> url object -> datatask session -> decode the data with our data model object
  -> resume the datatask. Also make sure to run the process in the main thread like in the user View instead of the Background in the controller
  
- learn UIViewDataSource and UIViewDelegate to show fetched data to populate on UIView with each artical as one cell in the view

- customerize each UIViewCell in with an Article cell class

- Cache the image and check if image and url exist in Cache, then return the image in return instead of download from the url again.

- set up segue for app navigation like tap on a cell and direct to another UIView (WebView in this case) 

- animation such as fade in fade out and loading bar 

How to run the project:

* clone the project, download xcode to your mac/macbook and then just open the whole project with Xcode

