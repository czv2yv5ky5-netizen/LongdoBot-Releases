# LongdoBot Releases

ที่เก็บสาธารณะนี้ใช้เผยแพร่เฉพาะไฟล์โปรแกรม LongdoBot สำหรับ Windows และ
signed update manifest เท่านั้น ไม่มี source code, ระบบหลังบ้าน, รหัสผ่าน,
token หรือ private signing key อยู่ใน repository นี้

## การใช้งาน

1. ดาวน์โหลด `LongdoBot-Windows-x64.exe` จากหน้า Releases
2. เปิดโปรแกรมและเข้าสู่ระบบด้วยบัญชี LongdoBot
3. หนึ่งบัญชีใช้งานได้ตามจำนวนเครื่องที่เจ้าของระบบกำหนด ผู้ที่ไม่มีบัญชี
   หรือบัญชีถูกระงับจะไม่สามารถใช้ฟังก์ชันบอทได้

โปรแกรมรุ่นที่รองรับระบบอัปเดตจะตรวจ `update-manifest.json` ซึ่งลงนามด้วย
Ed25519 และตรวจ SHA-256/ขนาดไฟล์ก่อนติดตั้งทุกครั้ง

> หมายเหตุ: ลายเซ็น Ed25519 ใช้ยืนยันไฟล์ในระบบอัปเดต ไม่ใช่ Windows
> Authenticode หากไฟล์รุ่นใดยังไม่มี Authenticode Windows อาจแสดง
> “Unknown publisher” แม้การตรวจ signed manifest จะผ่านครบถ้วน

Source code และระบบหลังบ้านยังคงอยู่ใน private repositories และไม่เผยแพร่จาก
ที่เก็บนี้
