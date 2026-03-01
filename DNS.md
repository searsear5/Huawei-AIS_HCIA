client->local DNS server->internet

Local DNS Server = DNS ตัวแรกที่เครื่องคุณถาม
มักอยู่ที่ Router บ้าน หรือ DNS ของ ISP
ทำหน้าที่ตอบจาก cache หรือไปถามอินเทอร์เน็ตให้

    ตัวอย่างการทำงาน

        คุณพิมพ์ facebook.com

        เครื่องถาม Local DNS

        ถ้ามี cache → ตอบ IP กลับทันที

        ถ้าไม่มี → ไปถาม Root → TLD → Authoritative DNS บน Internet

        ส่ง IP กลับมาที่เครื่องคุณ

Authoritative DNS Server คือเซิร์ฟเวอร์ที่ “เก็บข้อมูลโดเมนจริง ๆ” และเป็นคนตอบคำถามสุดท้ายว่า example.com มี IP อะไร

    1️⃣ ผู้ให้บริการ DNS เช่น

    Cloudflare

    Amazon Web Services

    Google Cloud

    2️⃣ บริษัท Hosting / Domain Provider

    เช่น

    GoDaddy

    Namecheap