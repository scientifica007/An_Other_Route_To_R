# مراجعة أدبيات: طرق بناء الأعداد الحقيقية خارج ديدكاند وكوشي

**تاريخ المراجعة:** 2026-08-30  
**حالة الوثيقة:** خريطة أدبيات أولية موسعة؛ قابلة للتحديث.  
**سؤال المشروع:** ما الطرق المعروفة لبناء بنية مكافئة لـ \(\mathbb{R}\) دون اتخاذ قطوع ديدكاند أو متتاليات كوشي بوصفها الكائن البدائي؟

---

## 1. المرجع المسحي المركزي

أهم نقطة انطلاق وجدناها هي:

- Ittay Weiss, **“The real numbers – A survey of constructions”**, *Rocky Mountain Journal of Mathematics*, 45(3), 737–762 (2015). DOI: `10.1216/RMJ-2015-45-3-737`.

الورقة تعلن صراحة أنها تجمع معظم، إن لم يكن كل، البناءات المعروفة في الأدبيات حتى وقتها، سواء المنطلقة من \(\mathbb{Q}\) أو من \(\mathbb{Z}\). وهي مرجع المقارنة الأساسي للمشروع، لكن يلزم استكمالها بأعمال لاحقة على 2015.

القاعدة المقارنة التي تتبناها الورقة مفيدة لنا: يختار كل بناء مجموعة من الكائنات الأبسط التي تقابل الأعداد الحقيقية، ثم يعرّف الترتيب والعمليات ويثبت أن الناتج حقل مرتب كامل.

---

## 2. معيارنا لتصنيف «البديل»

لا يكفي اختلاف الشكل الخارجي. سنستعمل ثلاث درجات:

### A — بديل تأسيسي قوي
الكائن البدائي ليس cut ولا Cauchy sequence/filter/nest، وآلية تحديد العدد مختلفة بنيويًا.

### B — بديل تمثيلي/إنشائي معتبر
لا يستعمل كوشي أو ديدكاند مباشرة، لكنه يستعيد العمليات أو الاكتمال بواسطة تقريبات، suprema، أو آليات قريبة من الإكمال التقليدي.

### C — اختلاف شكلي أو فرع من البناءين القياسيين
الطريقة تعود بصورة واضحة إلى قطع ديدكاند أو إكمال كوشي، حتى إن اختلفت اللغة.

هذا تصنيف تحليلي خاص بالمشروع، وليس تصنيفًا رسميًا في الأدبيات.

---

## 3. المسارات ذات الاستقلال البنيوي الأقوى

### 3.1. Eudoxus / Schanuel / Street / near-endomorphisms of \(\mathbb{Z}\)

**الفكرة:** البدء مباشرة من المجموعة الجمعية للأعداد الصحيحة، لا من \(\mathbb{Q}\). الكائنات الأساسية هي دوال

\[
f:\mathbb{Z}\to\mathbb{Z}
\]

ذات عيب جمعي محدود:

\[
f(m+n)-f(m)-f(n)
\]

يبقى ضمن مجموعة محدودة. ثم نأخذ هذه الدوال modulo الفرق المحدود. الناتج يمكن تنظيمه كحقل مرتب كامل مماثل لـ \(\mathbb{R}\).

**المراجع الرئيسة:**

