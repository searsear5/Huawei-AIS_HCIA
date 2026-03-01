                              Internet
                                  |
                                Router
                                  |
                            Edge Firewall
                                  |
        ----------------------------------------------------------
        |                          |                           |
       DMZ                     Internal Zone                VPN Zone
        |                          |                           |
      WAF                  ------------------              VPN Gateway
        |                  |   Firewall    |                   |
   Web Server  --------->  ------------------               Remote Users
        |                      |           |
     IDS/IPS               Database     User LAN
                                         |
                                       Switch
                                         |
                                     PC / Server


    DMZ (Demilitarized Zone)
โซนกลางสำหรับเครื่องที่ต้องเปิดให้ Internet เข้าถึง
เช่น:
Web Server
Mail Server
API Server
ถ้า Web Server โดน hack
Attacker จะยังไม่เข้าถึง LAN ตรง ๆ


    WAF (Web Application Firewall)
WAF จะอยู่หน้า Web Server
หน้าที่:
ป้องกัน SQL Injection
XSS
RCE
ตรวจ HTTP request ระดับ Layer 7
ตัวอย่างเช่น
Cloudflare
F5

    IDS / IPS

IDS = แจ้งเตือน
IPS = บล็อก
ตรวจจับ:
Port scanning
Exploit attempt
Malware traffic

**แบบที่ 2 ความปลอดภัยสูงกว่า**

                                Internet
                                    |
                                    Router
                                    |
                                Edge Firewall
                                    |
            ----------------------------------------------------------------
            |                         |                                   |
            DMZ                    User LAN                            VPN Zone
            |                         |                                   |
            WAF                      Switch                           VPN Gateway
            |                         |                                   |
        Web Server                    PC / Server                    Remote Users
            |
            | (Allow only DB Port)
            |
    -------------------------------
    |   Internal Segmentation     |
    |        Firewall (ISFW)      |
    -------------------------------
                    |
            Database Zone
                    |
                Database
