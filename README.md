py-arin-rws-api
===============

**Python Library for ARIN's REG-RWS REST API**

https://www.arin.net/resources/restful-interfaces.html

- Author: Benton Snyder
- Website: http://bensnyde.me
- Created: 8/30/2014
- Revised: 12/31/2014

- Revised: 5/27/2015
- Revisions by: Nick Buraglio
- Email: nick (at) buraglio.com
- WWW: https://www.forwardingplane.net/

Add env and requirements notes

ToDo: Add some more robust instructions

Requirements:
sudo pip install requests


Usage
---
```
arin = Arin("API-XXXX-YYYY-ZZZZ-XXXX")
print arin.get_net("NET-XXX-YYY-ZZZ-0-1")

# Reassign NET
netblock = NetBlockPayload("S", "", "XXX.15.219.0", "XXX.15.219.31", "27")
net = NetPayload("", "YYYY", "", "NET-XXX-15-128-0-1", "YYYY-XXX-15-219-0", "ASXXXX", netblock)
print arin.reassign_net("NET-XXX-15-128-0-1", net)
```
