# school_district_analysis

## Overview:

Due to the fact that the cvs file: ***students_complete.csv***, shows evidence of academic dishonesty in ninth grade at the High School Thomas (THS), we had to modify this resource file to substitute with NaN values all the entries for this grade to be able to generate the following reports to the School Board.

The following reports were generated: 

  1. A district summary
  2. School summary
  3. Top 5 and bottom 5 performing schools based on overall passing rate
  4. The average math score for each grade level from each school
  5. The average reading score for each grade level from each school
  6. The scores by school speding per student, by school size and by school type

## Results:

By replacing with NaN values all the scores for THS for 9th grade, we 'removed' from the analysis 461 students. Before removing these students the total ```student_count``` was 39,170 and after subtracting the 461 9th students identified from THS, the ```new_student_count``` was 38,709.

We can see this student count in the image with the code below:

![student_count](https://user-images.githubusercontent.com/78564912/136856224-f6a375c7-cec3-453e-aa14-7cf008f4abce.png)

We address the following questions from the School Board:

**1. How is the district summary affected?**

  Since we are removing from the calculation the 9th math and reading grades' scores for THS there is a slight difference:
  
  - Before:
    
    - % Passing Math: 75.0%
    
    - % Passing Reading: 85.8%
    
    - % Overall Passing: 65.2%
    
    ![district_summary_before](https://user-images.githubusercontent.com/78564912/136855909-b4ee6992-2367-4176-acf6-8e91d550742d.png)
    
  
  - After:
      
    - % Passing Math: 74.8%
    
    - % Passing Reading: 85.7%
    
    - % Overall Passing: 64.9%
    
    ![distric_summary_after](https://user-images.githubusercontent.com/78564912/136855919-bae2bef9-a50b-4728-8327-f6d661f6f6e4.png)

**2. How is the school summary affected?**

This Data Frame is the one with the biggest changes in the analysis:

  - Before:
    
    - % Passing Math: 66.91%
    
    - % Passing Reading: 69.66%
    
    - % Overall Passing: 65.07%
  
  ![school_summary_before](https://user-images.githubusercontent.com/78564912/136864981-d0cedc1f-b74f-41a5-8a22-b0f9b9eca32f.png)

  - After:
      
    - % Passing Math: 93.18%
    
    - % Passing Reading: 97.01%
    
    - % Overall Passing: 90.63%

  ![school_summary_after](https://user-images.githubusercontent.com/78564912/136864990-ff3b344c-ee91-44a8-ad9e-87d7167b080a.png)

**3. How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?**

Generally the performance of Thomas High School relative to the other High Schools, improved ~ 25% from ~ 60% for the above three metrics to ~ 90%, where the biggest difference is seen in the % Passing Reading from 69.66% to 97.01%

- How does replacing the ninth-grade scores affect the following:
  
  -  Math scores by grade:
     
     The only the visible changes for the math scores by grade were the NaN values.

    ![math_after](https://user-images.githubusercontent.com/78564912/136866164-9d9d0bcd-53a4-4d2a-b16f-8704b2d2bd43.png)   ![math_before](https://user-images.githubusercontent.com/78564912/136866175-57c3883a-df82-44e9-8fd0-66934fb1256d.png)
    
  -  Reading scores by grade:
     
     Only the visible changes for the reading scores by grade were the NaN values.
 
    ![reading_after](https://user-images.githubusercontent.com/78564912/136866259-9975170f-791f-4f25-bbc0-2f8620c6c9e9.png)   ![reading_before](https://user-images.githubusercontent.com/78564912/136866277-40496000-84c0-40d8-9891-f4872843c358.png)

  -  Scores by school spending:
  
     The scores before and after by spending are very subtle for row of $630-644 for the 5 metrics analyzed.
    
    ![spending_before](https://user-images.githubusercontent.com/78564912/136866434-eb3069c3-d441-4175-a5c5-c38724f1fd12.png)
    
    ![spending_after](https://user-images.githubusercontent.com/78564912/136866413-3eb73b44-b0d8-448a-83fb-63b3911ceee8.png)

  -  Scores by school size:
     
     Also for this data frame the changes are very subtle, but now for row of school size 'Medium' for all 5 five metrics.
  
    ![size_before](https://user-images.githubusercontent.com/78564912/136866457-183d6c8f-5b06-4f64-99c2-eaae53660ce3.png)

    ![size_after](https://user-images.githubusercontent.com/78564912/136866476-3a437eed-29b8-4a89-8379-2a3ce6f507f4.png)


  -  Scores by school type:
     
     Finally, the changes before and after replacing with NaN related to the school type are very margin, where the school type Charter   is the one presenting these differences.
 
    ![type_before](https://user-images.githubusercontent.com/78564912/136866568-e7222193-c534-42dd-afbf-412c98252432.png)
    
    ![type_after](https://user-images.githubusercontent.com/78564912/136866581-dbfbaa79-bfda-48f7-9c71-8122a5bc6528.png)

## Summary:

While analyzing and merging both datasets and before removing the values for 9th grade for THS, this school, 1) was in the 8th in the '% Overall Passing' ranking with a 65.07%, 2) and after removing those values, the same metric, made it climb in the ranking position until the 3rd place with 90.63% 'Overall Passing' score, being one of the top 5 High Schools. 3) THS, also improved its '% Passing Math' and '% Passing Reading', the difference in both metrics after removing the NaN values increased by more than 20%.
