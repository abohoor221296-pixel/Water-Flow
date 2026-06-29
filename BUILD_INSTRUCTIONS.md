# تعليمات البناء والتشغيل - Water Flow 🚀

## المتطلبات الأساسية

✅ **Visual Studio 2019 أو أحدث** (مع WPF و .NET Framework 4.7.2+)
✅ **Windows 7 فما فوق**
✅ **مساحة تخزين:** 1 GB

---

## خطوات البناء والتشغيل

### 1️⃣ استنساخ المستودع
```bash
git clone https://github.com/abohoor221296-pixel/Water-Flow.git
cd Water-Flow
```

### 2️⃣ فتح المشروع في Visual Studio
1. اضغط على **File → Open → Project/Solution**
2. اختر ملف **`WaterFlow.sln`**
3. سينتظر Visual Studio قليلاً ليحمل جميع المشاريع

### 3️⃣ استعادة الحزم (NuGet)
1. انتقل إلى **Tools → NuGet Package Manager → Package Manager Console**
2. شغل الأمر:
```bash
Update-Package -Reinstall
```

أو اضغط على **Project → Restore NuGet Packages**

### 4️⃣ تكوين قاعدة البيانات
1. في **Package Manager Console** شغّل:
```bash
Enable-Migrations -ProjectName WaterFlow.Data
```

2. ثم:
```bash
Add-Migration InitialCreate -ProjectName WaterFlow.Data
```

3. أخيراً:
```bash
Update-Database -ProjectName WaterFlow.Data
```

### 5️⃣ تعيين المشروع الرئيسي
1. اضغط بزر اليمين على **`WaterFlow.UI`** 
2. اختر **Set as Startup Project**

### 6️⃣ التشغيل
1. اضغط **F5** أو **Debug → Start Debugging**
2. أو انقر على زر التشغيل الأخضر ▶️

---

## هيكل المشروع

```
Water-Flow/
├── WaterFlow.sln                 # ملف الحل الرئيسي
├── WaterFlow.UI/                 # الواجهة الرسومية (WPF)
│   ├── App.xaml & App.xaml.cs
│   ├── MainWindow.xaml & .cs
│   ├── Views/
│   │   ├── DashboardView.xaml
│   │   ├── CategoriesView.xaml
│   │   ├── ProductsView.xaml
│   │   ├── AdditionView.xaml
│   │   ├── WithdrawalView.xaml
│   │   ├── AnalyticsView.xaml
│   │   ├── ReportsView.xaml
│   │   └── SettingsView.xaml
│   ├── Resources/
│   └── WaterFlow.UI.csproj
├── WaterFlow.Models/             # نماذج البيانات
│   ├── Product.cs
│   ├── Category.cs
│   ├── Transaction.cs
│   └── WaterFlow.Models.csproj
├── WaterFlow.Data/               # طبقة البيانات
│   ├── ApplicationDbContext.cs
│   ├── Repositories/
│   │   ├── IRepository.cs
│   │   └── Repository.cs
│   └── WaterFlow.Data.csproj
├── WaterFlow.Services/           # الخدمات
│   ├── ExcelService.cs
│   ├── AnalyticsService.cs
│   └── WaterFlow.Services.csproj
├── App.config                    # إعدادات التطبيق
└── README.md
```

---

## استكشاف الأخطاء

### ❌ خطأ: "NuGet packages not found"
**الحل:**
1. حذف مجلد `packages`
2. حذف ملفات `bin` و `obj`
3. شغّل `Update-Package -Reinstall`

### ❌ خطأ: "The XAML file doesn't load"
**الحل:**
1. تأكد من أن `.NET Framework 4.7.2` مثبت
2. أعد بناء الحل: **Build → Clean Solution** ثم **Build → Build Solution**

### ❌ خطأ: "Database initialization failed"
**الحل:**
1. احذف ملف `WaterFlow.db` من مجلد البرنامج
2. شغّل `Update-Database` مرة أخرى

### ❌ خطأ: "Could not find project 'WaterFlow.Data'"
**الحل:**
1. في Package Manager Console اختر: **Default Project → WaterFlow.Data**
2. ثم شغّل الأوامر مرة أخرى

---

## الإعدادات الأولية بعد التشغيل

1. **أضف التصنيفات:**
   - انتقل إلى → **التصنيفات**
   - أضف تصنيفات مثل: "المشروبات", "الأطعمة", "الملحقات"

2. **أضف المنتجات:**
   - انتقل إلى → **المنتجات**
   - أضف منتجاتك مع الأسعار والكميات

3. **ربط Excel:**
   - انتقل إلى → **الإعدادات**
   - حدد مسار ملف Excel
   - اضغط **مزامنة الآن**

---

## الملفات المهمة

- **`App.config`** - إعدادات الاتصال بقاعدة البيانات
- **`WaterFlow.db`** - قاعدة البيانات (ينشأ تلقائياً)
- **`WaterFlow.xlsx`** - ملف Excel للمزامنة

---

## الدعم الفني

إذا واجهت مشاكل:
1. تحقق من رسالة الخطأ
2. ابحث في **Issues** على GitHub
3. أنشئ issue جديد مع تفاصيل المشكلة

---

**نسخة:** 1.0.0  
**آخر تحديث:** 2026  
**الحالة:** ✅ جاهز للاستخدام
