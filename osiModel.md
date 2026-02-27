Application layer(HTTP,FTP,Telnet)
-ชั้นที่ใกล้ผู้ใช้ที่สุด เป็นที่ที่แอปพลิเคชันเข้าถึงเครือข่าย
-ให้บริการเครือข่ายกับโปรแกรมต่างๆ

Presentation layer(login)
-แปลงและจัดรูปแบบข้อมูลให้แอปพลิเคชันเข้าใจได้
-เข้ารหัส/ถอดรหัส (encryption/decryption) เช่น HTTPS, SSL/TLS
-บีบอัดข้อมูล (compression) เช่น ZIP, GZIP
-แปลง character encoding (ASCII, Unicode, UTF-8) ให้แสดงภาษาไทยได้
-แปลงไฟล์ format เช่น JPEG, PNG, MP4, GIF
-ตัวอย่าง: เว็บ HTTPS เข้ารหัสข้อมูลก่อนส่ง, รูปภาพถูกบีบอัดให้เล็กลง

Session layer
-รักษาสิทธิ์หลัง login (เช่น session cookies บนเว็บ)
-ถ้าการเชื่อมต่อขาด สามารถ reconnect และกลับมาทำงานต่อได้
-จัดการว่าใครส่งข้อมูลก่อนหลัง (dialog control)

Transport layer(TCP UDP)
-โปรโตคอล: TCP (reliable, มีการตรวจสอบ) และ UDP (fast, ไม่รับประกัน)
-ใช้ Port numbers เพื่อระบุแอปพลิเคชัน (เช่น HTTP=80, HTTPS=443, SSH=22)
-ตัวอย่าง: TCP สำหรับเว็บและอีเมล, UDP สำหรับวิดีโอสตรีมและเกม

Network layer(IP)
-หาเส้นทาง (routing) ที่ดีที่สุดเพื่อส่งข้อมูลไปยังปลายทาง
-ใช้ IP address ในการระบุปลายทาง
-แบ่งข้อมูลเป็น packets
-โปรโตคอล: IP (IPv4, IPv6), ICMP (ping), OSPF, BGP (routing protocols)
-อุปกรณ์: Router
-ตัวอย่าง: Router เลือกเส้นทางที่เร็วที่สุดส่งข้อมูลจากบ้านไป Google

Data link layer(MAC ADDRESS)
-ส่งข้อมูลระหว่างอุปกรณ์ที่อยู่ใน network เดียวกัน (local network)
-ใช้ MAC address ในการระบุอุปกรณ์
-แบ่งข้อมูลเป็น frames
-ตรวจสอบ error ในระดับ physical
-โปรโตคอล: Ethernet, Wi-Fi (802.11), PPP, ARP (แปลง IP เป็น MAC)
-อุปกรณ์: Switch, Bridge, NIC (Network Interface Card)
-ตัวอย่าง: Switch ส่งข้อมูลจากคอมพ์เครื่องหนึ่งไปอีกเครื่องในออฟฟิศ

Physical layer(สาย lan)
-ส่งข้อมูลแบบ raw bits (0 และ 1) ผ่านสื่อกายภาพ
-กำหนดรูปแบบทางกายภาพ เช่น รูปแบบสาย, ความถี่, แรงดันไฟฟ้า
-สื่อกลาง: สายแลน (UTP, STP, Fiber optic), คลื่นวิทยุ (Wi-Fi, Bluetooth), สัญญาณไฟฟ้า
-อุปกรณ์: Hub, Repeater, สายแลน, NIC
-ตัวอย่าง: สัญญาณไฟฟ้าวิ่งผ่านสายแลนหรือคลื่นวิทยุของ Wi-Fi