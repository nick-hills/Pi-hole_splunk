Pi-hole {http://pi-hole.net) is a Linux network-level advertisement and internet tracker blocking application which acts as a DNS sinkhole (And optionally a DHCP server), intended for use on a private network.
It is designed for use on embedded devices with network capability, such as the Raspberry Pi, but can be used on other machines running Linux and cloud implementations.
Pi-hole has the ability to block traditional website adverts as well as adverts in unconventional places, such as smart TVs and mobile operating system adverts


This Splunk Application consumes the output logs from Pi-hole and provides CIM extractions, and a simple dashboard to display statistics

github:

https://github.com/nick-hills/Pi-hole_splunk

Installation:

1.) Install the app from SplunkBase, or upload the package file

2.) Create an input for the log file. The following is an example you could add to inputs.conf if you are using the default paths.
Be sure to set the sourcetype to pihole:log

[monitor:///var/log/]
whitelist = pihole\.lo.+
disabled = false
sourcetype = pihole:log

3.) Marvel at the dashboards and how many requests are being blocked by Pi-hole

4.) Optionally enabled Datamodel Acceleration for the Network Resolution (DNS) datamodel, and start pivoting.
