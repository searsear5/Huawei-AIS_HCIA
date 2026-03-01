Firewall คืออะไร?
Firewall เป็นอุปกรณ์หรือซอฟต์แวร์ที่ใช้ควบคุมและกรอง traffic ตาม policy โดยพิจารณาจาก IP, Port และ Protocol บางรุ่นสามารถตรวจสอบถึงระดับ Application ได้มีหน้าที่ป้องกันการเข้าถึงที่ไม่ได้รับอนุญาตทั้งขาเข้าและขาออกครับ
    เช่น กำหนด rule ว่า:
    อนุญาตแค่ port 80, 443 เข้า Web Server
    ปิด port อื่นทั้งหมด
    ถ้า attacker ยิง port 22 เข้ามา
    → Firewall บล็อก

Basic firewall → Layer 3–4 (IP, Port)