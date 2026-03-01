Data Link Layer 
    คือ Layer 2 ของ OSI Model ทำหน้าที่ควบคุมการสื่อสารในเครือข่ายเดียวกัน เช่น LAN
    หน้าที่หลักคือการห่อหุ้มข้อมูลจาก Network Layer ให้เป็น Frame ใส่ Source และ Destination MAC Address และตรวจสอบความถูกต้องของข้อมูลด้วยกลไกอย่าง CRC
    อุปกรณ์ที่ทำงานใน Layer นี้คือ Switch ซึ่งจะใช้ MAC Address Table ในการตัดสินใจส่งข้อมูล

ARP Spoofing → หลอกว่าเราเป็น Gateway เพื่อดักข้อมูล
    เมื่อเหยื่อ broadcast ARP request ถามว่า IP นี้มี MAC อะไร attacker จะส่ง ARP reply ปลอมกลับไป โดยอ้างว่า IP นั้นมี MAC เป็นของ attacker ทำให้เหยื่ออัปเดต ARP table ผิด และส่ง traffic มาที่ attacker และสามารถทำ Man-in-the-Middle ได้
MAC Flooding → ทำให้ Switch Table เต็ม แล้วดักข้อมูลได้
    MAC Flooding คืออะไร?คือการส่ง MAC Address ปลอมจำนวนมากเข้าไปจน MAC Table เต็ม
VLAN Hopping → กระโดดข้าม VLAN ที่ถูกแยกไว้
    VLAN Hopping คืออะไร?คือการหาทาง “กระโดด” จาก VLAN หนึ่งไปอีก VLAN หนึ่ง
    โดยอาศัยการ config ผิดพลาด เช่น trunk port เปิดไว้

การโจมตีทั้ง 3 แบบนี้เกิดใน Layer 2 ซึ่งมักเกิดใน Internal Network มากกว่า External และมักอาศัย misconfiguration มากกว่าการ exploit ช่องโหว่ซอฟต์แวร์