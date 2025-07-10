# ICAI2025-ForensicLabs
ICAI 2025 - Digital Forensics and IR


Volatility

vol.py -f cridex.vmem imageinfo
vol.py -f cridex.vmem --profile=WinXPSP2x86 pslist
vol.py -f cridex.vmem --profile=WinXPSP2x86 pstree
vol.py -f cridex.vmem --profile=WinXPSP2x86 pstree

vol.py -f cridex.vmem --profile=WinXPSP2x86 connscan
vol.py -f cridex.vmem --profile=WinXPSP2x86 sockets

vol.py -f cridex.vmem --profile=WinXPSP2x86 cmdline

vol.py -f cridex.vmem --profile=WinXPSP2x86 procdump -p 1640 --dump-dir .
vol.py -f cridex.vmem --profile=WinXPSP2x86 meedump -p 1640 --dump-dir .
strings 1640.dmp | grep -Fi "41.168.5.140" -C 5