- Ross Street, **“An efficient construction of the real numbers”**, *Gazette of the Australian Mathematical Society* 12 (1985), 57–58.
- R. D. Arthan, **“The Eudoxus Real Numbers”** (2004), arXiv:`math/0405454`. يصرح بأنه بناء يعود إلى Stephen Schanuel وينتقل مباشرة من \(\mathbb{Z}\) إلى \(\mathbb{R}\)، متجاوزًا \(\mathbb{Q}\).
- Theo Grundhöfer, **“Describing the real numbers in terms of integers”**, *Archiv der Mathematik* 85(1) (2005), 79–81. DOI: `10.1007/s00013-005-1413-z`.
- Norbert A’Campo, **“A natural construction for the real numbers”**, *Elemente der Mathematik* 76(3) (2021), 89–105. DOI: `10.4171/EM/455`. يبني النظام مباشرة فوق المجموعة الجمعية لـ \(\mathbb{Z}\)، مع جذور مفهومية في rotation number لبوانكاريه.
- Ata Keskin, **“Eudoxus Reals”**, *Archive of Formal Proofs* (2023): formalization in Isabelle/HOL.
- A. J. Kumar, Reese Long, Andrew Tung, Ivan Wong, **“The Eudoxus Reals”** (2023), arXiv:`2310.04534`: يعيد تطوير near-endomorphism construction ويدرس تعميمه إلى مجموعات أبيلية أخرى.
- Steffen Kionke, **“Constructing the Completion of a Field Using Quasimorphisms”**, *p-Adic Numbers, Ultrametric Analysis and Applications* 11(4) (2019), 335–337. DOI: `10.1134/S2070046619040083`. يحول فكرة quasimorphism إلى طريقة عامة لبناء completion لحقل بالنسبة إلى قيمة مطلقة.

**تقييم المشروع:** A. هذا أقوى مسار معروف حاليًا من حيث اختلاف الكائن البدائي. لا يُعرّف العدد الحقيقي كـ«قيمة حد لمتتالية نسبية»، بل كسلوك كبير المقياس لدالة صحيحة إلى صحيحة modulo خطأ محدود.

**ملاحظة حاسمة:** عمل Kionke يبين أيضًا أن هذه الفكرة ليست مجرد حيلة خاصة بـ \(\mathbb{R}\)، بل يمكن تفسيرها كآلية completion أعم. هذا مهم لتحديد ما إذا كانت الجدة بنيوية أو مجرد تمثيل مختلف لعملية الإكمال.

---

### 3.2. de Bruijn: بناء الأعداد الحقيقية دون استعمال النسبية

- N. G. de Bruijn, **“Defining reals without the use of rationals”**, *Indagationes Mathematicae (Proceedings)* 79(2) (1976), 100–108. DOI: `10.1016/1385-7258(76)90055-X`.

يعتمد على توسعات رقمية/additive expansions مباشرة، مع معالجة العمليات والترتيب على السلاسل بدل المرور أولًا بحقل \(\mathbb{Q}\).

**تقييم المشروع:** A/B. مستقل فعليًا عن بناء \(\mathbb{Q}\) كمرحلة وسيطة، لكنه ينتمي إلى عائلة digit/expansion constructions، وقد تحتاج بعض أجزاء الحساب إلى مبادئ اكتمال أو suprema بعد بناء الترتيب.

---

### 3.3. Faltin–Metropolis–Ross–Rota: الأعداد الحقيقية بوصفها wreath product / strings

- F. Faltin, N. Metropolis, B. Ross, G.-C. Rota, **“The real numbers as a wreath product”**, *Advances in Mathematics* 16(3) (1975), 278–304. DOI: `10.1016/0001-8708(75)90115-2`.

الفكرة هي السماح بمعاملات صحيحة غير مقيدة في سلاسل شبيهة بـ formal Laurent series، ثم quotient بعلاقات carry. تصبح عمليتا الجمع والضرب شبيهتين بحساب السلاسل الشكلية، بينما تنتقل الصعوبة إلى تعريف الترتيب والتعامل مع carrying.

**تقييم المشروع:** A/B. بناء جبري/ترميزي مختلف بوضوح عن cut وCauchy، ويستحق الدراسة باعتباره مثالًا على أن «التراكم الرقمي» يمكن تنظيمه algebraically قبل فرض الترتيب.

---

### 3.4. Rieger: الكسور المستمرة كأساس لبناء \(\mathbb{R}\)

- G. J. Rieger, **“A new approach to the real numbers (motivated by continued fractions)”**, *Abhandlungen der Braunschweigischen Wissenschaftlichen Gesellschaft* 33 (1982), 205–217.

