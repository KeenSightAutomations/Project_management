# **Quarterly ROI Reporting Workflow Documentation**

This automated workflow compiles all completed projects in Airtable to produce quarterly reports, offering project managers key insights into project profitability and performance trends. By identifying projects with high and low ROI, the workflow aids decision-makers in optimizing strategies for future endeavors.
A new table is generated in Airtable each quarter, clearly indicating the corresponding quarter and year.
---

## **Global Workflow Overview**

<img width="674" alt="Quarterly ROI Reports" src="https://github.com/user-attachments/assets/d89c10ed-d179-487e-8f64-f249b035d7ff">


---

## **📊 Quarterly ROI Reporting**

This workflow automatically runs every quarter and generates a comprehensive report summarizing ROI performance for all completed projects. The report includes key insights such as the average ROI, ROI comparisons by project type, and identification of the top 10% highest and lowest ROI projects.

### **Workflow Steps**:
1. **Trigger: Scheduled Run**  
   The workflow is scheduled  to run at the end of each quarter. The trigger initiates the process of analyzing all projects marked as `Completed` in Airtable.

2. **Fetch Completed Projects**  
   The Airtable node retrieves all records where `Completion Status = "Completed"`. Key project details, such as `Project Name`, `Revenue Generated`, `Actual Costs`, `Project Type`, and `Client Name`, are fetched.

3. **Aggregate ROI Data**  
   Using a Code node, the workflow calculates:
   - **Average ROI:** Computes the average ROI across all completed projects.
   - **ROI by Project Type:** Groups projects by their `Project Type` and calculates the average ROI for each category.
   - **Top 10% Highest and Lowest ROI Projects:** Identifies the top 10% most and least profitable projects.

4. **Generate Airtable Report**  
   The aggregated insights are written back into Airtable, creating a detailed quarterly ROI report for easy reference and decision-making.


---


## **✨ Report Highlights**

### **1. Average ROI**
The report calculates and displays the average ROI for all completed projects in the quarter, offering an overview of overall performance.

### **2. Top 10% ROI Projects**
The top 10% most profitable projects are identified, highlighting factors contributing to their success.

### **3. Bottom 10% ROI Projects**
The bottom 10% least profitable projects are flagged, enabling project managers to review and address underlying issues.

---


## **Output & Result**

![image](https://github.com/user-attachments/assets/42efa3d4-6ec0-410e-bdf7-7a2e67dd6d53)


