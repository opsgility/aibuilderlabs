## Exercise 7 - Summarize text custom

- Start at the [AI Builder site](https://powerapps.microsoft.com/ai-builder/)

- With your environment selected choose **AI Models** from the navigation. If it is not visible you might have to click the **... More** navigation to add it to the menu. 

    ![](images/aimodels.png)
    
- Under the **Most Popular** tab select **Prompts now have their own section**

- This will redirect and then choose **Create text, summarize documents, and more with GPT**.

    ![](images/gpt1.png)
    
- On the left hand side choose **Summarize text** from the options available

    ![](images/summarize.png)

- Click on the **Create custom prompt**

    ![](images/customprompt.png)
    
- Then click on the link text that says **start from existing template**

    ![](images/existingtemplate.png)

- Select **Summarize text** from the available options

    ![](images/summarizetemplate.png)

- Use [this link](https://www.prnewswire.com/news-releases/giant-food-donates-11-000-turkeys-to-support-local-feeding-america-food-banks-and-nonprofits-this-holiday-season-301992824.html) to summarize a press release. And copy and paste the content in the **Test your prompt** section for **TextToSummarize**. Click on **Test prompt** and finally click **Save custom prompt**

    ![](images/savesummary.png)
    
- Click on the text that starts with **Custom prompt** and includes a Date/Time value. Update the text to be your initials+Summarize (eg. BNSummarize)
    
> Let's use our new custom prompt in a flow

- Start at https://make.powerautomate.com/ and make sure your environment is selected

- Select the **+ Create** link in the left hand navigation

    ![](images/create.png)

- Click on **Automated cloud flow**

    ![](images/autocloudflow.png)
    
- In the following dialog select **When a file is created** for **OneDrive for Business** then click **Create**

    ![](images/onedrive3.png)
    
- Similar to the previous exercises we need to configure this trigger step. So select the step and choose a folder to use (eg. Root)

    ![](images/root.png)
    
- Next click on the plus sign and select **Add an action**

    ![](images/addaction.png)
    
- Search for **gpt** and then select on **Create text with GPT (V2)**

    ![](images/gptv2.png)
    
- From the dropdown choose your custom summarize prompt that starts with your initials

    ![](images/bnsummarize.png)
    
- After a moment you will get an additional textbox. Click inside of it. Click the lightning bolt and choose **File content**

    ![](images/filecontent1.png)
    
- Next click on the plus sign and select **Add an action**

    ![](images/addaction.png)    
    
- Search for **approval** and select **Start and wait for an approval**

    ![](images/waitforapproval.png)
    
- From the properties panel for the **Approval type** dropdown select the first option **Approve/Reject - First to respond**

> Note: This is a required step for any OpenAI generated content. No OpenAI content should be published with out approving first.

- After selecting that option there are more fields available

    ![](images/approval.png)
    
- Use the following to fill it in

    - **Title**: Approval
    - **Assigned To**: (use email address you are logged in with)
    - **Details**: Select the lightning bolt and choose **Text**
    - **Item link**: (leave blank)
    - **Item link Description**: (leave blank)
    
    ![](images/approvalset.png)
    
- Next click on the plus sign and select **Add an action**

    ![](images/addaction.png)    
    
- Search for **notification** and then select **Send me an email notification**

    ![](images/emailnotification.png)

- Click in the **Subject** text box and type in **Summary**

    ![](images/subject.png)
    
- For **Body** select **Test** from the options

    ![](images/summarize-text.png)
    
- Click on **Save** and wait a few moments until you get a confirmation that the flow has been saved

    ![](images/readytotest.png)
    
- Then click on **Test** and choose the radio button for **Manually** and finally click the **Test** button. Similar to the previous exercise you need to kickoff the test, switch the **OneDrive** and upload one of the files in [this zip file](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/reviews.zip). 

- Now upload one of the review documents to **OneDrive for Business**

> Note: With this test we need to approve the generated text

- Visit **Outlook Web Access**. You might get other notifications from other flows created. Look for the **Approval** email. The content will be a summary of the provided review. Similar to the following for **review3.txt**

    ![](images/realapproval.png)
    
- Click on **Approve** and a comment box appears. Click the **Submit** button

    ![](images/approve.png)
    
- Stay in **Outlook Web Access** and await the notification with the Subject title of **Summary**

    ![](images/thesummaryresult.png)