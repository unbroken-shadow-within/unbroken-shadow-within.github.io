# คู่มือการตั้งค่า (Setup)

repo นี้เป็นปลายทางสำหรับ deploy เว็บบิลด์ของเกม *UNBROKEN · Shadow Within* ผ่าน GitHub Pages
ไม่มีซอร์สโค้ดของเกม มีเฉพาะไฟล์ที่ Godot 4.7 export ออกมาแล้ว
ภาพรวมโครงสร้างอ่านได้ที่ `CLAUDE.md`

## 1. รันเกมในเครื่อง

ไม่มีขั้นตอน build, lint หรือ test ให้รัน static server ที่รากของ repo แล้วเปิดในเบราว์เซอร์

```bash
python3 -m http.server 8000
```

- บิลด์เดสก์ท็อป: `http://localhost:8000/`
- บิลด์มือถือ: `http://localhost:8000/m/`
- บังคับบิลด์: ต่อท้าย `?desktop=1` หรือ `?mobile=1`

เปิดไฟล์ `index.html` ตรง ๆ ผ่าน `file://` ไม่ได้ เพราะเบราว์เซอร์ไม่ยอมโหลด WASM และ `.pck` จาก file URL

## 2. Deploy ขึ้น GitHub Pages

- GitHub Pages เสิร์ฟจาก branch `main` ที่รากของ repo
- ไฟล์ `.nojekyll` ต้องอยู่เสมอ เพื่อให้ Pages เสิร์ฟไฟล์ตามจริงโดยไม่ผ่าน Jekyll
- การ deploy คือการ commit ไฟล์ที่ export ใหม่จากโปรเจกต์ Godot ลง `main`
  ตามธรรมเนียมใช้ข้อความ commit ว่า `Web build <source-hash>` โดย hash คือ commit ของ repo ซอร์สเกมที่ export มา
- บิลด์หนึ่งครั้งมักเปลี่ยนแค่ `index.html`, `index.pck`, `m/index.html`, `m/index.pck`
  (ค่า `fileSizes` ใน `GODOT_CONFIG` ของ `index.html` ต้องตรงกับขนาดไฟล์ `.pck` และ `.wasm` จริง ตัว exporter เขียนให้อัตโนมัติ)
- ห้ามแก้ `index.js`, `*.wasm`, `*.pck` และไฟล์ audio worklet ด้วยมือ เพราะ export ครั้งถัดไปจะเขียนทับ

## 3. ตั้งค่า Claude Code ให้ทำงานกับ repo นี้

repo นี้อยู่ใต้ organization `unbroken-shadow-within` ไม่ใช่บัญชีส่วนตัว
Claude จะ push ได้ก็ต่อเมื่อ Claude GitHub App ถูกติดตั้ง **ที่ระดับ organization** และได้รับสิทธิ์เข้าถึง repo นี้

1. ไปที่ https://github.com/apps/claude/installations/select_target แล้วเลือก organization `unbroken-shadow-within`
   (ถ้าไม่ใช่ owner ของ org ต้องให้ owner เป็นคนติดตั้ง)
2. ให้แอปเข้าถึง repo `unbroken-shadow-within.github.io` หรือเลือก All repositories
3. ถ้าติดตั้งไว้แล้วแต่ยังขึ้น 403 ให้เชื่อม GitHub ใหม่ที่ https://claude.ai/customize/connectors?auth_start=github&auth_start_force=1

อาการเมื่อสิทธิ์ยังไม่ครบ: อ่าน repo ผ่าน API ได้ แต่ `git push` หรือการสร้าง branch ตอบ `403` พร้อมข้อความ
`Resource not accessible by integration` แปลว่าแอปติดตั้งอยู่บนบัญชีอื่น (เช่นบัญชีส่วนตัว) ไม่ใช่บน org

Claude Code อ่าน `CLAUDE.md` ที่รากของ repo ทุกครั้งที่เริ่ม session กฎที่กำหนดไว้ตอนนี้คือตอบผู้ใช้เป็นภาษาไทย
ส่วนโค้ด ชื่อไฟล์ และข้อความ commit เป็นภาษาอังกฤษ

## 4. ลิขสิทธิ์

เกมเป็นงานสงวนลิขสิทธิ์ (`LICENSE`) ส่วนประกอบของบุคคลที่สามอยู่ใน `THIRD_PARTY_NOTICES.md`
ซึ่งต้องตรงกับหน้าเครดิตในเกม ถ้าแก้ไฟล์นี้ต้องแก้ในซอร์สเกมด้วย