العدد يمثَّل بتوسع continued fraction: النسبي ينتهي، وغير النسبي يستمر بلا نهاية. يعاد تعريف الترتيب من بنية partial quotients، ثم تثبت خاصية least upper bound، وبعد ذلك تستعاد العمليات باستعمال التقريبات النسبية/truncations.

**تقييم المشروع:** B قوي. الكائن البدائي مختلف عن متتالية كوشي، والتمييز finite/infinite بين \(\mathbb{Q}\) واللاعقلانيات واضح جدًا؛ لكن استعادة الحساب تستعمل approximants وsuprema، ولذلك يجب ألا نصفه بأنه مستقل تمامًا عن فكرة الإكمال.

---

## 4. عائلة السلاسل والمنتجات اللانهائية

هذه العائلة مهمة لأنها تثبت أن طرقًا كثيرة جدًا يمكن أن تولد complete ordered field من تمثيلات لانهائية لا تعتمد على base ثابت ولا على Cauchy equivalence classes.

### 4.1. Shiu — subsets of natural numbers / harmonic subseries

- P. Shiu, **“A new construction of the real numbers”**, *The Mathematical Gazette* 58(403) (1974), 39–46. DOI: `10.2307/3615477`.

يعرّف العدد الحقيقي الموجب بوصفه صنف تكافؤ لمجموعات لا نهائية من الأعداد الطبيعية، بالاستفادة من subseries للسلسلة التوافقية. لكن علاقة التكافؤ نفسها تستعمل أن فرق partial sums هو null sequence.

**تقييم المشروع:** B/C. الشكل جديد، لكن أثر كوشي/التقارب موجود داخل علاقة التكافؤ؛ لذا لا نعده انفصالًا تأسيسيًا قويًا.

### 4.2. Knopfmacher & Knopfmacher — infinite products

- Arnold Knopfmacher & John Knopfmacher, **“A new construction of the real numbers (via infinite products)”**, *Nieuw Archief voor Wiskunde* (4) 5 (1987), 19–31.

بناء يستفيد من infinite product representations.

**تقييم المشروع:** B.

### 4.3. Engel and Sylvester series

- Arnold Knopfmacher & John Knopfmacher, **“Two concrete new constructions of the real numbers”**, *Rocky Mountain Journal of Mathematics* 18(4) (1988), 813–824. DOI: `10.1216/RMJ-1988-18-4-813`.

الورقة تقدم بناءين للحقل المرتب الكامل انطلاقًا من \(\mathbb{Q}\)، مستلهمين من Engel وSylvester series، وتؤكد أنهما لا يحتاجان اختيار base اعتباطي ولا equivalence classes.

**تقييم المشروع:** B قوي.

### 4.4. Alternating Engel / Sylvester

- Arnold Knopfmacher & John Knopfmacher, **“Two constructions of the real numbers via alternating series”**, *International Journal of Mathematics and Mathematical Sciences* 12(3) (1989), 603–613. DOI: `10.1155/S0161171289000736`.

بناءان إضافيان من سلاسل نسبية متناوبة، مع تشابه معلن مع طريقة Rieger.

**تقييم المشروع:** B قوي.

### 4.5. Pintilie

- Alexandru Pintilie, **“A Construction without factorization for the Real Numbers”**, *Libertas Mathematica* 8 (1988), 155–160.

ينتمي إلى عائلة infinite-series/subseries constructions.

**تقييم المشروع:** B، قريب مفهوميًا من Shiu.

### 4.6. تعميم حديث نسبيًا

- Patiwat Singthongla & Narakorn Rompurk Kanasri, **“SEL Series Expansion and Generalized Model Construction for the Real Number System via Series of Rationals”**, *International Journal of Mathematics and Mathematical Sciences* (2014), Article 654319. DOI: `10.1155/2014/654319`.

