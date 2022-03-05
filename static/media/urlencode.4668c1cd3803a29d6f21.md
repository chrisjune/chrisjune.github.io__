URL Encode and Decode Tool
==========================

Use the online tool from above to either encode or decode a string of text. 
For worldwide interoperability, URIs have to be encoded uniformly. 

To map the wide range of characters used worldwide into the 60 or so allowed characters in a URI, 
a two-step process is used:

*   Convert the character string into a sequence of bytes using the UTF-8 encoding
*   Convert each byte that is not an ASCII letter or digit to %HH, where HH is the hexadecimal value of the byte

For example, the string: François ,would be encoded as: `Fran%C3%A7ois`  
  
(The `"ç"` is encoded in UTF-8 as two bytes C3 (hex) and A7 (hex), 
which are then written as the three characters `"%c3"` and `"%a7"` respectively.) 
This can make a URI rather long (up to 9 ASCII characters for a single Unicode character), 
but the intention is that browsers only need to display the decoded form, and many protocols can send UTF-8 without the %HH escaping.

What is URL encoding?
---------------------

**URL encoding** stands for encoding certain characters in a URL by replacing them with one or more character triplets that consist of the percent character "`%`" followed by two hexadecimal digits. 
The two hexadecimal digits of the triplet(s) represent the numeric value of the replaced character.

The term **URL encoding** is a bit inexact because the encoding procedure is not limited to URLs ([Uniform Resource Locators](http://en.wikipedia.org/wiki/Url)), but can also be applied to any other URIs ([Uniform Resource Identifiers](http://en.wikipedia.org/wiki/Uniform_Resource_Identifier)) such as URNs ([Uniform Resource Names](http://en.wikipedia.org/wiki/Uniform_Resource_Name)). 
Therefore, the term percent-encoding should be preferred.

When and why would you use URL encoding?
---

When data that has been entered into HTML forms is submitted, the form field names and values are encoded and sent to the server in an HTTP request message using method GET or POST, or, historically, via email. The encoding used by default is based on a very early version of the general URI percent-encoding rules, with a number of modifications such as newline normalization and replacing spaces with "`+`" instead of "`%20`".

The MIME type of data encoded this way is `application/x-www-form-urlencoded`, and it is currently defined (still in a very outdated manner) in the HTML and XForms specifications. In addition, the CGI specification contains rules for how web servers decode data of this type and make it available to applications.

When sent in an HTTP GET request, application/x-www-form-urlencoded data is included in the query component of the request URI. When sent in an HTTP POST request or via email, the data is placed in the body of the message, and the name of the media type is included in the message's Content-Type header.

Which Characters Are Allowed in a URL?
---

The characters allowed in a URI are either _reserved_ or _unreserved_ (or a percent character as part of a percent-encoding). 
_Reserved_ characters are those characters that sometimes have special meaning, 
while _unreserved_ characters have no such meaning. 
Using percent-encoding, characters which otherwise would not be allowed are represented using allowed characters. 

The sets of reserved and unreserved characters and the circumstances under which certain reserved characters have special meaning have changed slightly with each revision of specifications that govern URIs and URI schemes.

According to [RFC 3986](http://www.gbiv.com/protocols/uri/rfc/rfc3986.html), 
the characters in a URL have to be taken from a defined set of unreserved and reserved [ASCII](http://en.wikipedia.org/wiki/ASCII) characters. 
Any other characters are not allowed in a URL.

The unreserved characters can be encoded, but should not be encoded. 
The unreserved characters are:  
  
`A B C D E F G H I J K L M N O P Q R S T U V W X Y Z a b c d e f g h i j k l m n o p q r s t u v w x y z 0 1 2 3 4 5 6 7 8 9 - _ . ~`

The reserved characters have to be encoded only under certain circumstances. 
The reserved characters are:  
  
`! * ' ( ) ; : @ & = + $ , / ? % # [ ]`


Encoding/Decoding a Piece of Text
---

[RFC 3986](http://www.gbiv.com/protocols/uri/rfc/rfc3986.html) does not define according to which character encoding table non-[ASCII](http://en.wikipedia.org/wiki/ASCII) characters (e.g. the umlauts ä, ö, ü) should be encoded. As **URL encoding** involves a pair of hexadecimal digits and as a pair of hexadecimal digits is equivalent to 8 bits, it would theoretically be possible to use one of the 8-bit code pages for non-ASCII characters (e.g. ISO-8859-1 for umlauts).

On the other hand, as many languages have their own 8-bit code page, 
handling all these different 8-bit code pages would be a quite cumbersome thing to do. 
Some languages do not even fit into an 8-bit code page (e.g. Chinese). 
Therefore, [RFC 3629](http://tools.ietf.org/html/rfc3629) proposes to use the [UTF-8](http://en.wikipedia.org/wiki/UTF-8) character encoding table for non-ASCII characters. 
The following tool takes this into account and offers to choose between the ASCII character encoding table and the UTF-8 character encoding table. If you opt for the ASCII character encoding table, 
a warning message will pop up if the **URL encoded/decoded** text contains non-ASCII characters.


External Links
---

*   More information about [percent-encoding](http://en.wikipedia.org/wiki/Percent-encoding) (Wikipedia)
*   [URL encoding](http://www.w3.org/International/O-URL-code.html) with Java (UTF-8 character encoding, source code available)
*   [W3C](https://www.w3schools.com/tags/ref_urlencode.asp) HTML URL Encoding Reference