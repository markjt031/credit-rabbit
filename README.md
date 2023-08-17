![](https://res.cloudinary.com/di8ugfihk/image/upload/t_Thumbnail/v1692311118/logo_mtc8zo.png)
# Credit Rabbit 

A data-driven, real-time credit score software that calculates and qualifies borrowers for credit and loans.

## Description 

This software application allows financial institutions and lenders to assess and qualify borrowers for credit and loans based on their financial and credit history. It provides a user-friendly interface for entering borrower information and enabling informed lending decisions.

This application was built for the Summer 2023 Financial Literacy Hackathon hosted by General Assembly. 

The project was a cross-team collaboration with the following members:

Software Engineers:
- Eric Hung
- Jessica Marks
- Aboubacar Zoungrana

Data Scientists:
- Jayson Villena
- Khalil K Davis

UX/UI Design:
- Dewey Song
- Michelle Lee

## Features
Our financial scoring algorithmns are based on public records and models built by the data team. Here is a snippet of our algorithmn that determines a percentage of income representing a debt to expense ratio and returns a passing or failing mark depending on the weighted standards.

```
    let percentage=loan_amnt/(person_income-other_payments)
    setFormData({...formData, percent_of_income: percentage})
    console.log(percentage)
    console.log(percentage<=.2)
    if (percentage<=.20 && percentage>0){
      console.log('here')
      loan_status=true
    }
    else if ((percentage<=0.5 && percentage>0.2) && cb_person_cred_hist_length>=2 && person_emp_length>=3 && person_age>=25){
      loan_status=true
    }
    else if ((percentage<=0.7 && percentage>0.5) && cb_person_cred_hist_length>=5 && person_emp_length>=5 && person_age>=28 && formData.defaultStatus==='no'){
      loan_status=true
    }
    else if ((percentage<1 && percentage>.7) && cb_person_cred_hist_length>=10 && person_emp_length>=10 && person_age>=30 && formData.defaultStatus==='no'){
      loan_status=true
    }
    else{
      loan_status=false
    }
```


## Technologies
![](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)

![](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

![](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)

![](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)

![](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

![](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)