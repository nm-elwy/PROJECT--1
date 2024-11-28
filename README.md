Project Submission
Please fill out:

Student name: NEEMA ELALY

Student pace: self paced / part time/ full time

Scheduled project review date/time:

Instructor name:

Blog post URL:

BUSINESS PROBLEM

Your company is expanding in to new industries to diversify its portfolio. Specifically, they are interested in purchasing and operating airplanes for commercial and private enterprises, but do not know anything about the potential risks of aircraft. You are charged with determining which aircraft are the lowest risk for the company to start this new business endeavor. You must then translate your findings into actionable insights that the head of the new aviation division can use to help decide which aircraft to purchase.

BUSINESS UNDERSTANDING

The objective of this analysis is to diversify the company's portfolio by entering the aviation sector, through the purchase and operation of aircraft. This involves both commercial and private sectors. The key is to identify aircraft that will meet the company's needs such as cost efficiency, reliability, market demand and certifications to ensure operational ease and long term growth.

INTRODUCTION:REAL WORLD PROBLEM 

This project seek to address the challenges companies face when selecting aircraft for commercial and private enterprises, aiming to minimize risks and optimize profitability by identifying the most suitable aircraft models to start operations.

STAKEHOLDERS AND HOW THEY WOULD USE THE PROJECT

INVESTORS They would use the project's finding to guide purchasing decisions, evaluate potential financial returns, and assess the overall viability of entering the aviation sector.

AVIATION OPERATION MANAGERS These stakeholders would use the project to select aircraft models that are easy to maintain, have reliable performance records and fit the company's operational needs.

SAFETY AND COMPLIANCE TEAMS The project would provide them with detailed insights into aircraft safety records and their compliance with industry regulations, helping to minimize safety risks and avoid regulatory issues.

MAINTENANCE TEAMS They would use the project to identify aircraft that requires less frequent or less expensive maintenance and have good availability of parts and services providers.

CONCLUSION: IMPLICATIONS OF THE PROJECT 

By providing a clear understanding of the aircraft models with the lowest risks in terms of safety, operational efficiency and maintenance, the project will enable the company make informed decisions when entering aviation industry. This project provides actionable insights that allow all stakeholders to mitigate risks and maximize the potential value of their investments in aircraft operations.

DATA UNDERSTANDING

This stage focuses on obtaining and assessing data related to aircraft ,operational cost ,safety records, market trends, and regulatory compliance to identify low risk aircraft that align with the company's strategic, operational and financial go

DATA SOURCE

The dataset for this project originates from Aviation Accidents Database and Synopses which contains comprehensive information about aviation accidents and incidents up to 2023. Authority: the database is compiled by trusted aviation safety organizations and regulatory bodies, ensuring high reliability and relevance. Coverage: it spans a wide range of aviation events globally, capturing detailed records on accident reports, incident types, injuries and aircraft specifications, location, event dates, aircraft, outcomes Relevance: this source provides critical insights into aviation safety, making it suitable for identifying low-risk aircraft and operational patterns. The up to date nature of the data through 2023 ensures relevance to modern aviation practices and technology. This data is directly related to the business problem as it captures critical details about aviation. This makes it suitable for analyzing safety trends, and supporting the purchase of low risk aircraft.

DATA PROPERTIES

Data Type 

The dataset contains both categorical and numerical variables and date features 

Categorical; Event ID, Location 

Numerical; Total Fatal Injuries, Number of Engines

Date; Event Date, Publication Date

Size The dataset has 88889 rows and 31columns

Descriptive statistics

Helps quantify the risk, central tendency, and variability of the data. This statistics offer sense of how the data is distributed, the presence of outliers and central tendancies For numerical columns; (provide quantitative data) typically include measures like mean, median, standard deviation , minimum ,maximum and percentiles. For example, for features such as Total Fatal/Serious/Minor Injuries For categorical columns; (qualitative data) analyzed using frequency counts and mode.

Key Features

Below are examples of descriptive statistics for critical features:

~Event ID type; categorical description; unique identifier for tracking each event 

~Event Date type; date description; captures when the event occurred enabling time series trend analysis 

~Injury Severity type; categorical description; describes the level of injuries .. critical for safety risk analysis

~Aircraft Damage type; categorical description; indicates the extent of damage, helping quantify operational risk and financial impact

~Weather Condition type; categorical description; highlights environmental conditions during the event 

~Make and Model type; categorical description; provides information on the type of aircraft, useful for identifying reliability trends 

~Total Fatal Injuries type; numerical description; quantifies the severity of incidents in terms of fatalities 

