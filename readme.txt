I. PROXYnotSHELL RCE exploit
This is Post-Auth RCE for ProxyNotShell, a valid cardentials are needed for command execution.
Affected versions
Exchange 2013,16,19 till 08.11.2022 patch
This exploit bypasses Microsoft Hotfix from Octorber 2022

II.

Usage: python3 poc.py -H https://192.168.1.3 -u user -p "12345678" -c cmd_file
Where cmd_file is a local file with a command to execute. cmd_file contents will be passed to `powershell -e "base64_encode(content(cmd_file))"`
It is HIGHLY recommended to use nslookup for testing. i.e getting subdomain from http://dnslog.cn/ and using nslookup domain.xxx
to verify if exchange is affected or not.

III.
Requirements:
Python3
pip -r requirements.txt