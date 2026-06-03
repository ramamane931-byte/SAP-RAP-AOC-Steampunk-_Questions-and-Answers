## Difference between %CID and %CID_REF: 


<img width="528" height="412" alt="image" src="https://github.com/user-attachments/assets/8b88f607-2888-4d56-8756-7d67ba1195e8" />


## RAP Response Parameters: FAILED, MAPPED, and REPORTED:


<img width="587" height="293" alt="image" src="https://github.com/user-attachments/assets/2674ebdd-ad88-4af5-b149-faa0e7c228f9" />


#### 1️. Trap: “Is a message with severity ERROR always required to fail the save?”

✅ Correct answer:

No.

In RAP, severity alone does not stop processing. The save will only stop if the instance is marked as failed.

👉 You must use failed-entity, not just an ERROR message.

<img width="593" height="379" alt="image" src="https://github.com/user-attachments/assets/8167ec08-ea79-438b-a838-45f4f5b3bde7" />


#### 2️. Trap: “Can a WARNING stop a save?”

✅ Correct:

Yes — if the instance is marked as failed, even a WARNING can stop the save.

👉 Severity controls UX, failed controls flow.

<img width="590" height="413" alt="image" src="https://github.com/user-attachments/assets/ca4f04f1-24fb-4440-891f-319ff840ad12" />



#### 3️. Trap: “If you don’t report a message, will RAP still fail the request?”

✅ Correct:

Yes.

RAP can fail a request without any reported message.

👉 The user just gets a generic error.

<img width="589" height="374" alt="image" src="https://github.com/user-attachments/assets/bb82afd2-d986-478b-b7f0-9f8951de5b1d" />



#### 4. Trap: “Mapped early is mandatory for validations, right?”

✅ Correct:

No.

Mapped early is optional and only improves error mapping and UX.

<img width="530" height="390" alt="image" src="https://github.com/user-attachments/assets/0178d33a-25ca-419c-8085-e0498002876e" />


#### 5️. Trap: “Is reported early the same as reported early response?”

❌ Wrong:

Yes, same thing.

✅ Correct:

No.

•	Reported early → developer action   // You write the message 📩

•	Reported early response → framework output   // System delivers it 📬

<img width="522" height="387" alt="image" src="https://github.com/user-attachments/assets/cd35f219-8af8-45aa-8d4f-d1b01a068c9c" />



#### 6️. Trap: “Can late message responses be customized?”
✅ Correct:

No.

Late responses come from framework or DB, not behavior code.


#### 7. Trap: “Why does my error message show but save still succeeds?”   // Check above Q.4 for detail answer.

Correct answer:

Because:

•	Message was reported

•	But instance was not marked as failed. 👉 Message ≠ stop.

#### 8️. Trap: “Where should duplicate checks be implemented?”

✅ Correct:

In check_before_save with early message response.

DB constraint is only a safety net.

Correct approach: check_before_save + early message

🧩 Behavior Definition

validation check_duplicate_email on save { create; update; }


#### 9️. Trap: “Are RAP messages always returned immediately?”

✅ Correct:

No.

Messages can be:

•	Early responses

•	Late responses

•	Or aggregated and returned at the end.

<img width="514" height="430" alt="image" src="https://github.com/user-attachments/assets/17c0c670-6e3e-4ce9-bde8-60f0e4f5e85e" />

<img width="424" height="86" alt="image" src="https://github.com/user-attachments/assets/bbe05fa4-986a-4504-b893-338f167342f9" />


#### 10. Trap: “Can you use MESSAGE e001(zmsg) in RAP?”

✅ Correct:

No.

RAP requires the message framework (new_message).

<img width="401" height="146" alt="image" src="https://github.com/user-attachments/assets/80c1adb2-d5e2-42bc-a73f-dddd48f60edf" />


#### 11. Trap: “If validation runs in draft, are messages returned multiple times?”

✅ Correct:

Yes.

Draft mode triggers validations frequently, so messages can appear repeatedly.


#### 12. Trap: “Does reporting a message always attach it to a field?”

✅ Correct:

No.

Field mapping is optional; messages can be:

•	Field-level

•	Entity-level

•	Global


<img width="517" height="400" alt="image" src="https://github.com/user-attachments/assets/0033a3b7-80e3-40d8-b7da-12f373c518a0" />

<img width="389" height="90" alt="image" src="https://github.com/user-attachments/assets/184f0b46-c527-49e2-a6ee-4f8139942774" />



#### 13. Trap: “Can early messages appear even if save fails later?”

✅ Correct answer:

Yes.

Early messages can be returned even if a late technical error occurs.

🎯 Scenario (Sales Order BO)

Rules:

1.	If amount > 10,000 → show early warning 

2.	During save → DB insert happens 

3.	But DB has a unique constraint → causes failure

<img width="517" height="350" alt="image" src="https://github.com/user-attachments/assets/7efa2003-3517-4ff6-8656-70ad29e9d5e2" />

✅ Correct approach (Real fix)

You must handle duplicates in RAP validation BEFORE DB

<img width="481" height="354" alt="image" src="https://github.com/user-attachments/assets/8828f06d-50fa-4ee6-86fc-8034474b19f5" />



#### 14. Trap: “Why do we avoid late message responses in Fiori apps?”

Correct answer:

Because:

•	No field mapping

•	Poor UX

•	Technical wording

•	Hard to fix by user

<img width="428" height="104" alt="image" src="https://github.com/user-attachments/assets/df54d561-50ac-4c0f-8027-a0c2d44bb894" />














      










