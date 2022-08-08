# Pewlett-Hackard-Analysis
# Overview of the Analysis:
Bobby’s manager has given us the assignment to determine the number of retiring employees per title and identify employees who are eligible to participate in a mentorship program. We will be preparing this report to summarize the analysis and help prepare Bobby’s manager for the “silver tsunami” as many current employees reach retirement age. 
#Results:
The analysis came up with 4 major points to be discussed. The first point was around Retirement titles. In collecting retirement titles, we were able to collect a list of all employees with the employee number and title and the dates they held those titles. A snapshot of the data is below. 
![image](https://user-images.githubusercontent.com/106719954/183322743-89afa5fd-904b-4342-99ca-79c08c8183fb.png)
This information was compiled and set aside as retirement titles as we would further clean through this data in our analysis.  

The second data set in the analysis consisted of gathering unique titles. Our first data set was not complete because it held duplicate values. For example, employee 10004- Christian Koblick is listed twice once when he was an Engineer and then the most recent time when he was a Senior engineer. We would only want the most recent titles for each employee, so we don’t have duplicates listed. We would also want to remove employees from this list for employees who have already left the company. A snapshot of the new cleaned data is below with duplicates removed is below: 
![image](https://user-images.githubusercontent.com/106719954/183322772-5251e260-3999-4fbf-8359-aa897836c26f.png)
Now that Bobby and I have all out employees with the most recent titles compiled we need to dig into the data and find out the retiring titles. Knowing the retiring titles will help our boss know which titles we will need to hire.  The thousands of rows in our earlier analysis have been drilled down into a clear snapshot of which titles will have retiring employees that we will replace. The new drilled down information is represented below: 
![image](https://user-images.githubusercontent.com/106719954/183322808-e0a7f977-ffee-4a43-b427-8d32c0d20931.png)
This data will give our manager exactly how many Engineers and other positions we will need to hire. 

The final piece of data we analyzed was around mentorship eligibility. The mentorship eligibility is for current employees who were born between 1/1/1965 and 12/31/1965. These employees are 57 years old and are eligible to participate in the company mentorship program. We have this list narrowed down to 1,550 employees who fit the criteria and we have all the information we need to know who they are, DOB, their titles and how long they have been in those titles. A snapshot of the data is below: 
![image](https://user-images.githubusercontent.com/106719954/183322833-09e1eb50-21fc-4dc3-ba6d-0a669659c8c2.png)
This is the final piece of data we collected for our manager and now he has all the information he needs to present to his manager. 

#Summary:
The analysis we ran gives our manager enough information to make informed decisions. He knows which employees are eligible for our mentorship and titles that will be needed to be filled for. I would want to know a snapshot of the exact number of employees approaching retirement so that our manager would know what recruiting efforrts we will need to make. For example the below query regarding number of employees retiring
SELECT COUNT(first_name)
FROM employees
WHERE (birth_date BETWEEN '1952-01-01' AND '1955-12-31')
AND (hire_date BETWEEN '1985-01-01' AND '1988-12-31');
This query lets us know that 41,380 employees retiring. This is a large number of employees retiring and will start to advertise at big ticket recruitment events such as college campus’s job fairs, online job boards and social media. 

Knowing the number of employees we have approaching retirement it would also be helpful to know the names of the employees who are approaching retirement. Maybe they would be open to working part time or transitioning to consultants while we are bringing in new employees. To narrow down that list of employees we would run the following query:
SELECT first_name, last_name
FROM employees
WHERE (birth_date BETWEEN '1952-01-01' AND '1955-12-31')
AND (hire_date BETWEEN '1985-01-01' AND '1988-12-31');
This data presents us with this table (in a snapshot view). 
 
These are the employee’s approaching retirement and if we want additional data on these employees such as departments, we did that analysis earlier. 

The data we have presented and the analysis we have run has given the manager enough information to make informed decisions on where the data is going around retiring employees. There is still a lot more analysis we could do should the manager need additional information but this is a good start. 
