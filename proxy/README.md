The Proxy Pattern is about providing a placeholder for another object to control access to it. It basically creates an object that has a reference to the real object. Then when clients object or guests ask a request, this object will do the filtering (for example, a layer of security).

A big advantage of this approach is that it gives us a separation of concerns, as the proxy takes care of access control while the real object is only concerned about business logic

### The following is the code’s story.
We have two market places (One and Two). However, before users can access it (find the price of a specific item), we would like to specify some level of security. Check whether the user has a password and is a premium member. Then they can search through all the market places. If a user just has a password but is not a premium member, then they can only search the MarketPlaceOne.

From the source code below, we have a class for MarketPlaceOne and MarketPlaceTwo, each inheriting from MarketPlace so they can access the method find_price. From the main program line, we create three users (John, Anne, and Jenn), each with specific data. For example, John has a password and premium member.

We create the MarketPlaceProxy class, which contains two object references to MarketPlaceOne and MarketPlaceTwo. A user requests find_price, which cannot be asked directly to the market place but must go through a proxy (because only a proxy with references to both market places is allowed).

It’s inside find_price in MarketPlaceProxy (the filtering part). It will check user properties first (password and premium member) and if it passes, then it will pass the request to the real market place find_price method.

The benefit of this logic is that users do not have to know how many market places a company has right now, and it hides the complexity of find_price logic from users. When a company adds another new market place, we just change the code inside the market place proxy.