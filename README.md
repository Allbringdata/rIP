## `rIP` detects Fraud in online surveys by tracing, scoring, and visualizing IP addresses

<!-- [![CRAN_Status_Badge](https://www.r-pkg.org/badges/version/rIP)](http://cran.r-project.org/package=rIP) -->
[![CRAN RStudio mirror downloads](http://cranlogs.r-pkg.org/badges/rIP)](http://www.r-pkg.org/pkg/rIP)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=plastic)](https://github.com/MAHDLab/rIP/pulls)
<!-- [![GitHub license](https://img.shields.io/github/license/MAHDLab/rIP.svg?style=plastic)](https://github.com/MAHDLab/rIP/blob/master/LICENSE) -->

Takes an array of IPs and the keys for the services the user wishes to use (IP Hub, IP Intel, and Proxycheck), and passes these to all respective APIs. Returns a dataframe with the IP addresses (used for merging), country, ISP, labels for non-US IP Addresses, VPS use, and recommendations for blocking. Users also have the option to visualize the distributions.

Especially important in this is the variable "block", which gives a score indicating whether the IP address is likely from a server farm and should be excluded from the data. It is codes 0 if the IP is residential/unclassified (i.e. safe IP), 1 if the IP is non-residential IP (hostping provider, proxy, etc. - should likely be excluded), and 2 for non-residential and residential IPs (more stringent, may flag innocent respondents).

`rIP` requires users to have active (free) accounts and/or valid keys at iphub, ipintel, and/or proxycheck.

We thank @tylerburleigh for his help on this tool.

See some related working papers [here](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3272468) and [here](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3327274). 
