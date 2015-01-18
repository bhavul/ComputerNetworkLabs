Basic Network Commands for Unix
=========================================

1. `ifconfig`
2. `iwconfig` - gives details pertaining to wireless network interface.
3. `iwlist` - gives details that are not shown in iwconfig, such as what all channels are being used, the frequency, transmission power, etc.
4. `arp` - maps mac address to IP address.
5. `route` - displays routing table or IP table (of particular node) entries. 
6. `ping`
7. `whois` (not installed by default) - to know the owner of a domain name. It connects to a database server and retrievs the information.
8. `netstat` 
9. `traceroute` - To know the path from source to destination.
10. `nslookup` 
11. `dig`
12. `nmap` - what all sockets that are open in your network or any node on the network.
13. `ssh` - to make a connection from local computer to a remote machine to control it. Way to use it is : `ssh username@remote-machine`
14. `scp` - to copy file from local machine to remote machine. Way to use it is : `scp file_to_be_copied.txt usernameRemote@IP_remote:/home/PATH` - it'll prompt for password for the `usernameRemote` on the Remote machine, when you enter that, the file would be successfully copied to the remote machine.

### Information

- IP address is a logical address. 
- Two mac addresses - they're unique. One is for wifi card, and one is for 
- In ifconfig, you have local loopback address - say you have a client server application, instead of deploying and testing it on 
- `iwlist frequency` : Each channel is 500Mhz. These are some bands which don't require any license. They are mostly used for short range communication. NFC, Bluetooth, and this - all use ISM bands.
- NFC operates on 13.xy MHz. 
- ISM bands vary from region to rbegion. If it's 868Mhz in US, in India, it's 2.412Ghz to 2.472Ghz.
- When you're connected to network, you're connected to gateway(router connecting two different networks). Now, say you're connecting from bits to smwheer in mumbai, your packets are transferred through gateway. Your arp 	table will help here.
- We'll learn more about `route` later on.
- in `ping` the ttl = time to leave, time = the round trip time. From src to dst and dst to src back, how much time it takes.
- in `netstat` you're able to know the unix protocols that are being used and the tcp and udp protocols that are being used.
- If you do `traceroute google.com` you'll see a row of IP addresses of google.com servers. Some of its routers might be secure/private and not reveal it's IP in which case it'll display `* * *`
- If you do `nslookup google.com` you'll see different addresses that host google.com. One of which will be same as one of the entries in traceroute wala command. This is the IP you're going to when you wrote google.com
- Each protocol will be having its own port number. Check command `nmap localhost`.


### Questions/Doubts/Unclear things

- Adopt network?
- in `iwconfig` command - What is `RTS thr`
- how to notify on which channel currently we are? (something related to iwlist)
- how does arp help in gateway and transmission?
- What do you mean by open/closed ports?

### Help make this better and Spread the knowledge

This is in no way exhaustive information source, nor might it be 100% correct. You can correct and open a PR, and add yourself to the authors list too. :) 


### Author and Date

Bhavul Gauri

Saturday, January 17 2015
