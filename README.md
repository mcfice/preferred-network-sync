# preferred-network-sync

A quick-and-dirty bash script I made to automate connecting to my preferred Wi-Fi network that can also be made to make sure KDE Connect restarts (it needs to when it has problems).

I have it set to a keyboard shortcut so I can easily connect to my mobile hotspot when I activate it.

This is very incredibly specific to my usecase ¯\_(ツ)_/¯

### Workings:
* Checks (using `nmcli`) if connected to the set network and only if not attempts to connect
* Displays results as a graphical window (using `zenity`)

### How to use:

Pass your desired network name as the first argument:
```bash
./prefered-network-sync "network_example"
```

You can pass **-kde** as an argument to make it also restart KDE before doing anything:
```bash
./prefered-network-sync "network_example" --kde
```

Pass **-v** as an argument to open a terminal and display debug information:
```bash
./prefered-network-sync "network_example" -v
```

### Requirements:
Since this is a personalized setup, it assumes you have the following installed on your Linux system:
* **NetworkManager** (`nmcli`)
* **Zenity** (for graphical popup notifications)
* KDE Connect (Optional: `kdeconnect-cli` & `kdeconnectd`)


