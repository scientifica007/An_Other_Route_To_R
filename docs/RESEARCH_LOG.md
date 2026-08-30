# RESEARCH LOG

سجل زمني للعمل البحثي. تُوثق فيه الأفكار والاختبارات والنتائج الإيجابية والسلبية وما تعلمناه منها.

---

## 2026-08-30 — تأسيس المشروع وصياغة السؤال

### السؤال الأولي

بدأت الدراسة من سؤال عام حول إمكان الانتقال إلى الأعداد الحقيقية بآلية مرتبطة بالتكرار أو التراكم، ثم أعيد ضبط السؤال كي لا يعتمد على تعريفات خاصة من مشروعات أخرى.

### إعادة الصياغة المعتمدة

السؤال الحالي هو:

> كيف يمكن الوصول إلى الأعداد الحقيقية بطريق أو طرق مختلفة عن ديدكاند وكوشي؟

### ملاحظة تأسيسية

الهدف ليس مجرد إيجاد صيغة أخرى لتمثيل عدد حقيقي معروف، بل دراسة آليات بناء بديلة فعلاً لبنية تماثل \(\mathbb{R}\).

### نتائج أولية من النقاش

1. توجد طرق معروفة متعددة لا تتخذ Dedekind cuts أو Cauchy sequences بوصفها الكائن البدائي.
2. من أبرز المرشحين للمقارنة:
   - digit expansions؛
   - continued fractions؛
   - nested intervals؛
   - classical Eudoxus ratios؛
   - modern Eudoxus reals via almost homomorphisms;
   - hyperrational/nonstandard quotient constructions؛
   - surreal constructions.
3. مجرد استعمال عملية لا نهائية لا يعني أن البناء مختلف عن كوشي؛ يجب تحليل البنية الداخلية لا المصطلحات.
4. هناك عائق عددي أساسي: \(\mathbb{Q}\) معدودة و\(\mathbb{R}\) غير معدودة، ولذلك يلزم في أي بناء كامل مصدر للمعلومات اللانهائية أو بنية تعطي قوة continuum.
5. Modern Eudoxus reals بدت ذات أهمية خاصة لأنها تستخرج السلوك الحقيقي من دوال صحيحة إلى صحيحة ذات defect جمعي محدود، modulo bounded functions، بدل اتخاذ متتالية تقارب كائنًا أوليًا.

### قرار البحث التالي

مقارنة ثلاثة مسارات بصورة صارمة قبل ابتكار مسار جديد:

- Continued Fractions.
- Classical Eudoxus Ratios.
- Modern Eudoxus Reals.

### سؤال المقارنة الحاكم

> ما الشيء الذي يحول بيانات صحيحة/منفصلة أو تكرارات صحيحة إلى معلومة كافية لتحديد عنصر من \(\mathbb{R}\)؟

### حالة الجدة

لا يوجد في هذه المرحلة أي ادعاء بالجدة. المرحلة الحالية استكشافية وتأسيسية.

---

## 2026-08-30 — المراجعة الأولى للأدبيات العلمية

### الهدف

البحث في المجلات العلمية والأدبيات عن محاولات فعلية لبناء \(\mathbb{R}\) خارج قطوع ديدكاند ومتتاليات كوشي، وتصنيفها بحسب استقلالها التأسيسي لا بحسب اختلاف التسمية فقط.

### المرجع المسحي المركزي

تم اعتماد Ittay Weiss (2015), **The real numbers – A survey of constructions**, *Rocky Mountain Journal of Mathematics* 45(3), 737–762، بوصفه خريطة الأدبيات الأساسية حتى 2015. الورقة تجمع معظم/كل البناءات المعروفة آنذاك من \(\mathbb{Q}\) أو \(\mathbb{Z}\).

### النتائج الرئيسة

1. توجد بالفعل عائلة واسعة من البناءات البديلة، وليس ديدكاند وكوشي إلا أشهرها تعليميًا.
2. أقوى عائلة بالنسبة إلى هدف المشروع هي Eudoxus/Schanuel/Street/near-endomorphisms: بناء مباشر من \(\mathbb{Z}\) بواسطة دوال شبه جمعية ذات defect محدود modulo bounded difference.
3. تؤكد أعمال Grundhöfer (2005)، A’Campo (2021)، formalization لـ Keskin (2023)، وKionke (2019) أن هذا المسار ليس مجرد ملاحظة قديمة معزولة؛ له امتدادات حديثة وتعميمات إلى completion of fields via quasimorphisms.
4. de Bruijn (1976) بنى reals دون استعمال rationals كمرحلة سابقة، بواسطة additive/digit expansions.
5. Faltin–Metropolis–Ross–Rota (1975) أعطوا بناء strings/formal Laurent series modulo carry relations.
6. Rieger (1982) بنى نموذجًا انطلاقًا من continued fractions؛ لكنه يستعمل rational truncations وsuprema لاسترجاع arithmetic، لذلك هو بديل معتبر لا استقلال مطلق عن فكرة الإكمال.
7. Shiu (1974) استعمل equivalence classes of sets of naturals/harmonic subseries، لكن علاقة التكافؤ تعتمد على null sequences؛ لذا يحتفظ بنكهة Cauchy واضحة.
8. Knopfmacher & Knopfmacher طوّرا عدة بناءات عبر infinite products، Engel/Sylvester series وalternating series (1987–1989)، وتوجد تعميمات لاحقة مثل SEL-series model (2014).
9. domain-theoretic constructions تجعل reals maximal elements of interval domains؛ مهمة حاسوبيًا وبنائيًا، لكنها قريبة من nested-approximation/completion logic.
10. ultrafilter/nonstandard constructions تعطي مسارًا مختلفًا، لكنه أثقل منطقيا ونظريًا؛ توجد formal verification حديثة منشورة في 2025.
11. abstractionist approaches (Hale 2000) وPanza 2026 تدرس ratios of magnitudes وbicimal developments من زاوية تأسيسية/إبستيمية، لكنها تحتاج تحليلًا منفصلًا قبل عدها بدائل مباشرة من \(\mathbb{N}\)/\(\mathbb{Z}\).
12. Bachmann nested intervals وBourbaki Cauchy filters لا تعد بدائل قوية وفق معيارنا؛ Maier–Maier essentially Dedekind; وArthan 2001 يستعمل Dedekind cuts صراحة رغم تغيير المسار الوسيط.

### نتيجة بحث سلبية مؤقتة

بحث موجه عن **integration-first construction** لم يكشف في هذه الجولة عن بناء راسخ يجعل التكامل أو Riemann accumulation هو العملية التأسيسية التي تنشئ \(\mathbb{R}\) من \(\mathbb{N}\)، \(\mathbb{Z}\)، أو \(\mathbb{Q}\). عادةً يظهر التكامل بعد افتراض بنية حقيقية مكتملة أو أدوات equivalent مثل suprema.

هذه ليست مبرهنة عدم وجود؛ إنها نتيجة بحث أولية يجب إبقاؤها مفتوحة.

### الوثيقة الناتجة

تم إنشاء:

- `docs/LITERATURE_REVIEW_2026-08-30.md`

وتحتوي على التصنيف والمراجع والـDOIs وترتيب الأولويات.

### قرار المرحلة التالية

قبل ابتكار أي طريق جديد، نفكك **Eudoxus/near-endomorphism construction** تفكيكًا تأسيسيًا كاملًا، ثم نكرر المنهج على Rieger وde Bruijn/FMRR.
