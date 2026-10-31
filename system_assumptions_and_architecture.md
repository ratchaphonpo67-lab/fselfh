## 1. ข้อสมมติและโครงสร้างระบบ

- **ชื่อรายวิชา**: นวัตกรรมและเทคโนโลยีสารสนเทศเพื่อการศึกษา (Educational Innovation and Information Technology)
- **รหัสวิชา**: ED32101
- **กลุ่มผู้เรียน**: นักศึกษาครุศาสตร์/ศึกษาศาสตร์ ชั้นปีที่ 2
- **สถาบัน**: มหาวิทยาลัยตัวอย่าง (Sample University)
- **จำนวนผู้เรียน**: 40 คน
- **โดเมนอีเมลสมมติ**: @student.su.ac.th
- **โครงสร้างระบบ**: 
  1. Frontend: Single-file HTML (`courseware.html`) ใช้ Tailwind CSS และ Alpine.js ผ่าน CDN พร้อม Supabase JS SDK.
  2. Backend: Supabase (PostgreSQL พร้อม Row Level Security, Triggers, Functions และ Private Storage Buckets).
  3. Security: RLS ป้องกันข้ามผู้ใช้, Column-level restrictions สำหรับคะแนนงาน, Private Buckets พร้อม Signed URLs.
- **ข้อสมมติเพิ่มเติม**: ผู้เรียนสมัครสมาชิกครั้งแรกด้วยรหัสนักศึกษา 11 หลัก ระบบจะตรวจสอบตารางรายชื่อ `students` และผูกบัญชีอัตโนมัติผ่าน Auth Trigger ผู้สอนใช้อีเมลนอกรูปแบบ 11 หลัก (เช่น `teacher@su.ac.th`) และตั้งค่าผ่านสิทธิ์ `is_teacher()`.