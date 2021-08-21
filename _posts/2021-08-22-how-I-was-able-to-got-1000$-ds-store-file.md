---
title: How I was able to got 1000$ bounty from a ds-store-file
author: xElkomy
categories: Bugbounty
tags: ["Bug bounty","How I was able to got 1000$ bounty from ds-store-file","Bug Bounty hunting","ds-store-file"]
math: true
---

<meta http-equiv=refresh content="0;url=https://xelkomy.medium.com/how-i-was-able-to-get-1000-bounty-from-a-ds-store-file-dc2b7175e92c">


![Thanks-h1](https://xelkomy.com/Images/_DSC6749_0.jpg)

## Hello
Hello gents and ladies :),
In this blog we will talk about one bug I was found before and to know I did not get this bug in just 5 minutes to know It needs experience with some patience to get some bug that was I mean, you need to learn more to be able to get a lot of bugs it's not a superpower but it's called a continuity pursuit.

## The Starter?
I will teach you how to get bounty from ds-store-file in 5 minutes [I Just kidding].
Let's Start with the starter pack..
In the first I was just collect some information about the subdomains and the ASNs numbers and check the Public CVEs with some tools I will montion them in below.
When I was collect the information I found the `/.DS_Store` I avilable I was know there is a tools easist to dump this file with the terminal I will montion there in the exploit section, I think to here we was talk about noting important let's go to the exploit section.

## Tools used in the Exploit

1 - [Subfinder](https://github.com/projectdiscovery/subfinder)
2 - [Httpx](https://github.com/projectdiscovery/httpx)
3 - [Nuclei](https://github.com/projectdiscovery/nuclei)
4 - [ds_store_exp](https://github.com/lijiejie/ds_store_exp)

Shout out to [@projectdiscovery](https://twitter.com/pdiscoveryio)

## Exploit
Hello again, In the first I was run a subfinder with httpx and got about 100 subdomain is alive and send this output to the nuclei public templates not a private.
And after this I will still wait to finish those tools but with the [owasp zap proxy](https://www.zaproxy.org/) I was do some manual searching about bug with this proxy and still nothing Important but after the Nuclei finished I found a subdomain with Info severity file called `/.DS_Store` after this I clone the `ds_store_exp` tool and use it to dump the file after dump I found a directory with a debug error from a Laravel Framework called Symfony watch the image below..

![Symfony-debug](https://xelkomy.com/Images/QtYCuPI.png)

But before that, I just saw a big error I can't understand anything about it but after some clicks, I got the image above.
let's continue

But after that, I report the bug as just debug enabled but one from the trigger team told me it's not a bug what is the impact you can get from it, In the first reaction from me it was I can't get anything but after some minutes about one hour, I click on the latest button on the left and found cookies and IP it's not formed me it was for one from the trigger team in the program and I try to use that cookie on the main site It was the exciting thing I take over the account with just a debug mode enabled just need one click from the user to go to the error page and I can just steal his cookies.

I think it is a high impact now but the team consider it as a medium, I don't understand why.

## Time Line

1 - Submit the Report at Aug 14th - 2021.
2 - More information at Aug 14th - 2021.
3 - Send a new information at Aug 14th - 2021.
4 - Triged at Aug 14th - 2021.
5 - Recive a bounty at Aug 19th - 2021 It was a 500$ bounty and 500$ bouns.


Please don't forget to follow me on the twitter to watch a new blogs from me on [@0xELkomy](https://twitter.com/0xElkomy) and if you have any comment also send to me thanks.
Feel free to connect with me if you have anything.
