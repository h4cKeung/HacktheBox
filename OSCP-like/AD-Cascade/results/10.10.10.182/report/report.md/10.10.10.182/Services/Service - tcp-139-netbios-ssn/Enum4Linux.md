```bash
enum4linux -a -M -l -d 10.10.10.182 2>&1
```

[/home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp139/enum4linux.txt](file:///home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp139/enum4linux.txt):

```
Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Fri Nov 18 15:56:55 2022

[34m =========================================( [0m[32mTarget Information[0m[34m )=========================================

[0mTarget ........... 10.10.10.182
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none


[34m ============================( [0m[32mEnumerating Workgroup/Domain on 10.10.10.182[0m[34m )============================

[0m[33m
[E] [0m[31mCan't find workgroup/domain

[0m

[34m ================================( [0m[32mNbtstat Information for 10.10.10.182[0m[34m )================================

[0mLooking up status of 10.10.10.182
No reply from 10.10.10.182

[34m ===================================( [0m[32mSession Check on 10.10.10.182[0m[34m )===================================

[0m[33m
[+] [0m[32mServer 10.10.10.182 allows sessions using username '', password ''

[0m
[34m ===========================( [0m[32mGetting information via LDAP for 10.10.10.182[0m[34m )===========================

[0m[33m
[+] [0m[32m10.10.10.182 appears to be a child DC

[0m
[34m ================================( [0m[32mGetting domain SID for 10.10.10.182[0m[34m )================================

[0mDomain Name: CASCADE
Domain Sid: S-1-5-21-3332504370-1206983947-1165150453
[33m
[+] [0m[32mHost is part of a domain (not a workgroup)

[0m
[34m ===================================( [0m[32mOS information on 10.10.10.182[0m[34m )===================================

[0m[33m
[E] [0m[31mCan't get OS info with smbclient

[0m[33m
[+] [0m[32mGot OS info for 10.10.10.182 from srvinfo:
[0mdo_cmd: Could not initialise srvsvc. Error was NT_STATUS_ACCESS_DENIED


[34m =======================================( [0m[32mUsers on 10.10.10.182[0m[34m )=======================================

[0mindex: 0xee0 RID: 0x464 acb: 0x00000214 Account: a.turnbull	Name: Adrian Turnbull	Desc: (null)
index: 0xebc RID: 0x452 acb: 0x00000210 Account: arksvc	Name: ArkSvc	Desc: (null)
index: 0xee4 RID: 0x468 acb: 0x00000211 Account: b.hanson	Name: Ben Hanson	Desc: (null)
index: 0xee7 RID: 0x46a acb: 0x00000210 Account: BackupSvc	Name: BackupSvc	Desc: (null)
index: 0xdeb RID: 0x1f5 acb: 0x00000215 Account: CascGuest	Name: (null)	Desc: Built-in account for guest access to the computer/domain
index: 0xee5 RID: 0x469 acb: 0x00000210 Account: d.burman	Name: David Burman	Desc: (null)
index: 0xee3 RID: 0x467 acb: 0x00000211 Account: e.crowe	Name: Edward Crowe	Desc: (null)
index: 0xeec RID: 0x46f acb: 0x00000211 Account: i.croft	Name: Ian Croft	Desc: (null)
index: 0xeeb RID: 0x46e acb: 0x00000210 Account: j.allen	Name: Joseph Allen	Desc: (null)
index: 0xede RID: 0x462 acb: 0x00000210 Account: j.goodhand	Name: John Goodhand	Desc: (null)
index: 0xed7 RID: 0x45c acb: 0x00000210 Account: j.wakefield	Name: James Wakefield	Desc: (null)
index: 0xeca RID: 0x455 acb: 0x00000210 Account: r.thompson	Name: Ryan Thompson	Desc: (null)
index: 0xedd RID: 0x461 acb: 0x00000210 Account: s.hickson	Name: Stephanie Hickson	Desc: (null)
index: 0xebd RID: 0x453 acb: 0x00000210 Account: s.smith	Name: Steve Smith	Desc: (null)
index: 0xed2 RID: 0x457 acb: 0x00000210 Account: util	Name: Util	Desc: (null)

user:[CascGuest] rid:[0x1f5]
user:[arksvc] rid:[0x452]
user:[s.smith] rid:[0x453]
user:[r.thompson] rid:[0x455]
user:[util] rid:[0x457]
user:[j.wakefield] rid:[0x45c]
user:[s.hickson] rid:[0x461]
user:[j.goodhand] rid:[0x462]
user:[a.turnbull] rid:[0x464]
user:[e.crowe] rid:[0x467]
user:[b.hanson] rid:[0x468]
user:[d.burman] rid:[0x469]
user:[BackupSvc] rid:[0x46a]
user:[j.allen] rid:[0x46e]
user:[i.croft] rid:[0x46f]
	User Name   :	r.thompson
	Full Name   :	Ryan Thompson
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Wed, 29 Jan 2020 12:11:53 AEDT
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Fri, 10 Jan 2020 06:31:26 AEDT
	Password can change Time :	Fri, 10 Jan 2020 06:31:26 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x455
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000002
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	j.wakefield
	Full Name   :	James Wakefield
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapDataDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Fri, 10 Jan 2020 07:34:44 AEDT
	Password can change Time :	Fri, 10 Jan 2020 07:34:44 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x45c
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	e.crowe
	Full Name   :	Edward Crowe
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapDataDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Mon, 13 Jan 2020 14:45:02 AEDT
	Password can change Time :	Mon, 13 Jan 2020 14:45:02 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x467
	group_rid:	0x201
	acb_info :	0x00000211
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : True
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	util
	Full Name   :	Util
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Wed, 29 Jan 2020 05:09:47 AEDT
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Mon, 13 Jan 2020 13:07:11 AEDT
	Password can change Time :	Mon, 13 Jan 2020 13:07:11 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x457
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000001
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	d.burman
	Full Name   :	David Burman
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapDataDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Tue, 14 Jan 2020 03:36:13 AEDT
	Password can change Time :	Tue, 14 Jan 2020 03:36:13 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x469
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	j.goodhand
	Full Name   :	John Goodhand
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapDataDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Mon, 13 Jan 2020 12:40:26 AEDT
	Password can change Time :	Mon, 13 Jan 2020 12:40:26 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x462
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	s.smith
	Full Name   :	Steve Smith
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapAuditDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Wed, 29 Jan 2020 10:26:39 AEDT
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Wed, 29 Jan 2020 06:58:05 AEDT
	Password can change Time :	Wed, 29 Jan 2020 06:58:05 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x453
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000010
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	s.hickson
	Full Name   :	Stephanie Hickson
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapDataDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Mon, 13 Jan 2020 12:24:28 AEDT
	Password can change Time :	Mon, 13 Jan 2020 12:24:28 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x461
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	BackupSvc
	Full Name   :	BackupSvc
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Tue, 14 Jan 2020 03:37:03 AEDT
	Password can change Time :	Tue, 14 Jan 2020 03:37:03 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x46a
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	b.hanson
	Full Name   :	Ben Hanson
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Tue, 14 Jan 2020 03:35:39 AEDT
	Password can change Time :	Tue, 14 Jan 2020 03:35:39 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x468
	group_rid:	0x201
	acb_info :	0x00000211
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : True
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	i.croft
	Full Name   :	Ian Croft
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapDataDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Thu, 16 Jan 2020 08:46:22 AEDT
	Password can change Time :	Thu, 16 Jan 2020 08:46:22 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x46f
	group_rid:	0x201
	acb_info :	0x00000211
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : True
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	CascGuest
	Full Name   :
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :	Built-in account for guest access to the computer/domain
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Thu, 01 Jan 1970 10:00:00 AEST
	Password can change Time :	Thu, 01 Jan 1970 10:00:00 AEST
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x1f5
	group_rid:	0x202
	acb_info :	0x00000215
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : True
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	j.allen
	Full Name   :	Joseph Allen
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:	MapDataDrive.vbs
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Tue, 14 Jan 2020 04:24:00 AEDT
	Password can change Time :	Tue, 14 Jan 2020 04:24:00 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x46e
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	arksvc
	Full Name   :	ArkSvc
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 30 Jan 2020 08:05:41 AEDT
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Fri, 10 Jan 2020 03:18:20 AEDT
	Password can change Time :	Fri, 10 Jan 2020 03:18:20 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x452
	group_rid:	0x201
	acb_info :	0x00000210
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x0000000d
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

	User Name   :	a.turnbull
	Full Name   :	Adrian Turnbull
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Mon, 13 Jan 2020 12:43:13 AEDT
	Password can change Time :	Mon, 13 Jan 2020 12:43:13 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x464
	group_rid:	0x201
	acb_info :	0x00000214
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False


[34m ================================( [0m[32mMachine Enumeration on 10.10.10.182[0m[34m )================================

[0m[33m
[E] [0m[31mNot implemented in this version of enum4linux.

[0m
[34m =================================( [0m[32mShare Enumeration on 10.10.10.182[0m[34m )=================================

[0mdo_connect: Connection to 10.10.10.182 failed (Error NT_STATUS_RESOURCE_NAME_NOT_FOUND)

	Sharename       Type      Comment
	---------       ----      -------
Reconnecting with SMB1 for workgroup listing.
Unable to connect with SMB1 -- no workgroup available
[33m
[+] [0m[32mAttempting to map shares on 10.10.10.182

[0m
[34m ============================( [0m[32mPassword Policy Information for 10.10.10.182[0m[34m )============================

[0m

[+] Attaching to 10.10.10.182 using a NULL share

[+] Trying protocol 139/SMB...

	[!] Protocol failed: Cannot request session (Called Name:10.10.10.182)

[+] Trying protocol 445/SMB...

[+] Found domain(s):

	[+] CASCADE
	[+] Builtin

[+] Password Info for Domain: CASCADE

	[+] Minimum password length: 5
	[+] Password history length: None
	[+] Maximum password age: Not Set
	[+] Password Complexity Flags: 000000

		[+] Domain Refuse Password Change: 0
		[+] Domain Password Store Cleartext: 0
		[+] Domain Password Lockout Admins: 0
		[+] Domain Password No Clear Change: 0
		[+] Domain Password No Anon Change: 0
		[+] Domain Password Complex: 0

	[+] Minimum password age: None
	[+] Reset Account Lockout Counter: 30 minutes
	[+] Locked Account Duration: 30 minutes
	[+] Account Lockout Threshold: None
	[+] Forced Log off Time: Not Set


[33m
[+] [0m[32mRetieved partial password policy with rpcclient:


[0mPassword Complexity: Disabled
Minimum Password Length: 5


[34m =======================================( [0m[32mGroups on 10.10.10.182[0m[34m )=======================================

[0m[33m
[+] [0m[32mGetting builtin groups:

[0mgroup:[Pre-Windows 2000 Compatible Access] rid:[0x22a]
group:[Incoming Forest Trust Builders] rid:[0x22d]
group:[Windows Authorization Access Group] rid:[0x230]
group:[Terminal Server License Servers] rid:[0x231]
group:[Users] rid:[0x221]
group:[Guests] rid:[0x222]
group:[Remote Desktop Users] rid:[0x22b]
group:[Network Configuration Operators] rid:[0x22c]
group:[Performance Monitor Users] rid:[0x22e]
group:[Performance Log Users] rid:[0x22f]
group:[Distributed COM Users] rid:[0x232]
group:[IIS_IUSRS] rid:[0x238]
group:[Cryptographic Operators] rid:[0x239]
group:[Event Log Readers] rid:[0x23d]
group:[Certificate Service DCOM Access] rid:[0x23e]
[33m
[+] [0m[32m Getting builtin group memberships:

[0m[35mGroup: [0mWindows Authorization Access Group' (RID: 560) has member: NT AUTHORITY\ENTERPRISE DOMAIN CONTROLLERS
[35mGroup: [0mPre-Windows 2000 Compatible Access' (RID: 554) has member: NT AUTHORITY\Authenticated Users
[35mGroup: [0mUsers' (RID: 545) has member: NT AUTHORITY\INTERACTIVE
[35mGroup: [0mUsers' (RID: 545) has member: NT AUTHORITY\Authenticated Users
[35mGroup: [0mUsers' (RID: 545) has member: CASCADE\Domain Users
[35mGroup: [0mGuests' (RID: 546) has member: CASCADE\CascGuest
[35mGroup: [0mGuests' (RID: 546) has member: CASCADE\Domain Guests
[33m
[+] [0m[32mGetting detailed info for group Network Configuration Operators (RID: 556)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Distributed COM Users (RID: 562)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Windows Authorization Access Group (RID: 560)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Performance Monitor Users (RID: 558)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Pre-Windows 2000 Compatible Access (RID: 554)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Remote Desktop Users (RID: 555)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Incoming Forest Trust Builders (RID: 557)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Certificate Service DCOM Access (RID: 574)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Users (RID: 545)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Cryptographic Operators (RID: 569)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group IIS_IUSRS (RID: 568)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Guests (RID: 546)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Performance Log Users (RID: 559)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Terminal Server License Servers (RID: 561)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Event Log Readers (RID: 573)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32m Getting local groups:

[0mgroup:[Cert Publishers] rid:[0x205]
group:[RAS and IAS Servers] rid:[0x229]
group:[Allowed RODC Password Replication Group] rid:[0x23b]
group:[Denied RODC Password Replication Group] rid:[0x23c]
group:[DnsAdmins] rid:[0x44e]
group:[IT] rid:[0x459]
group:[Production] rid:[0x45a]
group:[HR] rid:[0x45b]
group:[AD Recycle Bin] rid:[0x45f]
group:[Backup] rid:[0x460]
group:[Temps] rid:[0x463]
group:[WinRMRemoteWMIUsers__] rid:[0x465]
group:[Remote Management Users] rid:[0x466]
group:[Factory] rid:[0x46c]
group:[Finance] rid:[0x46d]
group:[Audit Share] rid:[0x471]
group:[Data Share] rid:[0x472]
[33m
[+] [0m[32m Getting local group memberships:

[0m[35mGroup: [0mHR' (RID: 1115) has member: CASCADE\s.hickson
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\krbtgt
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\Domain Controllers
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\Schema Admins
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\Enterprise Admins
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\Cert Publishers
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\Domain Admins
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\Group Policy Creator Owners
[35mGroup: [0mDenied RODC Password Replication Group' (RID: 572) has member: CASCADE\Read-only Domain Controllers
[35mGroup: [0mAudit Share' (RID: 1137) has member: CASCADE\s.smith
[35mGroup: [0mData Share' (RID: 1138) has member: CASCADE\Domain Users
[35mGroup: [0mAD Recycle Bin' (RID: 1119) has member: CASCADE\arksvc
[35mGroup: [0mIT' (RID: 1113) has member: CASCADE\arksvc
[35mGroup: [0mIT' (RID: 1113) has member: CASCADE\s.smith
[35mGroup: [0mIT' (RID: 1113) has member: CASCADE\r.thompson
[35mGroup: [0mRemote Management Users' (RID: 1126) has member: CASCADE\arksvc
[35mGroup: [0mRemote Management Users' (RID: 1126) has member: CASCADE\s.smith
[33m
[+] [0m[32mGetting detailed info for group RAS and IAS Servers (RID: 553)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group HR (RID: 1115)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Temps (RID: 1123)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Denied RODC Password Replication Group (RID: 572)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group DnsAdmins (RID: 1102)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Audit Share (RID: 1137)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group WinRMRemoteWMIUsers__ (RID: 1125)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Production (RID: 1114)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Finance (RID: 1133)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Cert Publishers (RID: 517)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Factory (RID: 1132)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Backup (RID: 1120)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Data Share (RID: 1138)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group AD Recycle Bin (RID: 1119)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group IT (RID: 1113)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Allowed RODC Password Replication Group (RID: 571)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32mGetting detailed info for group Remote Management Users (RID: 1126)

[0m[33m
[E] [0m[31mNo info found


[0m[33m
[+] [0m[32m Getting domain groups:

[0mgroup:[Enterprise Read-only Domain Controllers] rid:[0x1f2]
group:[Domain Users] rid:[0x201]
group:[Domain Guests] rid:[0x202]
group:[Domain Computers] rid:[0x203]
group:[Group Policy Creator Owners] rid:[0x208]
group:[DnsUpdateProxy] rid:[0x44f]
[33m
[+] [0m[32m Getting domain group memberships:

[0m[35mGroup: [0m'Domain Guests' (RID: 514) has member: CASCADE\CascGuest
[35mGroup: [0m'Group Policy Creator Owners' (RID: 520) has member: CASCADE\administrator
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\administrator
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\krbtgt
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\arksvc
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\s.smith
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\r.thompson
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\util
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\j.wakefield
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\s.hickson
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\j.goodhand
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\a.turnbull
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\e.crowe
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\b.hanson
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\d.burman
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\BackupSvc
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\j.allen
[35mGroup: [0m'Domain Users' (RID: 513) has member: CASCADE\i.croft
[33m
[+] [0m[32mGetting detailed info for group Domain Guests (RID: 514)

[0m	Group Name:	Domain Guests
	Description:	All domain guests
	Group Attribute:7
	Num Members:1

[33m
[+] [0m[32mGetting detailed info for group DnsUpdateProxy (RID: 1103)

[0m	Group Name:	DnsUpdateProxy
	Description:	DNS clients who are permitted to perform dynamic updates on behalf of some other clients (such as DHCP servers).
	Group Attribute:7
	Num Members:0

[33m
[+] [0m[32mGetting detailed info for group Group Policy Creator Owners (RID: 520)

[0m	Group Name:	Group Policy Creator Owners
	Description:	Members in this group can modify group policy for the domain
	Group Attribute:7
	Num Members:1

[33m
[+] [0m[32mGetting detailed info for group Domain Users (RID: 513)

[0m	Group Name:	Domain Users
	Description:	All domain users
	Group Attribute:7
	Num Members:16

[33m
[+] [0m[32mGetting detailed info for group Domain Computers (RID: 515)

[0m	Group Name:	Domain Computers
	Description:	All workstations and servers joined to the domain
	Group Attribute:7
	Num Members:0

[33m
[+] [0m[32mGetting detailed info for group Enterprise Read-only Domain Controllers (RID: 498)

[0m	Group Name:	Enterprise Read-only Domain Controllers
	Description:	Members of this group are Read-Only Domain Controllers in the enterprise
	Group Attribute:7
	Num Members:0


[34m ==================( [0m[32mUsers on 10.10.10.182 via RID cycling (RIDS: 500-550,1000-1050)[0m[34m )==================

[0m[33m
[I] [0m[36mFound new SID:
[0mS-1-5-21-3332504370-1206983947-1165150453
[33m
[I] [0m[36mFound new SID:
[0mS-1-5-21-2189247330-517467924-712900258
[33m
[+] [0m[32mEnumerating users using SID S-1-5-21-3332504370-1206983947-1165150453 and logon username '', password ''

[0mS-1-5-21-3332504370-1206983947-1165150453-500 CASCADE\administrator (Local User)
Use of uninitialized value $user_info in pattern match (m//) at ./enum4linux.pl line 1030.

S-1-5-21-3332504370-1206983947-1165150453-501 CASCADE\CascGuest (Local User)
	User Name   :	CascGuest
	Full Name   :
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :	Built-in account for guest access to the computer/domain
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Thu, 01 Jan 1970 10:00:00 AEST
	Password can change Time :	Thu, 01 Jan 1970 10:00:00 AEST
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x1f5
	group_rid:	0x202
	acb_info :	0x00000215
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : True
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

S-1-5-21-3332504370-1206983947-1165150453-502 CASCADE\krbtgt (Local User)
Use of uninitialized value $user_info in pattern match (m//) at ./enum4linux.pl line 1030.

S-1-5-21-3332504370-1206983947-1165150453-512 CASCADE\Domain Admins (Domain Group)
[33m
[E] [0m[31mNo info found


[0mS-1-5-21-3332504370-1206983947-1165150453-513 CASCADE\Domain Users (Domain Group)
	Group Name:	Domain Users
	Description:	All domain users
	Group Attribute:7
	Num Members:16

S-1-5-21-3332504370-1206983947-1165150453-514 CASCADE\Domain Guests (Domain Group)
	Group Name:	Domain Guests
	Description:	All domain guests
	Group Attribute:7
	Num Members:1

S-1-5-21-3332504370-1206983947-1165150453-515 CASCADE\Domain Computers (Domain Group)
	Group Name:	Domain Computers
	Description:	All workstations and servers joined to the domain
	Group Attribute:7
	Num Members:0

S-1-5-21-3332504370-1206983947-1165150453-516 CASCADE\Domain Controllers (Domain Group)
[33m
[E] [0m[31mNo info found


[0mS-1-5-21-3332504370-1206983947-1165150453-517 CASCADE\Cert Publishers (Local Group)
[33m
[E] [0m[31mNo info found


[0mS-1-5-21-3332504370-1206983947-1165150453-518 CASCADE\Schema Admins (Domain Group)
[33m
[E] [0m[31mNo info found


[0mS-1-5-21-3332504370-1206983947-1165150453-519 CASCADE\Enterprise Admins (Domain Group)
[33m
[E] [0m[31mNo info found


[0mS-1-5-21-3332504370-1206983947-1165150453-520 CASCADE\Group Policy Creator Owners (Domain Group)
	Group Name:	Group Policy Creator Owners
	Description:	Members in this group can modify group policy for the domain
	Group Attribute:7
	Num Members:1

S-1-5-21-3332504370-1206983947-1165150453-521 CASCADE\Read-only Domain Controllers (Domain Group)
[33m
[E] [0m[31mNo info found


[0mS-1-5-21-3332504370-1206983947-1165150453-1001 CASCADE\CASC-DC1$ (Local User)
	User Name   :	CASC-DC1$
	Full Name   :
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Fri, 18 Nov 2022 15:54:51 AEDT
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Fri, 18 Nov 2022 15:54:13 AEDT
	Password can change Time :	Fri, 18 Nov 2022 15:54:13 AEDT
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x3e9
	group_rid:	0x204
	acb_info :	0x00002100
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00001702
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : False
	Password does not expire : False
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : True
	Trusted for delegation   : True

[33m
[+] [0m[32mEnumerating users using SID S-1-5-21-2189247330-517467924-712900258 and logon username '', password ''

[0mS-1-5-21-2189247330-517467924-712900258-500 CASC-DC1\Administrator (Local User)
Use of uninitialized value $user_info in pattern match (m//) at ./enum4linux.pl line 1030.

S-1-5-21-2189247330-517467924-712900258-501 CASC-DC1\Guest (Local User)
	User Name   :	CascGuest
	Full Name   :
	Home Drive  :
	Dir Drive   :
	Profile Path:
	Logon Script:
	Description :	Built-in account for guest access to the computer/domain
	Workstations:
	Comment     :
	Remote Dial :
	Logon Time               :	Thu, 01 Jan 1970 10:00:00 AEST
	Logoff Time              :	Thu, 01 Jan 1970 10:00:00 AEST
	Kickoff Time             :	Thu, 14 Sep 30828 12:48:05 AEST
	Password last set Time   :	Thu, 01 Jan 1970 10:00:00 AEST
	Password can change Time :	Thu, 01 Jan 1970 10:00:00 AEST
	Password must change Time:	Thu, 14 Sep 30828 12:48:05 AEST
	unknown_2[0..31]...
	user_rid :	0x1f5
	group_rid:	0x202
	acb_info :	0x00000215
	fields_present:	0x00ffffff
	logon_divs:	168
	bad_password_count:	0x00000000
	logon_count:	0x00000000
	padding1[0..7]...
	logon_hrs[0..21]...
	Account Disabled         : True
	Password does not expire : True
	Account locked out       : False
	Password expired         : False
	Interdomain trust account: False
	Workstation trust account: False
	Server trust account     : False
	Trusted for delegation   : False

S-1-5-21-2189247330-517467924-712900258-513 CASC-DC1\None (Domain Group)
	Group Name:	Domain Users
	Description:	All domain users
	Group Attribute:7
	Num Members:16


[34m ===============================( [0m[32mGetting printer info for 10.10.10.182[0m[34m )===============================

[0mdo_cmd: Could not initialise spoolss. Error was NT_STATUS_ACCESS_DENIED


enum4linux complete on Fri Nov 18 15:59:37 2022



```
