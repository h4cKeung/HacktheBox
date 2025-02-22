```bash
whatweb --color=never --no-errors -a 3 -v http://10.10.11.186:80 2>&1
```

[/home/parallels/HacktheBox/Machines/10.10.11.186-MetaTwo/results/10.10.11.186/scans/tcp80/tcp_80_http_whatweb.txt](file:///home/parallels/HacktheBox/Machines/10.10.11.186-MetaTwo/results/10.10.11.186/scans/tcp80/tcp_80_http_whatweb.txt):

```
WhatWeb report for http://10.10.11.186:80
Status    : 302 Found
Title     : 302 Found
IP        : 10.10.11.186
Country   : RESERVED, ZZ

Summary   : HTTPServer[nginx/1.18.0], nginx[1.18.0], RedirectLocation[http://metapress.htb/]

Detected Plugins:
[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : nginx/1.18.0 (from server string)

[ RedirectLocation ]
	HTTP Server string location. used with http-status 301 and
	302

	String       : http://metapress.htb/ (from location)

[ nginx ]
	Nginx (Engine-X) is a free, open-source, high-performance
	HTTP server and reverse proxy, as well as an IMAP/POP3
	proxy server.

	Version      : 1.18.0
	Website     : http://nginx.net/

HTTP Headers:
	HTTP/1.1 302 Moved Temporarily
	Server: nginx/1.18.0
	Date: Wed, 07 Dec 2022 05:04:02 GMT
	Content-Type: text/html
	Content-Length: 145
	Connection: close
	Location: http://metapress.htb/

WhatWeb report for http://metapress.htb/
Status    : 200 OK
Title     : MetaPress &#8211; Official company site
IP        : 10.10.11.186
Country   : RESERVED, ZZ

Summary   : Cookies[PHPSESSID], HTML5, HTTPServer[nginx/1.18.0], MetaGenerator[WordPress 5.6.2], nginx[1.18.0], PHP[8.0.24], PoweredBy[--], Script, UncommonHeaders[link], WordPress[5.6.2], X-Powered-By[PHP/8.0.24]

Detected Plugins:
[ Cookies ]
	Display the names of cookies in the HTTP headers. The
	values are not returned to save on space.

	String       : PHPSESSID

[ HTML5 ]
	HTML version 5, detected by the doctype declaration


[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : nginx/1.18.0 (from server string)

[ MetaGenerator ]
	This plugin identifies meta generator tags and extracts its
	value.

	String       : WordPress 5.6.2

[ PHP ]
	PHP is a widely-used general-purpose scripting language
	that is especially suited for Web development and can be
	embedded into HTML. This plugin identifies PHP errors,
	modules and versions and extracts the local file path and
	username if present.

	Version      : 8.0.24
	Google Dorks: (2)
	Website     : http://www.php.net/

[ PoweredBy ]
	This plugin identifies instances of 'Powered by x' text and
	attempts to extract the value for x.

	String       : --

[ Script ]
	This plugin detects instances of script HTML elements and
	returns the script language/type.


[ UncommonHeaders ]
	Uncommon HTTP server headers. The blacklist includes all
	the standard headers and many non standard but common ones.
	Interesting but fairly common headers should have their own
	plugins, eg. x-powered-by, server and x-aspnet-version.
	Info about headers can be found at www.http-stats.com

	String       : link (from headers)

[ WordPress ]
	WordPress is an opensource blogging system commonly used as
	a CMS.

	Version      : 5.6.2
	Aggressive function available (check plugin file or details).
	Google Dorks: (1)
	Website     : http://www.wordpress.org/

[ X-Powered-By ]
	X-Powered-By HTTP header

	String       : PHP/8.0.24 (from x-powered-by string)

[ nginx ]
	Nginx (Engine-X) is a free, open-source, high-performance
	HTTP server and reverse proxy, as well as an IMAP/POP3
	proxy server.

	Version      : 1.18.0
	Website     : http://nginx.net/

HTTP Headers:
	HTTP/1.1 200 OK
	Server: nginx/1.18.0
	Date: Wed, 07 Dec 2022 05:04:03 GMT
	Content-Type: text/html; charset=UTF-8
	Transfer-Encoding: chunked
	Connection: close
	X-Powered-By: PHP/8.0.24
	Set-Cookie: PHPSESSID=fmd8525csbubv2je4is097a1q7; path=/
	Expires: Thu, 19 Nov 1981 08:52:00 GMT
	Cache-Control: no-store, no-cache, must-revalidate
	Pragma: no-cache
	Link: <http://metapress.htb/wp-json/>; rel="https://api.w.org/"
	Content-Encoding: gzip



```
