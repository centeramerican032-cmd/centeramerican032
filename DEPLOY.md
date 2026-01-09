نشر الموقع (Staging - GitHub Pages)

خطوات سريعة لعمل نشر على GitHub Pages:

1. تأكد أنّ المستودع في GitHub ولديك الفرع `main` مُحدّثاً.
2. قم بدفع (push) التغييرات إلى `main`:
   - git add . && git commit -m "Prepare site for GitHub Pages" && git push origin main
3. عند الدفع، سيُشغّل ملف Workflow `.github/workflows/deploy-pages.yml` عملية النشر الذاتية.
4. بعد اكتمال الـ Action، إختر صفحة GitHub Pages من إعدادات الريبو لتعيين مصدر النشر إلى `gh-pages` (إذا لزم).

بدلاً من ذلك محلياً يمكنك تشغيل النسخة الاختبارية عبر:

  npm install
  npm run start

ثم افتح http://127.0.0.1:8080 في المتصفح لمعاينة الموقع محلياً.

ملاحظة: لا أقوم بدفع الفرع نيابة عنك — أضفت الـ Workflow والأدوات المطلوبة، ويمكنك دفع التغييرات عندما تكون جاهزًا.