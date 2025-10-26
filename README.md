# Autonomous Vehicle Accidents
## Summary
The project focuses on analyzing autonomous vehicle accidents and proposing a human–engineering solution to the problems identified in the data. The analysis was based on a comprehensive dataset from California, including 646 accidents between 2019–2024. The data was cleaned and reduced to 57 key variables, analyzed using Python, and managed via GitHub. Findings revealed that autonomous vehicle accidents occur at higher rates than conventional ones at night and in early morning hours, mainly at intersections and certain geographic hotspots.

The main issues identified involve limitations in nighttime detection, intersection complexity, the influence of weekdays, weather conditions, geographic accident clusters, and interactions between human and autonomous drivers. The project focuses on one key problem: the high frequency of autonomous vehicle accidents in high-risk situations - night, intersections, and specific locations. Recent studies support these findings, showing that autonomous vehicles particularly struggle under these conditions.

To understand users, interviews were conducted with three representative participants: an autonomous vehicle owner, a conventional driver who drives through intersections in the early morning, and an experienced car designer. The results indicate that users expect transparency, reliability, and control, while conventional drivers fear unpredictable behavior from autonomous vehicles. Professionals highlight a gap between technological promises and actual user experience.

The proposed solution is a smart three-mode in-car system integrated into the vehicle display, combining a navigation map with visual, auditory, and tactile alerts. The system offers three modes — *Normal*, *Adaptive*, and *Take Control* - based on risk level. It uses real-time analysis of accident data, time of day, and road conditions to issue graduated alerts that enhance driver awareness and prevent accidents. Its key advantages include improved safety, increased public trust, and a personalized multi-sensory interface, while drawbacks include alert overload, driver dependence, and technical complexity.

To evaluate the solution, a driving simulator experiment (bonus stage) is proposed with dozens of participants. The test will compare regular driving with system-assisted driving in night, intersection, and hotspot scenarios. Both objective measures (reaction time, control takeover) and subjective measures (trust, perceived safety) will be assessed. Success will be determined by reduced accident rates and increased user confidence.

In conclusion, the project integrates empirical data analysis, user research, and innovative prototype development to reduce autonomous vehicle accidents in high-risk conditions and enhance user experience in advanced driving systems.


## Data Understanding  

The rapid advancement of **autonomous vehicles (AVs)** and the emergence of **autonomous taxi services** have the potential to transform urban mobility. However, public concerns about **AV safety** remain a major barrier to widespread adoption. While extensive AV testing has been conducted in controlled environments, **real-world accident data** is essential for understanding safety risks and improving public trust.  

The selected database, part of a project by **Su Yiming (project lead)**, **Jiao Junfeng**, and **Chen Yu**, published on [**Zenodo**](https://zenodo.org/records/15937591), presents detailed accident data for autonomous vehicles (**Levels 3, 4, and 4.5**). It includes a comprehensive dataset of AV-related accidents in **California**, covering all reported incidents involving autonomous vehicles between **January 1, 2019**, and **December 31, 2024**, totaling **646 records**. The dataset integrates information from the **California DMV accident reports**, **geographic coordinates** derived using **GIS tools**, and **semantic data** extracted with **large language models (LLMs)**. This **tabular dataset** supports a wide range of applications, including analyzing AV accident patterns, identifying contributing factors, assessing risks, refining safety algorithms, developing regulatory policies, and planning urban infrastructure.  

The original database contained **195 variables**, but not all were necessary for our research. Some were redundant, irrelevant, or added unnecessary noise. Therefore, we reduced the dataset to **57 key variables**, focusing only on the most relevant ones to ensure a more targeted, efficient, and high-quality analysis.  

After refining the dataset, we uploaded the **CSV file** to **ChatGPT** to obtain an initial overview of emerging trends and insights. Next, we proceeded to analyze the data using **Python**, chosen for its leading role in modern data analysis. Python provides advanced libraries such as **Pandas** and **NumPy** for data processing, and **Matplotlib** and **Seaborn** for visualization. These tools enabled us to perform complex analyses, identify trends, and generate insights far more efficiently than manual tools like **Excel**.  

Using code also allowed for **systematic documentation** of every step - from **data cleaning** to **building statistical models**. The reproducibility of code ensured consistent results, improving the **reliability** of our analysis and preventing manual errors.  

We managed the code through **GitHub**, a **version control** and **collaborative platform**. GitHub enabled all team members to work on different parts of the project simultaneously while maintaining synchronization and full transparency. It also provides **version history**, allowing us to revert changes if necessary, and **automatic cloud backups** for all code.  

The combination of **Python** and **GitHub** provided a major advantage: powerful and efficient analytical capabilities alongside a **professional, collaborative work environment**. This approach allowed us to perform the required analyses **reliably, transparently, and accurately**, maintaining high standards of **research quality**.

## Problem Identification

### Defining the Issues to Investigate

#### 1. Different Accident Rates by Time of Day  
Analysis shows that autonomous vehicles experience accidents during off-peak hours, mainly between 21:00 and 7:00, while conventional vehicle accidents are lower during these hours. This indicates that autonomous driving systems may face difficulties under low-light conditions or low vehicle activity. Human factors research can focus on improving vehicle sensing and response during these hours, as well as driver experience when transitioning between different lighting and traffic conditions.

#### 2. Impact of Road Type on Accidents  
Analysis of road types shows that intersections are a high-risk area for autonomous vehicles, with 259 accidents compared to 177 accidents in conventional vehicles. Narrow roads show relatively fewer accidents in both vehicle types. This raises questions about adapting autonomous systems to intersection complexity, the need for clearer road markings, and examining road design to reduce risks. Researching these aspects in UX can improve driving experience and safety.

#### 3. Impact of Day of the Week on Accidents  
Comparison across days shows that autonomous vehicle accidents remain high on weekends, while conventional vehicle accidents decrease. This indicates a gap between traffic patterns of autonomous versus conventional vehicles. Research could examine how autonomous systems adapt to weekly traffic changes and how user experience could include alerts or route adjustments depending on the day.

#### 4. Impact of Weather Conditions  
Although most accidents occurred in clear weather, this may be influenced by the local climate. A research issue involves the ability of autonomous systems to handle varying weather conditions, including daylight, low visibility, or rain. Studying system behavior in these conditions and providing clear information to the driver can improve user experience and safety.

#### 5. Geographic Risk Hotspots  
Mapping accidents by location identifies areas with a high concentration of accidents, which are risk hotspots. This allows research on user experience in navigation systems, where real-time alerts or alternative routes can reduce the risk of accidents for both autonomous vehicles and human drivers.

#### 6. Gaps Between Human and Autonomous Driving  
Differences in accident rates between autonomous and conventional vehicles highlight the need to understand interactions between human drivers and autonomous vehicles in mixed environments. Studying differences in driving patterns and responses to autonomous vehicles can lead to improved user interfaces, alerts, and feedback systems that help drivers understand vehicle status and surroundings.

#### 7. Differences in Risk Perception  
Differences between autonomous and conventional vehicles indicate a gap in risk perception and response by drivers or the autonomous system. UX research can focus on designing systems that provide intuitive and clear information about potential risks and user interface elements that improve real-time decision-making, especially in dangerous or unexpected situations.

#### 8. Differences Among Autonomous Vehicle Types  
Data shows that different autonomous vehicle types are involved in varying numbers of accidents. This raises a human factors and UX question: are these differences due to interface design and human-system interaction? Features such as information presentation, alert design, level of autonomy, and need for human intervention may affect driver engagement and accident prevention. This points to an issue for investigation: how does the design of the user interface and driving experience in autonomous vehicles actually influence accident rates?


