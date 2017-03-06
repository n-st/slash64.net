# IPv6. You're doing it wrong.

If you're reading this, you've probably been called out on assigning unreasonably small IPv6 subnets or even individual IPv6 addresses to your customers.  
Here's why you should reconsider and assign a separate /64 subnet to each customer:

* [RFC 6177: IPv6 Address Assignment to End Sites](https://tools.ietf.org/html/rfc6177#section-5):

  > The recommendation in RFC 3177 to assign /48s as a default is not a requirement of the
     IPv6 architecture; **anything of length /64 or shorter works from a
     standards perspective**.

* [Why Allocating a /64 is Necessary](http://etherealmind.com/allocating-64-wasteful-ipv6-not/):

  > * Simplicity
  > * Route Summarisation
  > * (Not) Breaking IPv6

* [IPv6 Email is a little different: One customer, one /64](https://wordtothewise.com/2015/07/ipv6-email-is-a-little-different/):

  > A large hosting company did that recently, assigning each of their customers a small range of IPv6 addresses out of a single /64 – and they discovered why it’s a terrible idea. They had no more than the usual level of email delivery problems on IPv4, but all of their IPv6 mail was blocked at a lot of destinations. Because a /64 is the smallest recommended range to assign to a user it’s also the smallest quantum that reputation services and blacklists will block by. Bad behaviour by one of their customers got the /64 that customer was sending from blocked – along with all the other customers sending from other parts of that /64.
  > 
  > So don’t do that.