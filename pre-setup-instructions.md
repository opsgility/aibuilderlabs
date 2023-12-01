# Environment Setup

## Task 1 – Setup

The following instructions should be completed by a single member of your team to setup your environment. 

Task #1 - Acquire your Microsoft Power Platform trial tenant

1.  Copy your **Microsoft 365 credentials** from the credentials provided to you by your coach. 

1.  Navigate to the following URL and select **Start free**.

    ```
    https://powerapps.microsoft.com/en-us/free/
    ```

1.  Click **Use Apps** and then **Start Using Apps**

    ![](images/start-trial.png)

1.  Under **Let's get started**, enter the email address provided to you and select **Start your free trial**. 

1.  If an extra page appears with **Start building apps** and **Start using apps** buttons, then click **Start using apps** - not Start building apps.

1.  If you see a prompt that you have an existing account with Microsoft. Select **Sign in**. 

1.  Enter the password provided by the Authorized Lab Hoster and select **Sign in**. 

1.  Select **Yes** to stay signed in. 

## Task 2 – Environment

Task #2 – Create environment

1.  Navigate to <https://admin.powerplatform.microsoft.com> and log in with your Microsoft 365 credentials, if prompted. 

1.  If you see a Welcome pop-up, select **Get Started**. 

1.  Select **Environments** and select **+ New**.

    1. For **Name**, enter **[My Initials] Practice** (Example: AJ Practice).

    1. For **Type**, choose **Trial** (Do not select the *Trial (subscription-based)* option).

    1. Change the toggle for **Add a Dataverse data store?** to **Yes**. 

    1. Leave all other selections as default and select **Next**. 

    1. Under the the **Security group** heading, use the **+ Select** button.

    1. Select the checkbox for the **None** item, under the **Open access** heading and then select **Done**.

    1. Leave the remaining options at their defaults and select **Save**. 

1.  Your **Practice** environment should now appear in the list of Environments. 

    > Your environment may take a few minutes to provision. Refresh the page if needed.
    
## Task 3 – AI Builder Trial

Task #3 - Setup a trial
1. Visit the [AI Builder site](https://powerapps.microsoft.com/ai-builder/)

1. Click **Start free**

    ![](images/startfree.png)
    
1. If you are not redirected click on the **Start free trial** button in the header

    ![](images/freetrial.png)
    
## Task 4 - Data setup

Task #4 - Manual data set up

1. Import [AIBuilderLabSolution_1_0_0_1](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/AIBuilderLabSolution_1_0_0_2.zip) solution to the Dataverse environment

   - On the left navigation, click Solutions (if it's missing look under More..)
   - Click Create a Database, when prompted uncheck Sample Data and Applications then click Create
   - it will take several minutes to create - refresh your browser occasionally until the database is created 
   - At the top of the screen, click Import Solution and browse to the downloaded solution file.
 
    This will create five (5) Dataverse tables - **Object Detection Product**, **Health Feedback**, **Online Shopping Intent**, **Travel Feedback**, and **Expenses**.

1. Step 2: Upload data to the entities created in step 1

- **Prediction**: Follow the instructions in to upload the **Online Shopping Intent** data.
     - Download the  [AIBPredictionSample_simpledeploy_v4.21.3.zip](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/AIBPredictionSample_simpledeploy_v4.21.3.zip)
     - Ensure that the file isn't blocked after you download. To do this:  
    In the Downloads folder, find the downloaded zip file, right-click, and then select Properties.
    
    ![](images/unblock.png)
    
    On the General tab, select the Unblock checkbox, and then select Apply.
    - Extract the .zip file, and look for PackageDeployer.exe in the extracted folder.
    
    ![](images/packagedeployer.png)
    - Run PackageDeployer.exe. The following screen will appear.
    
    ![](images/deployscreen.png)
    
    - Select Continue.

    - Select Office 365, and then select Login.
    
      ![](images/o365.png)
    - Enter the credentials that you use to sign in to the Power Apps maker portal, and then select Next.
    
    ![](images/creds.png)
    
    - If the sign-in is successful, you'll see the Welcome screen. Read the message, and then select Next.
    
    ![](images/sampledata.png)
    
    - On the Ready to Install screen, make sure you're installing the solution in the correct environment and then select Next.
    
    ![](images/ready.png)
    
    - On the Reading AIB Prediction Dataset Installer Configuration screen, read the summary information for the data and solutions being imported and then select Next.

    It will take a few minutes to import the data. As each step is completed successfully, you'll see a green circle with a check mark next to the step.
    
    ![](images/config.png)
    
    - On the Installation Complete screen, select Finish.
    
    ![](images/finish.png)
    
- **Category classification**: Go to the **Lab Data/CategoryClassification** folder within the lab files, and then upload the data from **[aib_categoryclassification](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/aib_categoryclassification.xlsx)**. Follow the instructions below:

    - Select the appropriate environment you want to work in.
    - Select Data > Tables.
    - Select Data > Get data > Get data from Excel from the ribbon of the selected table.
    
    ![](images/getdata.png)
    
    - On the Import data screen, select the [Excel file](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/aib_categoryclassification.xlsx) and then select Upload.
    
    ![](images/import.png)
    
    - To review the field mappings on the Column mappings for Text Category screen, select Map Columns.
    
    ![](images/mapping.png)
        
    The left side lists all columns defined in the table. The dropdown list on the right shows the columns available in the Excel file.

    Map the Tags, Text, and Id columns from Excel to the respective columns in the table.

    - After you've mapped the columns, go back to the import step by selecting Save changes in the upper-right corner.
    
    ![](images/save.png)
    
    - After you see the Mapping status as successful, begin the import process by selecting Import in the upper-right corner.
    
    ![](images/import2.png)
    
    - The import process might take a few minutes depending on the volume of data being imported. After a few minutes, refresh the Data tab of the table to find all the records imported from the Excel file.
    
- **Entity extraction**: Go to the **Lab Data/EntityExtraction** folder with the lab files, and then upload the data from **aib_travelfeedback**. 
    - Select Solutions > AIBuilderLabs > Tables > Travel Feedback.
    
    ![](images/travel.png)
    
    - Select Data > Get data > Get data from Excel from the ribbon.
    
    ![](images/getdata1.png)
    
    - You'll see the Import data screen:
    
    ![](images/importdata.png)
    
    - Select [aib_travelfeedback.csv](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/EntityClassification/aib_travelfeedback.csv), which has the data to be imported in this table.
    
    ![](images/import3.png)
    
    - Review the column mappings by selecting Map columns.

    - Map the Name and Comments columns in the Source values column, and select Save changes.
    
    ![](images/mapsave.png)
    
    You'll return to the Import data screen with status updated to reflect that the mappings are complete.
    
    ![](images/mappingsuccess.png)
    
    - Select **Import** on the top right for the import process to begin.

    It might take a few minutes for the import process to complete, depending on the rows included in the file provided.

    - Select the Data tab for the Travel Feedback table in the solution to view all the records imported
    
    ![](images/import4.png)

    > **Note**: For business card reader, document processing, identity document reader, object detection, receipt processing, and text recognition labs, you'll need images/pdfs that are available in the **[LabImages](https://opsgilitylabs.blob.core.windows.net/public/aibuilder/LabImages.zip)** downloaded folder.