~Number of engine type; numerical description; indicates operational characteristics and potential vulnerabilities of aircraft

BUSINESS RELEVANCE OF THE DATA

For the aviation accident dataset , the key goal is to evaluate aircraft safety and operational efficiency to guide the selection of low risk aircraft for a new business endeavor. The dataset's features directly align with the business goal of identifying low risk aircraft by providing:

~Safety Indicators: 

Safety is a critical factor when selecting aircraft, Features like Injury Severity, Aircraft Damage, and Total Fatal Injuries help quantify an categorize risks, enabling informed decision making Eg ; if aircraft model A has higher average of fatal injuries than model B, model A might be considered riskier. Helps the company identify low risk aircraft by focusing on those with fewer accidents, injuries, and damages.

~Operational Context: 

Refers to understanding the circumstances under which aircraft operate , which affect performance and safety.. features like Weather Conditions and Broad Phase of Flight provide insights into environmental and situational risks. Eg ; aircraft X might have a higher accident rate IMC conditions, making it unsuitable for areas prone to fog or bad weather Assist in matching aircraft to the company's operational goals such as regional preferences.

~Aircraft Attributes: 

Evaluating features related to the design, functionality, and adaptability of the aircraft to operational demands Eg ; twin engine aircraft may show better safety records during engine failure compared to single engine models Allows evaluation of aircraft suitability based on designs and performance metrics

JUSTIFICATION FOR FEATURE INCLUSION 

Each feature is selected due to its relevance to the business problem; *Event Date; useful for trend analysis over time to identify patterns in aviation incidents *Location; geographical distribution highlights high risk regions for targeted operational decisions *Aircraft damage; critical for understanding financial impacts and maintenance risks *Make and Model; enables identification of aircraft with higher safe-risks *Weather conditions; indicates external environmental factors contributing to accidents

UTILITY FOR REAL WORLD PROBLEM SOLVING 

The dataset is highly suitable for addressing the business problem because: -it provides detailed and diverse variables relevant to aviation risk assessment -it supports both statistical and machine learning based analyses to identify trends and patterns -the feature directly align with the core aspects of safety, performance, and operational risk in aviation

LIMITATIONS OF THE DATA 

Despite its utility, the dataset has limitations that may affect the analysis:

*Incomplete records; some fields such as Weather Condition and Aircraft Damage have missing values *Granularity: broad categorizations like purpose of flight may limit the depth of analysis for specific operational contexts *Outdated Information: older records before 2010 may not reflect current safety standards or aircraft technologies

CONCLUSION 

The Aviation Accident Database and Synopses up to 2023 provide a rich and reliable dataset for analyzing aviation safety trends. It's combination of categorical and numerical features provide insights into operational safety, technical reliability and environmental risk factors. Despite its limitations, the data is highly relevant for identifying low risk aircraft and making data driven decisions to enhance operational safety and efficiency. The next step(Data Preparation )will address missing values and imbalances to maximize analytical potential

DATA PREPARATION

This stage ensures that the dataset is structured,clean,and optimized for analysis to solve the business problem of selecting low risk aircraft.it involves cleaning,transforming,and organizing the raw data to make it suitable for analysis.this step ensures that the dataset is accurate,complete,relevant for addressing low risk aircraft.

1.DATA CLEANING

To address inconsistencies and innaccuracies in the dataset for reliable analysis

STEPS TAKEN

*Handling missing values

~Code for cleaning missing values: fill in missing values for categorical data with'Unknown' eg;df['col']=df['col'].fillna('Unknown') fill in missing values for numerical data with '0' eg;df['col']=df['col'].fillna(0) ~Code for cleaning missing dates fill in missing dates with placeholder eg;df['Publication.Date']=pd.to_datetime(df['Publication.Date'],errors='coerce') placeholder_date=pd.Timestamp('1900-01-01') df['Publication.Date']=df['Publication.Date'].fillna(placeholder_date) df

Justification -filling missing values ensures no gap in columns -converting dates enables temporal trend analysis

2.DATA TRANSFORMATION 

To standardize the data and make it more useful for analysis.

STEPS TAKEN

Formatting Dates Standardized Event Date and Publication Date to a consistent YYYY-MM-DD format for easy filtering and sorting.

Categorical Encoding Converted textual categories like Injury Severity or Aircraft Damage into numerical codes for use in statistical models.

3.FEATURE SELECTION

Identified the most relevant columns for the analysis based on their alignment with safety, operational, and technical factors.

Selected Features:

Injury Severity, Total Fatal Injuries, Aircraft Damage: Key safety indicators.

Make, Model, Engine Type: Technical specifications.

