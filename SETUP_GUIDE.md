# دليل الإعداد الكامل - Water Flow 💧

## أولاً: التثبيت

### ✅ المرحلة 1: البيئة
1. تثبيت **Visual Studio 2019/2022**
2. اختر **Desktop Development with C++** و **ASP.NET and web development**
3. تثبيت **.NET Framework 4.7.2+**

### ✅ المرحلة 2: استنساخ المشروع
```bash
git clone https://github.com/abohoor221296-pixel/Water-Flow.git
cd Water-Flow
```

### ✅ المرحلة 3: فتح المشروع
- اضغط **File → Open**
- اختر **WaterFlow.sln**

### ✅ المرحلة 4: استعادة الحزم
```bash
Update-Package -Reinstall
```

### ✅ المرحلة 5: قاعدة البيانات
```bash
Enable-Migrations -ProjectName WaterFlow.Data
Add-Migration InitialCreate -ProjectName WaterFlow.Data
Update-Database -ProjectName WaterFlow.Data
```

---

## ثانياً: التشغيل

1. اضغط **F5**
2. البرنامج سيفتح تلقائياً

---

## ثالثاً: الاستخدام الأول

### إضافة التصنيفات
1. من الواجهة → **التصنيفات** (القائمة اليسرى)
2. أضف: "مشروبات" و "أطعمة" و "ملحقات"
3. اضغط **إضافة**

### إضافة المنتجات
1. من الواجهة → **المنتجات**
2. أضف منتجات مع:
   - الرمز (كود فريد)
   - الاسم
   - التصنيف
   - الكمية
   - السعر

### استخدام الإضافة والصرف
1. **الإضافة:** استقبال منتجات جديدة
2. **الصرف:** توزيع المنتجات

---

## رابعاً: ربط Excel

1. افتح **الإعدادات** (من القائمة اليسرى)
2. اضغط **استعرض** واختر ملف Excel
3. اضغط **مزامنة الآن**
4. البيانات ستُحفظ تلقائياً في Excel

---

## خامساً: التقارير والتحليلات

### التحاليل
- عرض الإحصائيات العامة
- رسوم بيانية
- أفضل المنتجات

### التقارير
- يومية
- أسبوعية
- شهرية
- تصدير PDF/Excel

---

## ملخص الأوامر المهمة

```bash
# فتح Package Manager Console
Tools → NuGet Package Manager → Package Manager Console

# استعادة الحزم
Update-Package -Reinstall

# تفعيل Migrations
Enable-Migrations -ProjectName WaterFlow.Data

# إضافة Migration
Add-Migration InitialCreate -ProjectName WaterFlow.Data

# تحديث قاعدة البيانات
Update-Database -ProjectName WaterFlow.Data

# بناء الحل
Build → Build Solution (Ctrl + Shift + B)

# التشغيل
Debug → Start Debugging (F5)
```

---

## بيانات اختبارية

عند بدء البرنامج، ستجد 3 تصنيفات افتراضية:
- 🍹 المشروبات
- 🍔 الأطعمة  
- 🎁 الملحقات

أضف منتجات لهذه التصنيفات لاختبار البرنامج.

---

## نصائح مهمة ⭐

1. **احفظ العمل:** البرنامج يحفظ تلقائياً
2. **نسخة احتياطية:** نسخ Excel احتياطياً أسبوعياً
3. **التحديثات:** اتفقد التحديثات الجديدة بانتظام
4. **الدعم:** للمساعدة اضغط على Issues في GitHub

---

**مبروك! 🎉 البرنامج جاهز للاستخدام!**
