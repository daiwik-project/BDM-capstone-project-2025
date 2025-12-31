# BDM-capstone-project-2025

# Strategic Analysis and Enhancement of Admission Dynamics at Aishwarya College 🎓

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![Domain](https://img.shields.io/badge/Domain-Business_Data_Management-blue)
![Tools](https://img.shields.io/badge/Tools-Microsoft_Excel_|_Pivot_Tables-green)
![Institute](https://img.shields.io/badge/Institute-IIT_Madras_BS_Degree-orange)

> **A Data-Driven Capstone Project by Daiwik Rankawat**  
> *Identifying a ₹1 Crore revenue leakage and formulating a strategic roadmap to reverse a 47% admission decline.*

---

## 📑 Table of Contents
1. [Executive Summary](#-executive-summary)
2. [Chapter 1: The Problem Landscape](#-chapter-1-the-problem-landscape)
3. [Chapter 2: Data Collection & Methodology](#-chapter-2-data-collection--methodology)
4. [Chapter 3: Key Insights & Revenue Analysis](#-chapter-3-key-insights--revenue-analysis)
5. [Chapter 4: Strategic Recommendations (The 3 Pillars)](#-chapter-4-strategic-recommendations-the-3-pillars)
6. [Chapter 5: Implementation Roadmap](#-chapter-5-implementation-roadmap)
7. [Conclusion](#-conclusion)

---

## 🚀 Executive Summary

Aishwarya College, established in 2018, faced a critical challenge: a **47% decline in admissions** over three years (2021-2023). This project involved a rigorous analysis of admission data to identify the root causes of this decline.

The analysis revealed a systemic issue of **"Stream Switching"**—where students admitted into high-fee Science programs migrated to lower-fee Arts/Commerce programs due to a lack of perceived value and academic support. This, combined with transportation bottlenecks and program saturation, led to an estimated **₹1 Crore revenue leakage**.

This repository contains the data analysis, findings, and a proposed **3-Pillar Strategy** to revitalize admissions and secure financial stability.

---

## 📉 Chapter 1: The Problem Landscape

The institution is facing a "Structural Growth Bottleneck." The decline is not merely due to market forces but internal misalignments between student expectations and college infrastructure.

### 1.1 Admission Trend Analysis
The total number of admissions dropped significantly from **408 in 2021** to **217 in 2023**.

```mermaid
%%{init: {'theme':'dark'}}%%
graph LR
A["2021 - 408 Admissions"] -->|"12% Drop"| B["2022 - 359 Admissions"]
B -->|"39% Drop"| C["2023 - 217 Admissions"]
C --> D["CRITICAL & CRISIS POINT"]

style A fill:#4ade80,stroke:#ffffff,stroke-width:3px,color:#000000
style B fill:#facc15,stroke:#ffffff,stroke-width:3px,color:#000000
style C fill:#f87171,stroke:#ffffff,stroke-width:3px,color:#ffffff
style D fill:#000000,stroke:#f87171,stroke-width:4px,color:#ffffff

linkStyle 0 stroke:#38bdf8,stroke-width:3px
linkStyle 1 stroke:#38bdf8,stroke-width:3px
linkStyle 2 stroke:#f87171,stroke-width:3px

```

### 1.2 The "Hidden Failure": Stream Switching
A major discovery was that **32.3%** of students abandon their original academic stream after Class 12.

```mermaid
%%{init: {
  "theme": "base",
  "themeVariables": {
    "pie1": "#04b80b",
    "pie2": "#028af2",

    "pieTextColor": "#ffffff",
    "pieTitleTextColor": "#ffffff",

    "textColor": "#ffffff",
    "mainTextColor": "#ffffff",
    "labelTextColor": "#ffffff",
    "legendTextColor": "#ffffff",

    "pieTitleTextSize": "22px",
    "pieSectionTextSize": "16px"
  }
}}%%
pie showData
    title Student Stream Continuity (3-Year Avg)
    "Retained Stream" : 67.7
    "Switched Stream" : 32.3

```

### 1.3 Problem Hierarchy
Breaking down the core issues affecting the institution.

```mermaid
graph LR
    %% --- CENTRAL HUB ---
    Root(((CORE<br/>PROBLEMS)))

    %% --- BRANCH 1: REVENUE (Red Theme) ---
    Root ==> Rev{{Revenue<br/>Leakage}}
    Rev --> R1([High-Fee to<br/>Low-Fee Switching])
    Rev --> R2([Science to<br/>Arts Migration])
    Rev --> R3([Loss of ~20k<br/>per student])

    %% --- BRANCH 2: ENROLLMENT (Orange Theme) ---
    Root ==> Enr{{Enrollment<br/>Decline}}
    Enr --> E1([Outdated Program<br/>Perception])
    Enr --> E2([Lack of<br/>Career Focus])
    Enr --> E3([Gender<br/>Imbalance])

    %% --- BRANCH 3: INFRASTRUCTURE (Blue Theme) ---
    Root ==> Inf{{Infrastructure<br/>Gaps}}
    Inf --> I1([Transport<br/>Capacity Gap])
    Inf --> I2([Safety<br/>Concerns])
    Inf --> I3([Geographic<br/>Concentration])

    %% --- STYLING ---
    %% Root Style (Dark Grey)
    classDef rootStyle fill:#2d3436,stroke:#fff,stroke-width:4px,color:#fff,font-size:18px,font-weight:bold;
    
    %% Revenue Styles (Red/Pink)
    classDef revMain fill:#d63031,stroke:#fff,stroke-width:2px,color:#fff,font-size:14px,font-weight:bold;
    classDef revSub fill:#ff7675,stroke:#d63031,stroke-width:1px,color:#fff;

    %% Enrollment Styles (Orange/Yellow)
    classDef enrMain fill:#e17055,stroke:#fff,stroke-width:2px,color:#fff,font-size:14px,font-weight:bold;
    classDef enrSub fill:#fdcb6e,stroke:#e17055,stroke-width:1px,color:#2d3436;

    %% Infrastructure Styles (Blue/Cyan)
    classDef infMain fill:#0984e3,stroke:#fff,stroke-width:2px,color:#fff,font-size:14px,font-weight:bold;
    classDef infSub fill:#74b9ff,stroke:#0984e3,stroke-width:1px,color:#fff;

    %% Apply Styles
    class Root rootStyle;
    class Rev revMain;
    class R1,R2,R3 revSub;
    class Enr enrMain;
    class E1,E2,E3 enrSub;
    class Inf infMain;
    class I1,I2,I3 infSub;
```
### 1.4 The Vicious Cycle
How the current situation feeds into itself.

```mermaid
graph TD
    %% --- NODES ---
    A([Low Science<br/>Enrollment])
    B([Reduced<br/>Revenue])
    C([Less Investment<br/>in Labs/Faculty])
    D([Poor Program<br/>Perception])

    %% --- CONNECTIONS (Circular Flow) ---
    A ==> B
    B ==> C
    C ==> D
    D ==> A

    %% --- STYLING ---
    %% Gradient-like effect using distinct colors for each step of the decline
    classDef step1 fill:#ff9f43,stroke:#e67e22,stroke-width:2px,color:#fff,font-weight:bold;
    classDef step2 fill:#ee5253,stroke:#b33939,stroke-width:2px,color:#fff,font-weight:bold;
    classDef step3 fill:#ff6b6b,stroke:#c0392b,stroke-width:2px,color:#fff,font-weight:bold;
    classDef step4 fill:#feca57,stroke:#f39c12,stroke-width:2px,color:#2d3436,font-weight:bold;

    class A step1;
    class B step2;
    class C step3;
    class D step4;
```

---

## 📊 Chapter 2: Data Collection & Methodology

Data was collected from primary sources (admin logs) spanning three academic years. The raw data was cleaned, processed, and analyzed using Microsoft Excel.

### 2.1 Data Schema
The dataset comprises detailed student profiles.

```mermaid
classDiagram
    %% Styling
    classDef main fill:#0984e3,stroke:#fff,stroke-width:2px,color:#fff,font-weight:bold;
    classDef sub fill:#74b9ff,stroke:#0984e3,stroke-width:1px,color:#fff;

    class StudentData:::main {
        +String Name
        +String Gender
        +String Category
        +Date DOB
        +Float FamilyIncome
    }
    class AcademicData:::sub {
        +Float 10th_Percentage
        +Float 12th_Percentage
        +String Previous_Stream
        +Boolean Pre_Qualifying_Test
    }
    class AdmissionData:::sub {
        +String Program_Applied
        +String Field_of_Study
        +Date Admission_Date
        +String Mode_of_Study
    }
    class GeoData:::sub {
        +String Address
        +Int Pincode
        +Float Distance_From_College
    }

    StudentData --> AcademicData
    StudentData --> AdmissionData
    StudentData --> GeoData
```

### 2.2 Analysis Workflow
The step-by-step approach taken to derive insights.

```mermaid
graph TD
    %% --- NODES ---
    A([Raw Data Collection])
    B([Data Cleaning])
    C{Data Processing}
    D[Imputation]
    E[Normalization]
    F([Pivot Table Analysis])
    G([Trend Visualization])
    H{{Strategic Insights}}
    
    %% --- CONNECTIONS ---
    A ==> B
    B ==> C
    C -->|Fill Missing| D
    C -->|Standardize| E
    D --> F
    E --> F
    F ==> G
    G ==> H
    
    %% --- TOOLS SUBGRAPH ---
    subgraph Tools ["🛠️ Analysis Toolkit"]
        direction LR
        I[Excel Formulas]
        J[Pivot Charts]
        K[Staggered Histograms]
    end
    
    F -.-> Tools
    
    %% --- STYLING ---
    classDef start fill:#00b894,stroke:#fff,stroke-width:2px,color:#fff;
    classDef process fill:#0984e3,stroke:#fff,stroke-width:2px,color:#fff;
    classDef logic fill:#6c5ce7,stroke:#fff,stroke-width:2px,color:#fff;
    classDef endNode fill:#fdcb6e,stroke:#e17055,stroke-width:4px,color:#2d3436,font-weight:bold;
    classDef tool fill:#dfe6e9,stroke:#b2bec3,stroke-width:1px,color:#2d3436;

    class A,B start;
    class D,E,F,G process;
    class C logic;
    class H endNode;
    class I,J,K tool;
    
    style Tools fill:#f5f6fa,stroke:#b2bec3,stroke-width:2px,color:#2d3436
```

### 2.3 Variable Correlation Logic
We analyzed how different variables impacted the admission decision.

```mermaid
graph LR
    %% --- INPUTS ---
    A[Distance from College]
    C[12th Grade Stream]
    E[Pre-Qualifying Test]
    G[Gender]

    %% --- OUTPUTS ---
    B((Transport Need))
    D((Stream Switching Risk))
    F((Admission Quality))
    H((Program Preference))

    %% --- CONNECTIONS ---
    A ==>|High Correlation| B
    C ==>|High Correlation| D
    E -->|Medium Correlation| F
    G -->|Medium Correlation| H

    %% --- STYLING ---
    classDef input fill:#2d3436,stroke:#fff,stroke-width:2px,color:#fff;
    classDef highCorr fill:#d63031,stroke:#ff7675,stroke-width:4px,color:#fff,font-weight:bold;
    classDef medCorr fill:#0984e3,stroke:#74b9ff,stroke-width:2px,color:#fff;

    class A,C,E,G input;
    class B,D highCorr;
    class F,H medCorr;
```

---

## 💡 Chapter 3: Key Insights & Revenue Analysis

The most critical finding of this project is the quantification of revenue loss due to academic misalignment.

### 3.1 The ₹1 Crore Revenue Leakage
Students moving from Science (High Fee) to Arts (Low Fee) caused massive financial damage.

```mermaid
graph TD
    %% --- START ---
    Start(((Student Enters<br/>Class 12 Science)))

    %% --- DECISION POINT ---
    Start ==> Choice{{Admission<br/>Choice}}

    %% --- PATH 1: IDEAL (Green Theme) ---
    Choice -->|Ideal Path| C([B.Sc / BCA])
    C --> E[High Revenue:<br/>~32k/yr]

    %% --- PATH 2: ACTUAL (Red Theme) ---
    Choice -->|Actual Path| D([B.A. / B.Com])
    D --> F[Low Revenue:<br/>~21k/yr]

    %% --- FINANCIAL IMPACT CLUSTER ---
    subgraph Impact ["💸 FINANCIAL IMPACT"]
        direction TB
        G(Loss per Student:<br/>~11k - 20k)
        H(Total Switches:<br/>~150+)
        I{{Total Loss:<br/>~₹1 Crore}}
        
        F ==> G
        G ==> H
        H ==> I
    end

    %% --- STYLING ---
    classDef startNode fill:#2d3436,stroke:#fff,stroke-width:4px,color:#fff,font-weight:bold;
    classDef decision fill:#0984e3,stroke:#74b9ff,stroke-width:2px,color:#fff;
    
    classDef goodPath fill:#00b894,stroke:#55efc4,stroke-width:2px,color:#fff;
    classDef badPath fill:#d63031,stroke:#ff7675,stroke-width:2px,color:#fff;
    
    classDef impactBox fill:#2d3436,stroke:#d63031,stroke-width:2px,color:#fff;
    classDef finalLoss fill:#d63031,stroke:#fff,stroke-width:4px,color:#fff,font-size:16px,font-weight:bold;

    %% Apply Styles
    class Start startNode;
    class Choice decision;
    class C,E goodPath;
    class D,F badPath;
    class G,H impactBox;
    class I finalLoss;
    
    %% Subgraph Style
    style Impact fill:#dfe6e9,stroke:#b2bec3,stroke-width:2px,color:#2d3436
```

### 3.2 Transport Infrastructure Gap
A major barrier to entry for students living >15km away.

```mermaid
graph LR
    %% --- NODES ---
    Demand((Student Population<br/>Living > 15km))
    
    subgraph Gap_Analysis ["⚠️ The Infrastructure Gap"]
        direction TB
        Current[Current Capacity:<br/>2 Buses]
        Required[Required Capacity:<br/>8 Buses]
    end

    Result{{Lost Admissions<br/>due to Transport & Safety Issues}}

    %% --- CONNECTIONS ---
    Demand ==> Required
    Current -.->|Deficit of 6 Buses| Result

    %% --- STYLING ---
    %% Demand (Teal)
    classDef demand fill:#00cec9,stroke:#00b894,stroke-width:2px,color:#fff,font-weight:bold;
    
    %% Gap Analysis (Yellow/Orange for warning)
    classDef current fill:#ffeaa7,stroke:#fdcb6e,stroke-width:2px,color:#2d3436;
    classDef required fill:#fdcb6e,stroke:#e17055,stroke-width:2px,color:#2d3436,font-weight:bold;
    
    %% Result (Red for negative impact)
    classDef result fill:#ff7675,stroke:#d63031,stroke-width:4px,color:#fff,font-weight:bold,font-size:14px;

    %% Apply Styles
    class Demand demand;
    class Current current;
    class Required required;
    class Result result;
    
    %% Subgraph Styling
    style Gap_Analysis fill:#f5f6fa,stroke:#b2bec3,stroke-width:2px,stroke-dasharray: 5 5
```

### 3.3 Program Popularity vs. Market Trend
The disconnect between what the market wants and what students are choosing.

```mermaid
quadrantChart
    title Program Portfolio Analysis
    x-axis Low Market Demand --> High Market Demand
    y-axis Low Enrollment --> High Enrollment
    quadrant-1 Star Programs
    quadrant-2 Opportunity Gaps
    quadrant-3 Phase Out?
    quadrant-4 Cash Cows
    "B.Sc": [0.8, 0.3]
    "BCA": [0.9, 0.2]
    "B.A.": [0.3, 0.9]
    "B.Com": [0.5, 0.8]
```

### 3.4 Gender Distribution Imbalance
Analysis of gender ratios across streams.

```mermaid
graph TD
    %% --- ROOT ---
    Root(((Total<br/>Admissions)))

    %% --- SPLIT POINT ---
    Root ==> Split{Gender<br/>Split}

    %% --- MALE BRANCH (Teal Theme) ---
    Split --> Male([Male: Declining Trend])
    Male --> M_Insight[Science Stream<br/>Dominated by Males]

    %% --- FEMALE BRANCH (Purple Theme) ---
    Split --> Female([Female: Stable/Rising])
    Female --> F_Insight[Arts/Commerce<br/>Dominated by Females]

    %% --- STYLING ---
    classDef rootStyle fill:#2d3436,stroke:#fff,stroke-width:4px,color:#fff,font-weight:bold;
    classDef splitStyle fill:#b2bec3,stroke:#636e72,stroke-width:2px,color:#2d3436,font-weight:bold;
    
    %% Male Styles
    classDef maleNode fill:#00cec9,stroke:#00b894,stroke-width:2px,color:#fff,font-weight:bold;
    classDef maleInsight fill:#81ecec,stroke:#00cec9,stroke-width:1px,color:#2d3436;

    %% Female Styles
    classDef femaleNode fill:#a29bfe,stroke:#6c5ce7,stroke-width:2px,color:#fff,font-weight:bold;
    classDef femaleInsight fill:#dfe6e9,stroke:#a29bfe,stroke-width:1px,color:#2d3436;

    %% Apply Styles
    class Root rootStyle;
    class Split splitStyle;
    class Male maleNode;
    class M_Insight maleInsight;
    class Female femaleNode;
    class F_Insight femaleInsight;
```

---

## 🎯 Chapter 4: Strategic Recommendations (The 3 Pillars)

To reverse the trend, a three-pronged strategy is proposed.

### 4.1 The Strategy Framework

```mermaid
graph TD
    %% --- THE MAIN GOAL ---
    Goal{{GOAL:<br/>Reverse Decline &<br/>Recapture ₹1 Cr}}

    %% --- THE 3 PILLARS ---
    P1([Pillar 1:<br/>Academic Realignment])
    P2([Pillar 2:<br/>Admission Process])
    P3([Pillar 3:<br/>Strategic Outreach])

    %% --- ACTION ITEMS ---
    A1[Career-Oriented<br/>Programs]
    A2[Bridge<br/>Courses]

    B1[Scholarship<br/>Tests]
    B2[Incentivized<br/>Counseling]

    C1[Transport<br/>Expansion]
    C2[Parent-Specific<br/>Marketing]

    %% --- CONNECTIONS ---
    Goal ==> P1
    Goal ==> P2
    Goal ==> P3

    P1 --> A1
    P1 --> A2

    P2 --> B1
    P2 --> B2

    P3 --> C1
    P3 --> C2

    %% --- STYLING ---
    %% Goal Style (Gold/Premium)
    classDef goalStyle fill:#f1c40f,stroke:#f39c12,stroke-width:4px,color:#2c3e50,font-size:16px,font-weight:bold;

    %% Pillar 1 Style (Green/Growth)
    classDef p1Style fill:#2ecc71,stroke:#27ae60,stroke-width:2px,color:#fff,font-weight:bold;
    classDef aStyle fill:#bef2d6,stroke:#2ecc71,stroke-width:1px,color:#2d3436;

    %% Pillar 2 Style (Blue/Process)
    classDef p2Style fill:#3498db,stroke:#2980b9,stroke-width:2px,color:#fff,font-weight:bold;
    classDef bStyle fill:#d6eaf8,stroke:#3498db,stroke-width:1px,color:#2d3436;

    %% Pillar 3 Style (Purple/Outreach)
    classDef p3Style fill:#9b59b6,stroke:#8e44ad,stroke-width:2px,color:#fff,font-weight:bold;
    classDef cStyle fill:#e8daef,stroke:#9b59b6,stroke-width:1px,color:#2d3436;

    %% Apply Styles
    class Goal goalStyle;
    class P1 p1Style;
    class P2 p2Style;
    class P3 p3Style;
    class A1,A2 aStyle;
    class B1,B2 bStyle;
    class C1,C2 cStyle;
```

### 4.2 Pillar 1: Academic Innovation (Stopping the Leak)
Preventing stream switching by making Science/Tech attractive.

```mermaid
sequenceDiagram
    autonumber
    
    %% --- ACTORS ---
    actor S as 🎓 Student
    participant C as 🧑‍💼 Counselor
    participant A as 🏛️ College Admin

    %% --- PHASE 1: INTAKE (Deep Blue) ---
    rect rgb(20, 30, 60)
        Note over S, A: 🟦 PHASE 1: INITIAL CONTACT
        S->>A: Applies for Admission
        A->>S: Schedules Mandatory Counseling
    end

    %% --- PHASE 2: INTERVENTION (Deep Orange/Brown) ---
    rect rgb(60, 30, 10)
        Note over S, C: 🟧 PHASE 2: STRATEGIC GUIDANCE
        C->>S: Explains Career Value of Science/Tech
        C->>S: Offers "Bridge Course" for Confidence
    end

    %% --- PHASE 3: SUCCESS (Deep Green) ---
    rect rgb(10, 50, 20)
        Note over S, A: 🟩 PHASE 3: CONVERSION
        S->>A: Enrolls in B.Sc / BCA (Retained Stream)
        Note right of A: 💰 HIGHER REVENUE SECURED
    end
```

### 4.3 Pillar 2: The Scholarship Funnel
Converting high-potential students using a merit-based approach.

```mermaid
graph LR
    %% --- NODES ---
    Start((Inquiry))
    Test(Pre-Admission<br/>Scholarship Test)
    Analysis{Score<br/>Analysis}
    High([Offer Fee<br/>Waiver & Perks])
    Avg([Offer Career<br/>Counseling])
    Goal>CONVERSION]

    %% --- FLOW ---
    Start ==> Test
    Test ==> Analysis
    
    Analysis == High Score ==> High
    Analysis == Avg Score ==> Avg
    
    High ==> Goal
    Avg ==> Goal

    %% --- STYLING ---
    classDef startNode fill:#2d3436,stroke:#fff,stroke-width:2px,color:#fff,font-weight:bold;
    classDef processNode fill:#00b894,stroke:#00cec9,stroke-width:2px,color:#fff,font-weight:bold;
    classDef decisionNode fill:#0984e3,stroke:#74b9ff,stroke-width:2px,color:#fff,font-weight:bold;
    classDef offerNode fill:#6c5ce7,stroke:#a29bfe,stroke-width:2px,color:#fff;
    classDef goalNode fill:#fdcb6e,stroke:#e17055,stroke-width:4px,color:#2d3436,font-weight:bold,font-size:14px;

    class Start startNode;
    class Test processNode;
    class Analysis decisionNode;
    class High,Avg offerNode;
    class Goal goalNode;
```

### 4.4 Pillar 3: Infrastructure & Outreach
Addressing the physical barriers to entry.

```mermaid
graph TD
    %% --- MARKETING CLUSTER (Green Theme) ---
    subgraph Marketing ["📢 Marketing Strategy"]
        direction TB
        M_Budget([Budget: ~14 Lakhs]) ==> M_Alloc{Allocation}
        M_Alloc --> M1[Digital<br/>Campaigns]
        M_Alloc --> M2[School<br/>Partnerships]
        M_Alloc --> M3[Parent<br/>Outreach]
    end

    %% --- TRANSPORT CLUSTER (Blue Theme) ---
    subgraph Transport ["🚌 Transport Solution"]
        direction TB
        T_Issue([Transport<br/>Bottleneck]) ==> T_Sol{Strategic<br/>Fixes}
        T_Sol --> T1[Hire More<br/>Vehicles]
        T_Sol --> T2[Hostel<br/>Feasibility]
    end

    %% --- STYLING ---
    %% Marketing Styles
    classDef mMain fill:#00b894,stroke:#fff,stroke-width:2px,color:#fff,font-weight:bold;
    classDef mSub fill:#55efc4,stroke:#00b894,stroke-width:1px,color:#2d3436;
    
    %% Transport Styles
    classDef tMain fill:#0984e3,stroke:#fff,stroke-width:2px,color:#fff,font-weight:bold;
    classDef tSub fill:#74b9ff,stroke:#0984e3,stroke-width:1px,color:#fff;

    %% Apply Styles
    class M_Budget,M_Alloc mMain;
    class M1,M2,M3 mSub;
    
    class T_Issue,T_Sol tMain;
    class T1,T2 tSub;

    %% Subgraph Backgrounds (Dark Mode Compatible)
    style Marketing fill:#2d3436,stroke:#00b894,stroke-width:2px,color:#fff
    style Transport fill:#2d3436,stroke:#0984e3,stroke-width:2px,color:#fff
```

---

## 📅 Chapter 5: Implementation Roadmap

A phased approach to executing the strategy over the next 12 months.

### 5.1 The Timeline (Gantt Chart)

```mermaid
gantt
    title 🚀 Strategic Implementation Roadmap (2024-2025)
    dateFormat  YYYY-MM-DD
    axisFormat  %b %y
    excludes    weekends

    section 🏗️ Phase 1: Foundation
    Form Task Force           :crit, a1, 2024-05-01, 30d
    Finalize New Curricula    :a2, after a1, 60d
    Design Scholarship Test   :crit, a3, after a1, 45d
    
    section ⚡ Phase 2: Execution
    Launch Marketing Campaign :active, b1, 2024-09-01, 90d
    Conduct Scholarship Tests :b2, after b1, 60d
    Secure Transport Contracts:active, b3, 2024-11-01, 60d
    
    section 📈 Phase 3: Optimization
    Launch New Programs       :c1, 2025-03-01, 120d
    Implement Data Dashboard  :crit, c2, 2025-06-01, 90d
    Final Review & Scale      :active, c3, 2025-10-01, 2025-12-31
```

### 5.2 The Virtuous Cycle of Growth
The expected outcome of implementing these strategies.

```mermaid
graph TD
    %% --- NODES ---
    Start((START))
    A([Higher Quality<br/>Admissions])
    B([Investment in<br/>Faculty & Labs])
    C([Stronger<br/>Reputation])
    D([Reduced Stream<br/>Switching])
    E([Increased<br/>Revenue])

    %% --- CONNECTIONS (The Loop) ---
    Start ==> A
    A ==> B
    B ==> C
    C ==> D
    D ==> E
    E ==> A

    %% --- STYLING ---
    %% Green/Teal Theme for Growth
    classDef startNode fill:#2d3436,stroke:#fff,stroke-width:2px,color:#fff,font-weight:bold;
    classDef growth1 fill:#00b894,stroke:#006266,stroke-width:2px,color:#fff,font-weight:bold;
    classDef growth2 fill:#55efc4,stroke:#00b894,stroke-width:2px,color:#2d3436,font-weight:bold;
    classDef growth3 fill:#81ecec,stroke:#00cec9,stroke-width:2px,color:#2d3436,font-weight:bold;
    classDef growth4 fill:#74b9ff,stroke:#0984e3,stroke-width:2px,color:#fff,font-weight:bold;
    classDef growth5 fill:#a29bfe,stroke:#6c5ce7,stroke-width:2px,color:#fff,font-weight:bold;

    class Start startNode;
    class A growth1;
    class B growth2;
    class C growth3;
    class D growth4;
    class E growth5;
```

---

## ✅ Conclusion

The data has illuminated the path forward. By addressing the **₹1 Crore revenue leakage** through academic realignment and fixing the **transportation bottleneck**, Aishwarya College can convert its current challenges into a catalyst for future success.

**Key Outcomes Expected:**
1.  **Revenue Recovery:** Recapture lost revenue from stream switching.
2.  **Admission Growth:** Reverse the decline and aim for 400+ admissions.
3.  **Brand Positioning:** Establish a reputation for career-focused Science & Tech education.

---

## 📂 Repository Structure

```bash
├── Data/
│   ├── Raw_Admission_Data_2021_2023.xlsx
│   └── Processed_Analysis.csv
├── Reports/
│   ├── Project_Proposal.pdf
│   ├── Mid_Term_Report.pdf
│   └── Final_Capstone_Report.pdf
├── Presentation/
│   └── Strategic_Roadmap_Presentation.pdf
├── Visualizations/
│   ├── Revenue_Leakage_Chart.png
│   └── Stream_Switching_Sankey.png
└── README.md
```

---

## 👨‍💻 Author

**Daiwik Rankawat**  
*BS in Data Science and Applications, IIT Madras   -2027 (Graduate)*  
*B.Sc in Biology, JNVU -2023 (Graduate)*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/daiwik-rankawat/) 
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/daiwik-project)

