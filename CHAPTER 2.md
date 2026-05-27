**Difference between Association and Composition:**

<img width="594" height="141" alt="image" src="https://github.com/user-attachments/assets/308166d5-6d97-4e8a-b9f6-90afd4966a6c" />


**What is a Projection in SAP RAP?**

“Exposing only the required fields and operations from the main Business Object to external consumers like Fiori UI or OData services.”
A projection layer is an extraction of core functionality from reuse layer. The reuse layer offers all the full-blown functionality (FMs, Classes, Tables, Str…). 
For a particular user group, we want to design application, hence we don’t need entire functionality to be exposed to our user.

We take the Base (Reuse) layer, and build projection on top of it. Build the services, and UIs on top of it. The advantage is that you can design 
and develop many solutions for different user groups in your company like sales representative, sales manager, sales area head, sales accountant, 
sales lead, without compromising reusability. The redundancy is removed.


**What is Strict ( 2 ); keyword in RAP ?**

“strict ( 2 ) in RAP enables strong syntax and behaviour checks to enforce clean, cloud-ready, and future-proof RAP development standards.” Syntax check, 
clean coding, BTP Compatible coding, Strong validation/ Cleaner BO design. 

<img width="593" height="71" alt="image" src="https://github.com/user-attachments/assets/173ec088-c220-414e-84e6-a771c8627997" />


**Difference between MANAGED and UNMANAGED implementation:**

<img width="590" height="320" alt="image" src="https://github.com/user-attachments/assets/b96e00a1-a629-40b6-bfc9-53a1baf85486" />


**Difference between draft and collaborative draft?**

<img width="593" height="295" alt="image" src="https://github.com/user-attachments/assets/65d82853-4771-4695-a9a7-cf92c99e9dfc" />


**Persistence Table and Draft Table:**

The persistence table stores active business data. RAP framework tells that it should CREATE, UPDATE, MODIFY, DELETE data from which table that is a persistence table.

The draft table stores temporary editable copy of a data before final activation in RAP draft-enabled applications.

<img width="186" height="110" alt="image" src="https://github.com/user-attachments/assets/bb73711e-29cc-4d99-985a-1ac3d9c6d18c" />