يعطي خوارزمية توسع تعمم Sylvester وEngel وLüroth، ويستعمل series of rationals لبناء نموذج معمم للنظام الحقيقي.

**تقييم المشروع:** B. دليل مهم على أن expansion-based construction ليس حادثة تاريخية معزولة بل عائلة قابلة للتعميم.

---

## 5. التوسعات العشرية/الثنائية بوصفها بناءً مستقلاً

التوسعات الرقمية أقدم حدسيًا من ديدكاند وكوشي، لكن المشكلة ليست التمثيل بل تعريف العمليات بدقة والتعامل مع التمثيلات المزدوجة والحمل.

- Weiss (2015) يضع Stevin expansions ضمن خريطة البناءات، مع التنبيه إلى الصعوبات التقنية في arithmetic.
- Martin Klazar, **“Rethinking real numbers as infinite decimals”** (2021), arXiv:`2108.02046`: يعطي بناءً تفصيليًا للحقل المرتب الكامل باستعمال infinite decimal expansions ويدرس قابلية حساب الجمع والضرب في الترميز القانوني.
- Marco Panza, **Reals by Abstraction. An Inquiry about Epistemic Economy in Mathematics: Volume II — The Real Numbers**, Springer, Synthese Library 523 (2026), DOI: `10.1007/978-3-032-00431-4`. يقارن domain extension وratios of magnitudes ويقترح تعريفًا حديثًا بـ bicimal developments/pairs.

**تقييم المشروع:** B، مع أهمية خاصة لـ Panza (2026) لأنه أحدث مصدر وجدناه وينظر صراحةً في الاقتصاد التأسيسي لطرق تعريف \(\mathbb{R}\).

---

## 6. Domain theory / interval domain

هناك خط مختلف في الرياضيات البنائية والحساب الدقيق:

- Andrej Bauer & Iztok Kavkler, **“Implementing Real Numbers With RZ”**, *Electronic Notes in Theoretical Computer Science* 202 (2008), 365–384. DOI: `10.1016/j.entcs.2008.03.027`.
- Andrej Bauer & Iztok Kavkler, **“A constructive theory of continuous domains suitable for implementation”**, *Annals of Pure and Applied Logic* 159(3) (2009), 251–267. DOI: `10.1016/j.apal.2008.09.025`.

في interval-domain approach تظهر الأعداد الحقيقية كـ maximal elements في domain من intervals/approximations.

**تقييم المشروع:** B/C بحسب معيار الاستقلال. لغة order/domain مختلفة ومهمة جدًا للحوسبة، لكن جوهر «تضييق التقريب إلى نقطة» قريب من nested intervals/completion، ولذلك لا ينبغي عده تلقائيًا طريقًا تأسيسيًا مستقلًا عن كوشي.

---

## 7. Nonstandard / ultrafilter constructions

يمكن بناء hyperrationals من متتاليات نسبية modulo ultrafilter، ثم أخذ العناصر المحدودة modulo infinitesimals للحصول على حقل مماثل لـ \(\mathbb{R}\).

مثال حديث على formal verification لمسار من هذه العائلة:

- Guowei Dou & Wensheng Yu, **“A Machine Proof of the Filter-Method Construction for Real Numbers”**, *Mathematics* 13(17) (2025), 2707. DOI: `10.3390/math13172707`.

يبني \(^*\mathbb{N}, ^*\mathbb{Z}, ^*\mathbb{Q}\) باستخدام non-principal arithmetical ultrafilter ثم يحصل على \(\mathbb{R}\) بواسطة quotient لمجموعة جزئية من \(^*\mathbb{Q}\).

**تقييم المشروع:** A من حيث اختلاف الآلية، لكن بتكلفة منطقية/نظرية مجموعات مرتفعة، ولذلك ليس مرشحنا الأول لمسار «بسيط» أو «اقتصادي».

---

## 8. Reals by abstraction / ratios of quantities

- Bob Hale, **“Reals by Abstraction”**, *Philosophia Mathematica* 8(2) (2000), 100–123. DOI: `10.1093/philmat/8.2.100`.

