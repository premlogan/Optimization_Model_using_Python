# Optimization_Model_using_Python
Context: 
    This Optimization model was developed as a part of Data Analytics for Business & Policy course by Premkumar Loganathan, Yiting Hui, Chalisa Kallayanamitra, Swee Tian Lim

Abstract: 
A liner optimization model is built to determine Points of Dispense for supplying essential supplies during pandemic outbreaks like Covid-19 with the goal of minimizing travel distance for the residents, with budget and other constraints.

Problem: 
During an pandemic like Covid-19, it is essential for governments to distribute essential supplies (e.g. test kits, General purpose medicines, PPE) to the public. Location: Allegheny County

Purpose: 
Select a list of Points of Dispense (PODs) from the candidate sites to distribute essential supplies within budget constraints. Model proposed: Integer optimization under uncertainty

Goals:
1.	Minimize the maximum travel distance for anyone (P-center models) from their place of residence to the assigned PODs.
2.	Minimize the total travel distance of the population (P-median models)

Models built:
1.	Stochastic Multi-objective Optimization - Minimizing the total weighted travel distance of the households + fixed/operational costs
2.	Robust Optimization Objective - Minimizing the maximum travel distance for anyone
3.	Robust Optimization Objective - Minimizing the total weighted travel distance of the households

Recommendations: 
Based on the results from our model and the analysis, it is clear that the decision for policy makers can be based on the trade off between maximum travel distance for all households, total weighted distance for all households and the total cost. The multi-objective approach (the first model) allows us to see the Pareto optimal frontier which represents how the increase in total weighted distance lowers the total cost (building less POD sites reduces total cost but leads to higher total weighted distance). This information can help policymakers decide the location (assignment) of the POD depending on what they want to achieve most (minimizing total weighted distance or total cost). The second and the third models are the cases when counties want to utilize its budget constraint of $13 million. So, they can either choose to minimize the maximum travel distance so that the worst-off person travels the least distance (equity aspect) or to minimize the total weighted travel distance to make the overall people satisfied in terms of the travel distance (efficiency aspect).

Instructions to run the code:
1.	Ensure that the Gurobi license is active and a python programming environment with Jupyter notebook is set up.
2.	All the csv files are required for running our model and shall be placed in the working directory where the dabp_updated.ipynb
3.	Run the dabp_updated.ipynb for viewing the results and visualizations.
