## What is ‘side effect’ in SAP RAP?

A side effect informs the RAP UI framework that certain fields or associations may have changed because of a field modification 

or action execution, and therefore need to be refreshed automatically.


<img width="594" height="319" alt="image" src="https://github.com/user-attachments/assets/b2b8542a-3c34-4a5c-9187-d1d1bcdac1fa" />


<img width="590" height="288" alt="image" src="https://github.com/user-attachments/assets/96958365-3dc2-4915-ae21-ba0d1865da13" />




## What is a ‘Virtual Element’ in SAP RAP?


There is a requirement to expose extra attributes out of cds entities which are not part of database table. 
Basically, we need to add virtual elements, they are never persisted in DB. The value comes from calculations from a class which 
developer needs to implement (on fly). If you worked with SAP UI5 development there is a similar concept called formatter.


We need to implement a special class that returns the value of the virtual element on the fly.
“A virtual element is a CDS field that is calculated at runtime through an ABAP class and is not physically stored in the database.”

<img width="591" height="347" alt="image" src="https://github.com/user-attachments/assets/1769dcf2-09dd-492d-9021-89028362df75" />

<img width="590" height="273" alt="image" src="https://github.com/user-attachments/assets/2db63e5d-ede0-4234-993b-f368961be864" />



## What is ‘with Additional Save’ in SAP RAP?


In Some application scenarios, an external functionality needed to be integrated once the RAP framework completes the save to DB with a custom save logic. 

For eg:

•	trigger a workflow only once travel request is created, 

•	send a email to stakeholder, 

•	call an API

•	audit logging, change history creation, or updating related custom tables.

•	writing audit records whenever a Purchase Order or Sales Order is created or updated.


<img width="644" height="364" alt="image" src="https://github.com/user-attachments/assets/c934aaa0-8d27-46ca-8997-a82091cda71e" />

<img width="644" height="209" alt="image" src="https://github.com/user-attachments/assets/10833b20-70fb-41d3-b8ca-28dbebb0b405" />

<img width="1166" height="268" alt="image" src="https://github.com/user-attachments/assets/1c72d91b-6843-4aac-ae06-a7d41ffb7566" />


<img width="554" height="320" alt="image" src="https://github.com/user-attachments/assets/19867b00-da15-423c-a8bd-e2396759add0" />




## What is a ‘Collaborative Draft’ in SAP RAP?


Collaborative Draft is a RAP draft feature that allows multiple users to work on the same business object draft instead of locking the draft to a single user.

Collaborative Draft allows multiple users to work on the same draft business object simultaneously. 
It is useful in business processes where several departments contribute information before the document is activated.


<img width="643" height="409" alt="image" src="https://github.com/user-attachments/assets/0cb96f5f-7bc9-4145-b5f5-0b3042ecf7b3" />

<img width="644" height="197" alt="image" src="https://github.com/user-attachments/assets/81b27842-e97d-4487-8f2e-fdbf2ee69a30" />

<img width="642" height="376" alt="image" src="https://github.com/user-attachments/assets/3a816326-2676-40ca-8539-660a6b2e729d" />













