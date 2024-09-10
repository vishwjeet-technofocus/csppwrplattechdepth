# Level-up CSP Technical Training – Power Platform

# Automate Employee Onboarding using Power Platform

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

# Objective and Scenario

## Objective

Develop an app to onboard employees automatically.

## Solution focus area

Contoso Corp is a mid-sized technology company specializing in software
development and IT consulting. The company values innovation,
collaboration, and employee development. To streamline the onboarding
process for new hires, Contoso Corp has decided to develop an automated
process which will welcome the new hires, get their documents submitted
and schedule their orientation.

By implementing this automated onboarding process, Contoso Corp aims to
create a seamless transition for new employees, allowing them to focus
on their roles and contribute to the mission of driving innovation in
the technology sector. Contoso believes that a well-structured
onboarding experience not only enhances employee satisfaction but also
boosts overall productivity and engagement.

Contoso Corp needs a new solution that can:

- To create a seamless onboarding process,

- Design a comprehensive program that ensures new hires feel welcomed,
  informed, and equipped to succeed in their roles.

*B*ased on the above requirements, you have decided to leverage
Microsoft Power Platform tools, including Power Apps and Power Automate
to enhance the onboarding experience at Contoso Corp.

## Personas and Scenario 

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
  automate the approval workflow for Employee Onboarding app, which he
  then submits to Jane Miller for testing.

- After thorough testing and validation, Mark Brown officially hands
  over the app to the team, enabling them to Onboard new employee
  efficiently.

# Pre-requisites

For this use case, all participants will need the following:

- Microsoft Power Apps for Developer license

- Microsoft Power Automate License

- Microsoft 365 Business Premium/E3/E5

- Their own devices with Wi-Fi connection.

# Lab instructions

<span id="_Toc176777246" class="anchor"></span>**Exercise 1: Create
Employees, HR and Manager list in Share point**

In this exercise, you will create a Lists in SharePoint and which will
have employee information.

<span id="_Toc176777247" class="anchor"></span>**Task 1 : Create a site
in Share point**

1.  Navigate to https:\\\office.com and sign in with your office 365
    tenants

2.  Click om 9 dots and select **Sharepoint** from list of **apps**.

> <img src="./media/image1.png" style="width:3.16374in;height:4.14816in"
> alt="Graphical user interface, application Description automatically generated" />

3.  Click on **+Create site** on top menu

> <img src="./media/image2.png"
> style="width:3.83333in;height:4.30833in" />

4.  Select **Communication site** tile in **Create a site** window.

> <img src="./media/image3.png"
> style="width:6.49167in;height:3.91667in" />

5.  Scroll down and select Blank template.

<img src="./media/image4.png"
style="width:6.49167in;height:4.01667in" />

6.  Click on **Use template**.

<img src="./media/image5.png" style="width:6.5in;height:4.05in" />

7.  Enter Site name and description then click on **Next** button.

> Site Name : **Contoso Corp**
>
> Site Description : **Onboarding new employee**
>
> <img src="./media/image6.png" style="width:6.5in;height:3.95833in" />

8.  Keep the default anguage and then click on **Create Site.**

<img src="./media/image7.png"
style="width:6.49167in;height:3.81667in" />

<img src="./media/image8.png" style="width:6.5in;height:2.27778in"
alt="A screenshot of a computer Description automatically generated" />

<span id="_Toc176777248" class="anchor"></span>**Task 2 : Create a
Employees list in SharePoint site from CSV file**

1.  Click on **Home- \>New -\> List**

<img src="./media/image9.png" style="width:6.5in;height:3.71667in" />

2.  Select **From CSV** tile from **Create a list** window**.**

<img src="./media/image10.png"
style="width:6.49167in;height:4.84167in" />

3.  Click on **Upload file** and browse to **C:\Labfiles** and select
    **Employee.csv** file

<img src="./media/image11.png"
style="width:5.18333in;height:5.49167in" />

4.  Change **Work Email** column type to **single line of text** and
    then click on **Next**.

<img src="./media/image12.png" style="width:6.5in;height:3.575in" />

5.  Enter then Name as : **Employee Onboarding** and Description : **New
    Contoso Corp employee** and then click on **Create**.

<img src="./media/image13.png"
style="width:6.49167in;height:4.06667in" />

<img src="./media/image14.png" style="width:6.5in;height:2.99931in"
alt="A screenshot of a computer Description automatically generated" />

