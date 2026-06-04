## Method CHECK_BEFORE_SAVE use for Early messages or Late messages?: 

👉 CHECK_BEFORE_SAVE is used for late messages (but still before DB commit).

🧠 Why this is confusing (the trap):
“Before save” sounds like early, but in RAP lifecycle it is actually part of the late phase.


<img width="509" height="229" alt="image" src="https://github.com/user-attachments/assets/7246e1fa-ade2-4da4-9f66-69cbbd4389a9" />

<img width="481" height="313" alt="image" src="https://github.com/user-attachments/assets/80353504-548e-4990-ae96-1a5c3767a04a" />


## Created By Association:

Create by Association when there is need to create an instance based on another instance.

This type of creation used when there is an Association especially in case of Composition.

Create by Association (CBA) allows creation of a child entity instance through its parent association. 


<img width="515" height="145" alt="image" src="https://github.com/user-attachments/assets/5fa51f13-4ff2-4f0a-a015-23c6a7c28703" />

<img width="512" height="245" alt="image" src="https://github.com/user-attachments/assets/e7c765ff-7e20-4d79-abd8-e551c7a09445" />



## What is Pessimistic Concurrency in SAP RAP:

When one user edits a business object, the object is locked so that other users cannot modify it at the same time.
If a same record multiple users trying to edit then it will throw an error to other users except the user who first open the same record.
Pessimistic concurrency is preferred in highly transactional and conflict-prone business processes like finance, inventory, and reservations,


🧠 Why is it needed?

To prevent:

•	Lost updates 

•	Data inconsistencies 

•	Two users overwriting each other’s changes



<img width="565" height="345" alt="image" src="https://github.com/user-attachments/assets/06cf0691-4f52-496e-9091-a40dcc459b4a" />

<img width="568" height="421" alt="image" src="https://github.com/user-attachments/assets/73984ffa-ff62-4ed7-af99-326f81858bd5" />



## What is Optimistic Concurrency in SAP RAP?


Multiple users are allowed to edit the same business object simultaneously, and conflicts are checked only when saving.
Optimistic concurrency in RAP allows multiple users to edit the same business object simultaneously without locking. 
Conflicts are detected during save using ETags or timestamps to prevent overwriting changes made by another user.
Optimistic concurrency is better for low-conflict scenarios such as master data maintenance and collaborative applications.


<img width="569" height="311" alt="image" src="https://github.com/user-attachments/assets/bfcbd9e4-6447-4463-83dd-4adeea0baae1" />

<img width="566" height="279" alt="image" src="https://github.com/user-attachments/assets/8e67b9e4-19a1-45c5-8461-ae74e6521a47" />

<img width="563" height="376" alt="image" src="https://github.com/user-attachments/assets/0458b57e-f0c7-4b63-b39b-8303ad58c381" />



## Difference between Pessimistic and Optimistic Concurrency control

<img width="568" height="386" alt="image" src="https://github.com/user-attachments/assets/e18f3e5e-a576-4cdb-b60a-789c4ad7a454" />


Interview Trap Question

Q: Does ETag prevent two users from editing at same time?

✅ Correct: No


## Method check_before_save:

The method check_before_save is a validation hook that runs during the save sequence, just before the data is persisted to the database. 
Triggered before DB commit.

<img width="569" height="95" alt="image" src="https://github.com/user-attachments/assets/61dd7c12-a1b3-4afd-801c-ffcdd64fd6f9" />

Syntax:

Inside behavior implementation class:

METHOD check_before_save.

This method is redefined automatically when using unmanaged RAP or draft scenarios.


<img width="569" height="305" alt="image" src="https://github.com/user-attachments/assets/0d1aab97-8790-48bc-80fc-52a1664ae1e4" />


<img width="570" height="364" alt="image" src="https://github.com/user-attachments/assets/9d7561ab-d0af-4353-a179-b3c18ca093a4" />


RAP Save Sequence Overview

The RAP save lifecycle generally follows this order:

1.	Modify phase

•	create

•	update

•	delete

2.	Determinations

3.	Validations

4.	check_before_save

5.	Save to database

6.	Finalize










