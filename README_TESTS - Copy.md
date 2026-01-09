اختبارات CI وملف العمل

- تشغيل محلي سريع:
  - npm install
  - npm run start  # يفتح الموقع على http://127.0.0.1:8080
  - npm run test:axe  # فحص قائم على axe (مخرجات في reports/)
  - npm run test:devices  # اختبارات Playwright (يحتاج إلى متصفح + بيئة node)

- في GitHub Actions:
  - الملف `.github/workflows/playwright-tests.yml` يُشغّل عند الدفع أو فتح PR على `main`.
  - نتائج الفحص والتقاط الشاشة تُحمَّل كـ artifact في `reports/`.

ملاحظة: تشغيل Playwright في CI يتطلب تثبيت المتصفحات (الـ workflow يحتوي على `npx playwright install --with-deps`).