يقدم برنامجًا neo-Fregean لإدخال الأعداد الحقيقية بواسطة abstraction principles بوصفها ratios of quantities.

**تحفظ مهم:** في العروض اللاحقة، يحتاج الحساب إلى domain ذي بنية مناسبة، ويمكن توليد هذا domain عبر cut-abstraction مستوحى من ديدكاند. لذلك لا يصنف تلقائيًا كبديل مستقل تمامًا.

**تقييم المشروع:** ذو قيمة فلسفية وتأسيسية، لكن ليس المرشح الأول لبناء مباشر من \(\mathbb{N}\)/\(\mathbb{Z}\).

---

## 9. Weierstrass historical construction

Weiss يعرض بناء Weierstrass بواسطة bounded multisets من integers وunit fractions، مع ملاحظة أن الصياغة التاريخية لم تكن مكتملة الصرامة.

دراسة تاريخية حديثة:

- Detlef D. Spalt, **“The first and most elementary construction of real numbers – by Karl Weierstraß”**, *Mathematische Semesterberichte* 70 (2023), 25–41; published online 2022. DOI: `10.1007/s00591-022-00330-1`.

**تقييم المشروع:** مهم تاريخيًا؛ لا نعتمده قبل التحقق من الصياغة الرياضية الحديثة الكاملة.

---

## 10. طرق لا ينبغي عدّها «بدائل قوية» ضمن معيار المشروع

### Bachmann nested rational intervals
هي equivalence classes من nests ذات أطوال تؤول إلى الصفر. بنيويًا قريبة جدًا من Cauchy completion.

### Bourbaki Cauchy filters
هي completion صريح لـ \(\mathbb{Q}\) باستعمال minimal Cauchy filters؛ ليست خروجًا عن فكرة كوشي.

### Maier–Maier variation
Weiss يبين صراحة أنها في الجوهر Dedekind construction دون canonical representatives.

### R. D. Arthan, “An Irrational Construction of R from Z” (2001)
رغم الانتقال من \(\mathbb{Z}\) عبر حلقات جبرية بدل \(\mathbb{Q}\)، الورقة نفسها تصرح باستعمال Dedekind cuts؛ لذلك لا تحقق شرط المشروع الصارم.

### Conway surreal numbers
تعطي بنية أوسع بكثير تحتوي نسخة من \(\mathbb{R}\)، لكن تعريفها بواسطة left/right sets قريب مفهوميًا من cut constructions ويحل مشكلة أوسع من هدف المشروع.

---

## 11. نتيجة خاصة لمسار «التكامل/التراكم»

أُجري بحث موجه عن بناء للأعداد الحقيقية يكون فيه **التكامل أو Riemann sums هو الآلية التأسيسية الأولى** بدل أن يكون التكامل معرفًا بعد وجود \(\mathbb{R}\).

**النتيجة الحالية:** لم نعثر في البحث الأولي على بناء معروف ومكرس في الأدبيات يجعل التكامل نفسه primitive construction لـ \(\mathbb{R}\). المصادر القياسية والحديثة التي ظهرت تفترض عادةً وجود حقل حقيقي/اكتمال/سوبرميم قبل تطوير التكامل.

هذه **نتيجة بحث سلبية مؤقتة وليست برهانًا على عدم وجود مثل هذا البناء**.

إذا أردنا مستقبلًا اختبار مسار «التراكم/التكامل أولًا»، فعليه تجنب الدورية التالية:

\[
\mathbb{R}\;\Rightarrow\;\text{limits/suprema}\;\Rightarrow\;\text{integral}\;\Rightarrow\;\mathbb{R}.
\]

أي يجب تعريف عملية تراكم انطلاقًا من بيانات طبيعية/صحيحة/نسبية فقط، ثم استخراج حقل مرتب كامل منها دون افتراض مسبق لنهايات حقيقية أو suprema حقيقية.

---

