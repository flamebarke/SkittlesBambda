# SkittlesBambda

If you haven't heard of Bambdas before check out the [PortSwigger](https://portswigger.net/blog/introducing-bambdas) announcement first.

This Burp Suite Bambda was inspired by the below Bambda I stumbled across on github:

[https://github.com/BugBountyzip/Bambdas](https://github.com/BugBountyzip/Bambdas)

and this code posted on X by @irsdl:

[https://x.com/irsdl/status/1729261410830725368?s=20](https://x.com/irsdl/status/1729261410830725368?s=20)

I took a look at both Bambdas, combined some functions, added some extra code and came up with a Bambda that:

1. Identifies potentially vulnerable parameters 
2. Filters the requests within the http proxy history
3. Applies a colour highlight for each different vuln class (SSRF, SQLi, XSS, LFI, RCE)
4. If multiple classes of vulnerability apply the request is highlighted magenta
4. Adds a note annotation containing the potential vuln class and the matched parameter (concatenates multiple vuln classes if present)

It's super easy to modify this function, just add in new parameters or a whole new custom array if you are looking for something specific.

![Bambda](/bambda.png)
