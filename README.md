<!--
Location: ATX
Last edited by: Justin Castilla
Created by: Justin Castilla
(Extracted from a longer command line guide from WDI33)
-->

![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Clients, Servers, and You!

### Why is this important?
<!-- framing the "why" in big-picture/real world examples -->
*This workshop is important because:*

Most people are familiar with their computers' graphical user interface, rich with icons and buttons.   The command line interface, or CLI, is an alternative without these fancy graphics -- a plain, text-­based interface for performing tasks on a computer.

Many of the tasks developers perform are faster when done from the command line, and the command line interface usually has some extra features that are hidden in normal graphical interfaces. That's because programmers assume someone using the command line is more knowledgeable about their computer and less likely to make mistakes.  Think about that from an employment perspective, too. As a developer, you will be expected to be proficient with your computer, including performing basic tasks on the command line.

### What are the objectives?
<!-- specific/measurable goal for students to achieve -->
*After this workshop, developers will be able to:*

- Familiarize themselves with the basic technology transactions of browsing the web
- Understand the differencee between a domain name and an IP address
- Identity the main differences between a human-language domain address and an IP Address.


### Where should we be now?
<!-- call out the skills that are prerequisites -->
*Before this workshop, developers should already be able to:*

- Open an internet browser and navigate to a website
- Imagine invisible radio signals going from your laptop to somewhere else. 
- Realize that computers are NOT magic but are - in fact - quite logical and well-organized


## What is this client/server magic?

The client–server model is a distributed application structure that partitions tasks or workloads between the providers of a resource or service, called servers, and service requesters, called clients.  

<img src="http://www.reactiongifs.com/wp-content/uploads/2013/10/tim-and-eric-mind-blown.gif">
  
Often clients and servers communicate over a computer network on separate hardware, but both client and server may reside in the same system. 
 
A **server host** runs one or more server programs which share their resources with clients. 

A **client** does not share any of its resources, but requests a server's content or service function. Clients therefore initiate communication sessions with servers which await incoming requests. 
  
Examples of computer applications that use the client–server model are Email, network printing, music streaming services, social media, and pretty much the whole World Wide Web. 
 
<a href='https://en.wikipedia.org/wiki/Client%E2%80%93server_model'>- Source</a>



![](https://cloud.githubusercontent.com/assets/4304660/23087118/80f5e464-f526-11e6-8f74-6bde3cdaa66c.png)

## The how and why
There are currently **1,151,254,186** websites in existence.  You are currently on one laptop.  How are you able to travel to every single one of those websites from your little dinky laptop with an expectation of speed and accuracy?  

Domain Name System, or **DNS servers**, act as information redirectors that will direct your search for a certian website to it's actual physical server location.  When we enter `https://www.google.com` into our browser, we actually go on a fantastic and magical ride across at least three separate servers across our greater region (mainly in Dallas for WDI-11) that help us find the actual Google server.

The Process:  

1. Type www.google.com into your browser address bar.
 
2. Your browser sends an HTTP Request (internet magic) to a DNS server. HTTP - at this point - can be thought of as an envelope of information that is sent to and from clients and servers. It includes a request type, header information, information on what the HTTP request wants in return, and where the HTTP request wants to go.



3. The DNS server looks for a server that has a big list of all `.com` websites and sends us the IP address of that server.  An IP address is a series of digits that act just like a physical street address.

4. Now that we're in the `.com` server, they send us to yet *another* server that will send us to a more specific DNS server that, for example, maybe contains only websites that start with the letters `E` through `K`. 

5. We have finally been taken to the DNS server that knows where Google.com is! Yay!  The final DNS server gives us the specific IP address of Google.com (139.130.4.5).

6. Our browser finally goes to the address given by the last DNS Server and we see the beautiful Google landing page of the day!

<img width="698" alt="screen shot 2017-02-18 at 10 25 37 am" src="https://cloud.githubusercontent.com/assets/4304660/23095784/a542df90-f5c4-11e6-8c19-0909f77d6b9d.png">


## Cool, but now what?
We now have Google displayed on our browser. This is great! We made a **request** for the webpage, and we received a **response** from Google's server.  Now what do we do if we want to find awesome gif files of puppies? There's going to be another set of **requests** and **responses**.


<img src="http://i.giphy.com/l2YWxte7sJB2XuE8M.gif">


We now send a request to Google for puppy gifs.  It looks like this up in the address bar when we type in our search: 

```html
https://www.google.com/#safe=on&q=puppy+gifs
```

This is the piece of information that is sent to Google. The section of information `#safe=on&q=puppy+gifs` tells google we want safe search to be on (SFW, people!) and our **query** is for puppy gifs.  

We send this **request** to Google directly (no more DNS Servers.) Google receives our information, finds puppy gifs for us, then sends back a web page with the resulting information as a **response**. 

This pattern of **requests** for information from clients and relevant **responses** from servers is the backbone of modern internet activity. Neat, right?!

## Closing Thoughts
- DNS (Domain Name Systems) allow us to quickly and efficiently navigate to websites
- The Request and Response cycle of Client/Server communications is the foundation of all internet-based interactions.
- Requests and Responses are comprised of specific HTTP packets sent back and forth between the client and the server




### Additional Resources

* <a href="https://www.youtube.com/watch?v=GlZC4Jwf3xQ" target="_blank">Awkward but lovable guy gives technical description of DNS Servers</a>
* <a href="http://searchnetworking.techtarget.com/definition/client-server" target="_blank">A tangible article on TCP/IP Protocols</a>
* <a href="https://en.wikipedia.org/wiki/Domain_Name_System" target="_blank">Name Servers - A main component of DNS Servers</a>
* <a href="https://en.wikipedia.org/wiki/Name_server" target="_blank">DNS Server Wikipedia Page</a>


