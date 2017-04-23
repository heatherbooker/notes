Heather Booker (W1'16): @AJ Jordan (W2'17) remember when we dicussed with @Stanley Zheng (W1'16) about using a cdn to serve a site with https? can someone remind me why that's bad?

AJ Jordan (W2'17): @Heather Booker (W1'16) you mean with GitHub Pages?

Heather Booker (W1'16): yeah!

AJ Jordan (W2'17): Because the browser -> CloudFlare connection is fully protected but the CloudFlare -> GitHub Pages backend connection is very much vulnerable to man-in-the-middle attacks

AJ Jordan (W2'17): Because GitHub doesn't present a valid certificate so you have to configure CF to ignore cert errors

AJ Jordan (W2'17): Note that this only applies to custom domains - *.github.io like you have presents a valid HTTPS cert, so it's a non-issue
________________________________________________________________

AJ Jordan (W2'17): anyone who can listen in on a TLS connection is able to determine the domain name you're connecting to and the approximate amount of data you're sending, nothing else

AJ Jordan (W2'17): whereas your friend appears to think that you can determine which _page_ you're visiting when sampling a TLS connection, which is not true

AJ Jordan (W2'17): that's the technical inaccuracy

AJ Jordan (W2'17): *strictly technical inaccuracy

AJ Jordan (W2'17): another misconception, still mostly technical, is that the only reason to use HTTPS is for confidentiality (i.e. protecting "sensitive information")

AJ Jordan (W2'17): that's very much a misconception, albeit a widespread one

AJ Jordan (W2'17): another important thing that HTTPS provides is integrity

AJ Jordan (W2'17): there are documented cases of ISPs doing really nasty things to unencrypted web connections

AJ Jordan (W2'17): for example Comcast for a while would inject ads into pages going over its network (and they would make Comcast money, not the content owner)

AJ Jordan (W2'17): and if you Google for "Verizon supercookie" you can find documentation on a particularly disgusting practice in which Verizon would insert a unique tracking ID into every outbound HTTP request (based on the user's Verizon account ID), allowing servers to track you even if you used Private Browsing Mode, cleared your browser data, etc.

AJ Jordan (W2'17): also with HTTP you don't have to man-in-the-middle the connection... you can just passively spy on connections (though this might just be your friend using the term incorrectly)

AJ Jordan (W2'17): note also that passive attacks are way, way cheaper to perform than active man-in-the-middle attacks

AJ Jordan (W2'17): cheap enough that, say, a nation-state could do it to entire countries coughcoughNSA

AJ Jordan (W2'17): also, another technical inaccuracy I missed earlier - you don't have to be in the same physical location to attack an HTTP connection

AJ Jordan (W2'17): you can't do it from anywhere but anyone in a privileged network position can do it

AJ Jordan (W2'17): that includes the same physical location, but also includes the ISP, the server's ISP, etc.

AJ Jordan (W2'17): someone with access to the Internet backbone, maybe

AJ Jordan (W2'17): but to me the an argument that's far more compelling than any of that is this:

AJ Jordan (W2'17): when your friend says their site "doesn't contain sensitive information" it's not their place to make that assumption

AJ Jordan (W2'17): you don't know what's sensitive to your users
