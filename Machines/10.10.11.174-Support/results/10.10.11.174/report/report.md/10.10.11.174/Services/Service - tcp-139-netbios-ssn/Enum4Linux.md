```bash
enum4linux -a -M -l -d 10.10.11.174 2>&1
```

[/home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/tcp139/enum4linux.txt](file:///home/parallels/HacktheBox/Machines/10.10.11.174-Support/results/10.10.11.174/scans/tcp139/enum4linux.txt):

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Wed Nov 23 09:21:22 2022

[34m =========================================( [0m[32mTarget Information[0m[34m )=========================================

[0mTarget ........... 10.10.11.174
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none


[34m ============================( [0m[32mEnumerating Workgroup/Domain on 10.10.11.174[0m[34m )============================

[0m[33m
[E] [0m[31mCan't find workgroup/domain

[0m

[34m ================================( [0m[32mNbtstat Information for 10.10.11.174[0m[34m )================================

[0mLooking up status of 10.10.11.174
No reply from 10.10.11.174

[34m ===================================( [0m[32mSession Check on 10.10.11.174[0m[34m )===================================

[0m[33m
[+] [0m[32mServer 10.10.11.174 allows sessions using username '', password ''

[0m
[34m ===========================( [0m[32mGetting information via LDAP for 10.10.11.174[0m[34m )===========================

[0m[33m
[+] [0m[32m10.10.11.174 appears to be a child DC

[0m
[34m ================================( [0m[32mGetting domain SID for 10.10.11.174[0m[34m )================================

[0mDomain Name: SUPPORT
Domain Sid: S-1-5-21-1677581083-3380853377-188903654
[33m
[+] [0m[32mHost is part of a domain (not a workgroup)

[0m
[34m ===================================( [0m[32mOS information on 10.10.11.174[0m[34m )===================================

[0m[33m
[E] [0m[31mCan't get OS info with smbclient

[0m[33m
[+] [0m[32mGot OS info for 10.10.11.174 from srvinfo:
[0mdo_cmd: Could not initialise srvsvc. Error was NT_STATUS_ACCESS_DENIED


[34m =======================================( [0m[32mUsers on 10.10.11.174[0m[34m )=======================================

[0m[33m
[E] [0m[31mCouldn't find users using querydispinfo: NT_STATUS_ACCESS_DENIED

[0m
[33m
[E] [0m[31mCouldn't find users using enumdomusers: NT_STATUS_ACCESS_DENIED

[0m
[34m ================================( [0m[32mMachine Enumeration on 10.10.11.174[0m[34m )================================

[0m[33m
[E] [0m[31mNot implemented in this version of enum4linux.

[0m
[34m =================================( [0m[32mShare Enumeration on 10.10.11.174[0m[34m )=================================

[0mdo_connect: Connection to 10.10.11.174 failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)

	Sharename       Type      Comment
	---------       ----      -------
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available
[33m
[+] [0m[32mAttempting to map shares on 10.10.11.174

[0m
[34m ============================( [0m[32mPassword Policy Information for 10.10.11.174[0m[34m )============================

[0m[33m
[E] [0m[31mUnexpected error from polenum:

[0m

[+] Attaching to 10.10.11.174 using a NULL share

[+] Trying protocol 139/SMB...

	[!] Protocol failed: Cannot request session (Called Name:10.10.11.174)

[+] Trying protocol 445/SMB...

	[!] Protocol failed: SAMR SessionError: code: 0xc0000022 - STATUS_ACCESS_DENIED - {Access Denied} A process has requested access to an object but has not been granted those access rights.


[33m
[E] [0m[31mFailed to get password policy with rpcclient

[0m

[34m =======================================( [0m[32mGroups on 10.10.11.174[0m[34m )=======================================

[0m[33m
[+] [0m[32mGetting builtin groups:

[0m[33m
[+] [0m[32m Getting builtin group memberships:

[0m[33m
[+] [0m[32m Getting local groups:

[0m[33m
[+] [0m[32m Getting local group memberships:

[0m[33m
[+] [0m[32m Getting domain groups:

[0m[33m
[+] [0m[32m Getting domain group memberships:

[0m
[34m ==================( [0m[32mUsers on 10.10.11.174 via RID cycling (RIDS: 500-550,1000-1050)[0m[34m )==================

[0m[33m
[E] [0m[31mCouldn't get SID: NT_STATUS_ACCESS_DENIED.  RID cycling not possible.

[0m
[34m ===============================( [0m[32mGetting printer info for 10.10.11.174[0m[34m )===============================

[0mdo_cmd: Could not initialise spoolss. Error was NT_STATUS_ACCESS_DENIED


enum4linux complete on Wed Nov 23 09:21:47 2022



```