6.  The Employees list is created for you now.Rename the **Title**
    column to **Emp_id**.

<img src="./media/image15.png" style="width:6.5in;height:5.13333in" />

<img src="./media/image16.png" style="width:6.5in;height:3.375in" />

7.  Now the employee table should like this

<img src="./media/image17.png" style="width:6.5in;height:2.86458in"
alt="A screenshot of a computer Description automatically generated" />

8.  Click on **Settings -\>List settings.**

<img src="./media/image18.png"
style="width:6.49167in;height:3.59167in" />

9.  Click on **Department** column link.

<img src="./media/image19.png"
style="width:6.49167in;height:5.38333in" />

10. Change below values and then click on **Ok**.

    1.  Type of Column : **Choice**

    2.  Allow 'Fill-in' choices: **Yes**

<img src="./media/image20.png"
style="width:6.49167in;height:4.75833in" />

11. Repeat the above step for Job title column also

12. Seelct **Have you been to orientation yet?** Column and make below
    chagnes and then click **OK**.

    1.  Type of Column : **Choice**

    2.  Allow 'Fill-in' choices: **Yes**

    3.  Typeeach cchoice on a separate line : **Yes No**

<img src="./media/image21.png" style="width:6.5in;height:5.22986in"
alt="A screenshot of a computer Description automatically generated" />

13. Repeat above step for Orientation Location with below properties

    1.  Type of Column : **Choice**

    2.  Allow 'Fill-in' choices: **Yes**

    3.  Typeeach cchoice on a separate line : **Redmon Reno**

> <img src="./media/image22.png" style="width:6.5in;height:5.42153in" />

14. Repeat above step for **Manager** clumnwith below properties

    1.  Type of Column : **Choice**

    2.  Allow 'Fill-in' choices: **Yes**

> <img src="./media/image23.png" style="width:6.1672in;height:6.5589in" />

<span id="_Toc176777249" class="anchor"></span>**Task 3 : Create a HR
list in SharePoint site from CSV file**

1.  Click on **Home- \>New -\> List**

<img src="./media/image24.png" style="width:6.5in;height:4.19167in" />

2.  Select **From CSV** tile from **Create a list window.**

<img src="./media/image25.png" style="width:6.5in;height:4.09167in" />

3.  Click on **Upload file** and browse C:\Labfiles and select
    **Import_HR_M365.CSV** and click **Open**.

<img src="./media/image26.png"
style="width:5.35833in;height:4.86667in" />

4.  Change **Work Email** column type to **Single line of text** and
    then click on **Next** .

<img src="./media/image27.png" style="width:6.49167in;height:3.475in" />

5.  Enter below details

Name : **Contoso HR**

Description : **Contoso Human Resource**, then click on **Create**
button.

<img src="./media/image28.png"
style="width:6.45833in;height:3.75833in" />

6.  Click on **Title -\> Column settings -\> Rename** columnt to
    **Emp_id**.

<img src="./media/image29.png" style="width:6.5in;height:5.325in" />

<img src="./media/image30.png" style="width:6.5in;height:3.29167in" />

7.  The HR table should like below image now.

<img src="./media/image31.png" style="width:6.5in;height:2.20278in"
alt="A screenshot of a computer Description automatically generated" />

### Conclusion

After completing this exercise, you will have:

1.  Lists in SharePoint with Employee information

<span id="_Toc176777251" class="anchor"></span>**Exercise 2: Create
Power apps for SharePoint Lists**

In this exercise, you will build your application to send an email to
employee with official information and asking him to fill and upload
documents.

<span id="_Toc176777252" class="anchor"></span>**Task 1 : Customize
Employee form with PowerApps for HRs to fill.**

1.  From your **Sharepint-\> Employee onboarding**, copy URL and save it
    Notepad.

<img src="./media/image32.png" style="width:6.5in;height:3.31667in"
alt="A screenshot of a computer Description automatically generated" />

2.  Open a new tab and go to **<https://make.powerapps.com/>.** Sign in
    with your office 365 admin tenant and select your environment.

3.  Click on **Apps** from left navigation menu. Select **New App- \>
    Start with a page design.**

<img src="./media/image33.png" style="width:6.5in;height:3.9in"
alt="A screenshot of a computer Description automatically generated" />

4.  Select **Blank Canvas** tile**.**

