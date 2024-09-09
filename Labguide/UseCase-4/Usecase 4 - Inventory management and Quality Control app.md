# Level-up CSP Technical Training – Power Platform

# Facilitator Guide 

**Use case –Automate Inventory management and Quality control app using
Power Platform**

| Description      | A hands-on experience to inspire users to use Microsoft Power Platform tools to design and implement digital systems to meet business objectives.                                                                                                   |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prerequisites    | To get the most out of this training we recommend you have admin access with Power Apps for Developer and Power Automate.                                                                                                                           |
| Audience         | Microsoft partners will deliver this workshop to CSP customers, who have multiple employees in their company, have a Microsoft Power Apps for Developer and Microsoft Power Automate license, and have minimal Microsoft Power Platform experience. |
| Duration         | 60 minutes                                                                                                                                                                                                                                          |
| Publication date | September 2024                                                                                                                                                                                                                                      |

This document is provided “as-is”. Information and views expressed in
this document, including URL and other Internet Web site references, may
change without notice. You bear the risk of using it.

This document does not provide you with any legal rights to any
intellectual property in any Microsoft product. You may copy and use
this document for your internal reference purposes.

© 2024 Microsoft. All rights reserved.

# Contents

[Level-up CSP Technical Training – Power Platform
[1](#level-up-csp-technical-training-power-platform)](#level-up-csp-technical-training-power-platform)

[Facilitator Guide [1](#facilitator-guide)](#facilitator-guide)

[Objective and scenario
[4](#objective-and-scenario)](#objective-and-scenario)

[Objective [4](#objective)](#objective)

[Solution focus area [4](#solution-focus-area)](#solution-focus-area)

[Personas and scenario
[4](#personas-and-scenario)](#personas-and-scenario)

[Pre-requisites [5](#pre-requisites)](#pre-requisites)

[Lab instructions [6](#lab-instructions)](#lab-instructions)

[Automating Inventory Management and Quality Control App
[6](#automating-inventory-management-and-quality-control-app)](#automating-inventory-management-and-quality-control-app)

[**Exercise 1: Create Inventory management app**
[6](#_Toc176777011)](#_Toc176777011)

[**Task 1 : Create inventory management app using Copilot.**
[6](#_Toc176777012)](#_Toc176777012)

[**Task 2 : Create candy quality Screen**
[10](#_Toc176777013)](#_Toc176777013)

[**Task 3 : Notify the supplier when item is marked defective.**
[27](#_Toc176777014)](#_Toc176777014)

[**Task 4 : Generate an defective email to the supplier.**
[37](#_Toc176777015)](#_Toc176777015)

[Conclusion [39](#conclusion)](#conclusion)

[**Exercise 2: Create a flow to restock the inventory**
[39](#_Toc176777017)](#_Toc176777017)

[**Task 1 : Create a Power platform flow to trigger restock email**
[39](#_Toc176777018)](#_Toc176777018)

[**Task 2 : Test the restock flow**
[56](#_Toc176777019)](#_Toc176777019)

[Conclusion [62](#conclusion-1)](#conclusion-1)

# Objective and scenario

## Objective

Build an app using Power Apps and Copilot to digitalize Inventory
Management and automatically restock products when inventory gets below
a threshold. The app should notify the suppliers or production teams
whenever an item is marked as defective.

## Solution focus area

Contoso Corp prides itself on providing customers with the highest
quality products. To provide a seamless experience for the customers,
Contoso needs a constant supply of inventory. To streamline the
restocking process of the products, Contoso Corp aims to develop a
customized application to automatically restock products when the
inventory gets below a specified threshold. Additionally, to maintain
product quality, Contoso needs to add a feature that notifies the
suppliers or production teams whenever an item is marked as defective.

Contoso Corp needs a new solution that can:

- Create an app to raise a approval request hen the inventory gets below
  a specified threshold.

- Automatically restock inventory products once the request is approved

- Raise a notification to the supplier when the item is marked as
  defective.

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
  automate the approval workflow for restocking inventory of products ,
  which he then submits to Jane Miller for testing.

- After thorough testing and validation, Mark Brown officially hands
  over the app to the team, enabling them to Inventory management app
  efficiently.

# Pre-requisites

For this use case, all participants will need the following:

- Microsoft Power Apps for Developer license

- Microsoft Power Automate License

- Windows 10/11 Enterprise E3 Trial license

- Office 365 E5 Trial license

- Their own devices with Wi-Fi connection.

# Lab instructions

# Automating Inventory Management and Quality Control App

<span id="_Toc176777011" class="anchor"></span>**Exercise 1: Create
Inventory management app**

In this exercise, you will create a Inventory management app with the
help of Copilot .Add re-order point column in Dataverse table and create
Quality screen and Power automate flow raise a notification to the
supplier when item is marked as defective.

<span id="_Toc176777012" class="anchor"></span>**Task 1 : Create
inventory management app using Copilot.**

1.  Open a browser and go to https:\\\apps.powerapps.com and sign in
    with your Office 365 admin account.

2.  Click on the environment on right top corner and select **Dev one**
    environment

<img src="./media/image1.png" style="width:6.5in;height:2.5in" />

3.  Enter the below prompt and click on **Enter** button.

build a candy inventory management app

<img src="./media/image2.png" style="width:6.5in;height:3.03889in" />

4.  Copilot generates an app with table as shown in below image.

<img src="./media/image3.png" style="width:6.5in;height:3.90069in"
alt="A screenshot of a computer Description automatically generated" />

5.  Ener below prompt and click on Enter.This column is required to
    notify when the quantity went below the reorder point.

> Add reorder point column and image column
>
> <img src="./media/image4.png"
> style="width:6.49444in;height:4.03889in" />

6.  The table has been updated with reorder point and image columns.

<img src="./media/image5.png" style="width:6.5in;height:4.0875in"
alt="A screenshot of a computer Description automatically generated" />

7.  Click on the **Create app** button and wait for the app to create.

<img src="./media/image6.png" style="width:6.4875in;height:4.05764in" />

8.  The app gets created and should look like below image.

<img src="./media/image7.png" style="width:6.5in;height:3.00486in" />

9.  Click on the save button to save the app.

<img src="./media/image8.png" style="width:6.5in;height:2.43056in"
alt="A screenshot of a computer Description automatically generated" />

10. Open the app in a new tab. Click on Tables form left navigation .
    Select Candy inventory table.Add candyInStock column as Number type
    and enter some values .If Quantity is less than reorder points then
    Quantity column will automate add with candyInStock .

> <img src="./media/image9.png" style="width:6.5in;height:2.95208in"
> alt="A screenshot of a computer Description automatically generated" />

<span id="_Toc176777013" class="anchor"></span>**Task 2 : Create candy
quality Screen**

1.  Switch back to Power apps tab and click on **New Screen** and select
    **Blank** template.

> <img src="./media/image10.png"
> style="width:6.49375in;height:4.39097in" />

<img src="./media/image11.png" style="width:6.5in;height:3.25in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image12.png" style="width:6.49375in;height:3.26944in"
alt="A screenshot of a computer Description automatically generated" />

1.  Click on Edit button next to new table and enter below values and
    then click on **Save** button.

> Display Name : candy quality
>
> Description : candy quality check

<img src="./media/image13.png"
style="width:6.49375in;height:5.08333in" />

2.  Click on **New column** and select Edit column.

<img src="./media/image14.png"
style="width:6.30764in;height:3.94236in" />

3.  Enter the Display name as **Candy ID** and then click on Update
    button.

<img src="./media/image15.png" style="width:6.5in;height:4.94236in" />

4.  Click on New column and enter below details

<img src="./media/image16.png" style="width:6.5in;height:6.17292in" />

5.  Click on New Column and add a column with below details.

> <img src="./media/image17.png"
> style="width:6.49375in;height:6.37153in" />

6.  Add new column with below details.

<img src="./media/image18.png" style="width:6.5in;height:6.67917in" />

7.  Click on **Save and Close** button to create table.

<img src="./media/image19.png"
style="width:6.49375in;height:3.08333in" />

8.  You will navigate back to Power apps app page. Select the newly
    added screen and click on Insert and select **Edit form** as shown
    in below image.

<img src="./media/image20.png" style="width:6.5in;height:5.61528in" />

9.  click the container and select the data source table created above.

<img src="./media/image21.png"
style="width:6.49375in;height:3.68611in" />

10. Select the Form. Click on Insert and select **Button**.

<img src="./media/image22.png"
style="width:6.49375in;height:5.53194in" />

11. Drag the submit button and plays it in the middle of the container .
    Select the button and change the **properties** text to **Submit**
    as shown in below image.

<img src="./media/image23.png"
style="width:6.49375in;height:3.17917in" />

12. Select the Submit button and select OnSelect function and enter
    below function.

Note : Form1 in the formula should be replaced with your form name

SubmitForm(*Form1*);NewForm(*Form1*)    

<img src="./media/image24.png" style="width:6.5in;height:3.4875in" />

13. Select the container, under properties, select Default mode to
    **New**.

<img src="./media/image25.png"
style="width:6.49375in;height:3.64097in" />

14. Click on **Save** and then click on **Preview app** button as shown
    in below image.

<img src="./media/image26.png"
style="width:6.49375in;height:2.97431in" />

<img src="./media/image27.png" style="width:6.5in;height:3.39792in"
alt="A screenshot of a computer Description automatically generated" />

15. Enter Candy details and then click on Submit button.

> <img src="./media/image28.png" style="width:6.5in;height:3.13889in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image29.png" style="width:6.5in;height:3.33333in"
> alt="A screenshot of a computer Description automatically generated" />

16. Switch back to your Candy quality table in Dataverse environment and
    you should see the record added above.

> <img src="./media/image30.png" style="width:6.5in;height:2.80208in"
> alt="A screenshot of a computer Description automatically generated" />

17. Close the preview window.

<span id="_Toc176777014" class="anchor"></span>**Task 3 : Notify the
supplier when item is marked defective.**

1.  Open a new tab in a browser and go to https:\\\flow.microsoft.com
    and sign in with your Office 365 admin account.

2.  Select the **Dev One** environment. Click on **My flows** from left
    navigation menu. Click on **New flow -\> Automated cloud flow.**

> <img src="./media/image31.png" style="width:6.5in;height:2.06389in" />

3.  Enter the Flow Name : **Notificationsupplier**. Search for **when
    item added** and select **When a row is added ,modified or deleted**
    and then click on **Create**.

<img src="./media/image32.png"
style="width:6.49375in;height:4.15417in" />4. Select the action and map
below parameters.

Change Type : Added or Modified

Table name : candy quality

Scope : Organization

Advanced parameters : Select columns.

<img src="./media/image33.png"
style="width:6.49375in;height:4.78819in" />

<img src="./media/image34.png" style="width:6.5in;height:4.25625in" />

6\. Click on + and select **Add an action**.

<img src="./media/image35.png"
style="width:4.65417in;height:3.18611in" />

7\. Search for Condition and select Condition control as shown in below
image.

<img src="./media/image36.png" style="width:6.5in;height:3.45486in" />

8\. Click on chose a value and select choose a Enter the data from
previous step.

<img src="./media/image37.png"
style="width:6.49375in;height:2.41042in" />

11. Select **Quality** column.

<img src="./media/image38.png"
style="width:6.49375in;height:4.4875in" />

12. Select is equal to and enter the value as Defective

> <img src="./media/image39.png" style="width:6.5in;height:2.60903in" />

13. Under True condition, click **Add an action**.

<img src="./media/image40.png"
style="width:6.49375in;height:4.81389in" />

14. Select **Approvals** action.

<img src="./media/image41.png" style="width:6.5in;height:3.83333in" />

15. Select **Start and wait for an approval**.

<img src="./media/image42.png" style="width:6.5in;height:3.40417in" />

16. Select **Approval Type** as **Approve/Reject – First to Respond**.

> <img src="./media/image43.png"
> style="width:6.49375in;height:5.2625in" />

17. Enter below values and then collapse the window.

Title : Approve defective product

Assigned to : Your Office 365 admin account itd

Descirption:

Hi  
  
Product - is defective. Please approve to replace it.  
  
Thanks

<img src="./media/image44.png" style="width:6.5in;height:6.03194in" />

12\. Save the flow.

<img src="./media/image45.png"
style="width:6.49375in;height:4.12153in" />

<span id="_Toc176777015" class="anchor"></span>**Task 4 : Generate an
defective email to the supplier.**

1.  Switch back to your Power apps tab and preview the app.

> <img src="./media/image46.png" style="width:6.5in;height:3.38403in"
> alt="A screenshot of a computer Description automatically generated" />

2.  Enter product details and select **Quality** as **Defective** and
    then click on **Submit** button.

> <img src="./media/image47.png"
> style="width:6.49375in;height:3.07083in" />

3.  Switch back to your Power Automate flow tab and click on Flows.Your
    flow should have succeeded.

> <img src="./media/image48.png"
> style="width:6.49375in;height:3.4875in" />

4.  Open a new tab in browser and go to https:\\\outlook.com and sign in
    with your Office 365 admin account.

5.  You should see an email to approve replacement for defective
    product.

> <img src="./media/image49.png" style="width:6.5in;height:2.83681in"
> alt="A screenshot of a computer Description automatically generated" />

### Conclusion

After completing this exercise, you will have:

1.  An inventory App with inventory dashboard with a inventory table in
    Dataverse

2.  Product quality check screen

3.  Power Automate cloud flow to notify supplier for item quality check

This guarantees that you will have a fully functional **Inventory
management App**, complete with all essential screens.

<span id="_Toc176777017" class="anchor"></span>**Exercise 2: Create a
flow to restock the inventory**

In this exercise, you will create and test a approval request ot restock
the inventory flow and integrate it with the Inventory management App.

<span id="_Toc176777018" class="anchor"></span>**Task 1 : Create a Power
platform flow to trigger restock email**

1.  Switch back to Power automate tab and click on **My flows** -\>
    **New flow -\> Automated cloud flow.**

> <img src="./media/image50.png"
> style="width:6.49375in;height:3.39722in" />

2.  Enter the flow name as : **Candy Restock Flow** . Search for **When
    a row** is and select Dataverse’s **When a row is added or
    modified** action and then click on **Create**.

> <img src="./media/image51.png"
> style="width:6.49375in;height:4.16042in" />

3.  Select the action and set below parameters

> Change Type ; Added or Modified
>
> Table Name: Candy Inventory
>
> Scope : Organization

<img src="./media/image52.png"
style="width:6.49375in;height:4.03194in" />

4.  Add a action after when a row is added, modified or deleted.

<img src="./media/image53.png"
style="width:6.08333in;height:4.32708in" />

5.  Search for Condition and select Control’s Condition action.

> <img src="./media/image54.png" style="width:6.49375in;height:3.75in" />

6.  Click on Chose value and select choose form previous step dynamic
    action.

> <img src="./media/image55.png"
> style="width:6.49375in;height:3.85903in" />

7.  Search for Quantity column and select it.

> <img src="./media/image56.png"
> style="width:6.49375in;height:3.85903in" />

8.  Select a condition **is less than** and click on Enter data from
    previous actin

> <img src="./media/image57.png"
> style="width:6.49375in;height:3.80139in" />

9.  Search for Reorder points column and select it.

<img src="./media/image58.png"
style="width:6.49375in;height:3.87153in" />

10. Add an action under True condition.

<img src="./media/image59.png"
style="width:6.44861in;height:4.80764in" />

11. Select **Approvals** action

> <img src="./media/image60.png"
> style="width:6.49375in;height:3.21806in" />

12. Select **Start and wait for an Approvals.**

<img src="./media/image61.png"
style="width:6.49375in;height:3.58333in" />

13. Select Approval Type as : **Approve/Reject – First to Respond**.
    Enter Title as : **Approve to Restock –** and click on Dynamic
    button to select the data from previous step.

<img src="./media/image62.png"
style="width:6.49375in;height:4.14097in" />

14. Search for **Name** and select it.

<img src="./media/image63.png"
style="width:6.49375in;height:3.78194in" />

15. Enter below details

> Assigned to : Your Office 365 admin/ your personal email address.
>
> Details:
>
> Hi Sir,  
>   
> is out of stock - for customers to place an order. Please approve to
> restock.  
>   
> Thanks
>
> Note : You can customize details section as per your requirements.
>
> <img src="./media/image64.png"
> style="width:6.49375in;height:3.36528in" />

16. Add an action after approval action.

<img src="./media/image65.png"
style="width:6.49375in;height:5.00625in" />

17. Search for condition and select Control – Condition.

<img src="./media/image66.png"
style="width:6.49375in;height:3.35903in" />

18. Click on Choose value and select **Outcome** from Start and wait for
    an Approval action.

<img src="./media/image67.png"
style="width:6.49375in;height:5.08333in" />

19. Select the condition as **is equal to** and enter the value as
    **Approve**.

<img src="./media/image68.png" style="width:6.375in;height:4.225in" />

20. Under True condition, add an action.

<img src="./media/image69.png"
style="width:6.49375in;height:4.70486in" />

21. Search for **Update Row** and select it from **Microsoft Dataverse**
    section.

<img src="./media/image70.png"
style="width:6.49375in;height:4.44236in" />

22. Select your Candy inventory table and Click on Row Id select Dynamic
    action.

> <img src="./media/image71.png" style="width:6.5in;height:3.30139in" />

23. Search for unique identifier column form your table and select it.

> <img src="./media/image72.png"
> style="width:6.49375in;height:3.94236in" />

24. Click on Advanced Parameters drop down and select Quantity column.

<img src="./media/image73.png" style="width:6.5in;height:4.81389in" />

25. Enter the below function ( you type in your app ) and collapse the
    action.

> add(triggerBody()?\['cr5e0_quantity'\],triggerBody()?\['cr5e0_candyinstock'\])

<img src="./media/image74.png"
style="width:6.49375in;height:3.79792in" />

26. Click on **Save** button to save the Power automate flow.

<img src="./media/image75.png"
style="width:6.49375in;height:2.85903in" />

<span id="_Toc176777019" class="anchor"></span>**Task 2 : Test the
restock flow**

27. Switch back to **PowerApps** tab and click on Candy Inventories
    screen from left Tree view and select **play**.

<img src="./media/image76.png"
style="width:6.4875in;height:2.80764in" />

28. Select the Candy and click on **Edit**.

> <img src="./media/image77.png" style="width:6.5in;height:2.51528in" />

29. Enter the Quantity value less than reorder points and commit
    changes.

> <img src="./media/image78.png" style="width:6.5in;height:2.62639in" />

30. Switch back to Power Automate flow tab and click on My flows -\>
    Your flow .

<img src="./media/image79.png" style="width:6.5in;height:3.63611in" />

31. Flow is running and is at condition.

<img src="./media/image80.png" style="width:6.5in;height:3.67708in" />

32. Open a new tab and go to https:\\\outlook.com and sign in with your
    Office 365 admin account. You should have got an email to restock .
    **Approve** and **Submit**.

> <img src="./media/image81.png"
> style="width:6.49167in;height:3.18333in" />
>
> <img src="./media/image82.png" style="width:6.5in;height:4.23333in" />

33. The flow is successful now.

> <img src="./media/image83.png" style="width:6.5in;height:4in" />

34. Switch back to PowerApps and check the above product quantity it
    should have been updated with 100.

<img src="./media/image84.png" style="width:6.5in;height:3.90347in" />

### Conclusion

After completing this exercise, you will have:

1.  Power Automate flow to raise an Approval ticket when the quality is
    below threshold

2.  Power Automate flow to update quantity automatically when approver
    approve to restock the inventory.

This guarantees that you will have a fully functional **Inventory
management App**, complete with all essential screens.
