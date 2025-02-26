Loss Description Text Analysis for Claim Categorization

Task: Build an automated PowerBI dashboard to act as the central location of all human bodily injury claims, categorized by injury type.

Issues: 1. Claims data came from different types of lines of business 
        2. Loss descriptions were the only identifier of injury type
        3. Grammatical errors within the loss descriptions from client 
           data such as frequent typos, misspellings, acronyms, abbreviations,
           incorrect or no punctuations, etc.
        4. Loss descriptions incorrectly describing losses

This lead to keyword tables for injury identification queries returning incorrect results. What returned was a table that contained every 
claim involving human bodily injuries, while not every claim record existing in the table was of a human bodily injury. This was an appropriate
use case to apply machine learning methodologies as a resolution.

Method: Collect and properly annotate loss description sample data in order to train a predictive model to act as a secondary filter on the 
        initial SQL query pulling all claims with injury keywords identified. Models trained and tested were Support Vector Machines and Naive Bayes.
        Training data consisted solely of loss descriptions. Aim to reduce false negatives.

Data Pre-Processing: 1. Stopword removal
                     2. Drop word removal 
                     3. Identity definitions
                 

Results: The SVM proved to be reliable and accurate, able to effectively filter the data we needed to populate our central injury claims system.
         It was embedded into a new PowerBI Dashboard I built that automatically refreshes the SQL query to continuously import claims data and filter process
         it with the trained Support Vector Machine.
         

        
          
