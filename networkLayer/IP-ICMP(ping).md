common network layer protocols include IPv4,IPv6,ICMP,IGMP

IP Packet Forwarding
    เวลาเราส่งข้อมูล ข้อมูลจะถูกห่อเป็น IP packet
    ใน packet จะมี Source IP และ Destination IP
    ถ้าปลายทางอยู่นอกวง LAN → จะส่งไปที่ Router ก่อน
    Router จะดู Destination IP
    
    Router เปิดดูตารางเส้นทาง (Routing Table)แล้วตัดสินใจว่าจะส่ง packet ไปทางไหนต่อ
    แต่ละ Router ระหว่างทางจะทำแบบนี้ซ้ำ ๆ
    จน packet ไปถึงเครื่องปลายทาง

    🎯 สรุปสั้น ๆ
    **IP Forwarding = การที่ Router รับ packet มา แล้วส่งต่อไปยังเส้นทางที่ถูกต้องจนถึงปลายทาง**

ICMP 
    **ICMP (Internet Control Message Protocol) คือโปรโตคอลสำหรับส่ง “ข้อความแจ้งเตือน/สถานะ” ในเครือข่าย**
    ใช้บอกว่าแพ็กเก็ตส่งสำเร็จหรือมีปัญหา
    ไม่ได้ใช้ส่งข้อมูลปกติแบบ TCP/UDP
    คำสั่ง ping ใช้ ICMP Echo Request / Echo Reply
    ถ้าเข้าเว็บไม่ได้ อาจเจอ ICMP “Destination Unreachable”
    ช่วยวิเคราะห์ปัญหา network (troubleshooting)
    ทำงานอยู่ใน Layer 3 (Network Layer)
    บางครั้งถูกใช้ใน DDoS หรือ Ping Flood ได้

    🎯 สรุปสั้น ๆ
    ICMP = โปรโตคอลแจ้งเตือนสถานะเครือข่าย ใช้เช็คว่า “ถึงไหม / มีปัญหาไหม”

