# TRANSFOR19
Transportation Forecasting Competition

Organized by: ABJ70 Artificial Intelligence and Advanced Computing Applications 
Supported by: IEEE ITSS Technical Activities Sub-Committee “Smart Cities and Smart Mobility”
Sponsored by: Didi Chuxing


# Call Description 
With the overwhelming amount of transportation data being gathered worldwide, Intelligent Transportation Systems (ITS) are faced with several modeling challenges. New modeling paradigms based on Computational Intelligence (CI) take advantage of the advent of big datasets collected by users and vehicles moving on road networks. Nevertheless, transportation data often pose considerable challenges to researchers and practitioners: differences in data measurement techniques and frequencies, seasonality, local trends, structural breaks, outliers, zero and missing values, and so on. Further, transportation needs increase and services become more complex and demanding; for example, shared-use mobility, real time control and cooperative ITS often require short-term predictions of transportation conditions based on existing data from stationary and moving sensors. To this end, developing accurate and efficient forecasting algorithms for transportation applications becomes even more important and promising as a task.

The Transportation Research Board is happy to announce the 2019 Transportation Forecasting Competition workshop, which will be held at the Transportation Research Board (TRB) 98th Annual Meeting, for the second time since 2013. This year’s competition is also supported by the IEEE ITSS Technical Activities Sub-Committee “Smart Cities and Smart Mobility” and sponsored by Didi Chuxing Gaia Open Data Initiative.

The scope of the competition is to evaluate the accuracy of statistical, or CI methods in transportation data forecasting with particular reference to short term traffic forecasting. The focus will be on obtaining predictions, as close as possible to the real data. Solutions that will advance the current understanding in advanced computing, data preprocessing and traffic dynamics will be also favored. The competition is open to Teams (single participant or group of participants) that are willing to present their work at the 2019 TRB Annual Meeting. 

The competition will run in two stages: in the first stage (pre-selection), data will be made available through Gaia Open Data Initiative and submissions will be ranked according to prediction accuracy. The top 3 submissions will proceed to the next stage, which will take place on Sunday, January 13, 2019 during the TRB Annual Meeting Workshop sponsored by ABJ70 Committee, where the selected teams will briefly present their work (10 minutes for each presentation). The Organizing Committee will select the winner based on four criteria: i. Accuracy (50%), ii. Degree on novelty (25%) and iii. Quality of the code (10%), and iv. Quality of the presentation (15%). The first prize is $2000. The winner will be announced during the annual ABJ70 Committee Meeting in January 2019.

# The Dataset
This competition is built on the Didi Chuxing Gaia Open Data Initiative. The available data sets are derived from the trajectory data of DiDi Express and DiDi Premier drivers within the Second Ring Road of Xi'An City (October – November 2016). The measurement interval of the track points is approximately 2-4 seconds. The track points were bound to physical roads so that the trajectory data and the actual road information are matched. The driver and trip order information was encrypted and anonymized. When registering to get access to the data online, please clearly state that the purpose of use is TRANSFOR 19.

# Problem Formulation
Participants are asked to develop a traffic forecasting scheme to predict the average speed every 5 minutes at the road section enclosed by the following coordinates (WGS-84):

•	Point 1: 34.241, 108.943

•	Point 2: 34.241, 108.9415

•	Point 3: 34.234, 108.9415

•	Point 4: 34.234, 108.943

Predictions should be separately made for each direction of travel.

# Rules
•	Teams (single or multiple participants) must register for the data competition via email to Eleni I. Vlahogianni (elenivl@central.ntua.gr) by October 30, 2018.

•	At least one member of the team must register for the 2019 TRB meeting. Proof of TRB registration must be submitted via email along with the data competition registration.  

•	Following the registration deadline of October 30, 2018, the data will be provided to all registered teams in the form of a csv file (Predictions.csv). This csv file will include the time periods where the Teams should generate the speed predictions based on their models.

•	Prediction accuracy will be evaluated using the root mean squared error.

•	Participants may not exceed four submissions before the deadline. In the case of multiple submissions, the highest score will count at the end of the competition.

•	The final submission must include: 
  o	The Predictions.csv file with both observed and predicted values, 
  o	The code, which replicates the entire procedure (data preparation and visualization, model development, testing, visualization of results, predictions extraction etc.). Code must be properly commented to allow reviewers to understand the logic.  
  o	A short paper (no more than 3 pages) detailing the approach used, advantages and disadvantages and main outcomes.

•	Allowable languages/environments: R, Python, Matlab/Octave, C, C++, C#, Java, TensorFlow, Cognitive Toolkit. Other programming languages/environments may be allowed if proper justification is provided by the Team and approved by contest committee. Approval for other languages/environments must be sought prior to the submittal deadline.

•	Teams must agree to share their code using Jupyter Notebook.  The code will be archived and open to public through an open project that will be created in GitHub by the Committee. 

# Panel Members
Sherif Ishak, Old Dominion University (sishak@odu.edu), ABJ70 Committee Chair, Eleni I. Vlahogianni, National Technical University of Athens (elenivl@central.ntua.gr), Javier Sanchez Medina, IEEE ITS Society’s VP for Technical Activities (javier.sanchez.medina@ieee.org), David Reinke (dbreinke@alum.mit.edu), Emmanouil Barmpounakis, EPFL (manos.barmpounakis@epfl.ch) and Henry Liu, Vice President & Chief Scientist at Smart Transportation, Didi Chuxing (Professor, University of Michigan, US) (henryliu@didiglobal.com).

# Important Dates
October 30, 2018:	Deadline for team registration.
November 1, 2018:	Predictions.csv released to the registered teams. 
December 10, 2018:	Deadline for submission of results. 
December 17, 2018:	Notification of acceptance of top 3 submissions (Pre-selection stage). 
January 13, 2019:	TRB Annual Meeting (Final stage for nominating the winner).



# FAQs
1. Can I participate to more than one team? 
- Each participant should join only one Team.

2. What tool to use for coordinates conversion (between GCJ-02 and WGS-84) ?
- Since some teams have questions regarding the study area, we decided to share a screenshot from openstreetmaps. The red rectangle represents the study area. Be sure to use the same coordinate system using the eviltransform in python.

3. What is the timezone in Xi'an, Shaanxi, China?
- For the specific area GMT+8 is used. The same timezone is used in the Predictions.zip files.

4. What does the Predictions_north.csv include?
- The Predictions_north file includes the average speed of vehicles traveling to north (which means that latitude increasing) per 5 min intervals. The symbol "x" stands for the time intervals you are asked to generate predictions.

5. How are speeds  calculated in the Predictions files?
- The average speeds are calculated based on the distributed GPS data (extra day file). This extra day dataset does not contain trajectories for the specific road section during the prediction hours (marked with x in the predictions_north and south files). The average speed seen in the Predictions files is the average of all speeds of all vehicles traveling in the specific road section per direction of travel.