> <img src="./media/image34.png" style="width:6.5in;height:2.86667in"
> alt="A screenshot of a computer Description automatically generated" />

5.  Right click on Screen1 and select **Rename.**

<img src="./media/image35.png" style="width:6.49167in;height:4.90833in"
alt="A screenshot of a computer Description automatically generated" />

6.  Rename to **HrEmployeeform**

<img src="./media/image36.png" style="width:6.25833in;height:4.925in" />

8.  Select the form and **click on Insert-\> Edit form**

<img src="./media/image37.png" style="width:6.49167in;height:3.25in" />

7.  Search for **SharePoint** and select **SharePoint connector** from
    **Select a data source** dropdown**.**

> <img src="./media/image38.png" style="width:6.49167in;height:4.05833in"
> alt="A screenshot of a computer Description automatically generated" />

8.  Select **SharePoint** under **Add Connection.**

<img src="./media/image39.png" style="width:6.5in;height:4.00833in" />

9.  Enter the **SharePoint list url** copied form step 1 into Enter
    SharePoint URL text field and then click on **Connect**.

<img src="./media/image40.png" style="width:6.49167in;height:2.16667in"
alt="A screenshot of a computer Description automatically generated" />

9.  Select Employee Onboarding list and then click on **Connect**.

<img src="./media/image41.png" style="width:4.94167in;height:7.56667in"
alt="A screenshot of a computer Description automatically generated" />

10. Drag and fit the form into the container.

> <img src="./media/image42.png" style="width:6.5in;height:3.60764in"
> alt="A screenshot of a computer Description automatically generated" />

11. Drag the Form1 container little down and click on **Insert- \>
    Rectangle** to insert header to the form.

> <img src="./media/image43.png"
> style="width:6.49167in;height:3.53333in" />

12. Adjust the rectangle to the container width. Click on Insert- \>
    Text field.

<img src="./media/image44.png" style="width:6.5in;height:4.43333in" />

13. Change the width of the text field to the rectangle and update below
    properties.

**Tex: New Employee Onboarding Form**

**Font Size :** 27

**Font weight :** Bold

**Text alignment :** Centre

**Color :** White

<img src="./media/image45.png" style="width:6.5in;height:3.275in" />

14. Make **Emp_Id , First Name** and **Last_Name** as required fields.

15. Select **Emp_Id** field and change value **required** . Click on
    **Advanced** under **Properties** and select **Unlock to change
    properties**.

<img src="./media/image46.png"
style="width:6.49167in;height:2.11667in" />

16. Now Set Required value to true.You should see star next Emp_id
    field.

<img src="./media/image47.png" style="width:6.5in;height:2.84792in"
alt="A screenshot of a computer Description automatically generated" />

17. Repeat above two steps for **First Name** and **Last_Name**

Note : If you don’t see field then select the container- \>
properties-\> Edit( fields) .add field and re-order.

<img src="./media/image48.png" style="width:6.5in;height:1.78125in"
alt="A screenshot of a computer Description automatically generated" />

18. Select the Rectangular form /FormScreen1 and then click on **Insert
    -\> Button**.

<img src="./media/image49.png" style="width:6.5in;height:4.33333in" />

19. Drag and place the button under **Department** filed in the form and
    update below properties.

> **Text : Submit**

<img src="./media/image50.png"
style="width:6.49167in;height:3.03333in" />

20. Now , Add a new Screen. Click on **New Screen** and select
    **Success** template**.**

<img src="./media/image51.png" style="width:6.5in;height:6.125in" />

21. Select the new screen and **rename** to **Success** as shown in
    below images.

<img src="./media/image52.png"
style="width:6.49167in;height:3.60833in" />

22. Select **Lb1Successmsg1** and change the text to **New employee
    added**

<img src="./media/image53.png" style="width:6.49167in;height:3.725in" />

23. Now, Click on **Insert -\> Icons-\> Back arrow.**

<img src="./media/image54.png" style="width:6.5in;height:4.45in" />

24. Select Back Arrow and set below properties.

> Tool Tip **: Go Back**
>
> OnSelect **: Back(ScreenTransition.CoverRight)**

<img src="./media/image55.png"
style="width:6.49167in;height:2.93333in" />

25. Click on **HrEmployeeform.** Select **Button** and **select Onselect
    and enter below formula.**

**Note : Update the formula with your Sahrepoint Form)**

