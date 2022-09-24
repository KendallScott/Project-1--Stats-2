MSDS 6372 Project 1 Description
For this project, we are going to keep them from HW Unit 2 and investigate a data set involving the  automobile industry.  The data set is included in the file data1.csv.  A brief description of the variables are listed below.  (Yes you may use this table in your manuscript).  Rather than miles per gallon, we will be building models to better understand and predict the retail price of a vehicle using various attributes.  
Variable Name	Data Type	Description
MSRP	Numeric	The response variable
Car Make	Factor	The company that made the car. Ex: Honda, Toyota, etc.
Car Model	Factor	The model of the car. Ex: 4Runner, Accord, etc.
Year	Numeric	Year the car was produced
Engine Fuel Type	Factor	Type of fuel the car accepts.  Ex: Regular unleaded, Premium unleaded, Diesel
Engine HP	Numeric	Horsepower of the car’s engine.
Engine Cylinders	Numeric	Number of cylinders in the car’s engine.
Transmission Type	Factor	Type of transmission in the car. Usually manual or automatic, but there are a few specialty transmission types in the data.
Driven_Wheels	Numeric	The wheels that are powered by the engine.  Ex: Front Wheel, Rear Wheel, Four Wheel Drive
Number of Doors	Numeric	The number of doors that the car has. Usually 2 or 4
Market Category	Factor	Various special factors for each car.  Ex: Exotic, Luxury, High-Performance, Flex Fuel. Note: we created a new feature using Exotic/Not Exotic for our analysis
Vehicle Size	Factor	The size of the vehicle.  Ex: Midsize, Large, Compact
Vehicle Style	Factor	Body type of the vehicle. Ex: Coupe, Convertible, etc.
Highway MPG	Numeric	Fuel efficiency on the highway in MPG
City MPG	Numeric	Fuel efficiency in the city in MPG
Popularity	Numeric	A popularity score for each car.  The dataset does not detail how the popularity score is calculated.

There are two main objectives for Project 1.  Before providing the details to the objectives, the groups should investigate the data and make any additional logistic decisions like dealing with missing data if there is any, cleaning up variable names, changing their data types, etc.  Once that is complete, I want each group to subset the data set into 3 data sets.  Suggested:  80% train, 10% test, and 10%validate.  During the objective descriptions below, I will mention which data sets you can/should use.
Objective 1: Display the ability to build regression models using the skills and discussions from Unit 1 and 2 with the purpose of identifying key relationships and interpreting those relationships.  A key question of interest that must be addressed in this analysis is the importance of the “Popularity” variable.  While the details of this variable are vague, it was created from social media, and the “higher ups” are curious how much general popularity can play a role in the retail price of a vehicle.   
•	Build a model with the main goal to identify key relationships and is highly interpretable.  Provide detailed information on summary statistics, EDA, and your model building process. 
•	Provide interpretation of the regression coefficients of your final model including hypothesis testing, interpretation of regression coefficients, and confidence intervals. It’s also good to mention the Practical vs Statistical significance of the predictors.  Answer any additional questions using your model that you deem are relevant.
•	The training data set can be used for EDA and model fitting while the test set can be used to help compare models to make a final call.  There is no need to use the validation data set for this objective.
Practical Consideration for Objective 1:
EDA, EDA, EDA!  It helps you on so many fronts so use it to your advantage.  When writing a concise report, you do not have to literally step out every single step of your model building process.  I know you guys are going to being iterating on things many many times.  That does not all have to be there.  You can summarize that iteration stuff in a paragraph.  
What is key in the report is that you develop a “story” of your analysis.  Keep in mind that when you are finished with your analysis.  You know how it is going to end (what the final models look like).  You can use this to your advantage when selecting what parts of the EDA and additional information to show.  For example, if you know that predictor X7 is in your final model and it is one of the stronger relationships, that is probably a good one to show and discuss in the EDA part.  You would show the reader, “Hey look at these interesting trends”, “Hey look at these that are not”, etc.  When you report your final model and you are bringing back up the predictors discussed in EDA, it helps build the confidence of the reader in what you are doing is making sense.

