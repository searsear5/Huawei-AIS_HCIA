TTL
    **แพ็กเก็ตนั้นจะ “ผ่าน Router ได้กี่ครั้ง” ก่อนจะถูกทิ้ง**
    ตอนสร้าง packet จะกำหนดค่า TTL เช่น 64 หรือ 128
    ทุกครั้งที่ผ่าน Router → ค่า TTL จะลดลง 1
    ถ้า TTL = 0 → Router จะทิ้ง packet ทันที
    และส่ง ICMP Time Exceeded กลับมา

    ค่า TTL เริ่มต้นของแต่ละระบบ
    🪟 Windows
    ค่าเริ่มต้นส่วนใหญ่ = 128
    🐧 Linux
    ค่าเริ่มต้นส่วนใหญ่ = 64

    ใช้ ping เพื่อ check ได้
    ping 10.10.10.10
    Reply from 10.10.10.10: bytes=32 time=10ms TTL=63

        สรุปสั้น ๆ
    TTL = ตัวนับจำนวน hop (Router)
    หมดเมื่อไหร่ → packet ถูกทิ้ง