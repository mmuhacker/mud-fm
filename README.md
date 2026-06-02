<div align="center">

# 📁 File Metadata Extractor
# أداة استخراج البيانات الوصفية

**تعمل على نظام Kali Linux و تطبيق Termux**

꧁ঔৣ☬ Muhannad Daher ☬ঔৣ꧂

---

```
███████╗███╗   ███╗
 ██╔════╝████╗ ████║
 █████╗  ██╔████╔██║
 ██╔══╝  ██║╚██╔╝██║
██║      ██║ ╚═╝  ██║
╚═╝      ╚═╝      ╚═╝
```

![Version](https://img.shields.io/badge/1.0-%EF%BA%8D%EF%BB%B9%EF%BA%BB%EF%BA%AA%EF%BA%8D%EF%BA%AE-blue?style=for-the-badge)<br>
![Platform](https://img.shields.io/badge/%EF%BB%9B%EF%BA%8E%EF%BB%9F%EF%BB%B2%20%EF%BB%9F%EF%BB%B4%EF%BB%A8%EF%BB%9C%EF%BA%B2-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=kalilinux)<br>
![Platform](https://img.shields.io/badge/%EF%BA%84%EF%BB%A7%EF%BA%AA%EF%BA%AE%EF%BB%AE%EF%BB%B3%EF%BA%AA-%EF%BA%8D%EF%BB%9F%EF%BA%92%EF%BB%B4%EF%BA%8C%EF%BA%94-green?style=for-the-badge&logo=android)<br>
![Python](https://img.shields.io/badge/3.x-%EF%BA%91%EF%BA%8E%EF%BB%B3%EF%BA%9C%EF%BB%AE%EF%BB%A6-blue?style=for-the-badge&logo=python)<br>
![License](https://img.shields.io/badge/MIT-%EF%BA%8D%EF%BB%9F%EF%BA%98%EF%BA%AE%EF%BA%A7%EF%BB%B4%EF%BA%BA-red?style=for-the-badge)<br>
![Status](https://img.shields.io/badge/%EF%BB%A7%EF%BA%B8%EF%BB%82-%EF%BA%8D%EF%BB%9F%EF%BA%A4%EF%BA%8E%EF%BB%9F%EF%BA%94-blue?style=for-the-badge)

---

**المحتويات:**

</div>

- [الوصف](#الوصف)
- [المميزات](#المميزات)
- [التثبيت](#التثبيت)
  - [التثبيت على Termux](#التثبيت-على-termux)
  - [التثبيت على Kali Linux](#التثبيت-على-kali-linux)
- [التشغيل](#التشغيل)
- [طريقة الاستخدام](#طريقة-الاستخدام)
- [مثال](#مثال)
- [المتطلبات](#المتطلبات)
- [إخلاء المسؤولية](#إخلاء-المسؤولية)
- [المطوّر](#المطوّر)
- [الرخصة](#الرخصة)

---

<div align="center" id="الوصف">

## 📌 الوصف

</div>

أداة لاستخراج البيانات الوصفية (Metadata) من الملفات الرقمية. تدعم الصور (EXIF)، مستندات PDF، وملفات Word. تستخدم في التحقيق الجنائي الرقمي وتحليل الملفات المشبوهة داخل المختبرات الشخصية.

---

<div align="center" id="المميزات">

## ✨ المميزات

</div>

- 🖼️ استخراج بيانات EXIF من الصور (GPS، الكاميرا، التاريخ...)
- 📄 استخراج بيانات PDF (المؤلف، العنوان، التواريخ...)
- 📝 استخراج بيانات مستندات Word
- 💾 حفظ النتيجة كملف JSON
- 🎨 بانر احترافي ثلاثي الأبعاد
- 🌍 واجهة عربية بالكامل

---

<div align="center" id="التثبيت">

## ⚙️ التثبيت

</div>

<div align="center" id="التثبيت-على-termux">

### Termux

</div>

**الخطوة 1 — تحديث النظام**
```bash
pkg update && pkg upgrade -y
```

الخطوة 2 — تثبيت Python والمكتبات

```bash
pkg install python -y
pip install pillow PyPDF2 python-docx
```

الخطوة 3 — تنزيل الأداة

```bash
curl -o $PREFIX/bin/mud_fm.py https://raw.githubusercontent.com/mmuhacker/mud-fm/main/mud_fm.py
```

الخطوة 4 — صلاحيات التشغيل

```bash
chmod +x $PREFIX/bin/mud_fm.py
```

الخطوة 5 — رابط الاختصار

```bash
ln -sf $PREFIX/bin/mud_fm.py $PREFIX/bin/fm
```

⚡ أمر واحد مجمّع

```bash
pkg update && pkg upgrade -y && pkg install python -y && pip install pillow PyPDF2 python-docx && curl -o $PREFIX/bin/mud_fm.py https://raw.githubusercontent.com/mmuhacker/mud-fm/main/mud_fm.py && chmod +x $PREFIX/bin/mud_fm.py && ln -sf $PREFIX/bin/mud_fm.py $PREFIX/bin/fm && fm
```

---

<div align="center" id="التثبيت-على-kali-linux">

Kali Linux

</div>

الخطوة 1 — تحديث النظام

```bash
sudo apt update && sudo apt upgrade -y
```

الخطوة 2 — تثبيت المكتبات

```bash
pip install pillow PyPDF2 python-docx --break-system-packages
```

الخطوة 3 — تنزيل الأداة

```bash
sudo curl -o /usr/local/bin/mud_fm.py https://raw.githubusercontent.com/mmuhacker/mud-fm/main/mud_fm.py
```

الخطوة 4 — صلاحيات التشغيل

```bash
sudo chmod +x /usr/local/bin/mud_fm.py
```

الخطوة 5 — رابط الاختصار

```bash
sudo ln -sf /usr/local/bin/mud_fm.py /usr/local/bin/fm
```

⚡ أمر واحد مجمّع

```bash
sudo apt update && sudo apt upgrade -y && pip install pillow PyPDF2 python-docx --break-system-packages && sudo curl -o /usr/local/bin/mud_fm.py https://raw.githubusercontent.com/mmuhacker/mud-fm/main/mud_fm.py && sudo chmod +x /usr/local/bin/mud_fm.py && sudo ln -sf /usr/local/bin/mud_fm.py /usr/local/bin/fm && fm
```

---

<div align="center" id="التشغيل">

🚀 التشغيل

</div>

```bash
fm
```

أو بالأمر الكامل

```bash
mud_fm.py
```

---

<div align="center" id="طريقة-الاستخدام">

📖 طريقة الاستخدام

</div>

```bash
fm /path/to/file.jpg
```

---

<div align="center" id="مثال">

💡 مثال

</div>

```bash
fm ~/storage/downloads/sample.pdf
```

النتيجة:

```
[+] معلومات الملف الأساسية:
   📄 اسم الملف: sample.pdf
   📦 الحجم (بايت): 245760
   🕒 آخر تعديل: 2025-06-01 12:30:00

[+] البيانات الوصفية الخاصة:
   المؤلف: Muhannad Daher
   العنوان: تقرير تقني
   تاريخ الإنشاء: 2025-05-30

[✓] تم حفظ النتيجة في sample_metadata.json
```

---

<div align="center" id="المتطلبات">

🔧 المتطلبات

المتطلب الوصف
Python 3.6+ لغة البرمجة
Pillow للتعامل مع الصور
PyPDF2 لقراءة PDF
python-docx لقراءة Word

</div>

---

<div align="center" id="إخلاء-المسؤولية">

⚖️ إخلاء المسؤولية

</div>

هذه الأداة مخصصة لأغراض تعليمية واختبار الملفات التي تملكها فقط. استخدامها على ملفات بدون إذن يُعدّ مخالفاً للقانون.

---

<div align="center" id="المطوّر">

👨‍💻 المطوّر

Muhannad Daher

https://img.shields.io/badge/GitHub-mmuhacker-black?style=for-the-badge&logo=github

---

📄 الرخصة

MIT License — حر الاستخدام مع ذكر المصدر

---

Madarik Tools — صُنع بالعربية

⭐ إذا أعجبتك الأداة، لا تنسَ النجمة! ⭐

</div>
```
