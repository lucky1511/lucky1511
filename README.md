import platform
import os
data = str((platform.uname())).replace(')','').split('(')[1].split(",")
sysinfo={}
for info in data:
    sysinfo[info.split('=')[0].strip()] = info.split('=')[1].replace("'",'').strip()

print(sysinfo)
