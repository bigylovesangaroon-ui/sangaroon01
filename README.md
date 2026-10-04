# ระบบจัดตารางเวรปฏิบัติราชการ – กลุ่มงานสุขภาพดิจิทัล โรงพยาบาลตาพระยา

เว็บแอปหน้าเดียว (HTML + JavaScript ล้วน ไม่ต้องมีเซิร์ฟเวอร์) สำหรับจัดตารางเวรนอกเวลาราชการ
สร้างเอกสารขออนุมัติ/เบิกค่าตอบแทน (Word .docx, Excel .xlsx) และสรุปยอดเงินรายบุคคลรายเดือน

## วิธีนำขึ้น GitHub Pages
1. สร้าง repository ใหม่บน GitHub (เช่น `duty-roster`)
2. อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ (`index.html`, `.nojekyll`, `.github/workflows/pages.yml`, `README.md`) ไปที่สาขา `main`
3. ไปที่ **Settings → Pages → Build and deployment → Source** เลือก **GitHub Actions**
4. เมื่อ workflow "Deploy to GitHub Pages" ทำงานเสร็จ จะได้ลิงก์ `https://<ชื่อผู้ใช้>.github.io/<ชื่อ repo>/`

(หรือไม่ใช้ Actions: Settings → Pages → Source = *Deploy from a branch* → `main` / `/ (root)`)

## ข้อควรรู้
- ข้อมูลเวร ข้อความที่แก้ไข และการตั้งค่า เก็บใน **localStorage ของเบราว์เซอร์** แต่ละเครื่อง (ไม่แชร์ข้ามเครื่อง และไม่ถูกส่งไปที่ใด)
- ต้องต่ออินเทอร์เน็ตตอนเปิดหน้าเว็บ เพื่อโหลดไลบรารี JSZip และ ExcelJS จาก cdnjs และฟอนต์ Sarabun จาก Google Fonts
- ฟอนต์ Kanit และ TH SarabunIT๙ ฝังอยู่ในไฟล์แล้ว
- ไฟล์ Word ที่ดาวน์โหลดเป็น `.docx`
