Base64 (MIME) Encode Tool
=========================

Use this free tool to turn binary data into text (encode) or text into binary (decode). 

To allow binary data to be transmitted with textual data it must be encoded. An example of this is an attachment in an email. This is done via the [MIME](http://en.wikipedia.org/wiki/MIME) implementation of Base64. The MIME implementation uses the characters `A-Z`, `a-z`, and `0-9` for the initial 62 values that it can use to encode data.

For example, the text:

`Chris Tools are cool!`

Would be encoded as...

`RGFuJ3MgVG9vbHMgYXJlIGNvb2wh`

What is Base64 encoding?
---

The term **Base 64** is generic, and there are many implementations. MIME, which stands for Multi-Purpose Internet Mail Extensions, is the most common that is seen today. It is used to transmit attachments via email over the Simple Mail Transfer Protocol (SMTP). 

Other examples of Base64 encoding are [Radix-64](http://en.wikipedia.org/wiki/Base64#Radix_64_applications_not_compatible_with_Base64) and [YUI's Y64](http://www.yuiblog.com/blog/2010/07/06/in-the-yui-3-gallery-base64-and-y64-encoding/). Encoding data in Base64 results in it taking up roughly 33% more space than the original data.
MIME Base64 encoding is the most common, and is based on the [RFC 1420](http://tools.ietf.org/html/rfc1421) specification. It also uses a `=` character at the end of a string to signify whether the last character is a single or double byte.

When and why would you use Base64 encoding?
---

You should use Base64 whenever you intend to transmit binary data in a textual format.

Code Examples
---

### PHP
`base64_encode($string);`

`base64_decode($string);`

### Perl

`encode_base64($string);`

`decode_base64($string);`

Requires `use MIME::Base64;`

### C#

`System.Convert.ToBase64String(System.Text.Encoding.UTF8.GetBytes(plainTextBytes));`

`System.Text.Encoding.UTF8.GetString(System.Convert.FromBase64String(base64EncodedData));`

### Java

`Base64.encodeBase64(string);`

`Base64.decodeBase64(string);`

Requires `import org.apache.commons.codec.binary.Base64;`

### JavaScript

`btoa(string);`

`atob(string);`

### Ruby

Base64.encode64('string')

Base64.decode64(enc)

Requires `require "base64"`

External Links
---

*   More information about [Base64](http://en.wikipedia.org/wiki/Base64) (Wikipedia)