Objective 2:  While your model from Objective 1 may be interpretable there may be some additional complexity that you could incorporate to your model so that it can predict better at the expense of interpretations.  The purpose of this objective is to go through a process to compare multiple models with the goal of developing a model that can predict the best and do well on future data.  
•	Use the training and test set to build at least one additional multiple linear regression model that attempts to find a model with additional complexity than the interpretable model of objective two.  The point here is to make sure we understand how to add complexity to a linear regression model.   Hint:  Its not just including a model with predictors that you’ve eliminated from Objective 1.
•	I want you to use the ISLR text book (and the googe machine) and read up on one nonparametric technique to build a regression model.  I want you to select from k-nearest neighbors’ regression or regression trees. There is a chapter on trees in the ISLR book.  For information on knn regression, see Section 3.5.  It is important to know that knn can be applied to regression as well as classification problems.  Make sure your implementation in R is using the knn regression versions rather than the classification.  See me on this if you need help or reassurance.  You will use the training and test sets here to help determine the most appropriate tree or the most appropriate “k” in knn. 
•	At this point you should have at least 3 models, 2 linear regression models and 1 nonparameteric.  For each of the three models, provide measures of fit for comparisons:  test ASE and validation ASE are mandatory.  You may also include additional metrics for completeness like R squared/Adjusted Rsquared, AIC, and BIC where applicable.  This final to-do is the only point where the validation set is being used.  This is because we are truly validating our decisions that have been made using the training and test set.   It is important to do this step last when you have completed all other tasks.  Do not continue to update models to get your validation ASE to be smaller.  Just report it and offer a recap of the comparison of the results suggests.  Additional insight as to why one model is better than the other, or why they are all the same is encourage.
Practical Consideration for Objective 2:
Part of Objective 2 is to get comfortable with figuring new things out.  As you learn about knn or regression trees, consider providing a brief description of how that model is used to make a prediction.  It’s clearly different from multiple linear regression.  It doesn’t have to be technical they are both pretty intuitive approaches.

When all we care about is predictions, don’t be afraid to try things.  Transformations, interactions, creating new variables from old variables.  Let your EDA help you in coming up with outside the box ideas.  Note:  This tip could be applied to Objective 1 as well, as long as it yielded an interpretable model.

Many students will eventually migrate to more automated packages in R like Caret for Objective 2.  These packages may have the ability to run CV on all of the models simultaneously and provide a CV press statistic for each one of the models.  If this is the case (you should check because I don’t know), you can combine the train and test sets together to fit your models, just report the CV ASE/PRESS instead of the test ASE.  Validation ASE should still be provided.
Another graph that is helpful for just getting a sense for how your predictions are behaving is to plot the predicted values versus the true values in a scatterplot.  The closer the data is to the 45 degree line the better.
Additional details
NOTE: ALL ANALYSIS MUST BE DONE IN SAS OR R and all code must be placed in the appendix of your report. Python is okay for quick formatting of data and data visualization, but analysis should be in R or SAS.

Required Information and SAMPLE FORMAT

PAGE LIMIT: I do not necessarily require a page limit, but you should definitely be shooting for no more than 8 pages written for the main report (not including graphics and codes).  It of course will blow up quite larger than that due to graphics, tables, and code but good projects are clear, concise, and to the point.  You do not need to show output for every model you considered.  (You may put supporting plots/charts/tables etc. in the appendix if you want, just make sure you label and reference them appropriately.). Effective communication is critical here. 

The format of your paper (headers, sections, etc) is flexible although should contain the following information.  

1.	Introduction Required

2.	Data Description  Required

3.	Exploratory Data Analysis Required

4.	Addressing Objective 1:  Required
•	Restatement of Problem and the overall approach to solve it 
•	Model Selection 
		              Type of Selection
			Options: LASSO, RIDGE, ELASTIC NET,
			     Stepwise, Forward, Backward, 
		             	     Manual / Intuition,
			     A mix of all of the above.  	
•	Checking Assumptions 
			Residual Plots
			Influential point analysis (Cook’s D and Leverage)
•	Parameter Interpretation    
	       Interpretation                 
	       Confidence Intervals Not Required, but use if beneficial to the discussion.

5.	Addressing Objective 2:  Required

•	Restatement of problem and the overall objective 

•	Description of the approach for building a complex regression model.  Feature selection must be used here if only manually model fitting approaches were used in Objective 1.  

•	Brief description of how the nonparametric tool works intuitively.  Can this model overfit?  How?   

•	Comparison of model results 
			Table of test ASE, validation ASE, and any other relevant model fitting metrics.
Discussion and insight as to what the results suggest.  Why does one fit better than the other?  Or perhaps why does it appear that all the models appear to be performing about the same?
6.	Final summary Required
•	Quick recap of Objective 1 and Objective 2 findings
•	Provide any additional details and comments on the implications of the models.  Scope of inference?  What other data would this model be good/poor to apply to?   Problems/concerns with the data or data collection? What would you do if you have more time?  What else would you collect? etc.  
7.	Appendix  Required
•	Well commented SAS/R Code
•	Graphics and summary tables (Can be placed in the appendix or in the written report itself.)
•	Make sure you include figure labels and reference them in the report if you are using an appendix to communicate figures.
