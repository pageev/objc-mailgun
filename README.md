The Mailgun SDK allows your Mac OS X or iOS application to connect with the [Mailgun](http://www.mailgun.com) programmable email platform. Send and manage mailing list subscriptions from your desktop or mobile applications and connect with your users directly in your application.

Fork notes
===========

Forked to migrate to AFNetworking version 3.0. 

Original objc-mailgun stopped on AFNetworking v1.1.0 which is pretty outdated and produce problems when using others pods which require newer versions of AFNetworking.

Original objc-mailgun git repo can be found [here](https://github.com/rackerlabs/objc-mailgun).


Installation
============

Install via Cocoapods - Add:

    pod 'mailgun', :git => 'https://github.com/pageev/objc-mailgun'

to your Podfile.
  
Easy Image Attaching
====================
 
Using MGMessage will allow you to attach `UIImage` or `NSImage` instances to a message. It will handle converting the image for you and attaching it either inline or to the message header.

API Support
===========

At this time the full Mailgun REST API is not supported. Currently support is only provided to send messages, subscribe/unsubscribe from mailing lists and to check mailing lists subscriptions.

*Note* These features may be implemented at a later date.
 
Sending Example
===============

     Mailgun *mailgun = [Mailgun clientWithDomain:@"samples.mailgun.org" apiKey:@"key-3ax6xnjp29jd6fds4gc373sgvjxteol0"];
     [mailgun sendMessageTo:@"Jay Baird <jay.baird@rackspace.com>" 
                       from:@"Excited User <someone@sample.org>" 
                    subject:@"Mailgun is awesome!" 
                       body:@"A unicode snowman for you! ☃"];
