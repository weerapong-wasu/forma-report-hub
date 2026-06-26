# 🚀 Deploy Guide — forma-report-hub
ทำครั้งเดียว ครั้งต่อไปแค่ push แล้ว auto deploy เลย

---

## STEP 1 — สร้าง GitHub Repo ใหม่
1. ไปที่ https://github.com/new
2. Repository name: `forma-report-hub`
3. Visibility: **Private** (แนะนำ — มีรูปจริงฝังอยู่)
4. **อย่า** tick Add README
5. กด **Create repository**

---

## STEP 2 — Push จาก Terminal (Mac)
เปิด Terminal แล้วพิมพ์ทีละบรรทัด:

```bash
# 1. ไปที่โฟลเดอร์ที่ extract ZIP มา
cd ~/Downloads/forma-report-hub

# 2. Init git
git init

# 3. Add remote
git remote add origin https://github.com/weerapong-wasu/forma-report-hub.git

# 4. Add ไฟล์ทั้งหมด
git add .

# 5. Commit
git commit -m "Initial deploy: reno-wari79-69"

# 6. Push
git branch -M main
git push -u origin main
```

---

## STEP 3 — Connect Vercel
1. ไปที่ https://vercel.com/dashboard
2. กด **"Add New Project"**
3. เลือก **"Import Git Repository"**
4. เลือก repo **`forma-report-hub`**
5. Framework Preset: **Other**
6. Root Directory: **./** (ปล่อยว่าง)
7. กด **Deploy** ✅

---

## STEP 4 — Add Custom Domain
1. ใน Vercel project → **Settings → Domains**
2. พิมพ์: `report.formacorps.com`
3. กด **Add**
4. Vercel จะแสดง CNAME value ให้ copy

---

## STEP 5 — Hostinger DNS
1. Login https://hpanel.hostinger.com
2. Domains → formacorps.com → **DNS Zone**
3. กด **Add Record**
```
Type  : CNAME
Name  : report
Value : cname.vercel-dns.com   ← (หรือค่าที่ Vercel ให้มา)
TTL   : 3600
```
4. Save → รอ 5–30 นาที DNS propagate

---

## ✅ ผลลัพธ์
- `report.formacorps.com` → Hub page
- `report.formacorps.com/reno-wari79-69` → Renovation pitch (รูปจริง)

---

## 🔄 เพิ่ม Project ใหม่ในอนาคต
```bash
# 1. สร้างโฟลเดอร์ใหม่
mkdir roof-khaokew-69
# 2. ใส่ index.html
# 3. เพิ่ม route ใน vercel.json
# 4. Push
git add .
git commit -m "Add: roof-khaokew-69"
git push
# → Vercel auto deploy ทันที!
```
