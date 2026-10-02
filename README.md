<table>
<tr valign="top">
<td align="left">

```text
;ccccllllllooooddddddddxxxxdl:.'''.   . ....,:,;oxkxxxxdddddd 
;cccllllllooooooddddddxxoc'..  ..            ..''lkkxxxxxdddd
lollllllllooooodddddddl'.    ...               .'::xxxxxddddd
okkxollllllloooooddd;.                         ..,oxxdddddoo
okkkkkdollllloooool.            ....',..          .'ldddddoool
okkkkkkkxdoooooooo'          .:llodxkxxol;.      ..cdddooooll
okkkkkkkkkkxdooooo.        .'codddxxkOOOkkxdl'    'cddoooolll
dOOkkkkkkkkkkkxdoo'    ...,odxxddoooxO00OOkkxo.  .cddooollllc
dOOOOOOOkkkkkkkkxdo''',',cdxxxolcc:,.,lxOOOkx' 'odoooolllccc
dOOOOOOOOOOOOOOOOOolddo:cdxkOko;'.,,,,;odc;'..ldooolllcccc::
dOOOOOOOOOOOOOOOOOodlcocloxkO0Okdlc:;coOo..;:oddoolllcccccc:
dOOOO0,.;lxOOOOOOOkddoolcldxkO00OOkkxk0XKc;clOOOkkkxxddoooll
dOOOOO,;:c;d0OOOO00kxxcllloddxkOOkdox00XX0xxk000OOOkkkkkkxxx
dOOO0o:lodcO0OOOO00Okc:llodocdxkkxdccc:oxxkkk000OOOkkkkkkxxx
dOOO0cclocoO0OOOO0OOOl::cldddxxxdlocc:c:,ldxO000OOOOkkkkkkxx
okO0xclod:k0OOOkOl:cllc;;:llooddl:,;,,,;:;lO0000OOOOkkkkkkxx
oOO0lcloocO0OOkkx.   .lol:,,;clodddoc;;;:;ck000000OOOOkkkkkxx
okOk:cld:xOOOOkkc.   ;loooc;'',ldddddl:cld000000OOOOOkkkkkxxx
ok0o:lod:k0OOkko.   .codddolc:,',:ccllodO000000OOOOOOkkkkxxxx
oOOcclocoOOdl;.      .lddddollc:::::;lk00000000OOOOOkkkkxxxxx
oOdccc:''..           .:lodoollccclc..x00000000OOOkkkd;:clodd
,,......                .;lollllcc;.   .,lk000OOOkkxd;       
            .              .:cccc:;.        .:oxOOkkdo.       
                            .llc,.          ....,cool        
                             ;ol:.          .........        
                             .:,            .........        
                                            ....   .         
                                            .         ''.... 
                                                       ....
```

</td>
<td align="left">

```text
kyawwintun@profile ──────────────────────────
OS:            Kali Linux, Windows
Role:          Penetration Tester | OSCP+
Location:      Brooklyn, New York
Certs:         OSCP+ (OffSec)

Technical Skills ────────────────────────────
AD & Network:  Kerberoasting, Pass-the-Hash
Recon:         Nmap, Gobuster, NetExec
Web Exploits:  SQLi, XSS, Command Injection
Pivoting:      Chisel, Ligolo-ng, SSH
Post-Exploit:  LinPEAS, Mimikatz, GodPotato
Scripting:     Python, Bash, PowerShell

Contact & Links ─────────────────────────────
Website:       arakandata.com
Email:         kyawwintun.as@gmail.com
GitHub:        [github.com/kyawwintun](https://github.com/kyawwintun)
Languages:     English, Burmese, Rakhine
```

</td>
</tr>
</table>

---

### 🛡️ Security Projects & Portfolio

#### 1. Enterprise Active Directory Lab & Attack Simulation 
* **Design:** Designed and built a simulated enterprise network environment featuring multi-domain Active Directory, domain-joined workstations (`WIN-AS-DEV`, `WINLWINOO`), a Domain Controller (`ASPIRATION-DC`), and active antivirus defenses to create realistic attack-surface conditions.
* **Exploitation:** Achieved full Domain Controller compromise through a multi-stage attack chain: SMB enumeration → credential discovery in user descriptions → WinRM access (`Evil-WinRM`) → BloodHound AD analysis → Kerberoasting (`impacket-GetUserSPNs`) → hash cracking (`Hashcat`) → lateral movement via ACL abuse (`ForceChangePassword`) → SAM hash dumping → password reuse exploitation → DC compromise.
* **Evasion & Reporting:** Bypassed antivirus using manual enumeration when Mimikatz and `impacket-psexec` were blocked. Authored a 13-page report with executive summary, attack-chain walkthroughs, and four remediation categories: credential storage, AD ACL auditing, LAPS deployment, and audit/monitoring.

#### 2. Web Application Penetration Test Lab & Report 
* **Scope:** Conducted comprehensive web application penetration testing on a custom-built lab environment with both external and internal web applications, simulating a real-world engagement scope.
* **Execution:** Exploited a file upload vulnerability by bypassing `Content-Type` validation via Burp Suite, deploying a PHP backdoor for initial access, then escalated using `SeImpersonatePrivilege` abuse (`GodPotato`) to `NT AUTHORITY\SYSTEM.
* **Pivoting:** Pivoted into an internal network via Ligolo-ng, identified OS command injection in an internal reporting app running as SYSTEM, achieving full host compromise. Produced a 14-page report with remediation categories: file-upload hardening, input sanitization, privilege restriction, and network segmentation.

#### 3. ArakanData.com — Full-Stack Secure Web Application
* **Development:** Independently developed a full-stack web application incorporating role-based access control (RBAC), input sanitization, secure authentication workflows, and modern security controls to understand web security from a developer's defensive perspective.
* **Best Practices:** Implemented data validation, authorization boundaries, and OWASP best practices throughout the application stack, demonstrating practical application of secure development principles.
