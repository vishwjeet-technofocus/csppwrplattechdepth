# <img src="./media/image1.png" style="width:6.44028in;height:2.5in" />Level-up CSP Technical Training – Power Platform

# Digitize and automate approvals using Power Platform

| Description      |A hands-on experience to inspire users to use Microsoft Power Platform tools to design and implement digital systems to meet business objectives.                                                                                                   |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prerequisites    | To get the most out of this training we recommend you have admin access with Power Apps for Developer and Power Automate.                                                                                                                           |
| Audience         | Microsoft partners will deliver this workshop to CSP customers, who have multiple employees in their company, have a Microsoft Power Apps for Developer and Microsoft Power Automate license, and have minimal Microsoft Power Platform experience. |
| Duration         | 30 minutes                                                                                                                                                                                                                                          |
| Publication date | September 2024                                                                                                                                                                                                                                      |

This document is provided “as-is”. Information and views expressed in
this document, including URL and other Internet Web site references, may
change without notice. You bear the risk of using it.

This document does not provide you with any legal rights to any
intellectual property in any Microsoft product. You may copy and use
this document for your internal reference purposes.

© 2024 Microsoft. All rights reserved.

# Objective and scenario

## Objective

Develop an Expense Report application that streamlines and automates the
approval workflow for employee expenses.

## Solution focus area

Contoso Corp, a specialty Coffee Maker production company, manufactures
both consumer and commercial Coffee Makers. Currently, Contoso Corp has
been using a Microsoft Excel workbook to track employee expenses. When
an employee embarks on a business trip, they enter their total travel
expenses into a spreadsheet and then email the completed spreadsheet to
the Manager of the Accounts department. After the Manager has approved
the expenses, they will send the spreadsheet by email to the Accounts
Officer, which has its own internal approval process. Finally, the
employee will receive reimbursement.

Contoso Corp has faced several challenges with the current process,
which is not only lengthy but also complicates version control when
changes are required.

Contoso Corp needs a new solution that can:

- Create a mobile app so that employees can record expenses as they
  occur.

- Directly alert Accounts Officer of approvals automatically.

- Notify the employees about approval or rejection of the
  reimbursements.

Based on these requirements, you've decided to create a canvas app using
Power Apps and an approval flow using Power Automate. You will use
Microsoft Dataverse to store your data. Dataverse already has access to
your users and works with canvas apps seamlessly.

## Personas and scenario 

- **Remy Morris** - Digital Solutions Architect

- **Mark Brown** – Project lead

- **David Flores** – App developer

- **Jane Miller** – App tester

These personas will participate in the following sequential scenarios:

- Remy Morris, Digital Solutions Architect at Contoso Corp, creates and
  plans digital architecture that aligns with the business need and
  articulates this framework to Mark Brown, the Project Lead at Contoso
  Corp, and assists him in selecting the most suitable Power Platform
  tools for the implementation of the digital solutions.

- Mark Brown provides David Flores with an overview of the tools and
  processes involved in developing a canvas app using Power Apps and
  creating an approval flow using Power Automate.

- David successfully creates a canvas app and an approval flow,
  fulfilling all the requirements of Contoso Corp to streamline and
  automate the approval workflow for employee expenses, which he then
  submits to Jane Miller for testing.

- After thorough testing and validation, Mark Brown officially hands
  over the app to the team, enabling them to process the employee
  expense approvals efficiently.

# Pre-requisites

For this use case, all participants will need the following:

- Microsoft Power Apps for Developer license

- Microsoft Power Automate License

- Windows 10/11 License

- Microsoft 365 Business Premium/E3/E5

- Their own devices with Wi-Fi connection.

# Lab instructions

## Exercise 1: Create an Expense Report App

In this exercise, you will create a data model in Microsoft Dataverse,
build your application with the data model and add or modify screens in
the app.

### Task 1: Sign in to Power Apps

