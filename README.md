### Predicting Impact of Sub-Processes in Multi-Variate Device Analysis

**Geoffrey Sitwell**

#### Executive summary

#### Rationale
In non-linear systems with a very significant number of sub-components and assembly processes it can be nearly impossible
to determine the relevant relationships between highly-varied parameters. It can be difficult to isolate variables so ML
and AI offer a useful tool to attempt to disentangle those relationships.


#### Research Question
Can we eliminate screening critieria and relax current thresholds on the rest to improve the yields and reduce test time?


#### Data Sources
These data are sourced from our internal database and covers a single manufacturing campaign.

#### Methodology
I'm going to use some basic models to attempt and classify good die from bad, then see which model is most accurate and 
fastest of these:
1) Dummy model
2) SVC
3) Logistic Regression
4) KNN
5) Decision Tree 

Data must be anonymized so before analysis commences I have translated all of the column names into an anonymous form using
the format provided here:
HA# : Hierarchy of classes of product (Set - Subset - Sub-subset, etc.)
Param# : Test parameters
U# : Units

e.g. "Height [cm]" and "Weight [kg]" of a person would be translated to "Param1 [U1]" and "Param2 [U2]". If we were considering
income of a family it may be HA1 where income of an individual might be HA2.


#### Results
Results indicate that Logistic Regression is the best model for this problem and that certain parameters dominate the final
outcome for that particular analysis.


#### Outline of project

- [Comparison of models and presentation of test time and accuracy](Predictive_Model_Comparison.ipynb)
- [Exploration of the results for Logistic Regression](Logistsic_Regresssion_Exploration.ipynb)
- [A final summary of the results and suggestions for next steps](Final_Report.ipynb)


##### Contact and Further Information

Please feel free to reach out to me at :
geoffreysitwell@yahoo.com
with any further questions.

Subdirectories:
Coefficient_Outputs : Stores results from Logistic Regression on different test/train splits
Data : Stores the scaled and anonymized data and a mini version thereof for sharing
Plots : Stores the output plots of the notebooks
Presentation Materials : Stores a diagram used in the non-technical presentation
Test_Time_Tables : Stores the tables of train times and accuracies for each model on different test/train splits
Trees : Stores the images of decision trees from different test/train splits