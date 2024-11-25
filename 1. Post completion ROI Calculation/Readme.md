# **Post-Completion ROI Calculation Workflow Documentation**

This automated workflow designed to calculate the ROI (Return on Investment) for completed projects in Airtable. The workflow streamlines post-completion project analysis by automating ROI calculation, ensuring timely and accurate data for decision-making.

---

## **Global Workflow Overview**

<img width="613" alt="Post completion ROI Calculation" src="https://github.com/user-attachments/assets/45604c58-6065-44cd-ab2d-6c8fcfeee7b6">


---

## **📊 Post-Completion ROI Calculation**

This workflow triggers automatically whenever a project is marked as "Completed" in Airtable. Upon triggering, the workflow calculates the **ROI** using the formula:

\[
\text{ROI (\%)} = \frac{\text{Revenue Generated} - \text{Actual Costs}}{\text{Actual Costs}} \times 100
\]

### **Workflow Steps**:
1. **Trigger: Record Update**  
   The workflow uses an Airtable trigger to listen for updates to the "Completion Status" field. If a record's status is updated to `Completed`, the workflow is activated.

2. **Fetch Project Details**  
   The relevant project details, such as `Revenue Generated`, `Actual Costs`, and `Completion Status`, are retrieved from Airtable.

3. **Calculate ROI**  
   A calculation node applies the formula to determine the project's ROI.  
   Example:
   - **Revenue Generated:** $60,000  
   - **Actual Costs:** $40,000  
   - **ROI (\%):** \[
   \frac{60,000 - 40,000}{40,000} \times 100 = 50\%
   \]

## **📂 Comparison Between Webhook and Polling**

This workflow is designed using the **polling method** due to Airtable's limitations for webhooks:

- **Webhook Limitations**:  
   Airtable requires a **paid plan** to enable the script feature necessary to configure webhooks. Without this feature, webhooks cannot be directly implemented.

- **Polling Method**:  
   This workflow uses a **polling-based trigger** to periodically check for updates in Airtable. While less immediate than webhooks, it is an effective method for users on Airtable's free plan.

| **Feature**               | **Webhook**                                 | **Polling**                                  |
|---------------------------|---------------------------------------------|---------------------------------------------|
| **Trigger Speed**         | Real-time                                   | Scheduled intervals                         |
| **Cost**                  | Requires Airtable paid plan                 | Works on Airtable free plan                 |
| **Setup Complexity**      | Requires script activation                  | Simpler, no advanced configuration needed   |
| **Use Case**              | Ideal for immediate actions upon updates   | Suitable for periodic checks and updates    |

---


## ** Output & Result**

![image](https://github.com/user-attachments/assets/88d9ae44-786f-4483-970a-4cc39f609de2)

