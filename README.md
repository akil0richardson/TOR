# TOR
Standalone TOR set to UseBridges on Windows 10 (runs quietly in the background)

# This file details the steps taken for this to work as intended
# Tor Expert is not bundled with any PluggableTransports (i.e. obfs4proxy)
# To use Pluggable Transports, one must download a version of TOR that already has them (i.e. Tor Browser Bundle)

# This version of tor.exe was taken from my ZeroNet data directory, which was saved on my desktop (why it runs in the background):

# C:\Users\SysAdmin\Desktop\ZeroNet-win-dist-win64\ZeroNet-win-dist-win64\core\tools\tor

1. Copy the PluggableTransports folder and all of the dynamic link libraries to a new folder (any file with the ".dll" extension).

# C:\Users\SysAdmin\Desktop\TOR

2. Fetch trusted bridges from TorProject.

# bridges.torproject.org

3. Edit torrc and copy/paste bridges into the file (replace <bridge> with lines from Step 2).

"""

# Bridges
ClientTransportPlugin obfs4 exec PluggableTransports/obfs4proxy
<bridge>
<bridge>
<bridge>
UseBridges 1

"""
  
4. Check "Task Manager" for tor underneath "Processes" tab.
