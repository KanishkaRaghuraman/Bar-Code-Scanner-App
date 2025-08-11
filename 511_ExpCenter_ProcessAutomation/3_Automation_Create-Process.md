In this lesson, you will notify the user if the requested quantity is not available in the backend system.

1. Choose **+** on the **Default** branch of the condition.

    ![alt text](./Images/511-3-Add_Node_To_Condition.png) 

2. Choose **Form**.

    ![alt text](./Images/511-3-Choose-Node-Type.png) 

3. Paste the following prompt to the **Ask AI** field and then choose **Generate**.

    ~~~
    Create form that will notify the recepient that the requested material is not available with the requested quantity. The form should have the following inputs: availability status, material name, quantity.
    ~~~

    ![alt text](./Images/511-3-Use_GenAI_Prompt.png)

4. Select the new form and go to **General** tab. Enter **Material is not available** in the **Subject** field. Then choose **Users** field and in the popup window select **Process Inputs** > **salesorderdetails** > **email**.

    ![alt text](./Images/511-3-Fill_Form_General_Data.png) 

5. Select **Inputs** tab. Fill the following field with the following data:

    | Field                   | Data                                                               |
    | ----------------------- | ------------------------------------------------------------------ |
    | **Availability Status** | **Add new entity to ATPCheck 1** > **result** > **OverallStatus**  |
    | **Material Name**       | **Process Inputs** > **salesorderdetails** > **material**          |
    | **Quantity**            | **Process Inputs** > **salesorderdetails** > **quantity**          |
    
    ![alt text](./Images/511-3-Fill_Form_Inputs.png) 

    > NOTE: your input fields can be different as you see in the tutorial. It's ok, as the AI can generate unexpected output. Just use the common sense when you map the fields (e.g. you can leave some fields empty).

6. Open **General** tab again. Then choose **Open Editor**.

    ![alt text](./Images/511-3-Open_Editor.png) 

7. You can see the layout of the notification form here. In the productive scenarios you would probably want to change something here. But for the tutorial leave it as is. You can close the tab with the editor.

    ![alt text](./Images/511-3-Form_Overview.png) 

8. **Save** your work.

    ![Save](./Images/511-3-Save.png)
