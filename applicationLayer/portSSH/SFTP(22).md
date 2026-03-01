# SFTP (SSH File Transfer Protocol)

1. **คืออะไร**: โปรโตคอลถ่ายโอนไฟล์ที่ทำงานผ่าน SSH (Secure Shell)
2. **Port**: ใช้ port 22 (เหมือน SSH) แทน port 21 (FTP)
3. **ความปลอดภัย**: เข้ารหัสทั้งหมด - username, password, และไฟล์
4. **ต่างจาก FTP**: FTP ส่งแบบ plain text (อ่านได้หมด), SFTP เข้ารหัสทั้งหมด
5. **ต่างจาก FTPS**: FTPS = FTP + SSL/TLS | SFTP = SSH-based (คนละตัว)
6. **Connection**: ใช้ connection เดียว (ไม่มีปัญหา active/passive mode แบบ FTP)
7. **Authentication**: รองรับ password และ SSH key-based authentication
8. **สรุป**: SFTP ปลอดภัยกว่า FTP มาก - ใช้ SFTP เสมอถ้าทำได้