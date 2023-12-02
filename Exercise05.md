# ChatGPT and Flow

## Exercise 5 - Classify text

- Start at [Power Automate](https://make.powerautomate.com/)

- With your environment selected choose **+ Create** from the navigation on the left. 

- Next click on the **Automated cloud flow** button.

    ![](images/autocloudflow.png)
    
- In the following dialog select **When a file is created** for **OneDrive for Business** then click **Create**

    ![](images/onedrive3.png)


- Click the **When a file is created** action.

    ![](images/when-file-created.png)

    
- Similar to the previous exercises we need to configure this trigger step. So select the step and choose a folder to use (eg. Root)

    ![](images/root.png)
    
- Next click on the plus sign and select **Add an action**

    ![](images/addaction.png)
    
- Search for **prompt** and click on the **See more** link under **AI Builder**

    ![](images/aibuildercreate.png)

    
- Choose **Classify text into categories with the standard model**

    ![](images/categorytext.png)
    
- Select **English** from the first dropdown for the selected step. Then select the **Text** box below and select the lightning bolt to choose **File content**

- Next click on the plus sign and select **Add an action**

    ![](images/add-action-after-category.png)    
    
- Search for **notification** and then select **Send me an email notification**

    ![](images/emailnotification.png)

- Click in the **Subject** text box and click on the lightning bolt

    ![](images/subject.png)
    
- For both **Subject** and **Body** select **Classification** from the options

    ![](images/classification.png)
    
- Click on **Save** and wait a few moments until you get a confirmation that the flow has been saved

    ![](images/readytotest.png)
    
- Then click on **Test** and choose the radio button for **Manually** and finally click the **Test** button. Similar to the previous exercise you need to kickoff the test, switch the **OneDrive** and upload one of the files in the **AIBuilderLabFiles\Reviews** folder.

- Now upload one of the review documents to **OneDrive for Business**

- Review the emails sent in Outlook Web Access to see their classification. 


>**Note**: *Sometimes more than one notification will come across.*