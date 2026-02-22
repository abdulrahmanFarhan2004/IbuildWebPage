<div align="center">

# 🎨 IBuild — دليل UI/UX والهوية البصرية الشامل
### The Java Developer Club — Brand & Design System Guide

<br>

> **هذا المستند هو المرجع الرسمي والشامل** لجميع عناصر التصميم، الهوية البصرية، تجربة المستخدم، والأنماط المستخدمة في موقع IBuild.
> يُستخدم من قِبَل المصممين والمطورين لضمان التناسق البصري في أي تحديث أو إضافة مستقبلية.

</div>

---

## 📑 جدول المحتويات

| # | القسم | الوصف |
|---|-------|-------|
| 1 | [الشعار والعلامة التجارية](#1--الشعار-والعلامة-التجارية-logo--brand) | الشعار، الأيقونة، والاستخدام |
| 2 | [لوحة الألوان](#2--لوحة-الألوان-color-palette) | الألوان الأساسية، الثانوية، والتدرجات |
| 3 | [الخطوط والتدرج الهرمي النصي](#3--الخطوط-والتدرج-الهرمي-النصي-typography) | أنواع الخطوط وأحجامها واستخداماتها |
| 4 | [الأسلوب العام والفلسفة البصرية](#4--الأسلوب-العام-والفلسفة-البصرية-visual-style) | Glassmorphism، الظلال، والضبابية |
| 5 | [نظام الشبكة والتخطيط](#5--نظام-الشبكة-والتخطيط-layout--grid-system) | هيكل الصفحة والتنظيم |
| 6 | [المكونات الرئيسية](#6--المكونات-الرئيسية-components) | جميع مكونات UI بالتفصيل |
| 7 | [الحركة والميكرو-تفاعلات](#7--الحركة-والميكرو-تفاعلات-motion--micro-interactions) | الحركات والتأثيرات التفاعلية |
| 8 | [التصميم المتجاوب](#8--التصميم-المتجاوب-responsive-design) | نقاط الكسر والتكيف |
| 9 | [تجربة المستخدم UX](#9--تجربة-المستخدم-ux-patterns) | أنماط التنقل والتفاعل |
| 10 | [الوصولية](#10--الوصولية-accessibility) | معايير سهولة الوصول |
| 11 | [نبرة العلامة](#11--نبرة-العلامة-voice--tone) | أسلوب الكتابة والتواصل |
| 12 | [متغيرات CSS المرجعية](#12--متغيرات-css-المرجعية-css-custom-properties) | جدول كامل بالمتغيرات |
| 13 | [الأصول والموارد](#13--الأصول-والموارد-assets--resources) | الأصول المتاحة للاستخدام |
| 14 | [هيكل الملفات](#14--هيكل-الملفات-file-structure) | تنظيم المشروع |
| 15 | [إرشادات المساهمة](#15--إرشادات-المساهمة-contribution-guidelines) | كيفية المساهمة في المشروع |

---

## 1. 🏷️ الشعار والعلامة التجارية (Logo & Brand)

### الأيقونة (Logo Icon)
| الخاصية | القيمة |
|---------|--------|
| الشكل | مربع بحواف دائرية |
| نصف قطر الزوايا | `9px` |
| الأبعاد | `36×36px` (Nav) · `34×34px` (Footer) |
| الخلفية | `linear-gradient(135deg, #FF6B35, #FF3CAC, #00D4AA)` |
| النص الداخلي | **IB** — خط JetBrains Mono، وزن 800، أبيض |
| الظل | `0 0 20px rgba(255, 107, 53, .4)` |

### النص الشعاري (Logo Text)
| الخاصية | القيمة |
|---------|--------|
| النص | `IBuild.java` |
| الخط | JetBrains Mono, monospace |
| الوزن | 700 |
| الحجم | `0.92rem` (Nav) · `0.88rem` (Footer) |
| اللون | تدرج متحرك عبر `var(--grad)` |
| الحركة | `animation: gs 5s linear infinite` — تحريك خلفية التدرج |

### قواعد الاستخدام
- ✅ يُستخدم الشعار دائماً مع النص `IBuild.java`
- ✅ يُوضع في أقصى اليسار/اليمين (حسب اتجاه RTL) من شريط التنقل
- ❌ لا يُعدَّل التدرج اللوني للأيقونة
- ❌ لا يُصغَّر عن `34px`

---

## 2. 🎨 لوحة الألوان (Color Palette)

### الألوان الأساسية (Primary Colors)
| اللون | الكود | المتغير | الاستخدام |
|-------|-------|---------|-----------|
| 🟠 برتقالي أساسي | `#FF6B35` | `--jo` | لون العلامة التجارية الرئيسي، الأزرار، الروابط النشطة |
| 🟠 برتقالي فاتح | `#FF8C42` | `--jo2` | تدرجات ثانوية، نصوص hover |
| 🟡 برتقالي ذهبي | `#FFB347` | `--jo3` | أسماء الدوال في الكود، لمسات ذهبية |

### الألوان المساعدة (Accent Colors)
| اللون | الكود | المتغير | الاستخدام |
|-------|-------|---------|-----------|
| 🟢 تركوازي | `#00D4AA` | `--teal` | نقاط الحالة، حدود التحويم، حالات النجاح |
| 🔵 أزرق فاتح | `#4FC3F7` | `--blue` | شارات، عناوين القيادة |
| 🟣 بنفسجي | `#9B59FF` | `--pur` | الكلمات المفتاحية في الكود، شارات خاصة |
| 🩷 وردي | `#FF3CAC` | `--pink` | الأرقام في الكود، نقاط التمرير، لمسات إبداعية |

### ألوان الخلفية والأسطح (Background & Surface)
| اللون | الكود | المتغير | الاستخدام |
|-------|-------|---------|-----------|
| ⚫ خلفية داكنة | `#060A0F` | `--bg` | خلفية الصفحة الرئيسية |
| 🌑 سطح داكن | `#1A2332` | `--surf` | أسطح البطاقات المرتفعة |
| ⬜ زجاجي | `rgba(255,255,255,0.05)` | `--gb` | خلفية البطاقات والمكونات الزجاجية |
| ⬜ زجاجي hover | `rgba(255,255,255,0.09)` | `--gbh` | حالة التحويم للمكونات الزجاجية |
| ⬜ حدود زجاجية | `rgba(255,255,255,0.09)` | `--gbb` | حدود المكونات الشفافة |

### ألوان النصوص (Text Colors)
| اللون | الكود | المتغير | الاستخدام |
|-------|-------|---------|-----------|
| ⬜ أبيض نقي | `#FFFFFF` | `--tp` | العناوين الرئيسية والنصوص المهمة |
| 🩶 رمادي فاتح | `#94A3B8` | `--tm` | النصوص الثانوية والوصفية |
| 🌫️ رمادي داكن | `#475569` | `--tf` | النصوص الخافتة جداً والتعليقات |

### التدرجات (Gradients)
```css
/* التدرج الرئيسي — يُستخدم في الأزرار، الشعار، والخطوط البارزة */
--grad: linear-gradient(120deg, #FF6B35, #FF3CAC, #9B59FF, #00D4AA);

/* تدرج الخلفية العام */
background: radial-gradient(ellipse 80% 60% at 10% 10%, rgba(255,107,53,.12), transparent 60%),
            radial-gradient(ellipse 60% 70% at 90% 90%, rgba(0,115,150,.10), transparent 60%),
            radial-gradient(ellipse 50% 50% at 50% 0%, rgba(155,89,255,.08), transparent 50%),
            #060A0F;

/* تدرج الأزرار */
background: linear-gradient(135deg, var(--jo), var(--pink), var(--teal));

/* تدرج عنوان "Cyan" */
background: linear-gradient(135deg, #007396, #00D4AA, #4FC3F7);

/* تدرج عنوان "Orange" */
background: linear-gradient(135deg, #FF6B35, #FF8C42, #FFB347);
```

---

## 3. ✍️ الخطوط والتدرج الهرمي النصي (Typography)

### الخطوط المُستخدمة
| الخط | النوع | الاستخدام الرئيسي | الأوزان |
|------|-------|-------------------|---------|
| **Cinzel** | Serif | العناوين الرئيسية والفرعية | 400, 700, 900 |
| **JetBrains Mono** | Monospace | الأزرار، الشارات، الكود، الشعار | 400, 700, 800 |
| **Inter** | Sans-serif | النصوص المتنية الإنجليزية | 400, 600, 700 |
| **Tajawal** | Sans-serif | النصوص المتنية العربية | 400, 700, 900 |

### التسلسل الهرمي (Type Scale)
| المستوى | الخط | الحجم | الوزن | الاستخدام |
|---------|------|-------|-------|-----------|
| H1 — Hero | Cinzel | `clamp(2.6rem, 6.5vw, 5.4rem)` | 900 | عنوان البطل الرئيسي |
| H2 — Section | Cinzel | `clamp(2rem, 3.5vw, 3rem)` | 800 | عناوين الأقسام |
| H3 — Card Title | Cinzel | `1.05–1.2rem` | 700 | عناوين البطاقات |
| Body | Inter/Tajawal | `0.9–1.1rem` | 400–700 | النصوص المتنية |
| Code/Badge | JetBrains Mono | `0.6–0.78rem` | 700–800 | الشارات، الأزرار، الكود |
| Stat Number | JetBrains Mono | `2.6rem` | 800 | الأرقام الإحصائية |
| Caption | JetBrains Mono | `0.58–0.68rem` | 400–700 | التسميات الصغيرة |

### تنسيقات خاصة
```css
/* نص بتدرج متحرك */
background: var(--grad);
-webkit-background-clip: text;
background-clip: text;
-webkit-text-fill-color: transparent;
background-size: 200% auto;
animation: gs 4s linear infinite;

/* أحرف متباعدة للشارات */
letter-spacing: 0.14em;
text-transform: uppercase;
font-family: 'JetBrains Mono', monospace;
```

---

## 4. 🖼️ الأسلوب العام والفلسفة البصرية (Visual Style)

### Glassmorphism (الأسلوب الزجاجي)
النمط التصميمي الرئيسي للموقع يعتمد على **Glassmorphism** — خلفيات شبه شفافة مع تأثير ضبابي:

```css
/* النمط الزجاجي الأساسي */
background: rgba(255, 255, 255, 0.05);
backdrop-filter: blur(22px);
border: 1px solid rgba(255, 255, 255, 0.09);
box-shadow: 0 8px 32px rgba(0, 0, 0, 0.45);

/* النمط الزجاجي المعزز (Nav) */
background: rgba(6, 10, 15, 0.65);
backdrop-filter: blur(40px) saturate(2);

/* النمط الزجاجي للتيرمنال */
background: rgba(6, 10, 15, 0.85);
backdrop-filter: blur(24px);
```

### الظلال (Shadows)
| الحالة | القيمة |
|--------|--------|
| الافتراضي | `0 8px 32px rgba(0, 0, 0, 0.45)` |
| التحويم (Cards) | `0 24px 60px rgba(0, 0, 0, 0.6), 0 0 30px rgba(255,107,53, 0.1)` |
| التيرمنال | `0 40px 100px rgba(0, 0, 0, 0.6)` |
| الأزرار | `0 4px 24px rgba(255, 107, 53, 0.4)` |
| أزرار hover | `0 10px 40px rgba(255, 107, 53, 0.55)` |
| أيقونة الشعار | `0 0 20px rgba(255, 107, 53, 0.4)` |

### البقع الضوئية (Ambient Blobs)
عناصر ثابتة مطلقة الموضع تعمل كإضاءة محيطية:
| البقعة | الحجم | اللون | الحركة |
|--------|-------|-------|--------|
| amb-1 | 550px | برتقالي 14% | 14s ease-in-out alternate |
| amb-2 | 500px | تركوازي 12% | 17s ease-in-out alternate |
| amb-3 | 400px | بنفسجي 8% | 11s ease-in-out |
| amb-4 | 300px | وردي 7% | 13s ease-in-out alternate |

### الخلفية الشبكية (Grid Background)
```css
/* شبكة خفيفة في قسم Hero */
background-image:
  linear-gradient(rgba(255,107,53,.06) 1px, transparent 1px),
  linear-gradient(90deg, rgba(255,107,53,.06) 1px, transparent 1px);
background-size: 52px 52px;
mask-image: radial-gradient(ellipse 75% 75% at 50% 50%, black, transparent);
```

---

## 5. 📐 نظام الشبكة والتخطيط (Layout & Grid System)

### هيكل الصفحة
```
┌─────────────────────────────────────┐
│           Nav Bar (Fixed)           │  ← top: 16px, max-width: 960px
├─────────────────────────────────────┤
│         Hero Section (100vh)        │  ← flex-center, padding: 120px 24px 80px
├─────────────────────────────────────┤
│         Marquee (Auto-scroll)       │  ← padding: 24px 0
├─────────────────────────────────────┤
│         About Section               │  ← grid: 1fr 1fr, gap: 64px
├─────────────────────────────────────┤
│         Activities Section          │  ← grid: repeat(3, 1fr), gap: 18px
├─────────────────────────────────────┤
│         Projects Section            │  ← grid: repeat(2, 1fr), gap: 18px
├─────────────────────────────────────┤
│         OOP Docs (Video Cards)      │  ← grid: auto-fill, minmax(300px, 1fr)
├─────────────────────────────────────┤
│         Team Section                │  ← leaders: 1fr 1fr; members: auto-fill
├─────────────────────────────────────┤
│         Join CTA                    │  ← grid: 1fr auto, gap: 52px
├─────────────────────────────────────┤
│         Footer                      │  ← grid: 2fr 1fr 1fr 1fr, gap: 52px
└─────────────────────────────────────┘
```

### مواصفات التخطيط
| العنصر | النوع | الأعمدة | الفجوة | الحشوة |
|--------|-------|---------|--------|--------|
| Section | Block | — | — | `110px 64px` |
| About Grid | CSS Grid | `1fr 1fr` | `64px` | — |
| Stats Cluster | CSS Grid | `1fr 1fr` | `14px` | — |
| Activities Grid | CSS Grid | `repeat(3, 1fr)` | `18px` | margin-top: 56px |
| Projects Grid | CSS Grid | `repeat(2, 1fr)` | `18px` | margin-top: 56px |
| Video Grid | CSS Grid | `auto-fill, minmax(300px, 1fr)` | `22px` | max-width: 960px |
| Team Leaders | CSS Grid | `1fr 1fr` | `24px` | max-width: 760px |
| Team Members | CSS Grid | `auto-fill, minmax(150px, 1fr)` | `12px` | max-width: 860px |
| Join Inner | CSS Grid | `1fr auto` | `52px` | `88px 64px` |
| Footer Grid | CSS Grid | `2fr 1fr 1fr 1fr` | `52px` | — |

---

## 6. 🧩 المكونات الرئيسية (Components)

### 6.1 شريط التنقل (Nav Bar)
| الخاصية | القيمة |
|---------|--------|
| الموضع | `fixed`, top: 16px, centered |
| العرض الأقصى | `min(960px, calc(100% - 40px))` |
| الشكل | `border-radius: 9999px` (كبسولة) |
| الخلفية | `rgba(6, 10, 15, 0.65)` + `blur(40px) saturate(2)` |
| Z-index | `200` |
| المكونات | شعار يسار ← روابط وسط ← زر CTA يمين |
| روابط | حجم `0.82rem`، وزن 500، hover: خلفية زجاجية |
| زر CTA | تدرج لوني، `border-radius: 9999px`، JetBrains Mono |

### 6.2 قسم البطل (Hero)
| الخاصية | القيمة |
|---------|--------|
| الارتفاع | `min-height: 100vh` |
| التنسيق | Flex column, center, center |
| العنوان | Cinzel، حتى 5.4rem، وزن 900 |
| العبارة الفرعية | Inter/Tajawal, 1.1rem, لون `--tm` |
| الأزرار | Primary (تدرج) + Ghost (زجاجي) |
| كتل الكود العائمة | 4 كتل بخط JetBrains Mono، تطفو بحركات مختلفة |
| التيرمنال | محاكاة terminal بنقاط (أحمر/أصفر/أخضر)، كود Java ملون |

**تلوين الكود في التيرمنال:**
| الفئة | اللون | الاستخدام |
|-------|-------|-----------|
| `.t-kw` | بنفسجي `--pur` | الكلمات المفتاحية (public, class, void) |
| `.t-cl` | أزرق `--blue` | أسماء الكلاسات |
| `.t-fn` | ذهبي `--jo3` | أسماء الدوال |
| `.t-str` | تركوازي `--teal` | النصوص (Strings) |
| `.t-ann` | برتقالي `--jo` | التعليقات التوضيحية (Annotations) |
| `.t-num` | وردي `--pink` | الأرقام |
| `.t-comment` | رمادي شفاف | التعليقات |

### 6.3 شريط التمرير (Marquee)
| الخاصية | القيمة |
|---------|--------|
| الاتجاه | LTR (ثابت بغض النظر عن RTL) |
| السرعة | `40s linear infinite` |
| الخط | JetBrains Mono, `0.72rem` |
| الفاصل | نقطة ماسية وردية `◆` |
| التلاشي | تدرج شفاف على الأطراف (120px) |
| المحتوى | Java SE, Spring Boot, Data Structures, OOP, Design Patterns... |

### 6.4 البطاقات (Cards)
**النمط الأساسي لجميع البطاقات:**
```css
background: rgba(255, 255, 255, 0.05);
backdrop-filter: blur(22px);
border: 1px solid rgba(255, 255, 255, 0.09);
box-shadow: 0 8px 32px rgba(0, 0, 0, 0.45);
transition: all 0.4s cubic-bezier(0.22, 1, 0.36, 1);
```

**حد علوي متدرج عند التحويم:**
```css
.card::before {
  /* شريط متدرج أعلى البطاقة، مخفي افتراضياً */
  height: 2px;
  background: var(--grad);
  opacity: 0; /* يظهر عند hover */
}
.card:hover::before { opacity: 1; }
```

**أنواع البطاقات:**
| النوع | الحشوة | الزوايا | خاصية إضافية |
|-------|--------|---------|-------------|
| Stat Card | `30px 26px` | `16px` | رقم متدرج كبير 2.6rem |
| Activity Card | `34px 30px` | `20px` | أيقونة 54px مربعة + tag |
| Project Card | `30px` | `20px` | توهج خلفي `--proj-color` + حالة |
| Video Card | — | `18px` | صورة 16:9 + زر تشغيل + شريط gradient |
| Leader Card | `40px 32px 36px` | `24px` | avatar 90px + وهج خلفي 260px |
| Mini Member Card | `20px 14px 18px` | `14px` | avatar 46px صغير |

### 6.5 الشارات والعلامات (Badges & Chips)
**Chip (شريحة القسم):**
```css
padding: 5px 16px;
border-radius: 9999px;
font-family: 'JetBrains Mono', monospace;
font-size: 0.63rem;
letter-spacing: 0.14em;
text-transform: uppercase;
backdrop-filter: blur(12px);
```

**ألوان الشرائح:**
| النوع | الخلفية | الحد | لون النص |
|-------|---------|------|----------|
| Cyan | `rgba(79,195,247,.08)` | `rgba(79,195,247,.25)` | `--blue` |
| Orange | `rgba(255,107,53,.08)` | `rgba(255,107,53,.25)` | `--jo` |
| Green | `rgba(0,212,170,.08)` | `rgba(0,212,170,.25)` | `--teal` |
| Purple | `rgba(155,89,255,.08)` | `rgba(155,89,255,.25)` | `--pur` |

### 6.6 الأزرار (Buttons)
| النوع | الخلفية | الحشوة | الخط | التحويم |
|-------|---------|--------|------|--------|
| **Primary (btn-main)** | تدرج jo→pink→teal | `14px 36px` | Cinzel, 0.9rem, 700 | ↑4px + scale(1.04) + ظل معزز + shimmer |
| **Ghost (btn-ghost)** | `var(--gb)` + حد | `14px 36px` | Cinzel, 0.9rem, 600 | خلفية أغمق + حد تركوازي + ↑3px |
| **Nav CTA (btn-nav)** | تدرج | `8px 22px` | JetBrains Mono, 0.78rem | scale(1.06) + ظل معزز |

### 6.7 قسم الانضمام (Join CTA)
| الخاصية | القيمة |
|---------|--------|
| الزوايا | `28px` |
| الخلفية | زجاجية + `blur(30px)` |
| الهوامش | `0 64px 90px` |
| البقع الخلفية | دائرة برتقالية 450px يمين + بنفسجية 350px يسار |
| الخط العلوي | تدرج 5 ألوان بشفافية 45% |
| التخطيط | grid: `1fr auto`، العنوان يسار + أزرار يمين |

### 6.8 التذييل (Footer)
| الخاصية | القيمة |
|---------|--------|
| الحشوة | `56px 64px 38px` |
| الشبكة | `2fr 1fr 1fr 1fr`، فجوة `52px` |
| الحد العلوي | تدرج 5 ألوان |
| عناوين الأعمدة | JetBrains Mono, 0.66rem, تدرج متحرك |
| الروابط | Inter, 0.85rem, hover: `--jo2` + padding-left: 4px |
| الشارات السفلية | زجاجية، 0.58rem, حدود خفيفة |
| نص الحقوق | JetBrains Mono, 0.62rem, لون `--tf` |

---

## 7. ✨ الحركة والميكرو-تفاعلات (Motion & Micro-interactions)

### الحركات المُعرَّفة (Keyframes)
| الاسم | المدة | الاستخدام | الوصف |
|-------|-------|-----------|-------|
| `gs` | 4–5s linear infinite | التدرجات | تحريك background-position من 0% إلى 200% |
| `fadeUp` | 0.8s | الظهور الأول | من opacity:0 + translateY(32px) إلى الظهور |
| `cfloat` | 8–11s ease-in-out | كتل الكود | تطفو لأعلى 20px ثم تعود |
| `pulse` | 2s ease-in-out | نقاط الحالة | نبضة box-shadow تتوسع وتختفي |
| `blink2` | 1.1s step-end | مؤشر التيرمنال | وميض opacity بين 0 و 1 |
| `geoF` | 16s ease-in-out | البقع الهندسية | scale + translate بقيم مختلفة |
| `scroll` | 40s linear infinite | شريط التمرير | translateX(-50%) لحلقة لا نهائية |
| `a1`–`a4` | 11–17s | البقع المحيطية | translate + scale بطيء |

### منحنيات التسارع (Easing)
| المتغير | القيمة | الاستخدام |
|---------|--------|-----------|
| `--e1` | `cubic-bezier(0.22, 1, 0.36, 1)` | الانتقالات الناعمة (بطاقات، تخطيط) |
| `--e2` | `cubic-bezier(0.34, 1.56, 0.64, 1)` | الانتقالات النابضة (أزرار، مؤشر) |

### نظام الكشف (Reveal System)
```css
/* العنصر قبل الظهور */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: all 0.8s var(--e1);
}

/* بعد دخول مجال الرؤية */
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* تأخيرات متتالية */
.reveal-d1 { transition-delay: 0.1s; }
.reveal-d2 { transition-delay: 0.2s; }
.reveal-d3 { transition-delay: 0.3s; }
```
**يُفعَّل عبر Intersection Observer بعتبة 10%.**

### المؤشر المخصص (Custom Cursor)
| العنصر | الحجم | الوصف |
|--------|-------|-------|
| النقطة (dot) | 8px | تدرج برتقالي، تتبع فوري |
| الحلقة (ring) | 38px → 60px | حد برتقالي شفاف، تتبع متأخر (lerp 12%) |
| عند التحويم | النقطة: scale(2)، الحلقة: 60px + تركوازي | يُفعَّل على الروابط، الأزرار، البطاقات |

---

## 8. 📱 التصميم المتجاوب (Responsive Design)

### نقاط الكسر
| النقطة | القيمة | التغييرات |
|--------|--------|-----------|
| **Desktop** | > 960px | التخطيط الكامل كما هو |
| **Tablet/Mobile** | ≤ 960px | إخفاء الروابط، أعمدة مفردة |

### التحولات عند ≤ 960px
| العنصر | التغيير |
|--------|---------|
| **Nav** | padding: `10px 20px`، top: `10px`، إخفاء `.nav-links` |
| **Sections** | padding: `72px 24px` (بدلاً من `110px 64px`) |
| **About Grid** | عمود واحد |
| **Activities Grid** | عمود واحد (بدلاً من 3) |
| **Projects Grid** | عمود واحد (بدلاً من 2) |
| **Team Leaders** | عمود واحد |
| **Team Members** | `minmax(130px, 1fr)` (بدلاً من 150px) |
| **Footer Grid** | عمودان (بدلاً من 4) |
| **Join Section** | margin: `0 16px 64px`، padding: `52px 28px`، عمود واحد |
| **Code Floats** | `display: none` — مخفية بالكامل |

---

## 9. 🧭 تجربة المستخدم (UX Patterns)

### التنقل
- **شريط علوي ثابت** يبقى مرئياً أثناء التمرير
- **روابط سلسة** (`scroll-behavior: smooth`) للأقسام الداخلية
- **زر CTA واضح** "انضم إلينا →" دائماً متاح في الـ Nav
- **شريط Marquee** يعمل كفاصل بصري ومعرّف للتخصصات

### التفاعل
- **مؤشر مخصص** يتفاعل مع العناصر التفاعلية (يكبر ويتغير لونه)
- **تأثير الكشف** (Reveal) يمنح شعوراً بالحياة أثناء التمرير
- **حد علوي متدرج** يظهر على البطاقات عند التحويم كإشارة بصرية
- **Video cards** تظهر رابط "شاهد على YouTube" عند التحويم
- **تأثير Shimmer** على زر Primary عند التحويم

### بنية المحتوى
```
Hero (جذب الانتباه)
  → Marquee (إثبات التخصص)
    → About + Stats (بناء الثقة)
      → Activities (عرض القيمة)
        → Projects (إثبات الإنجاز)
          → OOP Docs/Videos (تعليم وتوثيق)
            → Team (الوجه الإنساني)
              → Join CTA (الدعوة للعمل)
                → Footer (المعلومات والروابط)
```

### اختيار النص (Selection)
```css
::selection {
  background: rgba(255, 107, 53, 0.3);
  color: #fff;
}
```

### شريط التمرير (Scrollbar)
```css
width: 4px;
track: var(--bg);
thumb: linear-gradient(to bottom, var(--jo), var(--pur));
border-radius: 2px;
```

---

## 10. ♿ الوصولية (Accessibility)

### الممارسات المُطبَّقة
| الممارسة | التفاصيل |
|----------|----------|
| اللغة | `lang="ar"` مع `dir="rtl"` |
| التحميل الكسول | `loading="lazy"` على الصور |
| Fallback للصور | `onerror` لتحميل صورة بديلة |
| تباين الألوان | نصوص بيضاء على خلفية داكنة — نسبة تباين عالية |
| التمرير السلس | `scroll-behavior: smooth` |
| overflow-x | `hidden` لمنع التمرير الأفقي غير المرغوب |

### ملاحظات للتطوير المستقبلي
- ⚠️ إضافة `aria-labels` للعناصر التفاعلية
- ⚠️ إضافة `alt` وصفي للصور
- ⚠️ دعم التنقل بلوحة المفاتيح مع المؤشر المخصص
- ⚠️ إضافة `prefers-reduced-motion` لتعطيل الحركات

---

## 11. 🗣️ نبرة العلامة (Voice & Tone)

### الأسلوب اللغوي
| الخاصية | الوصف |
|---------|-------|
| **اللغات** | عربية/إنجليزية ثنائية |
| **الأسلوب** | ودود، تشجيعي، واثق، تقني |
| **الجمهور** | مجتمع مطوري Java — طلاب ومتعلمين |
| **القيم** | العمل الجماعي، التعلم المستمر، البناء الحقيقي |

### أمثلة من الموقع
| العنصر | النص | الأسلوب |
|--------|------|---------|
| Hero H1 | "نبني. نتعلم. نبتكر." | قصير، قوي، ملهم |
| Hero Sub | "A community for Java enthusiasts..." | واضح، مهني |
| About | "النادي الذي كنت تبحث عنه" | شخصي، دافئ |
| Join CTA | "جاهز تنضم لعائلة IBuild؟" | تحفيزي، مباشر |
| متطلبات الانضمام | `// شغف + فضول + لابتوب` | فكاهي، تقني |
| Terminal Comment | `// Welcome to IBuild` | تقني، ترحيبي |

### قواعد الكتابة
- ✅ استخدام `//` كنمط تعليق في الشرائح والعلامات
- ✅ عبارات مختصرة وواضحة
- ✅ مزج العربية والإنجليزية بشكل طبيعي
- ✅ استخدام المصطلحات التقنية كما هي (Java, Spring Boot, OOP)
- ❌ عدم استخدام لغة رسمية جامدة
- ❌ عدم الإفراط في الإيموجي في النص الأساسي

---

## 12. 🔧 متغيرات CSS المرجعية (CSS Custom Properties)

```css
:root {
  /* الألوان الأساسية */
  --jo:   #FF6B35;    /* برتقالي أساسي */
  --jo2:  #FF8C42;    /* برتقالي فاتح */
  --jo3:  #FFB347;    /* برتقالي ذهبي */
  --teal: #00D4AA;    /* تركوازي */
  --blue: #4FC3F7;    /* أزرق فاتح */
  --pur:  #9B59FF;    /* بنفسجي */
  --pink: #FF3CAC;    /* وردي */

  /* الخلفيات والأسطح */
  --bg:   #060A0F;    /* خلفية الصفحة */
  --surf: #1A2332;    /* سطح مرتفع */
  --gb:   rgba(255, 255, 255, .05);   /* زجاجي */
  --gbh:  rgba(255, 255, 255, .09);   /* زجاجي hover */
  --gbb:  rgba(255, 255, 255, .09);   /* حدود زجاجية */

  /* النصوص */
  --tp:   #fff;       /* نص رئيسي */
  --tm:   #94A3B8;    /* نص ثانوي */
  --tf:   #475569;    /* نص خافت */

  /* المؤثرات */
  --sh:   0 8px 32px rgba(0, 0, 0, .45);  /* الظل الافتراضي */
  --e1:   cubic-bezier(.22, 1, .36, 1);    /* تسارع ناعم */
  --e2:   cubic-bezier(.34, 1.56, .64, 1); /* تسارع نابض */

  /* التدرج */
  --grad: linear-gradient(120deg, #FF6B35, #FF3CAC, #9B59FF, #00D4AA);
}
```

---

## 13. 📦 الأصول والموارد (Assets & Resources)

### الخطوط (Google Fonts)
```html
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700;800&family=Tajawal:wght@400;700;900&family=Inter:wght@400;600;700&family=Cinzel:wght@400;700;900&display=swap" rel="stylesheet">
```

### الأصول المقترحة للتصدير
| الأصل | الصيغة | الملاحظات |
|-------|--------|----------|
| شعار IB | SVG | مربع متدرج + نص JetBrains Mono أبيض |
| التدرج الرئيسي | CSS | جاهز كـ `var(--grad)` |
| نمط الخلفية | CSS/PNG | شبكة + بقع ضوئية (يمكن التصدير كصورة ثابتة) |
| أيقونات الأنشطة | Emoji/SVG | 🎓 ⚡ 🚀 🔍 🎤 🏆 |
| أيقونات المشاريع | Emoji/SVG | 🏦 📱 🧩 🤖 |

---

## 14. 📁 هيكل الملفات (File Structure)

```
IbuildWebPage/
├── index.html          # الملف الرئيسي (HTML + CSS + JS مدمج)
├── README.md           # هذا الملف — دليل UI/UX والهوية البصرية
└── LICENSE             # ترخيص MIT
```

> **ملاحظة:** المشروع حالياً ملف واحد (Single-file) يحتوي على HTML و CSS و JavaScript مدمجة. يُنصح مستقبلاً بفصل الأنماط إلى `styles.css` والسكربتات إلى `script.js`.

---

## 15. 🤝 إرشادات المساهمة (Contribution Guidelines)

### عند إضافة مكون جديد:
1. **استخدم متغيرات CSS** المُعرَّفة في `:root` — لا تستخدم ألواناً مباشرة
2. **اتبع نمط الزجاجية** — `var(--gb)` + `backdrop-filter` + `var(--gbb)` للحد
3. **أضف حركة reveal** — class `reveal` + Intersection Observer
4. **حافظ على التسلسل الهرمي** — Cinzel للعناوين، JetBrains Mono للشارات
5. **اختبر Responsive** — تأكد من السلوك تحت 960px

### عند تعديل الألوان:
- أي لون جديد يجب أن يُضاف كمتغير في `:root`
- يجب اختبار التباين مع الخلفية الداكنة `#060A0F`
- حافظ على الشفافية في الخلفيات (0.05–0.10 للبطاقات)

### الأنماط المرجعية السريعة:
```css
/* بطاقة جديدة */
.my-card {
  background: var(--gb);
  backdrop-filter: blur(22px);
  border: 1px solid var(--gbb);
  border-radius: 20px;
  box-shadow: var(--sh);
  transition: all .4s var(--e1);
}

/* شارة جديدة */
.my-badge {
  padding: 4px 12px;
  border-radius: 7px;
  font-family: 'JetBrains Mono', monospace;
  font-size: .6rem;
  letter-spacing: .06em;
  background: rgba(255, 107, 53, .08);
  border: 1px solid rgba(255, 107, 53, .2);
  color: var(--jo2);
}
```

---

<div align="center">

### 🏗️ Built with ☕ & 💙 by IBuild — The Java Developer Club

**© 2026 IBuild** · [الموقع](https://abdulrahmanfarhan2004.github.io/IbuildWebPage/) · [GitHub](https://github.com/abdulrahmanFarhan2004/IbuildWebPage)

> هذا الدليل يُحدَّث مع كل تغيير جوهري في تصميم الموقع.
> آخر تحديث: فبراير 2026

</div>
