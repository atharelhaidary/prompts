## Prompt #1

الأصلي:
الكود ده فيه غلط صلحه.
الناقص الأول: المدخلات (الكود والإيرور مش موجودين، فمفيش حاجة تتصلح).

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: راجع الكود المرفق، حدد الخطأ، صلحه، وحافظ على الوظيفة الحالية.
المدخلات: الكود + الإيرور اللي بيظهر.
القيود:

- متغيرش الـ business logic إلا لو ضروري، ولو غيرته قولي فين.
- حافظ على الـ structure الحالي، ومتحذفش أي functionality من غير توضيح السبب.
- متغيرش أي logic في components تانية.
  المخرج بالترتيب:

1. سبب الغلط (بشكل بسيط).
2. الكود بعد الإصلاح.
3. شرح مختصر للتعديلات.
4. خطوات اختبار الحل.
   معيار النجاح: الخطأ يتصلح بالكامل وبطريقة صحيحة من غير أي تغيير في الـ UI behavior أو الـ logic.
   أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #2

الأصلي:
اعمل صفحة عرض المستخدمين
الناقص الأول: السياق (الـ Stack والـ structure، من غيرهم النموذج بيخمّن الإطار والـ DB).
الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اعمل صفحة لعرض المستخدمين في جدول، بنفس الـ feature-based structure بتاع المشروع. اسم الـ collection في MongoDB: `users`.
المدخلات: الاسم، البريد الإلكتروني، رقم الهاتف، الدور/الصلاحية، حالة الحساب.
القيود:

- استخدم Next API Routes (full stack) والـ API الموجود في المشروع.
- افصل الـ logic وجلب البيانات عن الـ UI.
- Responsive (موبايل / تابلت / ديسكتوب).
- أضف Loading / Error / Empty states.
  المخرج: Structure الملفات + مكان كل ملف، الكود الكامل للصفحة والـ components، طريقة جلب البيانات، خطوات الاختبار.
  معايير القبول:
- القائمة والبيانات تظهر بوضوح وبشكل صحيح.
- الصفحة Responsive.
- الـ Loading / Error / Empty states شغالين.
- مفيش TypeScript errors أو Console errors.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #3

الأصلي:
اعملي API كامل للمشروع.
الناقص الأول: المدخلات (الـ features والـ entities، من غيرهم مفيش "API كامل" يتحدد).

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: صمّم ونفّذ API كامل يغطي العمليات والبيانات الأساسية للتطبيق، بـ RESTful conventions، مع فصل الـ business logic عن الـ API handlers، وبشكل منظم وقابل للتوسع.
المدخلات: هبعتلك الـ features، الـ entities وبياناتها، الـ models لو موجودة، متطلبات الـ authentication/authorization، وأي API موجود حاليًا.
القيود:

- التزم بالـ architecture الحالي ومتضيفش dependencies إلا للضرورة.
- Validation على بيانات الطلب.
- Error handling موحد وResponse structure موحد.
- Authentication/Authorization على الـ protected endpoints.
- متكررش الـ business logic بين الـ endpoints.
  المخرج بالترتيب:

1. تصميم الـ API والـ endpoints.
2. Folder structure المقترح.
3. الـ database/models.
4. كود الـ API كاملًا.
5. Request/Response examples لكل endpoint.
6. طريقة التعامل مع auth.
7. طريقة اختبار الـ API.
   معايير القبول: كل feature لها endpoints واضحة بالـ HTTP method المناسب، فيه validation وerror handling موحد، والكود بدون TypeScript errors، والـ frontend يقدر يستهلكها بسهولة.
   أسئلة التوضيح: لو معلومات المشروع أو الـ entities أو الـ database مش كافية، اسألني الأول ومتفترضش تفاصيل أساسية.

==================================================================

## Prompt #4

الأصلي:
اكتبلي دالة تحسب موعد الزيارة الجاية.
الناقص الأول: المدخلات (الدالة تاخد إيه وتحسب منين؟ تاريخ آخر زيارة والـ interval ووحدته).
الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اكتب دالة `calculateNextVisit` تحسب موعد الزيارة القادمة.
المدخلات:

- `lastVisitDate`: تاريخ آخر زيارة.
- `interval`: عدد الأيام/الأسابيع/الشهور بين كل زيارة والتانية.
- `unit`: وحدة الـ interval (`day` / `week` / `month`).
  القيود:
- استخدم dayjs.
- بدون any.
- لو `lastVisitDate` مش تاريخ صحيح (رقم أو نص عشوائي) طلع alert error.
- لو `interval` مش رقم صحيح أكبر من صفر طلع alert error.
  أمثلة (Unit Tests / Usage):
- `{ lastVisitDate: "2026-09-30", interval: 10, unit: "day" }` ← `2026-10-10`
- `{ lastVisitDate: "2026-09-30", interval: 2, unit: "week" }` ← `2026-10-14`
- `{ lastVisitDate: "2026-09-30", interval: 3, unit: "month" }` ← `2026-12-30`
  المخرج: ازاي استخدم الدالة، الـ Validation والـ Error Handling، ومكان الدالة في أنهي folder.
  معيار القبول: الدالة تحسب الموعد القادم بشكل صحيح.
  أسئلة التوضيح: لو المعلومات مش كافية، اسألني الأول.

==================================================================

## Prompt #5