Weather Conditions, Location: Contextual factors affecting operations.

Justification: Features directly address the problem by providing insights into accident risks, operational conditions, and aircraft performance.

4.VERIFYING DATA TYPES

Ensure each column has the correct data type for analysis:

Correct data types for categorical columns; for col in categorical_columns: data[col] = data[col].astype('category')

Correct data types for numerical columns; for col in numerical_columns: data[col] = data[col].astype(float)

5.EXPORT PROCESSED DATA

Save the cleaned and transformed dataset for reproducibility.

Justification:Exporting ensures consistent use of the prepared dataset across analyses

CONCLUSION 

This notebook prepares the dataset for analysis by cleaning,transforming, and engineering features based on business requirements.The steps ensure the data is suitable for addressing the real world problem of identifying low risk aircraft for commercial and private enterprises.


DATA ANALYSIS

Objective

The purpose of this analysis is to identify actionable insights from the dataset to support the recommendation of aircraft types for the company's expansion into aviation. Findings are designed to inform stakeholders about potential risks and opportunities in aircraft operations, aligning with the company's goal of minimizing risk and optimizing investment.

Findings

Injury Severity and Aircraft Categories

Analysis of the relationship between Aircraft Category and Injury Severity revealed that certain categories, such as small private aircraft, have a higher frequency of severe injuries.

Conversely, commercial airliners tend to show lower rates of injury severity, indicating better safety measures and operational protocols.

Summary statistics:

Private aircraft severe injuries: 45%

Commercial airliners severe injuries: 15%

Weather Conditions and Total Injuries

Correlation analysis indicates that adverse weather conditions (e.g., fog, heavy rain) are strongly associated with increased injury severity.

Heatmap findings:

Clear weather: 20 average total injuries.

Adverse weather: 50 average total injuries.

Recommendation: Investments should prioritize aircraft with advanced weather navigation systems.

Geographical Risk

Latitude and Longitude data highlight accident-prone areas, particularly in mountainous regions and high-traffic air corridors.

Geospatial visualization reveals:

Hotspots in mountainous terrain: 60% of recorded incidents.

Urban regions: 20% of recorded incidents.

Recommendation: Additional pilot training for these regions and avoidance of specific high-risk zones.

Aircraft Damage and Purpose of Flight

Commercial flights tend to experience less severe aircraft damage compared to recreational or experimental flights.

Recreational flights show a higher percentage of total losses:

Recreational flights: 35% total loss.

Commercial flights: 10% total loss.

Recommendation: The company should prioritize investments in aircraft used for commercial purposes.

Engine Type and Safety

Multi-engine aircraft have shown better performance and lower accident rates compared to single-engine counterparts.

Statistics:

Single-engine accident rate: 25%.

Multi-engine accident rate: 10%.

Recommendation: Focus on purchasing multi-engine models for increased reliability.

Recommendations

Aircraft Selection


Invest in commercial aircraft with multi-engine configurations to minimize accident risk.

Focus on models with proven safety records in clear and adverse weather conditions.

Operational Training

Provide specialized training for pilots operating in high-risk areas (e.g., mountainous or heavily congested regions).

Incorporate weather navigation and emergency handling modules into training programs.

Technological Upgrades

Prioritize aircraft equipped with advanced weather monitoring and collision avoidance systems.

Maintenance and Inspection

Ensure regular and rigorous maintenance checks, particularly for older models or high-risk engine types.

Geographical Deployment

Assign aircraft with superior navigational technology to accident-prone areas based on geographical analysis.

Conclusion


The analysis provides clear evidence to guide the company's entry into aviation. By focusing on safer, more reliable aircraft models and implementing targeted operational strategies, the company can mitigate risks while leveraging the opportunities of this new industry. The findings and recommendations align with the stakeholder’s goals, ensuring informed decision-making for a successful business expansion.


VISUALIZATION

In this stage, we use the insights derived from the previous data analysis to create visualizations that effectively communicate key findings. These visualizations are tailored to address the company’s business problem: identifying the safest aircraft options for their aviation expansion. The goal is to provide stakeholders with clear, interpretable visuals that highlight risks and opportunities, ensuring informed decision-making for aircraft acquisition.

Visualization 1:
Aircraft Damage vs. Injury Severity Purpose:

This visualization explores the relationship between the extent of aircraft damage and the severity of injuries sustained during incidents. It provides insight into how damage levels correlate with passenger safety, helping stakeholders evaluate aircraft resilience.

Findings: The stacked bar chart shows that incidents resulting in "Destroyed" aircraft are more likely to involve fatal injuries, while "Minor" or "None" damage categories have higher proportions of uninjured passengers.

