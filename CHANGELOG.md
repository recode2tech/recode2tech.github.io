# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased] - 2026-09-13

### Added
- **Dark Theme by Default & Interactive Theme Toggle Switcher**:
  - เพิ่มระบบสลับธีม (Light / Dark Mode Switcher) ให้สามารถกดสลับธีมได้ทันที และบันทึกค่าที่ผู้ใช้เลือกไว้ใน `localStorage`
  - ตั้งค่าให้ **Dark Theme เป็นธีมเริ่มต้น (Default)** เพื่อความสวยงาม สบายตา และเข้ากับสไตล์ Dev / Tech
  - นำไปประยุกต์ใช้ครบทั้ง 7 หน้าของเว็บไซต์:
    - `/index.html` (หน้าหลักของสตูดิโอ)
    - `/watermark-app/index.html`
    - `/watermark-app/privacy-policy/index.html`
    - `/watermark-app/terms-conditions/index.html`
    - `/pdf-image-converter/index.html`
    - `/pdf-image-converter/privacy-policy/index.html`
    - `/pdf-image-converter/terms-conditions/index.html`
- **Recode2Tech Studio Portal (Root Homepage)**:
  - `/index.html`: สร้างหน้า Landing Page หลักของเว็บไซต์ `https://recode2tech.github.io/` แทนที่หน้าจอเริ่มต้นเดิมที่ GitHub Pages ดึงเอาไฟล์ `README.md` ไปเรนเดอร์
    - ดีไซน์ทันสมัยแบบสตูดิโอผู้พัฒนาแอปพลิเคชันมือถือ พร้อมรองรับทั้ง Light / Dark Mode อัตโนมัติ
    - การ์ดแนะนำแอปพลิเคชันทั้ง 2 ตัว: **PDF Image Converter** และ **Watermark For You**
    - มีปุ่มเข้าชม Portal ของแต่ละแอป พร้อมลิงก์ตรงไปยัง Privacy Policy และ Terms & Conditions
    - แบนเนอร์แสดงจุดเด่นด้านความปลอดภัย: Local-First Architecture, Zero Cloud Upload, Full Offline Freedom
- **Watermark For You Legal & Landing Pages**:
  - `/watermark-app/privacy-policy/index.html`: สร้างหน้านโยบายความเป็นส่วนตัว (Privacy Policy) สำหรับ `Watermark For You`
    - ระบุการประมวลผลรูปภาพแบบ Local & Offline 100% บนตัวเครื่องของผู้ใช้ โดยไม่มีการส่งรูปภาพหรือโลโก้ขึ้น Server
    - อัปเดตการขอสิทธิ์ (Device Permissions) เช่น Media / Photos Access และ Camera Access (แบบ Optional)
    - อ้างอิง Third-Party SDKs ที่จำเป็นต่อการพัฒนา: Firebase Crashlytics, Google AdMob, Google Play Billing
  - `/watermark-app/terms-conditions/index.html`: สร้างหน้าข้อกำหนดและเงื่อนไข (Terms & Conditions) สำหรับ `Watermark For You`
    - เน้นย้ำสิทธิ์ความเป็นเจ้าของ (Copyright & Intellectual Property): ผู้ใช้ยังคงเป็นเจ้าของรูปภาพ, โลโก้ และเนื้อหาลายน้ำทั้งหมด 100% ทางผู้พัฒนาไม่มีสิทธิ์ในผลงานของผู้ใช้
    - ข้อกำหนดการใช้งานที่ยอมรับได้ (Acceptable Use): ห้ามใช้แอปในการละเมิดลิขสิทธิ์ของผู้อื่น
    - นโยบายการซื้อ In-App Purchase และการขอเงินคืนผ่าน Google Play
    - ข้อกำหนดเรื่องความปลอดภัย การปฏิบัติตามมาตรฐาน Digital Services Act (DSA)
  - `/watermark-app/index.html`: สร้างหน้า Landing Page และ Legal Portal กลางสำหรับ `Watermark For You` เชื่อมต่อไปยังหน้า Privacy Policy และ Terms & Conditions ตามโครงสร้างเดียวกับ `pdf-image-converter`

### Changed
- **PDF Image Converter Legal & Portal Fixes**:
  - `/pdf-image-converter/terms-conditions/index.html`: แก้ไขและจัดระเบียบเนื้อหาข้อกำหนดและเงื่อนไข (Terms & Conditions) ที่เคยถูกบันทึกทับด้วยหน้า Landing Page ให้กลับมาเป็นเอกสารกฎหมายฉบับเต็ม พร้อมดีไซน์พรีเมียม สลับแท็บกับหน้า Privacy Policy ได้อย่างสมบูรณ์
  - `/pdf-image-converter/index.html`: แก้ไขลิงก์ปุ่มนำทางจาก `privacy-policy.html` และ `terms-conditions.html` ให้เป็น `privacy-policy/` และ `terms-conditions/` เพื่อให้ตรงกับโครงสร้างโฟลเดอร์จริงและไม่เกิด Error 404