## 12. الترتيب الأولي لمسارات المشروع حسب الأهمية

### المرتبة 1 — Eudoxus / near-endomorphisms / quasimorphisms
السبب: يبدأ من \(\mathbb{Z}\) مباشرة، والكائن الحقيقي يظهر من السلوك الكلي لدالة ذات خطأ محدود، لا من cut أو Cauchy sequence. كما توجد تعميمات formal/general completion حديثة.

### المرتبة 2 — Rieger continued fractions
السبب: يربط بوضوح بين finite data و\(\mathbb{Q}\) وبين infinite data وirrationals، ويعطي كائنًا بدائيًا شديد البساطة.

### المرتبة 3 — de Bruijn + FMRR digit/string constructions
السبب: بناء مباشر من بيانات صحيحة/رقمية، مع اهتمام جبري واضح بكيفية نشوء العمليات.

### المرتبة 4 — Engel/Sylvester/alternating/product constructions
السبب: تثبت أن هناك عائلة واسعة من representations يمكن أن تتحول إلى complete ordered fields، وتوفر مختبرًا ممتازًا لفهم ما هو جوهري وما هو اعتباطي في construction of \(\mathbb{R}\).

### المرتبة 5 — domain theory
السبب: مفيد لفكرة «العدد بوصفه معلومة/تقريبًا متزايدًا»، خصوصًا حاسوبيًا، لكنه أقرب إلى completion mechanisms المعروفة.

### مسار جانبي مهم — abstraction/ratios and bicimal approaches
مهم لفهم foundations وepistemic economy، خاصة مع Panza (2026)، لكنه يحتاج فصلًا عن الهدف الجبري المباشر للمشروع.

---

## 13. الخلاصة البحثية المؤقتة

1. **نعم، الأدبيات تحتوي عددًا كبيرًا من محاولات بناء \(\mathbb{R}\) خارج العرضين المدرسيين ديدكاند/كوشي.**
2. ليست كلها مستقلة تأسيسيًا؛ بعضها مجرد completion أو cut في لغة أخرى.
3. أقوى عائلة مستقلة وجدناها للمشروع هي **Eudoxus/Schanuel near-endomorphism construction** المبنية مباشرة على \(\mathbb{Z}\).
4. الكسور المستمرة، digit strings، infinite series/products تعطي بدائل معتبرة لكنها غالبًا تستعيد الاكتمال أو العمليات بواسطة approximations/suprema في مرحلة لاحقة.
5. البحث الحديث لم يتوقف: توجد أعمال 2019، 2021، 2023، 2025 وكتاب 2026 تعيد دراسة أو تعميم أو formalize طرق بديلة.
6. لم نجد حتى الآن «integration-first construction» معروفًا يجعل التكامل نفسه الجسر التأسيسي من \(\mathbb{Q}\) أو \(\mathbb{Z}\) إلى \(\mathbb{R}\).

---

## 14. المهمة البحثية التالية المقترحة

بناء **مصفوفة تفكيك تأسيسي** لكل مسار من المرشحين الأربعة الأوائل، بحيث نسأل:

1. ما أصغر بنية يبدأ منها؟
2. ما الكائن البدائي الذي يمثل «عددًا حقيقيًا»؟
3. أين تدخل اللانهاية؟
4. أين تدخل علاقة التكافؤ، إن وجدت؟
5. كيف يُعرّف الترتيب؟
6. كيف يُعرّف الجمع؟
7. كيف يُعرّف الضرب؟
8. كيف يثبت وجود المعكوس؟
9. كيف يثبت الاكتمال؟
10. هل يستعمل في الخفاء limit/supremum/cut/completion مكافئًا لبناء تقليدي؟
11. ما العنصر البنيوي الذي يمكن إعادة استعماله في طريق جديد؟

ينبغي البدء بـ **Eudoxus/near-endomorphisms** ثم Rieger ثم de Bruijn/FMRR، وليس بابتكار بناء جديد الآن.
