# Censys-Query

Censys is a search engine that scans the Internet searching for devices and return reports on how resources (i.e. Devices, websites, and certificates) are configured and deployed. Censys daily scans of the IPv4 address space searching for any devices and collecting related information.

I needed a quick way to filter through all the IPs that are tagged to an particular organization, without screaming to loud with tools like amass.

The following script does just that, crawls the search links and outputs the ips to a text file, it uses httpie to conduct the web request and sed for parsing.

The following list of IP addresses have some type of signature to google.com, whether that’s through web response via body content, ftp or ssh banner, and more.

Why is this tool important? - I needed to solve an issue in a short amount of time, had I self-query censys website for the domain I was interested in, it would of took quite a while to compile that list. It would have been simpler to write out a script to parse the information out than to manually do it.

Direction and Future Direction? - As mentioned, there are already tools out there doing a much more detailed job. For this tool, it allows you to quickly and under the radar collect subdomains without introducing new libraries and whatnot. Every tool has a purpose, and this was made to simplify a task as quickly as possible.

## Requirements
httpie

## Running
./subdomains.sh google.com
