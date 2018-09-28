## `rIP` an `R` package to detect responses from server farms on MTurk surveys

Takes an array of IPs and the user's X-Key, and passes these to `iphub.info`. Returns a dataframe with the IP address (used for merging), country code, country name, asn, isp, block, and hostname.

Especially important is the variable `block`, which gives a score indicating whether the IP address is likely from a server farm and should be excluded from the data. It is codes 0 if the IP is residential/unclassified (i.e. safe IP), 1 if the IP is non-residential IP (hostping provider, proxy, etc. -- should likely be excluded), and 2 for non-residential and residential IPs (more stringent, may flag innocent respondents).

The recommendation from iphub.info is to block or exclude those who score block = 1.

Credit to @tylerburleigh for pointing out the utility of iphub.info. His method for incorporating this information into Qualtrics surveys can be found here: https://twitter.com/tylerburleigh/status/1042528912511848448?s=19.
