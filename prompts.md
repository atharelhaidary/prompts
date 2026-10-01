## Prompt #1

الأصلي:
تسجيل الدخول والصلاحيات (Auth)

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اعمل نظام تسجيل دخول بـ [NextAuth / JWT مخصص] مع أدوار المستخدمين.
المدخلات:

- الأدوار: [مثال: admin, technician, customer].
- حقول الدخول: [مثال: البريد + كلمة المرور].
  القيود:
- كلمة المرور تتخزن مشفّرة (hashed).
- الـ token أو الـ session يتخزن في httpOnly cookie.
- Validation على المدخلات (Zod).
- Error messages موحدة وواضحة.
- التزم بالـ feature-based structure ومتضيفش dependencies إلا للضرورة.
  المخرج: Structure الملفات، الـ API routes، صفحة الدخول، helper لقراءة المستخدم الحالي، وخطوات الاختبار.
  معيار القبول: اليوزر يسجل دخول ويطلع، والدور بيوصل للـ frontend، ومفيش بيانات حساسة بترجع في الـ response.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #2

الأصلي:
حماية الـ routes حسب الدور

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: احمي الـ routes اللي تحت [مثال: /dashboard] بحيث كل دور يدخل على صفحاته بس.
المدخلات: [جدول: الدور ← الصفحات المسموحة] + [طريقة الـ auth الحالية].
القيود:

- استخدم middleware (أو proxy حسب الإصدار) للتوجيه السريع.
- اتحقق من الصلاحية كمان جوه الـ API handlers والـ data layer، مش في الـ middleware بس.
- لو اليوزر مش مسجل دخول وجّهه لصفحة الدخول.
- لو مسجل بس مش مسموح له اعرض صفحة 403.
  المخرج: كود الحماية، helper للتحقق من الدور، مثال على protected API route، وخطوات الاختبار لكل دور.
  معيار القبول: مفيش دور يقدر يفتح صفحة أو يندهل API مش من صلاحياته.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #3

الأصلي:
بحث وفلترة و Pagination لقائمة الطلبات

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: ضيف بحث وفلترة وـ pagination لقائمة طلبات الصيانة.
المدخلات:

- البحث: [رقم الطلب / اسم الشركة / اسم الفني].
- الفلاتر: الحالة، الأولوية، نوع الصيانة، نطاق موعد الزيارة.
- حجم الصفحة: [مثال: 10 / 20 / 50].
  القيود:
- خزّن الفلاتر في الـ URL search params عشان الرابط يتشارك.
- Debounce للبحث.
- الفلترة والـ pagination تتم في MongoDB query (مش في الـ frontend).
- الـ React Query keys تتغير مع الفلاتر.
- متغيرش الـ UI الحالي إلا بالإضافات المطلوبة، وحافظ على الـ responsive.
  المخرج: تعديلات الـ API، الـ hook، مكوّنات الفلاتر والـ pagination، وخطوات الاختبار.
  معيار القبول: الفلاتر والبحث بيشتغلوا مع بعض، والـ refresh بيحافظ على الحالة، ومفيش طلبات زيادة.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #4

الأصلي:
لوحة إحصائيات (Dashboard)

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اعمل صفحة Dashboard لطلبات الصيانة فيها كروت إحصائيات ورسوم بيانية.
المدخلات:

- الكروت: إجمالي الطلبات، المتأخرة، قيد التنفيذ، المكتملة هذا الشهر.
- الرسوم: [الطلبات حسب الحالة (Pie)] + [الطلبات حسب الأسبوع (Bar/Line)].
  القيود:
- استخدم [Recharts] لو محتاج مكتبة رسوم.
- الحسابات تتم في MongoDB aggregation مش في الـ frontend.
- Responsive، مع Loading skeleton وError وEmpty states.
- ترجمة عربي/إنجليزي.
  المخرج: الـ aggregation queries، الـ API route، الـ hooks، الـ components، وخطوات الاختبار.
  معيار القبول: الأرقام مطابقة للبيانات الفعلية، والصفحة سريعة، والرسوم مقروءة على الموبايل.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #5

الأصلي:
رفع مرفقات الطلب

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اعمل رفع مرفقات (صور / PDF) لطلب الصيانة، مع عرضها وحذفها.
المدخلات:

- الأنواع المسموحة: [jpg, png, pdf].
- الحجم الأقصى: [مثال: 5MB للملف، 5 ملفات للطلب].
- مكان التخزين: [Cloudinary / S3 / local].
  القيود:
