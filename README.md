# 📊 Student Social Media Behavioral Analytics — Power BI Dashboard

[![Power BI](https://img.shields.io/badge/Visualization-Power%20BI%20Desktop-F2C811.svg?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/Analytics-Advanced%20DAX%20Measures-orange.svg)](https://github.com/mailmetanmaymandal92)
[![Domain](https://img.shields.io/badge/Domain-Education%20%26%20Behavioral%20Psychology-blue.svg)](https://github.com/mailmetanmaymandal92)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An interactive Power BI business intelligence dashboard analyzing the empirical correlation between daily social media screen time, academic GPA performance, sleep quality, and student mental wellness.

## 📋 Business Problem & Objective
Academic institutions and student counseling services needed an interactive visual analytics platform to quantify the impact of excessive social media screen time on academic achievements and mental health indicators across student cohorts.

## 📊 Dataset & Scope
- **Source**: University Student Behavioral & Academic Survey Dataset (`data/Students Social Media Addiction.xlsx`).
- **Scale**: 1,200 survey responses across multiple undergraduate majors.
- **Attributes**: `Student_ID`, `Age`, `Gender`, `Major`, `Daily_Screen_Time_Hours`, `Preferred_Platform`, `GPA`, `Sleep_Hours`, `Stress_Level`, `Academic_Distraction_Score`.

## 📈 Dashboard Highlights

| Academic Impact & Performance | Mental Health & Lifestyle |
|---|---|
| ![Academic Impact](./screenshots/academic_impact.png) | ![Mental Health](./screenshots/mental_health_&_lifestyle.png) |
| **Interactive Story View** | **Drill Through Profile** |
| ![Story View](./screenshots/interactive_story_view.png) | ![Drill Through](./screenshots/drill_through_student_profile.png) |

## 🔬 Methodology & DAX Engineering
1. **Star Schema Data Modeling**: Structured survey responses with dedicated dimension tables for demographic cohorts and platforms.
2. **Custom DAX KPI Measures**:
   - `Avg_GPA_By_ScreenTime = CALCULATE(AVERAGE(Students[GPA]), ALLEXCEPT(Students, Students[ScreenTime_Tier]))`
   - `HighRisk_Addiction_Rate = DIVIDE(CALCULATE(COUNTROWS(Students), Students[Daily_Screen_Time_Hours] > 4), COUNTROWS(Students), 0)`
3. **Interactive Slicers & Tooltips**: Dynamic cross-filtering across academic majors, preferred platforms, and gender demographics.

## 🔍 Key Findings & Insights
- **GPA Inversion Threshold**: Students with daily screen time exceeding 4.5 hours experienced a statistically significant average GPA drop of 0.62 points compared to moderate users (<2 hours).
- **Platform Disparity**: High usage of video-first platforms (TikTok, Instagram) correlated with higher reported anxiety scores and shorter sleep durations (average 5.2 hrs/night).
- **Major Vulnerability**: STEM students showed higher sensitivity in grade drop per additional hour of non-academic screen time.

## 💻 Tech Stack
- **BI Tool**: Power BI Desktop, DAX Formula Engine
- **Deliverables**: Interactive `.pbix` workbook (`dashboards/social_media_dashboard.pbix`) and executive PDF report (`dashboards/social_media_dashboard.pdf`).

## 🚀 How to Run / Reproduce
1. Clone the repository:
   ```bash
   git clone https://github.com/mailmetanmaymandal92/PowerBI-Student-Social-Media-Impact.git
   ```
2. Open `dashboards/social_media_dashboard.pbix` in [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).

---

## 👤 Author & Contact

**Tanmay Mandal** &bull; Data Analyst | Business Intelligence & Analytics Specialist  
- 🌐 **GitHub**: [mailmetanmaymandal92](https://github.com/mailmetanmaymandal92)  
- 💼 **LinkedIn**: [Tanmay Mandal](https://www.linkedin.com/in/tanmay-mandal-83976131a/)  
- 📧 **Email**: [mailme.tanmaymandal@gmail.com](mailto:mailme.tanmaymandal@gmail.com)
