## Validation:

Validation is used to check whether business data is correct before saving.

If data is invalid:

•	Error/warning message is shown 

•	Save operation can be stopped

•	Validation is a method triggered automatically during transactional processing.


<img width="700" height="398" alt="image" src="https://github.com/user-attachments/assets/92c49b15-6b50-4d91-95ec-851aac01c817" />

<img width="529" height="409" alt="image" src="https://github.com/user-attachments/assets/422d9444-619f-44b8-9a93-b801b09ec321" />



## What is Determination in RAP:


Determination is used to automatically derive, calculate, or fill data during transactional processing.

Unlike validation:

•	Determination does NOT block save 

•	It automatically updates fields


<img width="530" height="420" alt="image" src="https://github.com/user-attachments/assets/d7efec89-a1d9-4d0c-8c4c-c95e894bbb80" />

<img width="530" height="226" alt="image" src="https://github.com/user-attachments/assets/474e9b44-5de6-4512-9ecf-876d8d122cb7" />



## What is ‘precheck’ in RAP:

A Precheck is a RAP framework hook that executes before data is written to the transactional buffer.

<img width="531" height="416" alt="image" src="https://github.com/user-attachments/assets/96fb002e-c5f2-4d45-ab85-d75e357a58f4" />

<img width="535" height="289" alt="image" src="https://github.com/user-attachments/assets/68c2730a-e644-429f-84ac-76181c4fe295" />



## Difference between PRECHECK and DETERMINATION and VALIDATION?

<img width="592" height="182" alt="image" src="https://github.com/user-attachments/assets/296d31f2-acb7-4f57-ba95-7c2b9c3d998c" />



## What is Augmenting Operations in SAP RAP?

Augment in RAP is used to enhance or modify incoming create/update requests before standard RAP processing starts.


<img width="589" height="380" alt="image" src="https://github.com/user-attachments/assets/a1689035-9b66-402d-b1a2-a4d4e891482f" />

<img width="590" height="229" alt="image" src="https://github.com/user-attachments/assets/fe302176-9a86-4702-9319-a4d297d27140" />


## Difference between AUGMENT and DETERMINATION?

<img width="593" height="130" alt="image" src="https://github.com/user-attachments/assets/d2e6dd0e-cd7d-4f2e-9ac3-1ff7dd5a5d29" />



<img width="542" height="281" alt="image" src="https://github.com/user-attachments/assets/715f86c6-3aa6-47d1-b4e4-6b6cb7fb774b" />



### Q3. What is the use of IN LOCAL MODE?

Answer: It performs transactional buffer updates without immediate database commit.




## What is an Internal Action in SAP RAP?


<img width="589" height="374" alt="image" src="https://github.com/user-attachments/assets/854143c9-4bad-4bce-881f-774af12e246d" />

<img width="593" height="281" alt="image" src="https://github.com/user-attachments/assets/eb921a07-3133-46d7-88d7-8cf22e3215ed" />
























