# Using SNIP

When all of this is finished, you have a CORS, but only on your home network. 
You could port-forward to an Internet connection.
As an alternative, I set up a Windows Server instance in Azure called NTRIP1.
I added 2101 as an inbound port, both in Azure and in the Windows Firewall.

I installed the free version of SNIP.
- I set Casters and Clients, Caster IP to 10.0.0.4 (the private address of NTRIP1)
- I set the IP Mapping to the public address, 20.123.13.249. 
- I tested this by opening a web browser to 20.123.13.249:2101

I then sent a stream to the server as a pushed-in stream, from str2str.
There is one "gotcha", the free version of SNIP will only support a single pushed-in stream.