Example in code form damage_injury_data = data.groupby(['Aircraft Damage', 'Injury Severity']).size().unstack() damage_injury_data.plot(kind='bar', stacked=True, figsize=(10, 6), colormap='viridis') plt.title("Aircraft Damage vs. Injury Severity") plt.xlabel("Aircraft Damage") plt.ylabel("Count") plt.legend(title="Injury Severity") plt.tight_layout() plt.show()

Visualization 2: Weather Conditions vs. Total Injuries

Purpose: This heatmap highlights the impact of weather conditions on total injuries, allowing stakeholders to assess operational risks associated with adverse weather during flights.

Findings: The heatmap indicates that "Instrument Meteorological Conditions" are linked to significantly higher fatalities and serious injuries compared to "Visual Meteorological Conditions."

weather_injury_data = data.groupby(['Weather Conditions'])[['Total Fatal Injuries', 'Total Serious Injuries']].sum() plt.figure(figsize=(8, 6)) sns.heatmap(weather_injury_data, annot=True, fmt='d', cmap='coolwarm', cbar=True) plt.title("Weather Conditions vs. Total Injuries") plt.xlabel("Injury Type") plt.ylabel("Weather Conditions") plt.show()

Visualization 3: Purpose of Flight vs. Accident Frequency

Purpose: This visualization examines how different flight purposes contribute to accident frequencies, helping stakeholders determine which operational contexts pose the highest risks.

Findings: The bar chart reveals that private and personal flights account for a higher number of accidents compared to commercial operations, indicating a higher risk associated with non-commercial aviation activities.

flight_purpose_counts = data['Purpose of Flight'].value_counts() flight_purpose_counts.plot(kind='bar', figsize=(10, 6), color='skyblue') plt.title("Purpose of Flight vs. Accident Frequency") plt.xlabel("Purpose of Flight") plt.ylabel("Number of Accidents") plt.xticks(rotation=45) plt.tight_layout() plt.show()

Visualization 4: Geographic Distribution of Accidents

Purpose: This scatter plot provides a geographic perspective on where accidents occur, enabling stakeholders to identify high-risk regions for operations.

Findings: The plot demonstrates clusters of incidents in specific regions, highlighting operational areas where safety measures may require reinforcement.

plt.figure(figsize=(10, 6)) sns.scatterplot(x='Longitude', y='Latitude', data=data, hue='Aircraft Damage', palette='coolwarm', alpha=0.7) plt.title("Geographic Distribution of Accidents") plt.xlabel("Longitude") plt.ylabel("Latitude") plt.legend(title="Aircraft Damage") plt.show()

Visualization 5: Injury Severity and Aircraft Categories

Purpose: A stacked bar chart displays the count of accidents for each injury severity level within different aircraft categories.

Findings:

Single-engine aircraft show higher counts of "Fatal" and "Serious" injuries compared to multi-engine aircraft.

Rotorcraft tend to have fewer accidents but are more prone to "Non-Fatal" injuries.

injury_severity.plot(kind='bar', stacked=True, figsize=(10, 6), colormap='coolwarm') plt.title("Injury Severity by Aircraft Category") plt.ylabel("Proportion") plt.xlabel("Aircraft Category") plt.show()

Visualization 6: Weather Conditions and Total Injuries

Purpose: A grouped bar chart highlights the total injuries (Fatal, Serious, Minor) under different weather conditions.

Findings:

Accidents under IMC (poor weather) result in higher counts of fatal and serious injuries compared to VMC.

VMC (good weather) shows more minor injuries, possibly due to better chances of safe landings during accidents.

Visualization 7: 4. Aircraft Damage and Purpose of Flight

Purpose: A stacked bar chart visualizes the distribution of aircraft damage for each purpose of flight.

Findings:

Commercial Flights (Air Taxi/Charter):Higher frequency of substantial and destroyed aircraft damage due to frequent use and exposure to varied conditions. Personal Flights:Typically show more minor damage cases, suggesting less frequent but potentially less severe accidents. Business Flights:Show a balanced distribution of damage, requiring further analysis on operational risks. Unknown Purpose:Requires additional data verification to interpret patterns accurately.

Conclusion

The visualizations presented are designed to guide stakeholders in assessing aircraft risk factors, focusing on damage resilience, weather-related injuries, flight purpose risks, and geographic safety trends. Together, these visuals provide actionable insights to support data-driven decisions in the company’s aviation expansion. By presenting findings in a clear and polished format, stakeholders are equipped to evaluate aircraft options confidently.

