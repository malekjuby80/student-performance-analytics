[code_artifact.md](https://github.com/user-attachments/files/34195043/code_artifact.md)
# 📊 Student Academic Performance Analytics & Interactive Dashboard
### دراسة استكشافية تحليلية معمقة ولوحة تحكم تفاعلية لأداء الطلاب

[![GitHub Pages](https://img.shields.io/badge/Live_Demo-GitHub_Pages-2ea44f?style=for-the-badge&logo=github)](https://username.github.io/repository-name/)
[![Dataset](https://img.shields.io/badge/Dataset-395_Students_x_33_Variables-blue?style=for-the-badge)](student.csv)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

## 🌐 Live Interactive Demo | المعاينة الحية
👉 **[Click Here to Explore the Live Interactive Dashboard](https://username.github.io/repository-name/)**

*(Replace `username` and `repository-name` with your actual GitHub repository details).*

---

## 📌 Executive Overview | نظرة عامة على المشروع

### [English]
This project provides a comprehensive **Exploratory Data Analysis (EDA)** and a client-side **Interactive Analytical Dashboard** evaluating the academic performance of 395 secondary school students across 33 demographic, familial, academic, and behavioral attributes (sourced from `student.csv`). 

Rather than deploying standard black-box predictive models, the emphasis is placed on **methodological rigor, uncovering latent anomalies, dissecting Simpson's Paradox**, and translating data-backed insights into concrete educational interventions.

### [العربية]
يقدم هذا المشروع دراسة تحليلية استكشافية متقدمة (EDA) ولوحة معلومات تفاعلية بالكامل لتقييم الأداء الأكاديمي لـ 395 طالباً بالمرحلة الثانوية عبر 33 متغيراً تغطي الأبعاد الديموغرافية، الأسرية، الدراسية، والسلوكية (المستخرجة من `student.csv`).

يركز المشروع على التفكيك المنهجي للظواهر الإحصائية، معالجة القيم الشاذة، وتفكيك مفارقة سيمبسون وتحيز الانتقاء، بدلاً من الاكتفاء بالنماذج التنبؤية السطحية.

---

## 🔍 Key Data Discoveries & Analytical Rigor | أبرز الاكتشافات المنهجية

| Analytical Case / الفرضية التحليلية | Superficial View / النظرة السطحية | Deep Data Insight / التحليل الاستكشافي المعمق |
| :--- | :--- | :--- |
| **The Zero-Grade Anomaly & Simpson's Paradox**<br>ظاهرة الأصفار الـ 38 والغياب | Pearson Correlation shows negligible association between school absences and final grade ($r = +0.03$). | **38 students (9.6%) scored a flat zero ($G3 = 0$)** despite normal prior term scores ($G1 \approx 7.53$), with all 38 having **exactly 0 recorded absences** due to administrative dropout. Once isolated, the true negative impact of absences emerges strongly at **$r = -0.21$**. |
| **Selection Bias in Support Programs**<br>تحيز الانتقاء في الدعم المدرسي | Students receiving extra educational support (`schoolsup = yes`) have a lower mean score (9.43) than non-supported peers (10.56). | **Selection Bias (تحيز الانتقاء):** The institution mandatorily enrolls failing students into support programs post-Period 1 ($G1$). Support acts as an emergency safety net, not an intrinsic negative driver. |
| **Prior Failures vs. Study Habits**<br>تاريخ الرسوب مقابل ساعات الدراسة | Increasing study time alone is enough to guarantee high marks. | Prior failure history (`failures ≥ 1`) creates an entrenched deficit ($6.55$ mean vs. $11.25$). Students with previous failures struggle to cross the passing threshold ($10/20$) even with $>5$ hours of study, proving the necessity of remedial baseline courses. |
| **Intrinsic Motivation Impact**<br>قوة الدافعية الذاتية والتعليم العالي | Family income and background are the only decisive factors for success. | Desire for higher education (`higher = yes`) accounts for the widest singular performance gap (**$+3.81$ points**), outperforming several demographic baselines. |

---

## 🎛️ Interactive Dashboard Features | مميزات لوحة التحكم

1. **Instant Slicers & Dynamic KPIs Engine:** Filter data dynamically by School (`GP`/`MS`), Gender (`F`/`M`), Address (`Urban`/`Rural`), Higher Ed aspiration, Past failures, and Zero-grade handling (`G3 = 0` inclusion/exclusion). All 6 KPIs and 8 charts recalculate immediately in the browser.
2. **8 Analytical Visualizations:**
   * Multi-period Grade Distributions ($G1 \rightarrow G2 \rightarrow G3$).
   * True Pearson Correlation Ranking (All Cohort vs. Active Takers).
   * Study Time $\times$ Prior Failure Interaction Matrix.
   * Parental Occupational Impact Breakdown (`Mjob` & `Fjob`).
   * Behavioral Lifestyle Trajectories (Going out, Workday & Weekend Alcohol).
   * Absences Scatter Plot illustrating Simpson's Paradox.
   * Binary Demographic & Support Drivers Comparison.
   * Age and Travel Time geographic analysis.
3. **Custom Variable Explorer:** Single-click dropdown allowing exhaustive drill-down into **all 33 variables**, displaying distribution histograms and period-by-period progression.
4. **Searchable 33-Variable Data Dictionary:** Complete pedagogical taxonomy, distributions, and behavioral interpretations.

---

## 💡 Strategic Recommendations | التوصيات الاستراتيجية

* 🚨 **Early Warning Triggers (نظام الإنذار المبكر):** Mandatory intervention for any student scoring below $8/20$ in Period 1 ($G1$), arresting the dropoff before Period 3 abandonment.
* 🛠️ **Remedial Foundation Tracks (برامج التأسيس العلاجي):** Tailored foundational classes targeting fundamental learning gaps for students with prior failure records (`failures ≥ 1`).
* 🎓 **Academic Counseling (التوجيه الجامعي):** Structured motivational programs promoting university orientation to instill intrinsic commitment.

---

## ⚠️ Methodological Limitations | حدود الاستنتاجات

1. **Correlation $\neq$ Causation:** Associations between peer socialization (`goout`), relationship status (`romantic`), and grades cannot be deemed purely causal without accounting for latent confounders.
2. **Reverse Causality:** Observed in supplemental tutoring and remedial programs.
3. **Self-Reporting Bias:** Metrics including alcohol consumption (`Dalc`, `Walc`) and family relation quality (`famrel`) rely on self-administered questionnaires.

---

## 📁 Repository Structure | هيكلية المستودع

```text
├── index.html           # Full self-contained interactive analytical web dashboard
├── student.csv          # Raw data file (395 records x 33 attributes)
├── student.txt          # Attribute metadata and dataset dictionary
└── README.md            # Comprehensive project documentation
```

---

## 🚀 How to Run Locally | التشغيل المحلي

1. Clone the repository:
   ```bash
   git clone https://github.com/username/repository-name.git
   ```
2. Open `index.html` directly in any modern web browser (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari). No server or npm build steps required!

---

## 👨‍💻 Author & Attribution | إعداد وتطوير
* **Concept, Analysis & Engineering:** Eng. Malek Joubi (م. مالك جوبي)
* **Tools Used:** Python (EDA & Machine Learning Feature Weights), Vanilla JavaScript, Chart.js, Tailwind CSS.
