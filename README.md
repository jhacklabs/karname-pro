# کارنامه Pro — بسته انتشار وب و موبایل (PWA)
# Karnameh Pro — Web & Mobile Release Package (PWA)

---

## فارسی

### محتویات بسته
- `index.html`: فایل اصلی برنامه
- `manifest.json`: تنظیمات نصب روی موبایل و دسکتاپ
- `sw.js`: سرویس‌ورکر برای کش فایل‌ها و پشتیبانی پایه از اجرای آفلاین
- `icons/`: آیکون‌های نصب برنامه
### نحوه استفاده
برای استفاده میتوانید از لینک در فایل ریدمی و همچنین از بخش ریلیز استفاده کنید و یا اینکه فایل index.html را در مرورگر خود باز کنید 
## شوند.
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
### How to Use
To use it, you can follow the link provided in the README file, check the Releases section, or simply open the `index.html` file in your browser.

### Deploy to the web
1. Upload all files and folders to a static web host, preserving the existing directory structure.
2. The host must support HTTPS; opening the files directly with `file://` is not sufficient for PWA installation.
3. After deployment, open the site in Chrome or Edge and test installation. On iPhone, open the site in Safari, use the Share menu, and check **Add to Home Screen**.


### Technical checks
- Confirm that `index.html`, `manifest.json`, `sw.js`, and the icons are accessible at their expected paths.
- In Chrome DevTools, open **Application** to inspect the Manifest and Service Worker.
- After updating app files, increment `CACHE_VERSION` in `sw.js` so the cache can refresh to the new version.
