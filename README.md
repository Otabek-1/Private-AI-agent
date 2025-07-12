
# 🧠 Private-AI-Agent

**Private-AI-Agent** — bu sizga yordam beradigan AI bilan birlashtirilgan shaxsiy agent. Siz oddiy til orqali topshiriqlarni yozasiz va u ularni avtomatik bajaraydi — real vaqt statistikasi, xatoliklar haqida ogohlantirishlar, va fayl tahrirlash funksiyalari bilan.

---

## 📌 Maqsad

Yakka tartibdagi foydalanuvchilar va ish bilan band insonlar uchun zamonaviy, avtomatlashtirilgan va shaxsiy yordamchi yaratish. Asosiy maqsad — inson topshiriqlarini oddiy shaklda ifodalaydi, agent esa ularni bajaradi.

> "Do‘stlaringiz sizga yordam berolmasa, sizga Private-AI-Agent yordam beradi." 😉

---

## 🚀 Asosiy imkoniyatlar (MVP)

- ✍️ **Step-by-step** tasklar: Siz topshiriqlarni oddiy til bilan yozasiz
- 📂 **Fayl tahrirlash**: `.doc`, `.docx`, `.xlsx` fayllarni avtomatik o‘qish va yozish
- 📊 **Real-time statistika**: Qaysi ish bajarilmoqda, qancha qoldi, nechta muvaffaqiyatli yoki xatolik bo‘ldi
- 📬 **Gmail orqali bildirishnoma**: Har bir muvaffaqiyat yoki xatolik haqida email orqali habar
- 🌐 **VPS hosting**: Alwaysdata (1GB RAM VPS) da bepul joylashtirish
- 🔐 **Login bo‘lmasdan ishlash** (MVP uchun): Minimal soddalik, foydalanuvchi nomi va topshiriq kifoya

---

## 🛠 Texnologiyalar

| Texnologiya    | Maqsadi                              |
|----------------|----------------------------------------|
| **Node.js**    | Backend va agent logikasini boshqaradi |
| **React.js**   | Foydalanuvchi interfeysi (dashboard)   |
| **Express.js** | REST API yaratish uchun                 |
| **Multer**     | Fayl yuklash uchun                     |
| **Docx4js / XLSX** | DOC/DOCX/Excel fayllarni tahrirlash |
| **Nodemailer** | Gmail orqali email yuborish            |
| **Socket.IO**  | Real-time statistikani ko‘rsatish       |

---

## 📦 Loyihaning struktura sxemasi

```
private-ai-agent/
├── client/               # React frontend
│   └── src/
│       └── components/
├── server/               # Node.js backend
│   ├── routes/
│   ├── tasks/
│   └── utils/
├── uploads/              # Yuklangan fayllar
├── README.md
├── .env
└── package.json
```

---

## 💻 Ishlash prinsipi

1. Siz topshiriqni yozasiz:
    ```text
    1. docx fayldagi jadvaldagi ism va ballarni Excel faylga ikki qatorda joylashtir
    2. Faylni gmailga yubor
    ```
2. Agent topshiriqni tabiatiga ko‘ra bajara boshlaydi:
    - Faylni o‘qiydi
    - Kerakli ma'lumotni ajratadi
    - Excelga yozadi
    - Natijani yuboradi
3. Siz esa:
    - Real-time holatni dashtbordda ko‘rasiz
    - Email orqali bajarilganligi haqida bildirishnoma olasiz

---

## 📥 Topshiriq formatlari (Task Prompt)

| Namuna | Tushuntirish |
|--------|--------------|
| `Upload "login123", "pass456" bilan akkauntga fayl` | Web login va upload qilish |
| `Fayldan 3-sahifadagi jadvalni o‘qib, Excelga yoz`    | DOCX → XLS konvertatsiya |
| `Statistika faylini och, ball >80 bo‘lganlarni alohida ajrat` | Shartli ajratish |

> ⚠️ Kelajakda bu komandalar GPT yordamida avtomatik kodinga aylanadi!

---

## 📈 Real-time monitoring

- Har bir topshiriq uchun:
  - ⏳ Boshlangan vaqt
  - ✅ Bajarilganmi yoki yo‘q
  - ⚠️ Xatolik tafsilotlari (agar bo‘lsa)
- Web dashboard orqali kuzatish

---

## 🔔 Gmail notifikatsiya

Tizim tugallanganda yoki xatolik bo‘lsa:
- 📬 Email yuboriladi: 
    - `Subject: ✅ Task completed successfully!`
    - `Subject: ❌ Task failed - Error: File not found`

---

## 🧪 MVP rejasi

- [x] DOCX → XLSX fayl konvertori
- [x] Task queue (ketma-ket bajarish)
- [x] Real-time stats (Socket.IO)
- [x] Email notifications (Nodemailer)
- [x] Alwaysdata VPS deploy

---

## 🧱 Kelajakdagi rejalar

- [ ] Web automation (login, upload, download)
- [ ] Telegram/Slack bot interfeysi
- [ ] GPT asosida topshiriqni kodga aylantirish
- [ ] Faylni ovoz orqali topshiriq shaklida berish
- [ ] Task xotirasi: tarixni saqlash va yana ishlatish

---

## 🧠 Foydalanuvchi kimga kerak?

- Ish bilan band freelancerlar
- AI developerlar uchun test assistant
- Studentlar uchun hujjat avtomatizatsiyasi
- Shaxsiy yordamchi kerak bo‘lgan har bir kishi

---

## 🧾 Lisensiya & Mualliflik

- © 2025 CodeCraft Ltd  
- Muallif: Otabek Burhonov  
- Shaxsiy loyiha: motivatsiya, o‘rganish va real foyda beradigan agent qurish.

---

## ✍️ So‘nggi so‘z

> Bu loyiha menga va ChatGPT’ga omad olib kelsin!  
> Sog'liq uchun !

**2025 yil yozgi imzo:** `-_-Sign`  
