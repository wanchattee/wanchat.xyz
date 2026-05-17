# Deploy Guide — wanchat.xyz (ฟรีทั้งหมด)

## วิธีที่ดีที่สุด: GitHub Pages + Cloudflare (ฟรี 100%)

### ขั้นตอนทั้งหมด

---

## STEP 1 — สมัคร GitHub (ฟรี)
1. ไปที่ https://github.com → Sign up
2. ตั้ง username อะไรก็ได้ (เช่น `wanchat-xyz`)

---

## STEP 2 — สร้าง Repository
1. กด **New repository**
2. ตั้งชื่อว่า: `wanchat.xyz`  
   (หรือ `portfolio` ก็ได้)
3. ติ๊ก ✅ **Public**
4. กด **Create repository**

---

## STEP 3 — Upload ไฟล์เว็บ
1. กด **uploading an existing file**
2. ลาก `index.html` และ `avatar.png` เข้าไป
3. กด **Commit changes**

---

## STEP 4 — เปิด GitHub Pages
1. ไปที่ **Settings** → **Pages** (เมนูซ้าย)
2. Source: เลือก **Deploy from a branch**
3. Branch: `main` → folder: `/ (root)`
4. กด **Save**
5. รอ 1-2 นาที → จะได้ URL ฟรี เช่น:  
   `https://wanchat-xyz.github.io/wanchat.xyz`

---

## STEP 5 — ซื้อ domain wanchat.xyz (ราคาถูกมาก)
> .xyz domain ไม่สามารถได้ฟรี 100% แต่ราคาถูกมาก:
- **Porkbun.com** → ปีแรก ~$1.29 USD (~45 บาท) 🔥
- **Namecheap.com** → ~$0.99 USD
- **Cloudflare Registrar** → ~$8.57/ปี (ราคาต้นทุน ไม่บวกกำไร)

แนะนำ **Porkbun** ถูกที่สุดปีแรกครับ

---

## STEP 6 — เชื่อม Domain กับ GitHub Pages (ฟรี)

### 6a. ตั้งค่าใน GitHub
1. Settings → Pages → **Custom domain**
2. พิมพ์: `wanchat.xyz`
3. กด **Save**
4. ติ๊ก ✅ **Enforce HTTPS**

### 6b. ตั้งค่า DNS ที่ Porkbun (หรือ registrar ที่ใช้)
ไปที่ DNS Management แล้วเพิ่ม records นี้:

| Type  | Host | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | wanchat-xyz.github.io  |

รอ DNS propagate ~30 นาที ก็เสร็จแล้วครับ

---

## ผลลัพธ์สุดท้าย

| รายการ          | ค่าใช้จ่าย       |
|----------------|------------------|
| Hosting         | ฟรี (GitHub Pages) |
| SSL Certificate | ฟรี (auto HTTPS)  |
| Domain wanchat.xyz | ~45 บาท/ปี   |
| **รวม**         | **~45 บาท/ปี**   |

---

## ทางเลือกฟรี 100% (ไม่มี custom domain)

ถ้าไม่อยากซื้อ domain เลย ใช้:
- `wanchat-xyz.github.io` — GitHub Pages
- `wanchat.netlify.app` — Netlify
- `wanchat.pages.dev` — Cloudflare Pages

ทั้งหมดฟรี ไม่มีค่าใช้จ่ายใดๆ
