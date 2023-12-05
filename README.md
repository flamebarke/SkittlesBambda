# SkittlesBambda

If you haven't heard of Bambdas before check out the [Portswigger](https://portswigger.net/blog/introducing-bambdas) announcement first.

This Burp Suite Bambda was inspired by this Bambda I stumbled across on github:

[https://github.com/BugBountyzip/Bambdas](https://github.com/BugBountyzip/Bambdas)

and this gist posted on X by @irsdl:

[https://x.com/irsdl/status/1729261410830725368?s=20](https://x.com/irsdl/status/1729261410830725368?s=20)

I took a look at both Bambdas, combined some functions, added some extra code and came up with a Bambda that:

1. identifies potentially vulnerable parameters 
2. filters the requests within the http proxy history
3. applies a colour highlight for each different vuln class (SSRF, SQLi, XSS, LFI, RCE)
4. if multiple classes of vulnerability apply the request is highlighted magenta
4. adds a note annotation containing the potential vuln class and the matched parameter (concatenates multiple vuln classes if present)

It's super easy to modify this function, just add in new parameters or a whole new custom array if you are looking for something specific.

![Bambda](/assets/img/bambdas/bamba.png)
