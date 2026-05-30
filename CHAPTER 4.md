**What is ‘IN LOCAL MODE’ in SAP RAP?**


IN LOCAL MODE is used in RAP EML (Entity Manipulation Language) to process data inside the transactional buffer without triggering:

•	Database commit

•	Authorization checks

•	Determinations again

•	Validations again

•	Feature control


It works only within the current RAP transaction to improving performance and avoiding recursive framework execution.


<img width="650" height="314" alt="image" src="https://github.com/user-attachments/assets/db0470af-62e3-4686-b8b1-cc5ff68cdf78" />


<img width="648" height="214" alt="image" src="https://github.com/user-attachments/assets/b85b95ef-4cc1-4569-85c5-f5a81ac0ac7c" />


**Why is ‘IN LOCAL MODE’ mostly used in determinations?**


“Because determinations internally update entity data during transactional processing. LOCAL MODE prevents unnecessary RAP framework 
reprocessing and avoids recursive calls.”


**What is an ‘authorization master ( instance, global )’;**


<img width="531" height="413" alt="image" src="https://github.com/user-attachments/assets/329d6bd6-98e7-4186-883b-3ac713d72b6f" />


<img width="646" height="133" alt="image" src="https://github.com/user-attachments/assets/cdcb2587-2f0c-4a13-8f01-6a68d3ab0f54" />


**What is an ‘authorization dependent by _association’?**


“This child entity does not perform its own authorization check. It depends on the parent entity authorization.”


<img width="532" height="421" alt="image" src="https://github.com/user-attachments/assets/29613c82-b584-4182-a45f-511d35b07a07" />


<img width="535" height="328" alt="image" src="https://github.com/user-attachments/assets/e795fbbb-eb25-4ffb-a475-3efb7a41f3e5" />


**Difference between EARLY NUMBERING and LATE NUMBERING:**


<img width="475" height="392" alt="image" src="https://github.com/user-attachments/assets/cd56dc38-07b4-433d-bda9-e73263bccfb0" />


<img width="532" height="406" alt="image" src="https://github.com/user-attachments/assets/eb3b1edc-926b-4524-b60d-da85f53c5a6e" />



**What is ‘EARLYNUMBERING_CBA_BOOKING’?**


<img width="644" height="301" alt="image" src="https://github.com/user-attachments/assets/0e076b76-e426-42af-a54a-18516ce955c6" />








