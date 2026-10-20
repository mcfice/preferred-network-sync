# preferred-network-sync

A quick-and-dirty bash script I made to automate connecting to my preferred Wi-Fi network that can also be made to make sure KDE Connect restarts (it needs to when it has problems).

I have it set to a keybord shortcut so i can easily connect to my mobile hotspot when i activate it.

Workings:

    Checks (using nmcli) if connected to the set network and only if not attempts to connect
    Displays results as a graphical window (using zenity)

How to use:

    Pass your desired network name as the first argument

```./prefered-network-sync *network_example*```

    You can pass **-kde** as an argument to make it also restart kde before doing anything

```./prefered-network-sync *network_example*''' **-kde**```

    Pass **-v** as an argument to open terminal and display debug information

```./prefered-network-sync *network_example*''' **-v**```

Requirements:

    Since this is a personalized setup, it assumes you have the following installed on your Linux system:
    -**NetworkManager** (`nmcli`)
    -**Zenity** (for graphical popup notifications)
    -optional (KDE Connect (`kdeconnect-cli` & `kdeconnectd`))

