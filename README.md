# ThreatPinch Lookup

## Introduction

ThreatPinch Lookup creates informational tooltips when hovering oven an item of interest on any website. It helps speed up security investigations by automatically providing relevant information upon hovering over any IPv4 address, MD5 hash, SHA2 hash, and CVE title. It’s designed to be completely customizable and work with any rest API.

![](https://cloud.githubusercontent.com/assets/6827829/19833788/3c4df320-9e1d-11e6-8c4e-1095e3cc1ac6.png)
_A sample of the type of data that can be displayed when hovering over an IPv4 address._

![](https://github.com/cloudtracer/ThreatPinchLookup/blob/master/talosblog2.gif)

_See it in action on Cisco Talos Blog._


## Current IOC Support
- IPv4
- MD5
- SHA1
- SHA2
- CVE
- FQDN (EFQDN is for Internet FQDN, IFQDN is for internal domains)
- Add your own in the options with regex!

## Current Integrations
- ThreatMiner for IPv4, FQDN, MD5, SHA1 and SHA2 lookups.
- Alienvault OTX for IPv4, MD5, SHA1 and SHA2 lookups.
- IBM X-Force Exchange for IPv4, EFQDN lookups.
- VirusTotal for MD5, SHA1, SHA2 and FQDN lookups.
- Cymon.io for IPv4 lookups.
- CIRCL (Computer Incident Response Center Luxembourg) for CVE lookups.
- PassiveTotal for FQDN Whois lookups
- MISP for MD5 and SHA2 (If you want more submit an issue in this github)
- Censys.io for IPv4 lookups
- Shodan for IPV4 lookups
- Add your own in the developers options page!

## Support

Check out the [Wiki](https://github.com/cloudtracer/ThreatPinchLookup/wiki) for documentation.

Please log an issue with any questions/comments. We'll respond as soon as possible. 

Follow [@ThreatPinch](https://twitter.com/ThreatPinch) on Twitter.

Youtube channel with [Demos](https://www.youtube.com/channel/UCuhYaI1qbb-exuhzscp3HBQ).

## Chrome Web Store

You can download the ThreatPinch Lookup extension directly from the [Chrome Web Store](https://chrome.google.com/webstore/detail/threatpinch-lookup/ljdgplocfnmnofbhpkjclbefmjoikgke)

## Where is my data stored?

There is no backend server or database for ThreatPinch Lookup. All data related to API integrations or lookup configurations resides in your Chrome session storage, this allows your configurations to work in any Chrome browser your account is linked to.  Look up history information is stored in your browsers local storage due to the Chrome session storage limits, and lookup history can be viewed or wiped in the developers options for now. This means your lookup history will not follow you from browser to browser.

Optionally, in the developers options you can configure a CouchDB server to sync your API responses with. See the [Wiki](https://github.com/cloudtracer/ThreatPinchLookup/wiki) for more details.

## Release Notes
- 1.0.37: 2017-02-22 - Added Shodan IPv4 Lookup and API group, enhancements to bulk lookup interface, added pivot API related items to Request Lookup & Lookup Type schemas.
- 1.0.35: 2017-02-14 - Updates to config pushing.
- 1.0.31: 2017-02-13 - Added options for case sensitive API requests.
- 1.0.30: 2017-02-13 - First attempt at API Groups for quick API key management. Bulk search page updates, SHA1 IOCs and lookups, edge case fixes for popover, Censys.io lookup for IPv4 addresses, added a number of observable detection regex for future use, added context menu highlight select and send to search page.
- 1.0.29: 2017-01-23 - Options interface make over, basic bulk lookup functionality, some fixes to improve observable detection and prevention in editable html elements.
- 1.0.28: 2017-01-04 - Performance improvements for pages with large quantities of observables.
- 1.0.26: 2017-01-02 - Break fix for local storage of lookup types.
- 1.0.25: 2017-01-01 - MISP integrations, disable buttons in options, moved lookup types to local storage (regex for EFQDN is too big to save in sync), enhancements to EFQDN lookups, lots of refactoring.
- 1.0.24: 2016-12-18 - Fix for delete buttons in options page.
- 1.0.23: 2016-12-14 - Fixes to CouchDB top level metadata, fix to IPv4 regex to filter out in-addr.arpa, fix to EFQDN to filter out URLs (URL IOC will come later..), added EFQDN lookups for IBM X-Force and VirusTotal
- 1.0.19: 2016-12-11 - Added FQDN support, regex updates, PassiveTotal support for FQDN/Whois, ThreatMiner FQDN, support for de-fanged IOCs
- 1.0.17: 2016-12-10 - Improved preformance, added top level IOC pivots, threat indicators and tactics to saved requests for use in CouchDB/ELK aggregations
- 1.0.10: 2016-11-02 - Initial Public Release  
