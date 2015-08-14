dnstwist
========
See what sort of trouble users can get in trying to type your domain name. Look for registered domains similar to your own, only distinguished by [typos](https://en.wikipedia.org/wiki/Typosquatting) (or cosmic ray). Useful as an additional source of targeted threat intelligence. Can detect fraud, phishing attacks and corporate espionage.

Credit
------
Original code created and distribuited by Marcin Ulikowski (https://github.com/elceef/dnstwist). The changes I made were simply to add a date/time stamp to the beginning of each line.

Required modules
----------------
If you want *dnstwist* to develop full power, please make sure the following Python modules are present on your system. If missing, *dnstwist* will still work, but without some cool features.

* [Python GeoIP](https://pypi.python.org/pypi/GeoIP/)
* [A DNS toolkit for Python](http://www.dnspython.org/)

Dependency installation
----------------
*GeoIP*
```
brew install geoip
sudo pip install geoip
curl -O http://geolite.maxmind.com/download/geoip/database/GeoLiteCountry/GeoIP.dat.gz
gunzip GeoIP.dat.gz
cp GeoIP.dat /usr/local/var/GeoIP/
```
*DNSPython*
```
curl -O http://www.dnspython.org/kits/1.12.0/dnspython-1.12.0.tar.gz
tar zxf dnspython-1.12.0.tar.gz
cd dnspython-1.12.0
python ./setup.py build
python ./setup.py install
```
Articles and blog posts on using dnstwist
-----------------------------------------
* [Security List Network: DNSTWIST - Generate and resolve domain variation to detect typo squatting, phising and corporate espionage](http://seclist.us/dnstwist-generate-and-resolve-domain-variations-to-detect-typo-squatting-phishing-and-corporate-espionage.html)
* [Heise-Online: Dnstwist variiert und testet Domainnamen](http://www.heise.de/newsticker/meldung/Dnstwist-variiert-und-testet-Domainnamen-2690418.html)
* [Newday International: dnstwist varies and tests domain name](https://www.newday.mk/dnstwist-varies-and-tests-domain-name/)
* [ISC StormCast for Tuesday, June 16th 2015](https://isc.sans.edu/podcastdetail.html?id=4529)

Special thanks
--------------
* Patricia Lipp
* Steve Steiner
* Christopher Schmidt
* James Lane
* Piotr Chmyłkowski
* Marcin Ulikowski (original code - https://github.com/elceef/dnstwist)

Contact
-------
To send questions or comments, send an e-mail at [peasead@gmail.com](mailto:peasead@gmail.com)

Example report
--------------
```
$ ./dnstwist.py github.com
dnstwist (20150630) by variable
Processing 132 domains !!!!!!!.!..!!!..!!.!..!...!!!.!.!!!!!!!.!!!.!!!!!!.!!!!..!!!!.!!!!.!!.!!!.!!.!.!!!!!...!....!!.....!..!.!...!!....!...!....!..!!.... 73 hit(s)

6-30-2015	Bitsquatting    fithub.com      4.35.164.141/United States MX:aspmx3.googlemail.com
6-30-2015	Bitsquatting    eithub.com      174.136.12.111/United States MX:eithub.com
6-30-2015	Bitsquatting    cithub.com      14.63.216.242/Korea, Republic of
6-30-2015	Bitsquatting    oithub.com      54.68.76.21/United States
6-30-2015	Transposition   gtihub.com      199.59.243.120/United States
6-30-2015	Transposition   gihtub.com      216.40.47.17/Canada MX:inbound.homesteadmail.com
...
```
