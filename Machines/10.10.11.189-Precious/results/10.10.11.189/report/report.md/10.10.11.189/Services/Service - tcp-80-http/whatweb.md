```bash
whatweb --color=never --no-errors -a 3 -v http://10.10.11.189:80 2>&1
```

[/home/parallels/HacktheBox/Machines/10.10.11.189-Precious/results/10.10.11.189/scans/tcp80/tcp_80_http_whatweb.txt](file:///home/parallels/HacktheBox/Machines/10.10.11.189-Precious/results/10.10.11.189/scans/tcp80/tcp_80_http_whatweb.txt):

```
WhatWeb report for http://10.10.11.189:80
Status    : 302 Found
Title     : 302 Found
IP        : 10.10.11.189
Country   : RESERVED, ZZ

Summary   : HTTPServer[nginx/1.18.0], nginx[1.18.0], RedirectLocation[http://precious.htb/]

Detected Plugins:
[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : nginx/1.18.0 (from server string)

[ RedirectLocation ]
	HTTP Server string location. used with http-status 301 and
	302

	String       : http://precious.htb/ (from location)

[ nginx ]
	Nginx (Engine-X) is a free, open-source, high-performance
	HTTP server and reverse proxy, as well as an IMAP/POP3
	proxy server.

	Version      : 1.18.0
	Website     : http://nginx.net/

HTTP Headers:
	HTTP/1.1 302 Moved Temporarily
	Server: nginx/1.18.0
	Date: Fri, 02 Dec 2022 05:45:12 GMT
	Content-Type: text/html
	Content-Length: 145
	Connection: close
	Location: http://precious.htb/

WhatWeb report for http://precious.htb/
Status    : 200 OK
Title     : Convert Web Page to PDF
IP        : 10.10.11.189
Country   : RESERVED, ZZ

Summary   : HTML5, HTTPServer[nginx/1.18.0 + Phusion Passenger(R) 6.0.15], nginx[1.18.0], Ruby-on-Rails, UncommonHeaders[x-content-type-options], X-Frame-Options[SAMEORIGIN], X-Powered-By[Phusion Passenger(R) 6.0.15], X-XSS-Protection[1; mode=block]

Detected Plugins:
[ HTML5 ]
	HTML version 5, detected by the doctype declaration


[ HTTPServer ]
	HTTP server header string. This plugin also attempts to
	identify the operating system from the server header.

	String       : nginx/1.18.0 + Phusion Passenger(R) 6.0.15 (from server string)

[ Ruby-on-Rails ]
	Ruby on rails is an MVC web application framework written
	in the ruby language. Doesn't detect all RoR sites

	Website     : http://www.rubyonrails.org.

[ UncommonHeaders ]
	Uncommon HTTP server headers. The blacklist includes all
	the standard headers and many non standard but common ones.
	Interesting but fairly common headers should have their own
	plugins, eg. x-powered-by, server and x-aspnet-version.
	Info about headers can be found at www.http-stats.com

	String       : x-content-type-options (from headers)

[ X-Frame-Options ]
	This plugin retrieves the X-Frame-Options value from the
	HTTP header. - More Info:
	http://msdn.microsoft.com/en-us/library/cc288472%28VS.85%29.
	aspx

	String       : SAMEORIGIN

[ X-Powered-By ]
	X-Powered-By HTTP header

	String       : Phusion Passenger(R) 6.0.15 (from x-powered-by string)

[ X-XSS-Protection ]
	This plugin retrieves the X-XSS-Protection value from the
	HTTP header. - More Info:
	http://msdn.microsoft.com/en-us/library/cc288472%28VS.85%29.
	aspx

	String       : 1; mode=block

[ nginx ]
	Nginx (Engine-X) is a free, open-source, high-performance
	HTTP server and reverse proxy, as well as an IMAP/POP3
	proxy server.

	Version      : 1.18.0
	Website     : http://nginx.net/

HTTP Headers:
	HTTP/1.1 200 OK
	Content-Type: text/html;charset=utf-8
	Transfer-Encoding: chunked
	Connection: close
	Status: 200 OK
	X-XSS-Protection: 1; mode=block
	X-Content-Type-Options: nosniff
	X-Frame-Options: SAMEORIGIN
	Date: Fri, 02 Dec 2022 05:45:14 GMT
	X-Powered-By: Phusion Passenger(R) 6.0.15
	Server: nginx/1.18.0 + Phusion Passenger(R) 6.0.15
	X-Runtime: Ruby
	Content-Encoding: gzip



```
