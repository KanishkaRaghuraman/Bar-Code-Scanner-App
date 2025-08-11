In this lesson, you will use the **ATP_Check** Action Project, which is already available in the lobby. This project leverages a service developed using **ABAP** to validate the availability of a requested material in the specified quantity. The service checks inventory and supply data and provides a response confirming whether the requested quantity can be fulfilled.

1. Open your **Sales Orders Management {placeholder\|userid}** project.

- Accept the **Disclaimer** if prompted.

2. Select the **Sales Order Processing** artifact.

   ![2_1_openprocess](./Images/410-2_1_openprocess.png)

   > The process begins with an API trigger, which will later be initiated by the application created using SAP Build Apps.

   ![2_1_process](./Images/410-2_1_process.png)

- In the following steps, we can check if the requested product is available in the specified quantity through an **Action** using a custom OData service developed in ABAP. 

3. As you see this process the first time, you probably want to know how it works. Choose **Generate** button and then choose **Explain this process**.

   ![explain](./Images/511-2-Explain_process.png)

4. The explanation may look like on the screenshot below. For example you can see that the approval step is depending on the requested quantity. We want to change it: the approval should be started only if the requested material is available in the backend.

   ![explanation](./Images/511-2-Process_Explanation.png)

5. Select **(+)** icon after the trigger to add a step to the process.

   ![2_1_addstep](./Images/410-2_1_addstep.png)

6. Select **Action** followed by **Browse All Actions**.

   ![2_AddActionProject](./Images/410-2_AddActionProject-2.png)

7. In the Browse library page, find the Action project **Add new entity to ATPCheck** and select **Add**.

   ![2_2_atpcheck](./Images/410-2_2_atpcheck.png)

8. In the **General** tab, look for the Destination Variable and select **+ Create Destination Variable** in the drop down.

   ![2_3_CreateDestinationVariable](./Images/410-2_3_CreateDestinationVariable.png)

9. A dialog opens to create a destination variable. Enter **ATPCheck** in the field **Identifier** and then select **Create**.

   ![ConfigureDestinationVariable](./Images/410-2_4_namedestvar.png)

10. Select the **Inputs** tab and configure the inputs section with the following fields

   | Form Input Fields    | Process Content Entry  |
   | -------------------- | ---------------------- |
   | Material             |  **material**          |
   | Quantity             |  **quantity**          |

   ![Auto Approval](./Images/410-2_5_configAction.png)

11. Select the **Condition** operator in the process editor and select **Open Condition Editor** to modify the condition.

   ![2_5_Condition](./Images/410-2_5_Condition.png)

12. Change the branch condition value to:

   **OverallStatus**   -   **is equal to** -  **available**

13. **Apply** the changes.

      ![2_6_condition_modify](./Images/410-2_6_condition_modify.png)
