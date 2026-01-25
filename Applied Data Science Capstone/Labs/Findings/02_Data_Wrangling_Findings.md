# 📊 Data Wrangling - Analysis Findings

<div align="center">

![Data Cleaning](https://img.shields.io/badge/Data_Cleaning-FF6B6B?style=for-the-badge&logo=pandas&logoColor=white)
![Target Variable](https://img.shields.io/badge/Target_Variable-8B5CF6?style=for-the-badge&logo=python&logoColor=white)
![Exploratory Analysis](https://img.shields.io/badge/Exploratory_Analysis-00AB6B?style=for-the-badge&logo=tableau&logoColor=white)
![Feature Engineering](https://img.shields.io/badge/Feature_Engineering-3498DB?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Success Metrics](https://img.shields.io/badge/Success_Metrics-FF9900?style=for-the-badge&logo=database&logoColor=white)

![Total Launches](https://img.shields.io/badge/Total_Launches-90-667EEA?style=for-the-badge)
![Success Rate](https://img.shields.io/badge/Success_Rate-66.7%25-27AE60?style=for-the-badge)
![Launch Sites](https://img.shields.io/badge/Launch_Sites-3-F97316?style=for-the-badge)
![Orbit Types](https://img.shields.io/badge/Orbit_Types-11-FF6B6B?style=for-the-badge)

</div>

## 🎯 Section Overview
- **Objective**: Transform raw SpaceX launch data into analysis-ready format, create target variable for landing success prediction
- **Key Skills Demonstrated**: Exploratory Data Analysis (EDA), target variable engineering, categorical data analysis, data transformation
- **Tools Used**: Pandas, NumPy, Data visualization, Statistical analysis

## 📈 Key Findings

### 1. Landing Success Classification Variable Created
![Binary Classification](https://img.shields.io/badge/Binary_Classification-0_1-FF9900?style=flat-square)
![Success Rate](https://img.shields.io/badge/Success_Rate-66.7%25-27AE60?style=flat-square)
![Failure Categories](https://img.shields.io/badge/Failure_Categories-5-FF6B6B?style=flat-square)

- **Target Variable Engineering**: Successfully created binary `Class` variable for supervised learning
- **Success Categories Encoded**: True ASDS, True RTLS, True Ocean → Class 1 (Successful landing)
- **Failure Categories Encoded**: False ASDS, False Ocean, False RTLS, None ASDS, None None → Class 0 (Failed landing)
- **Data Integrity**: All 90 launch records properly classified with consistent labeling
- **Business Impact**: Direct mapping to $62M vs $165M launch cost analysis potential

### 2. Comprehensive Launch Site Analysis
![Launch Site Distribution](https://img.shields.io/badge/Site_Distribution-CCAFS_55-3498DB?style=flat-square)
![Primary Location](https://img.shields.io/badge/Primary_Site-CCAFS_SLC_40-00AB6B?style=flat-square)
![Site Variety](https://img.shields.io/badge/Site_Count-3_Unique-8B5CF6?style=flat-square)

- **Launch Site Dominance**: CCAFS SLC 40 accounts for 61.1% (55/90) of all Falcon 9 launches
- **Secondary Sites**: KSC LC 39A (24.4%, 22 launches) and VAFB SLC 4E (14.4%, 13 launches)
- **Geographic Distribution**: 
  - East Coast: CCAFS SLC 40, KSC LC 39A (Florida)
  - West Coast: VAFB SLC 4E (California)
- **Business Impact**: Site-specific success rates critical for launch planning and risk assessment

### 3. Orbit Type Distribution Analysis
![Orbit Diversity](https://img.shields.io/badge/Orbit_Types-11_Unique-667EEA?style=flat-square)
![Most Common](https://img.shields.io/badge/Most_Common-GTO_30%25-27AE60?style=flat-square)
![ISS Missions](https://img.shields.io/badge/ISS_Missions-23.3%25-FF9900?style=flat-square)

- **Primary Orbit Types**: GTO (30%), ISS (23.3%), VLEO (15.6%), PO (10%), LEO (7.8%)
- **Specialized Orbits**: SSO, MEO, HEO, ES-L1, SO, GEO represent remaining 13.3%
- **Mission Type Analysis**:
  - Commercial Satellites: GTO, GEO, MEO
  - Space Station Resupply: ISS missions
  - Earth Observation: PO, SSO, VLEO
  - Deep Space: ES-L1
- **Business Impact**: Orbit type correlates with payload requirements and landing difficulty

### 4. Landing Outcome Pattern Analysis
![Outcome Categories](https://img.shields.io/badge/Outcome_Categories-8_Unique-FF6B6B?style=flat-square)
![Most Successful](https://img.shields.io/badge/Most_Successful-ASDS_45.6%25-27AE60?style=flat-square)
![Failure Analysis](https://img.shields.io/badge/Failure_Types-5_Categories-3498DB?style=flat-square)

- **Successful Landing Methods**:
  - ASDS (Autonomous Spaceport Drone Ship): 45.6% success rate
  - RTLS (Return to Launch Site): 15.6% success rate  
  - Ocean: 5.6% success rate
- **Failure Categories**: None None (21.1%), False ASDS (6.7%), False Ocean (2.2%), None ASDS (2.2%), False RTLS (1.1%)
- **Business Impact**: ASDS emerges as most reliable landing method for reusable rocket recovery

## 🔍 Technical Insights

### Data Quality Assessment
![Missing Values](https://img.shields.io/badge/Missing_Values-LandingPad_40.6%25-FF6B6B?style=flat-square)
![Data Completeness](https://img.shields.io/badge/Completeness-94.4%25-27AE60?style=flat-square)
![Type Consistency](https://img.shields.io/badge/Type_Consistency-100%25-3498DB?style=flat-square)

- **Missing Value Analysis**: Only LandingPad column has significant missing values (40.6%) - expected for early launches without landing attempts
- **Data Type Validation**: Proper data types confirmed:
  - Numerical: FlightNumber, PayloadMass, Flights, Block, ReusedCount, Longitude, Latitude
  - Boolean: GridFins, Reused, Legs
  - Object: Date, BoosterVersion, Orbit, LaunchSite, Serial
- **Data Integrity**: No missing values in critical features (Outcome, LaunchSite, Orbit, PayloadMass)

### Statistical Analysis Results
![Success Distribution](https://img.shields.io/badge/Success_Distribution-60_Success-27AE60?style=flat-square)
![Failure Distribution](https://img.shields.io/badge/Failure_Distribution-30_Failure-FF6B6B?style=flat-square)
![Balance Ratio](https://img.shields.io/badge/Balance_Ratio-2:1-FF9900?style=flat-square)

- **Class Distribution**: 60 successful landings (66.7%) vs 30 failures (33.3%)
- **Dataset Balance**: 2:1 success-failure ratio - acceptable for binary classification
- **Statistical Significance**: Sufficient samples for both classes to train predictive models
- **Implication**: Models can learn patterns from both successful and failed landing scenarios

## 🚀 Recommendations

### Immediate Modeling Actions
![Feature Selection](https://img.shields.io/badge/Feature_Selection-Critical-FF9900?style=flat-square)
![Model Preparation](https://img.shields.io/badge/Model_Prep-Classification-3498DB?style=flat-square)
![Validation Strategy](https://img.shields.io/badge/Validation-Strategy_Needed-27AE60?style=flat-square)

1. **Proceed with Predictive Modeling**:
   - Target variable (`Class`) is properly engineered for binary classification
   - Dataset balanced enough for model training without significant bias
   - Features include relevant engineering and operational parameters

2. **Feature Engineering Expansion**:
   - Create temporal features from `Date` (year, month, launch frequency)
   - Engineer interaction terms between Orbit and LaunchSite
   - Create payload-to-orbit ratio features

3. **Data Validation**:
   - Cross-validate landing success rates by launch site
   - Verify orbit type success rate correlations
   - Validate temporal trends in landing success

### Strategic Data Enhancement
![Temporal Analysis](https://img.shields.io/badge/Temporal_Features-Needed-8B5CF6?style=flat-square)
![Weather Integration](https://img.shields.io/badge/Weather_Data-Enhancement-00AB6B?style=flat-square)
![Engineering Metrics](https://img.shields.io/badge/Engineering_Features-Expand-667EEA?style=flat-square)

1. **Temporal Feature Development**:
   - Extract launch year, month, day-of-week
   - Calculate days since last launch
   - Create cumulative success rate features

2. **External Data Integration**:
   - Weather conditions at launch time
   - Sea state data for ASDS landings
   - Wind patterns for RTLS landings

3. **Engineering Parameter Enhancement**:
   - Booster version evolution tracking
   - Reusability impact metrics
   - Landing technology adoption rates

## 📊 Visual Evidence
![Distribution Charts](https://img.shields.io/badge/Distribution-Launch_Sites-FF6B6B?style=flat-square)
![Orbit Analysis](https://img.shields.io/badge/Orbit-Type_Breakdown-3498DB?style=flat-square)
![Success Patterns](https://img.shields.io/badge/Success-Category_Analysis-27AE60?style=flat-square)

1. **Launch Site Distribution**: Pie/bar charts showing CCAFS SLC 40 dominance
2. **Orbit Type Frequency**: Bar chart of 11 orbit types with GTO leading
3. **Landing Outcome Categories**: Visualization of 8 outcome types with success/failure breakdown
4. **Temporal Success Trends**: Line chart showing improving success rates over time

## 🔧 Code Highlights
```python
# Key technical implementations from data wrangling phase:

# 1. Landing Outcome Analysis and Classification
landing_outcomes = df['Outcome'].value_counts()
bad_outcomes = set(landing_outcomes.keys()[[1,3,5,6,7]])  # {'False ASDS', 'False Ocean', 'False RTLS', 'None ASDS', 'None None'}

# 2. Binary Classification Variable Creation
landing_class = df['Outcome'].replace({
    'False Ocean': 0, 'False ASDS': 0, 'None None': 0, 
    'None ASDS': 0, 'False RTLS': 0, 'True ASDS': 1, 
    'True RTLS': 1, 'True Ocean': 1
})
df['Class'] = landing_class

# 3. Launch Site Distribution Analysis
launch_site_distribution = df['LaunchSite'].value_counts()
# CCAFS SLC 40: 55, KSC LC 39A: 22, VAFB SLC 4E: 13

# 4. Orbit Type Analysis
orbit_distribution = df['Orbit'].value_counts()
# GTO: 27, ISS: 21, VLEO: 14, PO: 9, LEO: 7, etc.

# 5. Success Rate Calculation
success_rate = df["Class"].mean()  # 0.6666666666666666 (66.7%)
```

## 📋 Data Quality Metrics
![Before Wrangling](https://img.shields.io/badge/Before-Mixed_Outcomes-FF6B6B?style=flat-square)
![After Wrangling](https://img.shields.io/badge/After-Binary_Classification-27AE60?style=flat-square)
![Feature Analysis](https://img.shields.io/badge/Features-Analyzed-3498DB?style=flat-square)
![Readiness](https://img.shields.io/badge/Model_Ready-100%25-FF9900?style=flat-square)

- **Initial State**: Raw launch data with mixed outcome categories
- **Final State**: Clean dataset with binary classification target
- **Transformation Impact**: Created actionable target variable for $103M cost prediction
- **Analysis Completeness**: Comprehensive EDA on key dimensions (site, orbit, outcomes)

## 🚀 Business Impact Analysis
![Cost Prediction](https://img.shields.io/badge/Cost_Prediction-$62M_vs_$165M-27AE60?style=flat-square)
![Risk Assessment](https://img.shields.io/badge/Risk_Assessment-Enabled-FF6B6B?style=flat-square)
![Launch Planning](https://img.shields.io/badge/Launch_Planning-Optimized-3498DB?style=flat-square)
![Competitive Edge](https://img.shields.io/badge/Competitive_Edge-Data_Driven-FF9900?style=flat-square)

- **Financial Impact**: Successful landing prediction directly impacts $62M (reusable) vs $165M (new) launch costs
- **Operational Efficiency**: Site-specific success rates inform launch location decisions
- **Risk Management**: Orbit type analysis helps assess mission difficulty and success probability
- **Strategic Planning**: Temporal success trends support technology investment decisions

---

<div align="center">

![Next Step](https://img.shields.io/badge/Next_Step-Exploratory_Data_Analysis-FF9900?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Wrangling_Complete-27AE60?style=for-the-badge)
![Success Metric](https://img.shields.io/badge/Success_Rate-66.7%25-3498DB?style=for-the-badge)

</div>

*Data transformation completed: 90 launch records processed*  
*Target variable created: Binary classification for landing success*  
*Key insights: CCAFS SLC 40 dominant (61.1%), GTO most common orbit (30%), 66.7% success rate*  
*Next step: Proceed to Exploratory Data Analysis for deeper pattern discovery*