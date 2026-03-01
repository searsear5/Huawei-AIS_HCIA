TCP
    TCP คือการส่งข้อมูลแบบ “ต้องถึงแน่นอน” มีการยืนยันรับ
    TCP Header จะมี: Source Port, Destination Port, Sequence Number, ACK, Flags
    มีการเรียงลำดับแพ็กเก็ตและตรวจสอบความถูกต้อง
    เหมาะกับเว็บ, ไฟล์, อีเมล (ต้องครบ ไม่หาย)
UDP
    UDP คือการส่งแบบ “ส่งเลย ไม่รอเช็ค” เร็วกว่า
    UDP Header มีแค่: Source Port, Destination Port, Length, Checksum
    ไม่มีการยืนยันรับ และไม่เรียงลำดับแพ็กเก็ต
    เหมาะกับเกมออนไลน์, วิดีโอสตรีม, VoIP