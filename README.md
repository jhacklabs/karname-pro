# کارنامه Pro — بسته انتشار وب و موبایل (PWA)
# Karnameh Pro — Web & Mobile Release Package (PWA)

---

## فارسی

### محتویات بسته
- `index.html`: فایل اصلی برنامه
- `manifest.json`: تنظیمات نصب روی موبایل و دسکتاپ
- `sw.js`: سرویس‌ورکر برای کش فایل‌ها و پشتیبانی پایه از اجرای آفلاین
- `icons/`: آیکون‌های نصب برنامه

### انتشار روی وب
1. همه فایل‌ها و پوشه‌ها را با حفظ ساختار فعلی روی یک سرویس میزبانی وب استاتیک بارگذاری کنید.
2. میزبان باید از HTTPS پشتیبانی کند؛ اجرای مستقیم با `file://` برای نصب PWA کافی نیست.
3. پس از انتشار، سایت را در Chrome یا Edge باز کنید و نصب برنامه را آزمایش کنید. در iPhone، از منوی Share در Safari گزینه **Add to Home Screen** را بررسی کنید.

### نکات مهم پیش از انتشار عمومی
- برنامه از `localStorage` استفاده می‌کند؛ اطلاعات معمولاً فقط در همان مرورگر و دستگاه ذخیره می‌شوند. پاک‌کردن داده‌های مرورگر ممکن است آن‌ها را حذف کند. پیش از استفاده واقعی، خروجی گرفتن و بازیابی نسخه پشتیبان را آزمایش کنید.
- کتابخانه نمودار و فونت از CDNهای بیرونی بارگذاری می‌شوند؛ برای اجرای کاملاً آفلاین باید این منابع به‌صورت محلی میزبانی و دوباره آزمایش شوند.
- این بسته یک PWA قابل نصب است، نه فایل APK امضاشده و آماده انتشار در فروشگاه. برای Google Play باید نسخه اندرویدی (برای مثال با Trusted Web Activity/Bubblewrap یا Capacitor)، کلید امضا و آزمون‌های لازم آماده شوند.
- پیش از انتشار عمومی، حریم خصوصی، مجوزها، صحت محاسبات، پشتیبان‌گیری و عملکرد روی دستگاه‌های واقعی را بررسی کنید.

### بررسی فنی
- مطمئن شوید `index.html`، `manifest.json`، `sw.js` و آیکون‌ها از مسیرهای مورد انتظار در دسترس هستند.
- در Chrome DevTools، بخش **Application** را برای بررسی Manifest و Service Worker باز کنید.
- پس از تغییر فایل‌های برنامه، مقدار `CACHE_VERSION` را در `sw.js` افزایش دهید تا کش نسخه جدید به‌روزرسانی شود.

---

## English

### Package contents
- `index.html`: Main application file
- `manifest.json`: Installation metadata for mobile and desktop
- `sw.js`: Service worker for asset caching and basic offline support
- `icons/`: App installation icons

### Deploy to the web
1. Upload all files and folders to a static web host, preserving the existing directory structure.
2. The host must support HTTPS; opening the files directly with `file://` is not sufficient for PWA installation.
3. After deployment, open the site in Chrome or Edge and test installation. On iPhone, open the site in Safari, use the Share menu, and check **Add to Home Screen**.

### Important notes before public release
- The app uses `localStorage`; data generally stays in the same browser and on the same device. Clearing browser data may erase it. Test data export and backup restoration before real-world use.
- The chart library and font are loaded from external CDNs. Fully offline operation requires hosting these assets locally and testing again.
- This package is an installable PWA, not a signed APK ready for app-store submission. Publishing to Google Play requires an Android package (for example, using Trusted Web Activity/Bubblewrap or Capacitor), a signing key, and the required store testing and preparation.
- Before public release, review privacy, permissions, calculation accuracy, backups, and behavior on real devices.

### Technical checks
- Confirm that `index.html`, `manifest.json`, `sw.js`, and the icons are accessible at their expected paths.
- In Chrome DevTools, open **Application** to inspect the Manifest and Service Worker.
- After updating app files, increment `CACHE_VERSION` in `sw.js` so the cache can refresh to the new version.
