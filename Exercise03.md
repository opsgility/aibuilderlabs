## Exercise 3 - Extract information from receipts

- Start at the [AI Builder site](https://powerapps.microsoft.com/ai-builder/)

- With your environment selected choose **AI Models** from the navigation. If it is not visible you might have to click the **... More** navigation to add it to the menu. 

    ![](images/aimodels.png)

- In the main portion of the screen click on the **Documents** tab to filter the results. Finally, select **Extract information from receipts**

    ![](images/textfromreceipts.png)
    
- In the dialog, click on **Use prebuilt model** and choose **Use in a flow** option from the dropdown. This means we will build a re-usable Power Automate Flow to create a re-usable Flow to Extract all the text in photos and PDF documents (OCR). 

- Select the **Track expenses by scanning receipts to your OneDrive for Business** template that is already pre-created.

    ![](images/expenses.png)

- Very similiar to the previous exercise validate that you see green checks next to all the connections. Then click **Continue**

    ![](images/continue2.png)
    
- Before configuring the **Flow** click on the nine square in the upper-right hand corner. Then select the three dots next to **OneDrive** and choose **Open in new tab**

    ![](images/onedrivetab.png)
    
- Upload the following [file](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/Receipts.xlsx) to use in this exercise.

- In OneDrive click on the **Add new** button and choose **Files upload**

- Select the **Receipts.xlsx** file previously downloaded and upload to **OneDrive**.

- Return to the **Flow** tab in the browser

- There are two steps that need additional configuration. Select the first step called **When a file is created**. When selected the properties panel will open. Click on the **folder** icon and choose **Root** to select the top level folder in **OneDrive**.

    ![](images/rootselected.png)
    
- Now select the fourth, and last step, called **Add a row into a table**. **Note:** this does require the file to uploaded from the previous step. 

    ![](images/addarow.png)
    
- In the properties panel choose the **Document Library** and select **OneDrive**

    ![](images/onedrive2.png)
    
- Next click on the folder icon and select the **Receipts.xlsx** file previously uploaded.

- In the **Table** dropdown select **Table1** which is defined in the Excel spreadsheet that was uploaded to OneDrive.

    ![](images/ttable1.png)
    
- In the **Advanced parameters** section you should see some pre-populated values. Click on the **Show all** link. This will show all the potential values available.

    ![](images/showall.png)
    
- From the **DateTime Format** dropdown choose **ISO 8601**

    ![](images/iso.png)

- To add additional parameters you can use the following animation to assist.

    ![](images/parmsmapping.gif)
    

- Click on **Save** in the upper right-hand corner

    ![](images/save1.png)
    
- Before running a test make sure you understand the steps

    - After clicking the **Test** button You will need to switch the the OneDrive tab, previously left open
    - Then you need to upload a receipts file to the root of OneDrive from the **ReceiptsProcessing_Contoso** folder previously downloaded.
    - When the file is uploaded it will trigger the **Flow** to activate
    
- Then click on **Test** and choose the radio button for **Manually** and finally click the **Test** button

    ![](images/test3.png)
    
- This shows the completed **Flow**

    ![](images/receiptsflow.png)
    
- Now switch back to the **OneDrive** tab and open the **Receipts.xlsx** file

- Depending on the parameters added and file chosen you might see different values

    ![](images/receiptout.png)