1.  Use an In-Private or Incognito window and go to [Microsoft Power
    Apps](https://make.powerapps.com/).

2.  Select the **Dev One** environment from the **Environment** dropdown
    menu in the upper-right corner.

<img src="./media/image2.png" style="width:6.5in;height:2.64931in"
alt="A screenshot of a computer Description automatically generated" />

### Task 2: Create a table with Microsoft Dataverse

Now that you have changed your default environment, it’s time to set up
the application database. 

1.  On the left navigation, select **Tables**.

> If the **Tables** tab is not visible on the left navigation, select
> **More** and then select **Tables**.

<img src="./media/image3.png" style="width:6.5in;height:3.56736in"
alt="A screenshot of a computer Description automatically generated" />

2.  From the upper ribbon, select **New table \> Set advanced
    properties**.

<img src="./media/image4.png" style="width:4.84209in;height:4.05869in"
alt="A screenshot of a computer Description automatically generated" />

3.  On the **New table** pane, on the **Properties** tab, enter the
    following information.

    - **Display name** - Expenses on business trip

    - Select **Enable attachments**.

<img src="./media/image5.png" style="width:5.21712in;height:7.51732in"
alt="A screenshot of a computer Description automatically generated" />

4.  Select the **Primary column** tab, enter **Name of employee** in the
    **Default name** field and select **Save**.

<img src="./media/image6.png" style="width:3.91489in;height:5.60967in"
alt="A screenshot of a computer Description automatically generated" />

5.  You will be directed to a page informing you that your table has
    been provisioned successfully.

<img src="./media/image7.png" style="width:6.5in;height:2.36458in"
alt="A screenshot of a computer Description automatically generated" />

6.  In the **Expenses on business trip columns and data** area, select
    **Create a new column** to add columns.

<img src="./media/image8.png" style="width:6.5in;height:2.38333in"
alt="A screenshot of a computer Description automatically generated" />

7.  On the **New column** pane, enter the following information and
    select **Save**.

    - **Display name** – Email ID

    - **Data type** – Single line of format

    - **Format** – Text

    - **Required** – Business required

<img src="./media/image9.png"
style="width:3.12605in;height:6.01322in" />

8.  Once the column is saved, select the ‘**+**’ sign to add a new
    column.

9.  Enter the following information in the **New column** pane and
    select **Save**.

    - **Display name** – Employee position

    - **Data type** – Single line of text

    - **Format** – Text

    - **Required** – Business required

<img src="./media/image10.png" style="width:3.60865in;height:7.37564in"
alt="A screenshot of a computer Description automatically generated" />

10. Add a new column with the following details and then select
    **Save**.

- **Display name** – Trip destination

- **Data type** – Single line of text

- **Format** – Text

- **Required** – Business required

<img src="./media/image11.png" style="width:3.15766in;height:6.40242in"
alt="A screenshot of a computer Description automatically generated" />

11. Add a new column with the following details and then select
    **Save**.

- **Display name** – Number of days of travel

- **Data type** – Number \> Whole number

- **Required** – Business required

<img src="./media/image12.png" style="width:3.06628in;height:6.28197in"
alt="A screenshot of a computer Description automatically generated" />

12. Add a new column with the following details and then select
    **Save**.

- **Display name** – Date of application

- **Data type** – Date and time \> Date only

- **Format** – Date only

- **Required** – Business required

<img src="./media/image13.png" style="width:3.23333in;height:6.35791in"
alt="A screenshot of a computer Description automatically generated" />

13. Add a new column with the following details and then select
    **Save**.

- **Display name** – Amount requested

- **Data type** – Number \> Decimal

- **Required** – Business required

<img src="./media/image14.png" style="width:3.66698in;height:7.21729in"
alt="A screenshot of a computer Description automatically generated" />

### Task 3: Build your application with Microsoft Dataverse

1.  Select **Create** on the left navigation and then
    select **Dataverse**.

<img src="./media/image15.png" style="width:6.5in;height:4.00972in" />

2.  On the **Connections** page, select **New connection**.

<img src="./media/image16.png"
style="width:6.13386in;height:3.56698in" />

3.  Select **Microsoft Dataverse** from the Connections list.

<img src="./media/image17.png"
style="width:3.70184in;height:3.71326in" />

4.  Select **Create**. A Sign-in pop-up will appear. **Sign in** with
    your **Tenant Admin credentials**.

<img src="./media/image18.png" style="width:6.5in;height:2.35347in" />

5.  After signing in, select **Allow access** on the pop-up window.

<img src="./media/image19.png"
style="width:4.70484in;height:3.67684in" />

6.  Once the Dataverse connection is established, you can see the tables
    in your environment. Choose **Expenses on business trips** table.
    Select **Connect**.

<img src="./media/image20.png" style="width:6.5in;height:4.22708in"
alt="A screenshot of a computer Description automatically generated" />

7.  This will take you to the Power Apps Studio. Select **Skip** on the
    **Welcome to Power Apps Studio** dialog box. 

> <img src="./media/image21.png" style="width:6.5in;height:3.9875in"
> alt="A screenshot of a computer Description automatically generated" />

8.  Click on **App** on the **Tree view**. In the dialog that pops up
    on the right side of the screen, enter **Expense Report App** in the
    **App name** field. 

> <img src="./media/image22.png" style="width:6.5in;height:2.41806in"
> alt="A screenshot of a computer Description automatically generated" />

9.  Click on **DetailScreen** and from the drag down click on
    **DetailForm1**.

> <img src="./media/image23.png" style="width:6.5in;height:3.80625in"
> alt="A screenshot of a computer Description automatically generated" />

10. On the right-hand side of the screen, search for **Fields** and
    select the hyperlink in front of it.

<img src="./media/image24.png" style="width:6.5in;height:3.69514in"
alt="A screenshot of a computer Description automatically generated" />

>  

11. Go to **Add field**, then select the fields that you created in your
    **Expenses on business trip** table. Thereafter, click **Add**. 

<img src="./media/image25.png"
style="width:4.19203in;height:5.7505in" />

12. To remove the fields that are not required, select the ellipses by
    the side of the field and select **Remove**.

<img src="./media/image26.png" style="width:4.40038in;height:3.20861in"
alt="A screenshot of a computer Description automatically generated" />

13. You can rearrange the fields in the preferred order you want them to
    show on your app. Click on the ellipsis sign (**…**) by the side of
    the field and move it to the position you want it to be.

>  

<img src="./media/image27.png"
style="width:4.42538in;height:4.10036in" />

14. The fields should be arranged in the following order.

    - Name of employee

    - Email ID

    - Employee position

    - Trip destination

    - Number of days of travel

    - Date of application

    - Amount requested

<img src="./media/image28.png" style="width:3.26695in;height:3.97534in"
alt="A screenshot of a phone Description automatically generated" />

15. Next, on the **Tree view** select **EditScreen** section and then
    select **EditForm1**.

<img src="./media/image29.png" style="width:6.5in;height:3.86875in"
alt="A screenshot of a computer Description automatically generated" />

16. On the right side of the screen under the section **Fields**, click
    the **Edit fields**.

<img src="./media/image30.png" style="width:3.20861in;height:3.5003in"
alt="A screenshot of a computer Description automatically generated" />

17. Select **Add field**, then select the fields that you created in
    your **Expenses on business trip** table. Thereafter, click **Add**.
    Remove the fields that are not required.

18. Arrange the fields in the same format as in **DetailForm1**.

<img src="./media/image31.png" style="width:6.5in;height:3.95556in" />

### Task 4: Add a Home Screen 

1.  Click on **New screen** at the top left corner of the screen and
    select **Blank**.

<img src="./media/image32.png"
style="width:5.51756in;height:4.38632in" />

2.  Add an image for visual impact on the **Home** screen. Select
    the **Media** button on the menu to the left of the tree view, and
    then select **Add media \> Upload**.

<img src="./media/image33.png"
style="width:3.37529in;height:4.51706in" />

3.  Select the **HomeScreen.png** file and upload it into your app.

4.  Select the **HomeScreen.jpg** image from **Images** pane on the left
    side. The image will be seen on the **Home screen** of the app.

<img src="./media/image34.png" style="width:6.5in;height:3.66528in" />

5.  Now, you have the appropriate image on your **Home** screen.

6.  Drag the corners of the **Image** control to resize the app and then
    position it to occupy about two thirds of the screen. You might
    notice an extra space above and below the picture because the image
    is a different size than the screen.

<img src="./media/image35.png" style="width:6.5in;height:3.37292in"
alt="A screenshot of a map Description automatically generated" />

7.  To correct this issue, change the **Image position** value
    from **Fit** to **Fill** on the **Properties** pane.

<img src="./media/image36.png" style="width:3.18361in;height:2.62523in"
alt="A screenshot of a computer Description automatically generated" />

8.  Change the following properties of your **HomeScreen** image.

- **X**: 0

- **Y**: 142

- **Width**: 640

- **Height**: 800

<img src="./media/image37.png" style="width:6.5in;height:3.38542in" />

9.  Click in the empty space above the image and then select **Insert**.

10. Select **Text label** to add a new label to your screen.

<img src="./media/image38.png"
style="width:2.58356in;height:3.35029in" />

11. Change the following properties of your **Text label** control by
    using the **Properties** pane or the **Advanced** pane. Some
    properties are also available in the command bar.

- **Text**: Expense Report App

- **Size**: 30

- **Font Weight**: Bold

- **Text Alignment**: Center

- **X**: 0

- **Y**: 0

- **Width**: 640

- **Height**: 142

<img src="./media/image39.png" style="width:3.18361in;height:5.96718in"
alt="A screenshot of a computer Description automatically generated" />

12. Now let's add a button to the **Home** screen that would take us to
    the next page whenever clicked. At the top of the screen select
    **Insert \>** **Button**.

<img src="./media/image40.png"
style="width:2.53355in;height:3.95868in" />

13. Change the following properties of your **Button** control by using
    the **Properties** pane or the **Advanced** pane. Some properties
    are also available in the command bar.

- **Text**: Register request

- **Size**: 24

- **Font Weight**: Semibold

- **Text Alignment**: Center

- **X**: 160

- **Y**: 999

- **Width**: 320

- **Height**: 70

<img src="./media/image41.png" style="width:6.5in;height:4.17569in"
alt="A screenshot of a computer Description automatically generated" />

14. Change the dropdown menu on the upper ribbon to **OnSelect**. This
    property sets the action of the button when a user selects it and is
    automatically set to false or do nothing.

15. Set the **OnSelect** property to ***Navigate(BrowseScreen)**.*
    **BrowseScreen** is the name of the next screen.

<img src="./media/image42.png" style="width:6.5in;height:4.07153in"
alt="A screenshot of a computer Description automatically generated" />

16. Select the **Tree** view, select your **Home** screen. Select the
    ellipses by the side of the **Home** Screen and rename it to
    **Scr_Welcome**.

<img src="./media/image43.png" style="width:4.80875in;height:5.81717in"
alt="A screenshot of a computer Description automatically generated" />

17. Select the **Scr_Welcome** screen and then select **Move up**. Move
    the **Scr_Welcome** screen to the top.

<img src="./media/image44.png"
style="width:4.27537in;height:5.8005in" />

### Task 5: Modify the Browse Screen

1.  Select the **BrowseScreen**. Select **Insert** and select
    **Button**.

<img src="./media/image45.png" style="width:5.10044in;height:4.70874in"
alt="A screenshot of a computer Description automatically generated" />

2.  Change the following properties of the **Button** by using
    the **Properties** pane or the **Advanced** pane. Some properties
    are also available in the command bar.

- **Text**: Back to Home

- **Font Size**: 24

- **Font Weight**: Semibold

- **Text Alignment**: Center

- **X**: 180

- **Y**: 1022

- **Width**: 280

- **Height**: 70

<img src="./media/image46.png" style="width:6.5in;height:4.1875in"
alt="A screenshot of a computer Description automatically generated" />

3.  Change the **OnSelect** property for the button to
    ***Navigate(Scr_Welcome)**.*

<img src="./media/image47.png" style="width:6.5in;height:4.25347in"
alt="A screenshot of a computer Description automatically generated" />

4.  Select the **Save** icon on the top-right corner to save your app.

<img src="./media/image48.png" style="width:6.5in;height:4.24306in" />

### Conclusion

After completing this exercise, you will have:

1.  A table dedicated to expenses related to business trips within
    Dataverse.

2.  An **Expense Report App** developed utilizing Microsoft Dataverse.

3.  A **Home Screen** designed for your application.

4.  An enhanced **Browse Screen**.

This guarantees that you will have a fully functional **Expense Report
App**, complete with all essential screens.

## Exercise 2: Create an Expense Approval Request flow 

In this exercise, you will create an Expense Approval Request flow and
integrate it with the Expense Report App.

1.  On the **Tree view**, select **BrowseScreen** and then select
    **IconNewItem1**.

<img src="./media/image49.png" style="width:6.5in;height:3.84097in"
alt="A screenshot of a computer Description automatically generated" />

2.  While keeping the **IconNewItem1** selected, click the **Power
    Automate flow** icon from the left bar.

<img src="./media/image50.png" style="width:3.26695in;height:4.83375in"
alt="A screenshot of a computer Description automatically generated" />

3.  Select **Create new flow**.

<img src="./media/image51.png" style="width:3.38363in;height:3.44197in"
alt="A screenshot of a computer Description automatically generated" />

4.  On **Create your flow** window, select **Create from blank**.

<img src="./media/image52.png" style="width:6.5in;height:3.91181in" />

5.  On **Create your flow** window, select the **New step** tab.

<img src="./media/image53.png" style="width:6.5in;height:1.56042in"
alt="A screenshot of a computer Description automatically generated" />

6.  On **Choose an operation**, search for and select **When row is
    added, modified or deleted**.

<img src="./media/image54.png" style="width:6.5in;height:5.725in"
alt="A screenshot of a computer Description automatically generated" />

7.  Add the following information and then select **Next step**.

    - **Change type** – Added or modified

    - **Table name** – Expenses on business trip

    - **Scope** – Organization

<img src="./media/image55.png" style="width:6.5in;height:4.92083in"
alt="A screenshot of a computer Description automatically generated" />

8.  On **Choose an operation**, search for and select **Start and wait
    for an approval**.

<img src="./media/image56.png" style="width:6.5in;height:5.72569in"
alt="A screenshot of a computer Description automatically generated" />

9.  On **Send and wait for an approval** enter the following
    information.

    - **Approval type** – Approve/Reject – First to respond

    - **Title** – Approve the expense approval request

    - **Assigned to** – Enter your **Tenant Admin credentials**

    - **Details** – From **Dynamic content**, select **Name of
      > employee**, **Employee position**, **Trip destination** and
      > **Number of days of travel**

<img src="./media/image57.png"
style="width:6.39222in;height:4.39205in" />

10. Add **New step**.

11. Select **Condition**.

<img src="./media/image58.png" style="width:6.34222in;height:4.80042in"
alt="A screenshot of a computer Description automatically generated" />

12. Enter the following condition:

‘**Outcome is equal to Approve’**. Add **Outcome** from **Dynamic
content**.

<img src="./media/image59.png" style="width:6.43389in;height:1.84183in"
alt="A screenshot of a computer Description automatically generated" />

13. In the **If yes** branch, Select **Add an action**.

<img src="./media/image60.png"
style="width:6.39222in;height:1.94184in" />

14. Search for and select **Send an email (V2)**.

<img src="./media/image61.png" style="width:6.5in;height:5.46458in" />

15. In the Send an email (V2) step, enter the following information.

- **To** – Add **Email-ID** from Dynamic content

- **Subject** - Expense request approved

- **Body** - Your expense request is approved.

<img src="./media/image62.png" style="width:6.5in;height:4.86875in"
alt="A screenshot of a computer Description automatically generated" />

16. In the **If no** branch, Select **Add an action**.

<img src="./media/image63.png" style="width:6.38389in;height:1.9585in"
alt="A red box with blue text and a red rectangle Description automatically generated" />

17. Search for and select **Send an email (V2)**.

<img src="./media/image64.png" style="width:6.5in;height:5.48542in"
alt="A screenshot of a computer Description automatically generated" />

18. In the Send an email (V2) step, enter the following information.

- **To** – Add **Email-ID** from Dynamic content

- **Subject** - Expense request rejected

- **Body** - Your expense request is rejected. Please check the comments
  > by the Accounting Officer. Add **Responses Comments** from **Dynamic
  > content**.

- As soon as you add **Responses Comments** from **Dynamic content**,
  > the **Responses** field is added above **Send an email (V2)**.

<img src="./media/image65.png" style="width:6.5in;height:5.12639in"
alt="A screenshot of a computer Description automatically generated" />

19. Enter the name of your flow as **Expense approval request flow**.

20. Select **Save**.

<img src="./media/image66.png" style="width:6.5in;height:3.04306in"
alt="A screenshot of a computer Description automatically generated" />

21. Once the flow is saved, you will be navigated back to **Power Apps
    Studio**. The flow is added to the app.

22. **Save** your app.

<img src="./media/image67.png" style="width:6.5in;height:1.72917in"
alt="A screenshot of a computer Description automatically generated" />

23. Make sure that the **IconNewItem1** is selected.

24. Change the **OnSelect** property of **IconNewItem1** to
    *NewForm(EditForm1);Navigate(EditScreen,
    ScreenTransition.None);Expenseapprovalrequestflow.Run()*

<img src="./media/image68.png" style="width:6.5in;height:1.74236in"
alt="A screenshot of a computer Description automatically generated" />

25. **Save** the app.

### Conclusion

After completing this exercise, you will have:

1.  An **Expense approval request flow** created in Power Automate.

2.  The **IconNewItem1** button integrated with the **Expense approval
    request flow**.

This ensures that the **Expense approval request flow** is seamlessly
integrated with the **Expense Report App** and will be triggered by the
**IconNewItem1** button.

## Exercise 3: Test the app

In this exercise, you will test the app by submitting an expense
approval request. When the flow runs, you will review the request as an
Accounting Officer and then either approve or reject the request, check
the respective notifications and finally verify different stages of the
workflow.

### Task 1: Submit an Expense Approval request

1.  Open a new tab on your browser and enter the URL
    <https://outlook.office365.com/> to browse **Microsoft Outlook**.

2.  Sign in with your **Tenant Admin credentials**.

<img src="./media/image69.png" style="width:6.5in;height:2.62917in"
alt="A computer screen with a message Description automatically generated" />

3.  Navigate back to the **Power Apps** tab. To test your app, select
    **Tree view** and then select the **Scr_Welcome** screen.

4.  Select the **Play** icon on the top-right corner.

<img src="./media/image70.png" style="width:6.5in;height:4.21806in"
alt="A screenshot of a computer Description automatically generated" />

5.  Select **Register request** button on the **Home screen**.

<img src="./media/image71.png"
style="width:4.15036in;height:6.05886in" />

6.  You will be navigated to **BrowseScreen**. Select the **+** sign.

7.  On the **EditScreen**, enter the following information.

    - **Name of employee** – Mark Brown

    - **Email ID** – Enter your active Email ID

    - **Employee position** – Project Operations Manager

    - **Trip destination** - Seattle

    - **Number of days of travel** -3

    - **Date of application** – Select the date of application

    - **Amount requested** - 30000

<img src="./media/image72.png" style="width:3.97534in;height:6.10053in"
alt="A screenshot of a computer Description automatically generated" />

8.  Select the **Check mark** on the top-right corner.

<img src="./media/image73.png" style="width:3.97534in;height:6.10053in"
alt="A screenshot of a computer Description automatically generated" />

9.  Once the expense approval request is saved, you will be navigated to
    **BrowseScreen**. You can see the request enlisted on the
    **BrowseScreen**.

10. Select your recent request.

<img src="./media/image74.png" style="width:3.94201in;height:6.02552in"
alt="A screenshot of a computer Description automatically generated" />

11. You will be navigated to the **DetailScreen** to check the details
    of your request.

<img src="./media/image75.png" style="width:3.93367in;height:6.00885in"
alt="A screenshot of a computer Description automatically generated" />

12. You can **Edit** or **Delete** your request from the
    **DetailScreen**.

<img src="./media/image76.png" style="width:3.93367in;height:6.00885in"
alt="A screenshot of a computer Description automatically generated" />

### Task 2: Approve the Expense approval request

1.  Once you submit the **Expense approval request**, you will receive
    an email on your **Tenant Admin Outlook account**.

2.  The email contains all the details of the requestor.

3.  Check the details and select **Approve**.

<img src="./media/image77.png" style="width:6.5in;height:3.67153in" />

4.  **Add comments** and then select **Submit**.

<img src="./media/image78.png" style="width:6.5in;height:3.27569in" />

5.  As soon as you click the **Submit** button, the requestor will get
    email notification.

6.  To check the email notification received by the requestor, go to an
    InPrivate or Incognito window. On the new tab enter the URL
    <https://outlook.office365.com/> to browse **Microsoft Outlook**.

7.  Sign in with the **Requestor credentials**. For this scenario, sign
    in with the credentials that are used for Mark Brown.

8.  Once logged in, you can view the email notification that your
    **Expense approval request is approved**.

<img src="./media/image79.png" style="width:6.5in;height:1.96111in"
alt="A white rectangular object with a black border Description automatically generated" />

### Task 3: View different stages of Expense approval request flow

1.  Navigate to the **Expense Report App**. Close it.

<img src="./media/image80.png" style="width:6.5in;height:4.42431in"
alt="A screenshot of a computer Description automatically generated" />

2.  Select the matrix on the upper ribbon of Power Apps.

<img src="./media/image81.png" style="width:5.05044in;height:5.97552in"
alt="A screenshot of a computer Description automatically generated" />

3.  Select **Power Automate**.

<img src="./media/image82.png" style="width:3.12527in;height:4.6504in"
alt="A screenshot of a computer Description automatically generated" />

4.  You will be navigated to **Power Automate** Tab. Make sure that you
    are in the **Dev One** environment.

<img src="./media/image83.png" style="width:6.5in;height:2.20764in" />

5.  Select **My flows** and then select **Expense approval request
    flow**.

<img src="./media/image84.png" style="width:6.5in;height:3.29444in"
alt="A screenshot of a computer Description automatically generated" />

6.  On the **Expense approval request flow** page, view the runs.

7.  Select the status of the Expense approval request by Mark Brown. The
    status is ‘**Succeeded**’.

<img src="./media/image85.png" style="width:6.5in;height:5.19444in"
alt="A screenshot of a computer Description automatically generated" />

8.  Open that run and see how the app automatically moves through the
    different approval stages.

<img src="./media/image86.png" style="width:5.7505in;height:6.38389in"
alt="A screenshot of a computer Description automatically generated" />

### Task 4: Reject the Expense approval request

1.  Submit the Expense approval request using the steps in **Task 7:
    Test the app**.

2.  Once you submit the **Expense approval request**, you will receive
    an email on your **Tenant Admin Outlook account**.

3.  Check the details and select **Reject**.

<img src="./media/image87.png" style="width:6.5in;height:3.77847in" />

4.  Write in the comments box – ‘**Please check the maximum expenses
    limit that can be approved for this employee position.**’ Select
    **Submit**.

<img src="./media/image88.png" style="width:6.5in;height:4.74792in"
alt="A screenshot of a computer Description automatically generated" />

5.  To check the email notification received by the requestor, go to an
    InPrivate or Incognito window. On the new tab enter the URL
    <https://outlook.office365.com/> to browse **Microsoft Outlook**.

6.  Sign in with the **Requestor credentials**. For this scenario, sign
    in with the credentials that are used for Mark Brown.

7.  Once logged in, you can view the email notification that your
    **Expense approval request is rejected**. View the comments.

> <img src="./media/image89.png" style="width:6.5in;height:1.86389in"
> alt="A screenshot of a computer Description automatically generated" />

### Conclusion

After completing this exercise, you will have:

1.  An **Expense Report App** that has undergone successful testing for
    both outcomes: the approval of an Expense Approval request and its
    rejection.

2.  An examination of the various phases involved in the Expense
    approval request process following submission.

This guarantees that you have a comprehensively tested and validated
**Expense Report App**, facilitating the efficient management of
employee expense approvals.
