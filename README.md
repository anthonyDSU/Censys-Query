# Censys-Query

Censys is a search engine that scans the Internet searching for devices and return reports on how resources (i.e. Devices, websites, and certificates) are configured and deployed. Censys daily scans of the IPv4 address space searching for any devices and collecting related information.

I needed a quick way to filter through all the IPs that are tagged to an particular organization, without screaming to loud with tools like amass.

The following script does just that, crawls the search links and outputs the ips to a text file, it uses httpie to conduct the web request and sed for parsing.

The following list of IP addresses have some type of signature to google.com, whether that’s through web response via body content, ftp or ssh banner, and more.

# ./subdomains.sh google.com
