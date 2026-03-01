Switch คืออะไร?
    Switch คืออุปกรณ์เครือข่ายที่ทำงานใน OSI Layer 2 (Data Link Layer)
    หน้าที่หลักคือ ส่งข้อมูลไปยังเครื่องปลายทางที่ถูกต้อง โดยดูจาก MAC Address ไหนอยู่พอร์ตไหน
    เลยส่งข้อมูลได้ตรงเครื่อง ไม่กระจายมั่ว

เวลาเครื่อง A ส่งข้อมูลไปหาเครื่อง B:
    -ข้อมูลจะมี Source MAC และ Destination MAC
    -Switch จะอ่าน MAC Address
    -Switch จะดูในตารางที่เรียกว่า MAC Address Table (CAM Table)
    -ถ้ารู้ว่า MAC ปลายทางอยู่พอร์ตไหน → ส่งออกแค่พอร์ตนั้น
    -ถ้าไม่รู้ → จะ Flood ส่งออกทุกพอร์ต (ยกเว้นพอร์ตที่รับเข้ามา)

ในมุม Pentest ต้องระวังเรื่อง MAC flooding, ARP spoofing และ VLAN misconfiguration ครับ
"ถ้า attacker อยู่ใน network เดียวกันกับ switch จะโจมตีอะไรได้บ้าง?"
ควรตอบ:
ARP spoofing ส่ง arp reply ปลอม IP นี้ = MAC ของฉัน
MAC flooding
VLAN hopping
Sniff traffic ถ้า config ไม่ดี