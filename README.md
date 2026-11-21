# Masareef | مصاريف — iOS Capacitor Project

مشروع جاهز لبناء تطبيق **مصاريف (Masareef)** بصيغة `.ipa` غير موقعة (Unsigned IPA) عبر **GitHub Actions** دون الحاجة لحساب مطور Apple مدفوع أو رفعه إلى App Store، بحيث يعمل 100% أوفلاين على الآيفون.

## محتويات المشروع
- `www/index.html`: واجهة التطبيق الكاملة (تعمل بدون إنترنت بالكامل مع حفظ البيانات محلياً).
- `package.json`: إعدادات وحزم Capacitor iOS.
- `capacitor.config.json`: إعدادات التطبيق (`com.alhawari.masareef`).
- `.github/workflows/build-ipa.yml`: ملف البناء التلقائي على خوادم macOS في GitHub لإنتاج `Masareef-unsigned.ipa`.

## خطوات استخراج ملف `.ipa`
1. أنشئ مستودعاً جديداً (Repository) على حسابك في **GitHub** (يمكن أن يكون Private أو Public).
2. ارفع جميع الملفات والمجلدات الموجودة داخل هذا المجلد (بما في ذلك المجلد المخفي `.github`).
   - **مهم جداً:** تأكد من رفع مجلد `.github/workflows/build-ipa.yml`.
3. افتح تبويب **Actions** في المستودع على GitHub.
4. اختر **Build Unsigned iOS IPA** واضغط **Run workflow** (أو سيبدأ تلقائياً عند الرفع على فرع `main`).
5. بعد انتهاء البناء (حوالي 3–5 دقائق)، انزل إلى قسم **Artifacts** في أسفل صفحة التشغيل وحمّل ملف **`Masareef-unsigned-ipa`**.
6. فك الضغط عنه لتحصل على **`Masareef-unsigned.ipa`**، ثم ثبّته على الآيفون باستخدام **Sideloadly** أو **AltStore** أو **TrollStore**.