- اتحقق من النوع والحجم في الـ frontend والـ backend.
- معاينة (preview) للصور قبل الرفع، وـ progress bar.
- متخزنش الملف في MongoDB، خزّن الرابط والـ metadata بس.
- Responsive وبدون any.
  المخرج: الـ API route، الـ upload hook، المكوّن، شكل البيانات في الـ model، وخطوات الاختبار.
  معيار القبول: الرفع والعرض والحذف شغالين، وملف غلط النوع أو الحجم بيترفض برسالة واضحة.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #6

الأصلي:
صفحات الـ Loading والـ Error والـ Not Found

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: ضيف loading.tsx وerror.tsx وnot-found.tsx للـ routes الأساسية بشكل متسق.
المدخلات: [قائمة الـ routes] + [الـ design tokens أو الألوان لو فيه].
القيود:

- error.tsx لازم يكون Client Component وفيه زر "حاول مرة تانية" (reset).
- Skeleton في الـ loading يطابق شكل الصفحة.
- رسائل عربي/إنجليزي.
- متغيرش الـ logic الحالي.
  المخرج: الملفات لكل route، ومكوّنات مشتركة (ErrorState, PageSkeleton)، وإزاي أختبر كل حالة.
  معيار القبول: أي error أو route غلط يظهر صفحة واضحة بدل شاشة بيضا.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #7

الأصلي:
Dark Mode

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: ضيف Dark Mode (light / dark / system) للمشروع.
المدخلات: [نسخة Tailwind] + [الألوان الحالية].
القيود:

- بدون وميض (flash) عند أول تحميل.
- الاختيار يتحفظ بين الزيارات.
- متغيرش الـ UI behavior، وحافظ على التباين (contrast) مقروء.
- متضيفش مكتبة إلا لو ضرورية، ولو أضفت [next-themes] وضّح ليه.
  المخرج: إعدادات Tailwind، الـ provider، زر التبديل، مثال تعديل component، وخطوات الاختبار.
  معيار القبول: التبديل شغال في كل الصفحات من غير hydration warnings.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #8

الأصلي:
راجعة كود Refactor

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: راجع الكود المرفق وقولي المشاكل مرتبة بالأهمية، وبعدين اعمل refactor.
المدخلات: [الكود] + [الـ feature اللي تبعه].
القيود:

- متغيرش السلوك الحالي (logic / UI behavior).
- اقترح بس، وفرّق بين "لازم" و"تحسين اختياري".
- متعملش premature optimization.
- لو هتنقل ملفات، وضّح الـ structure الجديد.
  المخرج بالترتيب:

1. ملخص المشاكل (أمان / أخطاء محتملة / قراءة وصيانة / أداء).
2. الكود بعد الـ refactor.
3. إيه اللي اتغير وليه.
4. إزاي أتأكد إن السلوك لسه زي ما هو.
   معيار القبول: الكود أنضف وأسهل في الصيانة من غير أي regression.
   أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #9

الأصلي:
إشعارات لحظية للفني

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اعمل نظام إشعارات للفني لما يتعمل له طلب جديد، مع عداد غير مقروء وصفحة الإشعارات.
المدخلات:

- أنواع الإشعارات: [طلب جديد / تغيير حالة / تأخير].
- أسلوب التحديث: [Polling كل X ثانية / SSE]، واشرحلي الفرق واختار الأنسب.
  القيود:
- لو Polling، استخدم refetchInterval في React Query.
- "تحديد كمقروء" بـ optimistic update.
- Responsive وترجمة عربي/إنجليزي.
- ملحوظة: لو هتنشر على Vercel، وضّح محدودية WebSockets/SSE.
  المخرج: Notification model، الـ API routes، الـ hooks، المكوّنات (جرس + قائمة)، وخطوات الاختبار.
  معيار القبول: الفني يشوف الإشعار في خلال [X] ثانية من إنشاء الطلب، والعداد بيتحدث صح.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #10

الأصلي:
كتابة Tests لـ Component

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js [رقم الإصدار] (App Router), React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اكتب tests للـ component أو الـ hook ده.
المدخلات: [الكود] + [الحالات المهمة اللي عايزة أتأكد منها].
القيود:

- استخدم [Vitest أو Jest] + React Testing Library.
- اختبر السلوك اللي اليوزر بيشوفه، مش تفاصيل التنفيذ.
- اعمل mock للـ API (مثلًا MSW) ولـ React Query provider.
- غطي: الحالة العادية، Loading، Error، Empty.
- بدون any.
  المخرج: ملفات الـ test، الـ setup المطلوب، أمر التشغيل، وإيه اللي مش مغطى.
  معيار القبول: الـ tests بتعدي، وبتفشل لو السلوك اتكسر.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.
