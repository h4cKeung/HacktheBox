```bash
nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 3268 --script="banner,(ldap* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN "/home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp3268/tcp_3268_ldap_nmap.txt" -oX "/home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp3268/xml/tcp_3268_ldap_nmap.xml" 10.10.10.182
```

[/home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp3268/tcp_3268_ldap_nmap.txt](file:///home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp3268/tcp_3268_ldap_nmap.txt):

```
# Nmap 7.93 scan initiated Fri Nov 18 15:56:55 2022 as: nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 3268 "--script=banner,(ldap* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp3268/tcp_3268_ldap_nmap.txt -oX /home/parallels/HacktheBox/OSCP-like/AD-Cascade/results/10.10.10.182/scans/tcp3268/xml/tcp_3268_ldap_nmap.xml 10.10.10.182
Nmap scan report for 10.10.10.182
Host is up, received user-set (0.032s latency).
Scanned at 2022-11-18 15:57:03 AEDT for 16s

PORT     STATE SERVICE REASON  VERSION
3268/tcp open  ldap    syn-ack Microsoft Windows Active Directory LDAP (Domain: cascade.local, Site: Default-First-Site-Name)
| ldap-search: 
|   Context: DC=cascade,DC=local
|     dn: DC=cascade,DC=local
|         objectClass: top
|         objectClass: domain
|         objectClass: domainDNS
|         distinguishedName: DC=cascade,DC=local
|         instanceType: 5
|         whenCreated: 2020/01/09 15:31:32 UTC
|         whenChanged: 2022/11/18 04:53:44 UTC
|         subRefs: DC=ForestDnsZones,DC=cascade,DC=local
|         subRefs: DC=DomainDnsZones,DC=cascade,DC=local
|         subRefs: CN=Configuration,DC=cascade,DC=local
|         uSNCreated: 4099
|         uSNChanged: 340052
|         name: cascade
|         objectGUID: 6fd3434-bae0-484b-92be-88e4c5926638
|         objectSid: 1-5-21-3332504370-1206983947-1165150453
|         wellKnownObjects: B:32:6227F0AF1FC2410D8E3BB10615BB5B0F:CN=NTDS Quotas,DC=cascade,DC=local
|         wellKnownObjects: B:32:F4BE92A4C777485E878E9421D53087DB:CN=Microsoft,CN=Program Data,DC=cascade,DC=local
|         wellKnownObjects: B:32:09460C08AE1E4A4EA0F64AEE7DAA1E5A:CN=Program Data,DC=cascade,DC=local
|         wellKnownObjects: B:32:22B70C67D56E4EFB91E9300FCA3DC1AA:CN=ForeignSecurityPrincipals,DC=cascade,DC=local
|         wellKnownObjects: B:32:18E2EA80684F11D2B9AA00C04F79F805:CN=Deleted Objects,DC=cascade,DC=local
|         wellKnownObjects: B:32:2FBAC1870ADE11D297C400C04FD8D5CD:CN=Infrastructure,DC=cascade,DC=local
|         wellKnownObjects: B:32:AB8153B7768811D1ADED00C04FD8D5CD:CN=LostAndFound,DC=cascade,DC=local
|         wellKnownObjects: B:32:AB1D30F3768811D1ADED00C04FD8D5CD:CN=System,DC=cascade,DC=local
|         wellKnownObjects: B:32:A361B2FFFFD211D1AA4B00C04FD7D83A:OU=Domain Controllers,DC=cascade,DC=local
|         wellKnownObjects: B:32:AA312825768811D1ADED00C04FD8D5CD:CN=Computers,DC=cascade,DC=local
|         wellKnownObjects: B:32:A9D1CA15768811D1ADED00C04FD8D5CD:CN=Users,DC=cascade,DC=local
|         objectCategory: CN=Domain-DNS,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         gPLink: [LDAP://CN={31B2F340-016D-11D2-945F-00C04FB984F9},CN=Policies,CN=System,DC=cascade,DC=local;0]
|         dSCorePropagationData: 1601/01/01 00:00:00 UTC
|         masteredBy: CN=NTDS Settings,CN=CASC-DC1,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=cascade,DC=local
|         msDs-masteredBy: CN=NTDS Settings,CN=CASC-DC1,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=cascade,DC=local
|         msDS-IsDomainFor: CN=NTDS Settings,CN=CASC-DC1,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=cascade,DC=local
|         dc: cascade
|     dn: CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: container
|         cn: Users
|         description: Default container for upgraded user accounts
|         distinguishedName: CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:31:39 UTC
|         whenChanged: 2020/01/09 15:31:39 UTC
|         uSNCreated: 5696
|         uSNChanged: 5696
|         name: Users
|         objectGUID: d231c67-414-df4d-b413-e4aa7349bc19
|         objectCategory: CN=Container,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=krbtgt,CN=Users,DC=cascade,DC=local
|     dn: CN=Domain Computers,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Domain Computers
|         description: All workstations and servers joined to the domain
|         distinguishedName: CN=Domain Computers,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:15 UTC
|         whenChanged: 2020/01/09 15:32:15 UTC
|         uSNCreated: 12330
|         uSNChanged: 12332
|         name: Domain Computers
|         objectGUID: 2853eb7-44a1-7b42-9415-41f15eae55eb
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-515
|         sAMAccountName: Domain Computers
|         sAMAccountType: 268435456
|         groupType: -2147483646
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=Domain Controllers,CN=Users,DC=cascade,DC=local
|     dn: CN=Schema Admins,CN=Users,DC=cascade,DC=local
|     dn: CN=Enterprise Admins,CN=Users,DC=cascade,DC=local
|     dn: CN=Cert Publishers,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Cert Publishers
|         description: Members of this group are permitted to publish certificates to the directory
|         distinguishedName: CN=Cert Publishers,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:15 UTC
|         whenChanged: 2020/01/09 15:32:15 UTC
|         uSNCreated: 12342
|         memberOf: CN=Denied RODC Password Replication Group,CN=Users,DC=cascade,DC=local
|         uSNChanged: 12344
|         name: Cert Publishers
|         objectGUID: 1b379d6-64da-c849-bef9-8871c97d5e4
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-517
|         sAMAccountName: Cert Publishers
|         sAMAccountType: 536870912
|         groupType: -2147483644
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=Domain Admins,CN=Users,DC=cascade,DC=local
|     dn: CN=Domain Users,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Domain Users
|         description: All domain users
|         distinguishedName: CN=Domain Users,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:15 UTC
|         whenChanged: 2020/01/09 15:32:15 UTC
|         uSNCreated: 12348
|         memberOf: CN=Data Share,OU=Groups,OU=UK,DC=cascade,DC=local
|         memberOf: CN=Users,CN=Builtin,DC=cascade,DC=local
|         uSNChanged: 12350
|         name: Domain Users
|         objectGUID: 1586ba5b-c824-5844-8e39-827d18de329
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-513
|         sAMAccountName: Domain Users
|         sAMAccountType: 268435456
|         groupType: -2147483646
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=Domain Guests,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Domain Guests
|         description: All domain guests
|         distinguishedName: CN=Domain Guests,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:15 UTC
|         whenChanged: 2020/01/09 15:32:15 UTC
|         uSNCreated: 12351
|         memberOf: CN=Guests,CN=Builtin,DC=cascade,DC=local
|         uSNChanged: 12353
|         name: Domain Guests
|         objectGUID: 304928fd-4cdb-884c-ace2-5013aeca199e
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-514
|         sAMAccountName: Domain Guests
|         sAMAccountType: 268435456
|         groupType: -2147483646
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=Group Policy Creator Owners,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Group Policy Creator Owners
|         description: Members in this group can modify group policy for the domain
|         member: CN=Administrator,CN=Users,DC=cascade,DC=local
|         distinguishedName: CN=Group Policy Creator Owners,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:15 UTC
|         whenChanged: 2020/01/09 15:32:15 UTC
|         uSNCreated: 12354
|         memberOf: CN=Denied RODC Password Replication Group,CN=Users,DC=cascade,DC=local
|         uSNChanged: 12391
|         name: Group Policy Creator Owners
|         objectGUID: 3073956a-7a8d-649-bcea-8739bf522b6e
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-520
|         sAMAccountName: Group Policy Creator Owners
|         sAMAccountType: 268435456
|         groupType: -2147483646
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=RAS and IAS Servers,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: RAS and IAS Servers
|         description: Servers in this group can access remote access properties of users
|         distinguishedName: CN=RAS and IAS Servers,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:15 UTC
|         whenChanged: 2020/01/09 15:32:15 UTC
|         uSNCreated: 12357
|         uSNChanged: 12359
|         name: RAS and IAS Servers
|         objectGUID: c02dc1e4-663d-d645-9d5a-30686dd2195
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-553
|         sAMAccountName: RAS and IAS Servers
|         sAMAccountType: 536870912
|         groupType: -2147483644
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=Allowed RODC Password Replication Group,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Allowed RODC Password Replication Group
|         description: Members in this group can have their passwords replicated to all read-only domain controllers in the domain
|         distinguishedName: CN=Allowed RODC Password Replication Group,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:16 UTC
|         whenChanged: 2020/01/09 15:32:16 UTC
|         uSNCreated: 12402
|         uSNChanged: 12404
|         name: Allowed RODC Password Replication Group
|         objectGUID: 3aec39c4-53d3-e048-9f81-f12049ea1b9d
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-571
|         sAMAccountName: Allowed RODC Password Replication Group
|         sAMAccountType: 536870912
|         groupType: -2147483644
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=Denied RODC Password Replication Group,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Denied RODC Password Replication Group
|         description: Members in this group cannot have their passwords replicated to any read-only domain controllers in the domain
|         member: CN=Read-only Domain Controllers,CN=Users,DC=cascade,DC=local
|         member: CN=Group Policy Creator Owners,CN=Users,DC=cascade,DC=local
|         member: CN=Domain Admins,CN=Users,DC=cascade,DC=local
|         member: CN=Cert Publishers,CN=Users,DC=cascade,DC=local
|         member: CN=Enterprise Admins,CN=Users,DC=cascade,DC=local
|         member: CN=Schema Admins,CN=Users,DC=cascade,DC=local
|         member: CN=Domain Controllers,CN=Users,DC=cascade,DC=local
|         member: CN=krbtgt,CN=Users,DC=cascade,DC=local
|         distinguishedName: CN=Denied RODC Password Replication Group,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:16 UTC
|         whenChanged: 2020/01/09 15:32:16 UTC
|         uSNCreated: 12405
|         uSNChanged: 12433
|         name: Denied RODC Password Replication Group
|         objectGUID: b05816b1-eceb-8e49-ba6a-90dc61cfc25e
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-572
|         sAMAccountName: Denied RODC Password Replication Group
|         sAMAccountType: 536870912
|         groupType: -2147483644
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=Read-only Domain Controllers,CN=Users,DC=cascade,DC=local
|     dn: CN=Enterprise Read-only Domain Controllers,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: Enterprise Read-only Domain Controllers
|         description: Members of this group are Read-Only Domain Controllers in the enterprise
|         distinguishedName: CN=Enterprise Read-only Domain Controllers,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:16 UTC
|         whenChanged: 2020/01/09 15:32:16 UTC
|         uSNCreated: 12429
|         uSNChanged: 12431
|         name: Enterprise Read-only Domain Controllers
|         objectGUID: 19457d4b-b131-7749-bd68-cd7c4555fe5
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-498
|         sAMAccountName: Enterprise Read-only Domain Controllers
|         sAMAccountType: 268435456
|         groupType: -2147483640
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=DnsAdmins,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: DnsAdmins
|         description: DNS Administrators Group
|         distinguishedName: CN=DnsAdmins,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:55 UTC
|         whenChanged: 2020/01/09 15:32:55 UTC
|         uSNCreated: 12456
|         uSNChanged: 12458
|         name: DnsAdmins
|         objectGUID: 953d7327-cfd7-8e40-afa7-e7a6aaab7a4
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-1102
|         sAMAccountName: DnsAdmins
|         sAMAccountType: 536870912
|         groupType: -2147483644
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=DnsUpdateProxy,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: DnsUpdateProxy
|         description: DNS clients who are permitted to perform dynamic updates on behalf of some other clients (such as DHCP servers).
|         distinguishedName: CN=DnsUpdateProxy,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/09 15:32:55 UTC
|         whenChanged: 2020/01/09 15:32:55 UTC
|         uSNCreated: 12461
|         uSNChanged: 12461
|         name: DnsUpdateProxy
|         objectGUID: 9efd36ee-da3b-f245-b975-2c895f52f3d
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-1103
|         sAMAccountName: DnsUpdateProxy
|         sAMAccountType: 268435456
|         groupType: -2147483646
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 2020/01/09 17:59:34 UTC
|         dSCorePropagationData: 2020/01/09 15:48:57 UTC
|         dSCorePropagationData: 1601/07/14 22:36:49 UTC
|     dn: CN=WinRMRemoteWMIUsers__,CN=Users,DC=cascade,DC=local
|         objectClass: top
|         objectClass: group
|         cn: WinRMRemoteWMIUsers__
|         description: Members of this group can access WMI resources over management protocols (such as WS-Management via the Windows Remote Management service). This applies only to WMI namespaces that grant access to the user.
|         distinguishedName: CN=WinRMRemoteWMIUsers__,CN=Users,DC=cascade,DC=local
|         instanceType: 4
|         whenCreated: 2020/01/13 03:21:24 UTC
|         whenChanged: 2020/01/13 03:21:24 UTC
|         uSNCreated: 94238
|         uSNChanged: 94240
|         name: WinRMRemoteWMIUsers__
|         objectGUID: bf7326f-e427-3d42-9d10-5974833d2756
|         objectSid: 1-5-21-3332504370-1206983947-1165150453-1125
|         sAMAccountName: WinRMRemoteWMIUsers__
|         sAMAccountType: 536870912
|         groupType: -2147483644
|         objectCategory: CN=Group,CN=Schema,CN=Configuration,DC=cascade,DC=local
|         dSCorePropagationData: 2020/01/17 03:37:36 UTC
|         dSCorePropagationData: 2020/01/17 00:14:04 UTC
|         dSCorePropagationData: 1601/01/01 00:04:17 UTC
| 
| 
|_Result limited to 20 objects (see ldap.maxobjects)
| ldap-rootdse: 
| LDAP Results
|   <ROOT>
|       currentTime: 20221118045709.0Z
|       subschemaSubentry: CN=Aggregate,CN=Schema,CN=Configuration,DC=cascade,DC=local
|       dsServiceName: CN=NTDS Settings,CN=CASC-DC1,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=cascade,DC=local
|       namingContexts: DC=cascade,DC=local
|       namingContexts: CN=Configuration,DC=cascade,DC=local
|       namingContexts: CN=Schema,CN=Configuration,DC=cascade,DC=local
|       namingContexts: DC=DomainDnsZones,DC=cascade,DC=local
|       namingContexts: DC=ForestDnsZones,DC=cascade,DC=local
|       defaultNamingContext: DC=cascade,DC=local
|       schemaNamingContext: CN=Schema,CN=Configuration,DC=cascade,DC=local
|       configurationNamingContext: CN=Configuration,DC=cascade,DC=local
|       rootDomainNamingContext: DC=cascade,DC=local
|       supportedControl: 1.2.840.113556.1.4.319
|       supportedControl: 1.2.840.113556.1.4.801
|       supportedControl: 1.2.840.113556.1.4.473
|       supportedControl: 1.2.840.113556.1.4.528
|       supportedControl: 1.2.840.113556.1.4.417
|       supportedControl: 1.2.840.113556.1.4.619
|       supportedControl: 1.2.840.113556.1.4.841
|       supportedControl: 1.2.840.113556.1.4.529
|       supportedControl: 1.2.840.113556.1.4.805
|       supportedControl: 1.2.840.113556.1.4.521
|       supportedControl: 1.2.840.113556.1.4.970
|       supportedControl: 1.2.840.113556.1.4.1338
|       supportedControl: 1.2.840.113556.1.4.474
|       supportedControl: 1.2.840.113556.1.4.1339
|       supportedControl: 1.2.840.113556.1.4.1340
|       supportedControl: 1.2.840.113556.1.4.1413
|       supportedControl: 2.16.840.1.113730.3.4.9
|       supportedControl: 2.16.840.1.113730.3.4.10
|       supportedControl: 1.2.840.113556.1.4.1504
|       supportedControl: 1.2.840.113556.1.4.1852
|       supportedControl: 1.2.840.113556.1.4.802
|       supportedControl: 1.2.840.113556.1.4.1907
|       supportedControl: 1.2.840.113556.1.4.1948
|       supportedControl: 1.2.840.113556.1.4.1974
|       supportedControl: 1.2.840.113556.1.4.1341
|       supportedControl: 1.2.840.113556.1.4.2026
|       supportedControl: 1.2.840.113556.1.4.2064
|       supportedControl: 1.2.840.113556.1.4.2065
|       supportedControl: 1.2.840.113556.1.4.2066
|       supportedLDAPVersion: 3
|       supportedLDAPVersion: 2
|       supportedLDAPPolicies: MaxPoolThreads
|       supportedLDAPPolicies: MaxDatagramRecv
|       supportedLDAPPolicies: MaxReceiveBuffer
|       supportedLDAPPolicies: InitRecvTimeout
|       supportedLDAPPolicies: MaxConnections
|       supportedLDAPPolicies: MaxConnIdleTime
|       supportedLDAPPolicies: MaxPageSize
|       supportedLDAPPolicies: MaxQueryDuration
|       supportedLDAPPolicies: MaxTempTableSize
|       supportedLDAPPolicies: MaxResultSetSize
|       supportedLDAPPolicies: MinResultSets
|       supportedLDAPPolicies: MaxResultSetsPerConn
|       supportedLDAPPolicies: MaxNotificationPerConn
|       supportedLDAPPolicies: MaxValRange
|       supportedLDAPPolicies: ThreadMemoryLimit
|       supportedLDAPPolicies: SystemMemoryLimitPercent
|       highestCommittedUSN: 340084
|       supportedSASLMechanisms: GSSAPI
|       supportedSASLMechanisms: GSS-SPNEGO
|       supportedSASLMechanisms: EXTERNAL
|       supportedSASLMechanisms: DIGEST-MD5
|       dnsHostName: CASC-DC1.cascade.local
|       ldapServiceName: cascade.local:casc-dc1$@CASCADE.LOCAL
|       serverName: CN=CASC-DC1,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=cascade,DC=local
|       supportedCapabilities: 1.2.840.113556.1.4.800
|       supportedCapabilities: 1.2.840.113556.1.4.1670
|       supportedCapabilities: 1.2.840.113556.1.4.1791
|       supportedCapabilities: 1.2.840.113556.1.4.1935
|       supportedCapabilities: 1.2.840.113556.1.4.2080
|       isSynchronized: TRUE
|       isGlobalCatalogReady: TRUE
|       domainFunctionality: 4
|       forestFunctionality: 4
|_      domainControllerFunctionality: 4
Service Info: Host: CASC-DC1; OS: Windows 2008 R2; CPE: cpe:/o:microsoft:windows

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Nov 18 15:57:19 2022 -- 1 IP address (1 host up) scanned in 24.08 seconds

```
