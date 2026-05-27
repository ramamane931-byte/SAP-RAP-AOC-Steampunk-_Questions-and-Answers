# SAP-RAP-AOC-Steampunk-_Questions-and-Answers
SAP RAP ABAP on Cloud ( Embedded Steampunk ) Questions and Answers:---->

**What is SAP BTP?**
SAP Business Technology Platform (SAP BTP) official overview is SAP’s cloud platform for building, integrating, automating, extending, and analysing business applications.
“SAP BTP is SAP’s cloud platform used to build apps, integrate systems, automate processes, and analyze data. It helps extend SAP applications in a clean core and modern way 
using cloud services like HANA Cloud, Integration Suite, and SAP Build.”
SAP BTP is a Platform As A Service (PaaS) by SAP where the Infrastructure is provided by SAP partners (GCP, AWS, Azure). The platform can be used by development teams to 
design, develop, package, deploy, and manage end to end cloud applications (SaaS) for the business users.
The advantage of this platform is Scalability, Elasticity, Lower TCO. BTP is not just only used by development teams to develop applications but can be used to perform:
<img width="648" height="88" alt="image" src="https://github.com/user-attachments/assets/6062656c-47e8-4f8b-902a-49b982acc944" />
<img width="590" height="410" alt="image" src="https://github.com/user-attachments/assets/a6b00d65-7275-4923-9aa0-3fcccfb33dbe" />
<img width="593" height="337" alt="image" src="https://github.com/user-attachments/assets/6f9887f4-d447-45b3-967e-9d2fc9df76e7" />

**What is the meaning of clean core?**
Keep the SAP standard system (S/4HANA core) as unchanged as possible and build extensions only through released, upgrade-safe mechanisms.
<img width="596" height="353" alt="image" src="https://github.com/user-attachments/assets/4a108f04-061e-4854-9b55-400695de8a5b" />

**is RAP Steampunk a SaaS environment or else?**
RAP Steampunk refers to SAP BTP ABAP Environment, which is a PaaS offering on SAP BTP used to build cloud-native ABAP applications using RAP.
<img width="593" height="101" alt="image" src="https://github.com/user-attachments/assets/7bd91e25-e068-4f74-a350-cf87d48b9e4a" />

**is Cloud Foundry a PaaS Environment?**
Cloud Foundry is a PaaS environment. In SAP BTP, it is used to develop, deploy, and run cloud-native applications without managing underlying infrastructure.
<img width="591" height="137" alt="image" src="https://github.com/user-attachments/assets/d41c8168-64bd-488e-85a8-6329db02813b" />

**What is a Business Object (BO) in RAP?**
“A business object represents a composition tree which starts with a root node and have multiple child nodes inside = each node is a cds entity.”
Behavior Definition: Create, Update, Lock, Delete, Action, ETag, Authorizations, and Feature Control Draft.
Once the BO is ready to be used, we define services using service definition and service binding.
Once the services are ready, we can consume them to create a Fiori App or an Integration. Where user interaction phase with UI then SAVE sequence executed.
A Business Object in RAP is a business entity that combines data, behavior, validations, and actions to represent a complete business process.
<img width="593" height="195" alt="image" src="https://github.com/user-attachments/assets/7127dc94-4b19-438b-a6c0-b27cefd19fe1" />