الأصلي:
خلّي قائمة الطلبات أسرع.
الناقص الأول: المدخلات (كود الـ JSX والـ fetching، من غيرهم الرد نصايح عامة).
الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: حدد سبب البطء في قائمة الطلبات (JSX ولا fetching ولا الـ API ولا MongoDB queries)، وحله من غير ما تغير الـ logic أو الـ UI behavior.
المدخلات: كود الـ JSX + كود الـ fetching من الـ endpoint.
القيود:

- حافظ على الـ responsive ومتحذفش أي function بتستخدمها الـ component.
- متعملش premature optimization.
- متضيفش useMemo / useCallback / React.memo إلا لو الكود محتاجهم فعلًا.
- لو فيه API request متكرر، اعمل له reusable function.
  المخرج:
- سبب البطء في أنهي ملف.
- هل السبب: UI، React Query، API، ولا MongoDB queries؟
- الحل بعد التعديل.
  معيار القبول: استخدام القائمة يبقى سريع.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول ومتفترضش.

==================================================================

## Prompt #6

الأصلي:
ليه الإشعار مش بيوصل للفني
الناقص الأول: المدخلات (كود الإشعارات والـ fetching، من غيرهم التشخيص تخمين).

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: حدد ليه الإشعار مش بيوصل للفني أو مش بيظهرله. لو مش شايف المشكلة من الـ frontend، اسألني عن الحاجات اللي محتاج تتأكد منها في الـ backend وأنا أجاوبك.
المدخلات: كود الـ JSX + كود الإشعارات + كود الـ fetching من الـ API.
القيود: متغيرش الـ logic ولا الـ UI behavior.
المخرج: سبب المشكلة، مكانها في الكود، والفرق بين كودي والكود المعدل.
معيار القبول: الإشعار يوصل للفني ويظهرله فورًا في نفس وقت الـ create في الـ backend.
أسئلة التوضيح: لو المعلومات مش كافية، اسألني الأول ومتفترضش.

==================================================================

## Prompt #7

الأصلي:
اكتب query يجيب الطلبات المتأخرة
الناقص الأول: السياق (قاعدة البيانات والحقول، "query" ممكن تبقى SQL أو Mongo أو React Query).

الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اكتب Query تجيب كل طلبات الصيانة المتأخرة.
حقول الطلب: رقم الطلب، اسم الشركة، اسم الفني، حالة الطلب، الأولوية، نوع الصيانة، موعد الزيارة، تاريخ إنشاء الطلب.
الحالات: جديد، قيد الانتظار، قيد التنفيذ، مكتمل، ملغي.
الطلب المتأخر = موعد الزيارة في الماضي + الحالة مش مكتمل ولا ملغي.
المخرج: كود + مثال استخدام يوضح بيشتغل ازاي.
أسئلة التوضيح: لو المعلومات مش كافية، اسألني الأول ومتفترضش.

==================================================================

## Prompt #8

الأصلي:
ترجم رسايل الحالة
الناقص الأول: المدخلات (الرسائل نفسها وملفات الترجمة الحالية، من غيرهم مفيش حاجة تتترجم).
الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: ترجم رسائل الحالة الموجودة في المشروع للعربية والإنجليزية.
المدخلات: كود الـ JSX + ملفات الترجمة.
القيود: متغيرش الـ logic ولا الـ UI behavior، واعمل translation keys واضحة.
المخرج: الترجمة عربي وإنجليزي بنفس structure ملفات الترجمة الموجودة.
معيار القبول: رسائل الحالة مترجمة بشكل صحيح.
أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.

==================================================================

## Prompt #9

الأصلي:
اشرح الـ queues
الناقص الأول: السياق (قصدك Queue كـ data structure ولا Job Queue زي BullMQ؟ ومستواك إيه؟).
الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اشرح الـ Queues بطريقة بسيطة وواضحة، بالأساسيات من غير تفاصيل معقدة ملهاش لازمة، مع أمثلة كود بسيطة.
المخرج بالترتيب:

1. ما هي Queue؟
2. ازاي بتشتغل؟
3. أهم العمليات عليها.
4. مثال بسيط بالكود.
5. مثال عملي في مشروعي.
6. الفرق بينها وبين Stack.
   معيار القبول: أفهم فكرة الـ Queue، وامتى وليه أستخدمها في مشروعي.

==================================================================

## Prompt #10

الأصلي:
اعمل صفحة تسجيل طلب صيانة
الناقص الأول: المدخلات (الحقول اللي الفورم هتاخدها).
الدور: أنا Mid Level Frontend React/Next Developer.
السياق: Next.js, React, TypeScript (بدون any), Tailwind CSS, React Query, Next API Routes, MongoDB، بـ Feature-Based Architecture.
المهمة: اعمل صفحة لتسجيل طلب صيانة جديد.
المدخلات: العميل، الجهاز/الأصل، وصف المشكلة، الأولوية، نوع الصيانة، موعد الزيارة، الملاحظات، المرفقات.
القيود:

- React Hook Form + Zod للـ validation.
- Responsive.
- ترجمة عربي/إنجليزي.
- متغيرش الـ project architecture.
  المخرج: تصميم الصفحة، Form Component، Validation Schema، Submit Handler، ومثال على البيانات المرسلة للـ API.
  معيار القبول: اليوزر يسجل الطلب بسهولة؛ لو نجح يظهر alert إن الطلب اتسجل، ولو فشل يظهر error ويوضح مكان الخطأ.
  أسئلة التوضيح: لو المعلومات أو الملفات مش كافية، اسألني الأول.
