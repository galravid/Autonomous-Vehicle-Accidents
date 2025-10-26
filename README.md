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

## Problem Selection

The problem we chose to focus on, which we believe can be addressed, is the high number of accidents involving autonomous vehicles in high-risk situations. Data shows that autonomous vehicles are more likely to be involved in accidents during night and early morning hours (21:00–7:00), in complex areas such as intersections, and at geographic hotspots with a high concentration of accidents. These situations are particularly challenging for autonomous systems due to visibility limitations, multiple interactions with other road users (at intersections), or local environmental complexities. <br>
According to course learnings, solutions to this problem can be found through the integration of human factors and user experience approaches. <br>
Recent studies support the findings from our data, indicating that autonomous vehicles struggle especially under night conditions and at intersections. For example, a study published in [*Nature Communications*](https://www.nature.com/articles/s41467-024-48526-4) in 2024 found that vehicles equipped with autonomous driving systems had a higher rate of accidents during nighttime and while driving through intersections. The study highlights that visibility limitations, difficulty in detecting other road users (such as pedestrians and cyclists), and multiple interactions at intersections increase the likelihood of system errors and unexpected autonomous vehicle responses. This finding reinforces the claim that these situations are vulnerabilities that require targeted solutions.

## User Research

### Defining the Target Population for the Problem

The target population for the proposed solution is broad and includes several key groups of road users, each affected differently by the phenomenon of autonomous vehicle accidents in high-risk situations.  

The first and primary group is drivers and passengers in autonomous vehicles. These are the direct users of the technology, experiencing the risks of accidents at intersections, during nighttime hours, and in geographic hotspots. For them, the solution will improve both physical safety and the sense of security when using autonomous technology—a necessary condition for widespread adoption.  

Another group includes pedestrians and cyclists, who are particularly vulnerable in the transportation system. In intersections and dense urban areas, the risk of injury is high, especially when autonomous vehicles struggle to detect or predict their movements. Therefore, any solution that reduces the number of accidents will enhance the protection of this population and contribute to a safer urban environment.  

Additionally, conventional vehicle drivers are part of the target population. In the current traffic reality, autonomous and conventional vehicles share the road, so any accident involving an autonomous vehicle can also endanger human drivers. Improving the performance of autonomous vehicles in complex situations will reduce risk for these drivers as well, thereby fostering trust between road users and autonomous vehicles.  

Beyond individual users, the broader population and the transportation system as a whole are also stakeholders. As the number of autonomous vehicles on the road increases, unaddressed safety issues can affect traffic congestion, public trust in the technology, and the economic impact of road accidents. While this population is not direct users, it benefits indirectly from reduced accidents and increased efficiency in the transportation system.  

In this way, the target population is multi-layered: from autonomous vehicle passengers to pedestrians, cyclists, human drivers, and society as a whole. This underscores the need for a holistic human-engineering solution that considers the diverse users and their interactions.

### Defining the Solution Goal
The goal of the solution is to improve the safety of autonomous vehicles in high-risk situations by intelligently combining autonomous driving capabilities with human involvement. The solution aims to reduce accidents at intersections, during nighttime hours, and in geographic hotspots, while ensuring the safety of passengers and pedestrians and enhancing user confidence and trust in autonomous technology.

### The Main Problem It Solves
The primary problem addressed by the system is the high number of autonomous vehicle accidents under conditions where autonomous driving systems struggle to cope—nighttime, complex intersections, and areas with a history of accidents. This issue is reflected in relatively higher accident rates compared to conventional vehicles and constitutes a significant barrier to widespread adoption of autonomous vehicles.

### Defining Solution Success
The solution will be considered successful if it reduces the accident rate in high-risk situations, increases driver alertness in critical conditions, and enhances the sense of security for road users in autonomous vehicles. Success metrics include a reduction of over 30% in accidents at intersections and during nighttime compared to historical data, reduced driver reaction time when intervention is required, and 80% of autonomous vehicle drivers responding promptly to system alerts.

### Relevant Scenarios
The system is particularly relevant for three key scenarios: driving during high-risk hours (21:00–7:00) when accident rates are higher for autonomous vehicles; traveling on roads with intersections that serve as high-risk points; and navigating geographic areas with a history of multiple accidents. Additionally, when two or more of these scenarios occur simultaneously, the system becomes especially critical, requiring immediate driver intervention to prevent an accident.


### Defining Personas within the Target Population

#### We define three key personas representing the users:

**1. Noa – Autonomous Vehicle Owner**, age 28, engineering student, lives in California. Motivation: Travel safely without driving. Concerns: Accidents at intersections at night, uncertainty when the vehicle "gets confused". Needs: A system that provides transparency ("safety gauge") and a sense of control.  

**2. Dani – Private Vehicle Driver (Non-Autonomous)**, age 45, high-tech professional, commutes daily. Motivation: Maintain road safety even alongside autonomous vehicles. Concerns: Autonomous vehicle making unexpected maneuvers at intersections. Needs: A system that detects dangerous situations and slows the autonomous vehicle to avoid surprising other drivers.  

**3. Sarit – Autonomous Transportation Developer**, age 36, works in the R&D center of an autonomous vehicle fleet. Motivation: Ensure service reliability and reduce accidents. Concerns: The system may not provide early enough alerts in unusual situations. Needs: Clear risk alerts and guidance for the vehicle driver.

### Interviews with Three Users Representing the Personas

**1. Erez Or – Owner of a Level 2 Autonomous Vehicle (MG4)**, age 22, lives in Tel Aviv, primarily drives in the central area for commuting to work. Sometimes finishes work late and would have to drive tired if not for the autonomous mode. Travels to his parents in the north on weekends.  

**2. Ido Ravid – Owner of a private (non-autonomous) vehicle**, age 26, lives in Melbourne, Australia, works in construction. Drives daily at 4:00 AM to the construction site. Most driving occurs within the city, an area with multiple intersections and a high concentration of accidents.  

**3. Nir Kahan – Vehicle designer** with 25 years of experience, lives in central Israel.

### Insights from Users and Their Current Experience

During interviews with the three users, we gathered important insights on their motivation, goals, behavior, knowledge, and current experience with autonomous vehicles or driving alongside them.

**Erez Or**, as a Level 2 autonomous vehicle owner, expressed clear motivation to integrate the new technology into his daily routine, mainly due to the convenience it provides at intersections and during late-night driving after work. His main goal is to reduce driving effort and enjoy higher safety, but he is concerned about sudden interventions or situations where the vehicle "panics" at complex intersections. His knowledge of the technology is limited; he trusts the system but desires greater transparency to understand what is happening "behind the scenes". His current experience is convenient but accompanied by insecurity in certain situations.

**Ido Ravid**, as a private (non-autonomous) vehicle driver, is primarily motivated by the need to reach work on time and maintain safety in busy urban roads. His goal is to drive continuously without dangerous surprises from autonomous vehicles. He describes concern about unexpected maneuvers by smart vehicles at intersections, especially during early morning commutes when driver alertness is relatively low. His behavior is characterized by extra caution at intersections and trying to "read" the behavior of surrounding vehicles. His knowledge of autonomous vehicles is limited to media exposure or superficial familiarity, and he has no direct experience using the system. His current experience is marked by distrust of autonomous vehicles and a feeling of lack of control when they are present.

**Nir Kahan**, as an experienced vehicle designer, approaches the topic from a professional perspective. His motivation is to improve the reliability of autonomous vehicles and integrate them into the market in a way that ensures safety and convenience for road users. His main goal is to understand how users actually experience the technology to translate it into better design of systems and interfaces. His behavior involves constant evaluation of design and technology trends, looking for potential points of failure in existing interfaces. His knowledge is extensive, both technologically and from a design perspective. His current experience with autonomous vehicles is mainly professional, but he points out a gap between marketing promises and the actual user experience, particularly regarding transparency and clarity of alerts.

From the three users, a comprehensive picture emerges: users want to integrate autonomous vehicles into their lives but demand transparency, reliability, and a better understanding of system actions. Their current experience ranges from convenience and effort-saving (Erez), distrust and fear of unpredictable behavior (Ido), to professional identification of gaps in design and communication between vehicle and user (Nir).

### Competitive Analysis

In examining the current market, there are no commercial systems identical to the proposed solution – a three-state system in autonomous vehicles that performs a gradual transition between full autonomous driving, adaptive mode, and mandatory human control. However, there are several indirect competitors operating in related areas.

A key indirect competitor is **ADAS (Advanced Driver Assistance Systems)**, currently available in smart vehicles ([Wikipedia](https://en.wikipedia.org/wiki/Advanced_driver-assistance_system)). These systems provide alerts for lane departure, pedestrian detection, automatic braking, and driver fatigue warnings. Their advantage is that they are already widely implemented in the market, but their limitation is that they are not specifically tailored for autonomous vehicles and do not focus on risk-level-based adaptive alerts.

Additionally, autonomous vehicle manufacturers such as **Tesla**, **Waymo**, and **Cruise** integrate various safety mechanisms, such as requiring the driver to keep hands on the wheel or stopping the vehicle if no response is detected. However, existing approaches primarily focus on driver monitoring rather than intelligent integration of external risk data – including time of day, intersections, and accident hotspots. This is where our solution has an advantage, combining environmental behavior with driver involvement.

Other indirect competitors include external applications like **Waze**, which provide reports on accidents and risk hotspots. Nonetheless, these applications only offer informational alerts and are not directly connected to the vehicle control systems, so they cannot reduce speed or require the driver to take control.

In summary, our solution offers a clear relative advantage by combining real-time driving risk monitoring with dynamic management of driver control. This directly addresses the problem of accidents in high-risk situations – a niche currently underserved by competitors.

## Solution Including Prototype for the Identified Problem

Following our research, our proposed solution includes a prototype built using the **Base44** platform – a smart system integrated into the display screen of autonomous vehicles, combining visual, auditory, and haptic interfaces ([Prototype Link](https://guardian-drive-e3032e7f.base44.app/)).

In this system, the driver is presented with a navigation map and three clear operational modes according to the level of risk:

- **Mode 1 – Normal:** A simple green visual indicator shows that the vehicle is operating in full autonomous mode.
- **Mode 2 – Adaptive:** An orange indicator appears along with a short auditory alert, signaling the driver to be more attentive due to potential risks (night hours, accident hotspots, intersections). Haptic feedback is also provided to ensure the driver understands the need for increased alertness.
- **Mode 3 – Take Control:** A prominent red indicator is displayed, accompanied by a stronger auditory alert and intense vibration (if technology permits). The driver has 15 seconds to respond; otherwise, the vehicle initiates a safe stop procedure.
- <img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/58701d43-c566-461f-945e-0b300b3e1691" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/ce5089be-52bf-4daf-ba88-2eed26abfa3f" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/d943c919-2edd-4e67-900c-1d4a79bb1fe2" />