SubmitForm(*Form1*);ResetForm(*Form1*);Navigate(*Success*)

<img src="./media/image56.png" style="width:6.5in;height:3.75in" />

26. Select **Form1 ,** select **OnSuccess** and replace the formula with
    below formula

> ResetForm(Self); RequestHide();Notify("New Employee
> added",NotificationType.Success)
>
> <img src="./media/image57.png" style="width:6.5in;height:3.50833in" />

27. Click on **Save** button and enter the name as **EmpformforHr** and
    then click on **Save**.

<img src="./media/image58.png"
style="width:6.49167in;height:3.74167in" />

28. Select the form and change the Default mode to New and then click on
    the **Save -\>** **Preview** icon.

<img src="./media/image59.png"
style="width:6.49167in;height:3.36667in" />

29. Enter random **emp id, Frist name** and **Second name** and then
    click on **Submit** button**.**

<img src="./media/image60.png" style="width:6.5in;height:3.56736in"
alt="A screenshot of a computer Description automatically generated" />

30. You should see New employee added message**.** Click on **Back**
    button**.**

<img src="./media/image61.png" style="width:6.5in;height:3.3in"
alt="A screenshot of a computer Description automatically generated" />

31. Click on **Publish** button and then click on **Publish this
    version** button.

<img src="./media/image62.png"
style="width:6.49167in;height:3.93333in" />

32. Go back to Sharepoint tab in a browser and you should the above
    employee record in the list.

<span id="_Toc176777253" class="anchor"></span>**Task 2 : Create
employee onboarding Canvas app for the employee**

10. From your **Sharepint-\> Employee onboarding**, copy URL and save it
    Notepad.

<img src="./media/image32.png" style="width:6.5in;height:3.31667in" />

11. Open a new tab and go to **<https://make.powerapps.com/>.** Sign in
    with your office 365 admin tenant and select your environment.

12. Click on **Apps** from left navigation menu. Select **New App- \>
    Start with a page design.**

<img src="./media/image33.png" style="width:6.5in;height:3.9in" />

13. Select **Blank Canvas** tile**.**

> <img src="./media/image34.png" style="width:6.5in;height:2.86667in" />

14. Right click on Screen1 and select **Rename.**

<img src="./media/image35.png"
style="width:6.49167in;height:4.90833in" />

15. Rename to **Employeeform**

> <img src="./media/image63.png"
> style="width:5.81667in;height:4.98333in" />

16. Click on **Insert** and select **Edit** form**.**

<img src="./media/image64.png" style="width:6.5in;height:3.375in" />

17. Search for **SharePoint** and select **SharePoint connector** from
    **Select a data source** dropdown**.**

> <img src="./media/image38.png"
> style="width:6.49167in;height:4.05833in" />

18. Select **SharePoint** under **Add Connection.**

<img src="./media/image65.png" style="width:6.5in;height:3.4in" />

19. Enter the **SharePoint list url** copied form step 1 into Enter
    SharePoint URL text field and then click on **Connect**.

20. Under **Select a list**- \> select **Employee Onboarding** list and
    then click on **Next.**

<img src="./media/image40.png"
style="width:6.49167in;height:2.16667in" />

21. Select Employee Onboarding list and then click on Connect.

<img src="./media/image41.png"
style="width:4.94167in;height:7.56667in" />

22. Drag and fit the form into the container.

<img src="./media/image66.png" style="width:6.5in;height:2.90139in"
alt="A screenshot of a computer Description automatically generated" />

23. Select **Form 1** and **Display** mode to **New** under properties.

<img src="./media/image67.png"
style="width:6.49167in;height:2.41667in" />

24. Drag the Form1 container little down and click on **Insert- \>
    Rectangle** to insert header to the form.

<img src="./media/image68.png" style="width:6.5in;height:3.575in" />

25. Change the width of the rectangle to the container and select
    **Insert -\> Text label**.

<img src="./media/image69.png" style="width:6.5in;height:3.23333in" />

26. Select the Label and set below **properties**

    1.  **Text : Employee Onboarding Form**

    2.  **Font Size : 25**

    3.  **Font weight : Bold**

    4.  **Text alignment : Centre**

    5.  **Color : White**

<img src="./media/image70.png" style="width:6.5in;height:2.56667in" />

27. Select the EmployeeId field name and change **Font size** to **16**
    and **Font weight** to **Bold** under Properties.

<img src="./media/image71.png" style="width:6.5in;height:2.68333in" />

28. Repeat above step for all fields.

> <img src="./media/image72.png" style="width:6.5in;height:3.48611in" />

29. Select **Orientation location** item and set **Visible** property to
    **false.**

<img src="./media/image73.png" style="width:6.5in;height:2.86667in" />

30. Select **Have you been to orientation yet**?’s text field and click
    on **edit** label.

<img src="./media/image74.png"
style="width:6.49167in;height:2.39167in" />

31. Change label value to **Orientationdropdown**

<img src="./media/image75.png"
style="width:6.48333in;height:2.54167in" />

32. Select **Orientation Location data card** and select **Visible** and
    place below formula as shown in below image.

If(*Orientationdropdown*.Selected.Value="No",true,false)

<img src="./media/image76.png" style="width:6.49167in;height:3.775in" />

33. Click on **Save** and enter app name as : **EmployeeOnboardinForm**
    and then click on **Save** button.

<img src="./media/image77.png" style="width:6.49167in;height:3.25in" />

34. EmployeeId , First Name ,Last Name and **Manager** will be filled by
    HR so change the display mode to **View**.

35. Select the field and click **on Advanced-\> Unlock to change
    properties** and update **Display mode** to
    **Parent.DisplayMode.View**

> <img src="./media/image78.png" style="width:6.5in;height:2.11667in" />

<img src="./media/image79.png" style="width:6.49167in;height:1.625in" />

<img src="./media/image80.png" style="width:6.5in;height:2.02639in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image81.png" style="width:6.5in;height:1.82292in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image82.png" style="width:6.5in;height:2.34167in"
alt="A screenshot of a computer Description automatically generated" />

36. Select the **Workemail** Field -\> Unlock property and update
    **Required** property to **true.** Repeat for other fields if
    required.

> <img src="./media/image83.png" style="width:6.49167in;height:2.575in" />

37. Select the Forms and update **OnFailed** field value to

> Notify("Required Fields can't be empty.",NotificationType.Error)
>
> <img src="./media/image84.png" style="width:6.5in;height:3.45833in" />

38. Select **OnSuccess** and set the value to

Notify("Thank you for filling out the form",NotificationType.Success)

> <img src="./media/image85.png"
> style="width:6.49167in;height:2.84167in" />

39. Now, Lets add button to submit at the end of the form. Click on
    **Inset- \> Button.**

> <img src="./media/image86.png" style="width:6.5in;height:3.75in" />

40. Change the Properties of the button and save the form.

    1.  Text -\> **Submit**

    2.  Onselct **: SubmitForm(*Form1*);NewForm(*Form1*)**

<img src="./media/image87.png" style="width:6.5in;height:2.53333in" />

41. Click on Save and then click on Preview app buttons.

> <img src="./media/image88.png" style="width:6.5in;height:3.525in" />

42. Enter details and then click on Submit.

<img src="./media/image89.png" style="width:6.5in;height:3.59444in" />

43. You should see success notification.

<img src="./media/image90.png" style="width:6.5in;height:3.27361in" />

44. Close the preview window.

45. Click ‘on App from Tree View .Select OnStart and enter the below
    formula.

> Set(
>
>     onboardinglistitem,
>
>     LookUp(
>
>         'Employee Onboarding',
>
>         ID = Value(Param("ItemID"))
>
>     )
>
> )
>
> <img src="./media/image91.png"
> style="width:6.49167in;height:3.89167in" />

46. Select the Form1 from Tree View. Select item and enter the value as
    : **onboardinglistitem**

<img src="./media/image92.png" style="width:6.5in;height:3.86667in" />

47. Click on **Save** and **Publish -\> Publish this version**.

<img src="./media/image93.png"
style="width:6.49167in;height:3.94167in" />

48. Go back to the PowerApps Home page, Click on Apps-\> Your app-\>
    Details.

<img src="./media/image94.png"
style="width:6.49167in;height:3.60833in" />

49. Copy the Weblink to use in next task.

<img src="./media/image95.png"
style="width:6.49167in;height:2.98333in" />

50. Close the preview window and navigate to your SharePoint tab and
    check the above record in the list.

> <img src="./media/image96.png" style="width:6.5in;height:2.71319in" />

<span id="_Toc176777254" class="anchor"></span>**Task 3 : Create Power
Automate flow to send a form to the new employee**

1.  **Go back to SharePint tab and copy the URL.**

> <img src="./media/image97.png"
> style="width:6.49167in;height:2.99167in" />

2.  Open a new tab and go to https:\\\flow.microsoft.com and sign in
    with your Office 365 admin account**.**

3.  Click on **Flows** from left navigation menu**.** Click on **New
    Flow-\> Automated Cloud flow.**

> <img src="./media/image98.png"
> style="width:6.49167in;height:2.34167in" />

4.  Enter the flow name as : **Onboarding new employee** . Search for
    **When an item is created** and select it from SharePoint and then
    click on **create**.

> <img src="./media/image99.png" style="width:6.5in;height:4.16667in" />

5.  Select the action. Click on **Site Address -\> Enter custom value.**

<img src="./media/image100.png" style="width:6.5in;height:3.36667in" />

6.  Enter the Adress copied in Step 1 and then select the Employee
    Onboarding list as shown in below image.

<img src="./media/image101.png"
style="width:6.49167in;height:3.90833in" />

7.  Click on + to add new action.

<img src="./media/image102.png"
style="width:4.85833in;height:3.18333in" />

8.  Seach for Send and email and select **Send and email (V2)**

> <img src="./media/image103.png" style="width:6.5in;height:4.39167in" />

9.  Click on To text field and select Enter the data from previous step
    .

> <img src="./media/image104.png" style="width:6.5in;height:2.31667in" />

10. Select **Wrokemail**

<img src="./media/image105.png"
style="width:6.49167in;height:2.76667in" />

11. Enter the Subject line as : **Welcome to Firm** select First Name
    from Previous step.

<img src="./media/image106.png" style="width:6.49167in;height:4.05in" />

12. Enter below data in Body of the email. Insert dynamic values as
    shown in image.

> Hi Firstname Lastname,
>
> Please click on link below to complete your onboarding form.
>
> <img src="./media/image107.png" style="width:6.49167in;height:3.81667in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image108.png" style="width:6.43389in;height:3.867in"
> alt="A screenshot of a computer Description automatically generated" />

13. Enter the Weblink copied in Task 2 – and add **&itemID=** at the end
    of the link and select Dynamic ID as shown in below image.

> <img src="./media/image109.png" style="width:6.5in;height:2.83333in" />
>
> <img src="./media/image110.png" style="width:6.5in;height:3.47361in"
> alt="A screenshot of a computer Description automatically generated" />

14. Cut the link and then enter the text : **Onboarding Form** and
    select and click on link icon. paste the link copied from above
    step.

> <img src="./media/image111.png" style="width:6.5in;height:4.98333in" />

15. Save the flow now.

> <img src="./media/image112.png" style="width:6.49167in;height:3.3in" />
>
> <img src="./media/image113.png" style="width:6.5in;height:2.22778in"
> alt="A screenshot of a computer Description automatically generated" />

<span id="_Toc176777255" class="anchor"></span>**Task 4 : Test the
flow.**

1.  Go back to PoweApps tab, select Hr form **.**

<img src="./media/image114.png" style="width:6.5in;height:3.76667in" />

2.  IF asked then allow permissions.

<img src="./media/image115.png" style="width:6.5in;height:3.42431in"
alt="A screenshot of a computer Description automatically generated" />

3.  Fill the form with your details. Enter workemail as your Office 365
    admin id and Submit the form

<img src="./media/image116.png" style="width:6.5in;height:3.61667in" />

<img src="./media/image117.png" style="width:6.5in;height:3.16667in"
alt="A screenshot of a computer Description automatically generated" />

4.  Go back to the Power Automate flow and check flow Stats.

<img src="./media/image118.png" style="width:6.5in;height:1.925in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image119.png" style="width:6.5in;height:4.15556in"
alt="A screenshot of a computer Description automatically generated" />

5.  Open a new tab and go to https:\\\outlook.com and sign in with your
    O365 admin account and check inbox.Click on the **Onboarding Form**
    link in the email generated from HR

> <img src="./media/image120.png"
> style="width:6.49167in;height:3.10833in" />

### Conclusion

After completing this exercise, you will have:

1.  Employee Onboarding app using Power Apps

2.  Power Automate clod flow to generate an email to employee to
    complete Onboarding process.

This guarantees that you will have a fully functional **Employee
Onboarding App**, complete with all essential screens.
