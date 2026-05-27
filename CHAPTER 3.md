**What is a LOCK MASTER in RAP framework?**


<img width="593" height="209" alt="image" src="https://github.com/user-attachments/assets/6a2b32bc-6e1d-414d-bc61-f06eb44b08a9" />


**What is a LOCK MASTER TOTAL in RAP Framework?**


<img width="596" height="221" alt="image" src="https://github.com/user-attachments/assets/19f4e682-79c5-4612-a191-347f7634cae7" />



**What is a LOCK MASTER TOTAL ETAG LASTCHANGEAT in RAP Framework?**


<img width="592" height="368" alt="image" src="https://github.com/user-attachments/assets/93f9bb1e-d970-456f-bf5e-d0a79e94e587" />


**What is a ‘LOCK DEPENDENT BY _association’?**


“This child entity does not have its own lock. It depends on the parent entity’s lock.” 

That means a child entity does not maintain its own lock mechanism.


<img width="593" height="361" alt="image" src="https://github.com/user-attachments/assets/bac1a41e-dc3d-45a3-8440-8f77e89d5b32" />


**What is a ‘ETag DEPENDENT BY _association’?**


“This child entity does not maintain its own ETag field. It depends on the parent entity’s ETag for concurrency checking.” 


<img width="592" height="321" alt="image" src="https://github.com/user-attachments/assets/3bfdcd11-0ac7-4996-acda-e7d06eb0e928" />


**Difference between LOCK MASTER and ETAG MASTER?**


<img width="591" height="133" alt="image" src="https://github.com/user-attachments/assets/c1dc4757-0bd0-4d15-a221-4c5737e6b0cc" />



🎯 1. What is ETag in RAP?
✅ Answer:
ETag in RAP is used for optimistic locking. It ensures that a user does not overwrite changes made by another user by comparing 
a timestamp field (like LocalLastChangedAt) before saving.

________________________________________

🎯 2. Difference between etag master and etag dependent?
✅ Answer:
etag master uses the root entity’s timestamp for concurrency control, while etag dependent ensures consistency across the entire business 
object by using the parent entity’s ETag via association. In real projects, etag dependent is preferred for composed entities.

________________________________________

🎯 3. What happens if you don’t use ETag?
✅ Answer:
Without ETag, multiple users can overwrite each other’s changes, leading to data inconsistency and lost updates.

________________________________________

🎯 4. Difference between Locking and ETag?
✅ Answer:
Locking is pessimistic control (prevents others from editing), while ETag is optimistic control (detects conflicts at save time).

________________________________________

🎯 5. What is lock master total?
✅ Answer:
It locks the entire business object (root + child entities) during a transaction to prevent concurrent modifications.

________________________________________

🎯 6. Can we use both Lock and ETag together?
✅ Answer:
Yes, and it is recommended. Lock prevents parallel editing, while ETag ensures no overwrite happens if data changes after reading.

________________________________________

🎯 7. What is LocalLastChangedAt?
✅ Answer:
It is a timestamp field used by RAP to track the last modification of a record and is used for ETag comparison.

________________________________________

🎯 8. Where do you define ETag?
✅ Answer:
ETag is defined in the Behavior Definition (BDEF) using:** etag master LocalLastChangedAt**

________________________________________

🎯 9. What is etag dependent by _association?
✅ Answer:
It means the entity uses the parent entity’s ETag via the given association for concurrency control.

________________________________________

🎯 10. If a child entity is updated, how do you ensure the header detects it?
✅ Answer:
By using etag dependent by _association, so that any change in child updates the parent’s timestamp and triggers conflict detection.

________________________________________

🎯 11. How do you handle concurrency in RAP?
✅ Answer:
In RAP, I use both pessimistic and optimistic locking. I define lock master total to prevent parallel updates and use ETag with 
LocalLastChangedAt for conflict detection. For composed entities, I use etag dependent to ensure full business object consistency.





