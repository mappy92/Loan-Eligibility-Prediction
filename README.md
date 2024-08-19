<h2>Loan Eligibility Prediction</h2>
<h3>Problem Statement</h3>
The objective is to predict the loan eligibility of applicants based on various factors such as education, marital status, gender, applicant and co-applicant income, loan amount, and other variables. This prediction helps in automating the decision-making process for approving loans.

<h3>Solution Overview</h3>
We approach the problem using supervised learning and classification techniques. The process involves training a model using historical loan data (loan-train.csv) and testing its accuracy. Once the model is validated, it is used to predict loan eligibility for new applicants using fresh data (loan-test.csv).

<h3>Implementation Steps</h3>
<h4>1. Data Exploration</h4>
<b>Shape and Info: </b>Used to understand the structure of the data, including the number of entries, features, and their data types.<br/>
<b>Describe: </b>Provides statistical summary of numerical features to get insights like mean, median, standard deviation, etc.<br/>
<b>Box Plot: </b>Visualizes numerical data to identify outliers that may affect model performance.<br/>
<b>Histograms: </b>Used to check the distribution of data across different features.<br/>
<h4>2. Handling Missing Values</h4>
<b>Categorical Variables:</b> Missing values are filled using the mode (most frequent value).<br/>
<b>Numerical Variables: </b>Missing values are imputed using the mean.<br/>
<h4>3. Data Transformation</h4>
<b>Normalization: </b>Applied log transformation to numerical values to normalize data dispersion.<br/>
<b>Feature Engineering: </b>Created a new variable Total_Income by summing Applicant_Income and Coapplicant_Income.<br/>
<h4>4. Encoding Categorical Variables</h4>
Converted categorical variables (e.g., Education, Gender, Married) into numerical format using encoding techniques.<br/>

<h4>5. Feature Scaling</h4>
Scaled the numerical data to minimize the range differences between variables, improving model performance.<br/>

<h4>6. Model Training and Evaluation</h4>
<b>Decision Tree: </b>Used with entropy criterion; achieved approximately 72% accuracy.<br/>
<b>Naive Bayes: </b>Applied and found an accuracy of around 82%.
<h4>7. Prediction on New Data</h4>
Repeated the data cleaning and transformation steps on loan-test.csv to predict loan eligibility for new applicants.

<h3>Results</h3>
The Naive Bayes model outperformed the Decision Tree model, achieving an accuracy of 82%. This model was then used to predict the eligibility of applicants in the test dataset.

<h3>Conclusion</h3>
This project demonstrates how machine learning can be used to predict loan eligibility, helping financial institutions make data-driven decisions. Further improvements can be made by exploring more sophisticated models or fine-tuning hyperparameters.
