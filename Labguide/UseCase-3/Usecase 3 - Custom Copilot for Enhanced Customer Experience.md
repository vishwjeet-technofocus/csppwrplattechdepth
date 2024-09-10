# Level-up CSP Technical Training – Power Platform Facilitator Guide

# Custom Copilot for Enhanced Customer Experience

| Description       | This scenario extends the functionality of the Virtual Assistant copilot for Contoso Electronics, initially developed to assist customers with product discovery and post-purchase activities like return eligibility and refund requests. The enhancement introduces automated case escalation, allowing the copilot to seamlessly transfer conversations to live agents when it cannot resolve a query or when the customer requests human assistance. This ensures a more personalized and efficient customer service experience by blending automated responses with human support for complex issues. |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prerequisites     | To get the most out of this lab guide we recommend you have to develop copilot use case 2 (Build a copilot for your customer’s webpage), Microsoft dynamic 365 trial license, Copilot Studio, Power Pages trial license.                                                                                                                                                                                                                                                                                                                                                                                   |
| Duration          | 30 mins                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Publication date  | September 2024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

This document is provided “as-is”. Information and views expressed in
this document, including URL and other Internet Web site references, may
change without notice. You bear the risk of using it. 

This document does not provide you with any legal rights to any
intellectual property in any Microsoft product. You may copy and use
this document for your internal, reference purposes. 

 

© 2024 Microsoft. All rights reserved.  

# **Objective & Scenario**

## Objective

This is an extension of **Use Case 2**, where we developed a standalone
Virtual Assistant copilot for Contoso Electronics' webpage to help
customers discover the best products based on their needs and
preferences, as well as manage post-purchase activities such as
verifying return eligibility and submitting refund requests seamlessly.
In this use case, the goal is to enhance the copilot by introducing
automated case escalation to live agents when the copilot cannot resolve
a customer’s issue or when the customer requests human support.

## Solution Focus Area

In **Use Case 2**, the copilot was created and published on Contoso
Electronics' website to assist customers with product discovery and
post-purchase processes like returns and refunds. Now, the focus shifts
towards **enhancing customer support** by enabling the copilot to
smoothly escalate conversations to live agents when required. This
ensures that customers receive timely and effective assistance when the
virtual assistant alone is not sufficient.

The enhancement will focus on:

1.  **Automated Case Escalation**: Automatically transitioning the
    conversation to a live agent when the copilot cannot provide
    relevant information or fully address the customer’s concern.

2.  **Live Agent Requests**: Allowing customers to request live agent
    assistance at any point during their interaction with the copilot,
    ensuring they can access human support when needed.

## Persona and Scenario

- **Remy Morris** - Digital Solutions Architect 

<!-- -->

- **Mark Brown** – Project lead 

<!-- -->

- **David Flores** – App developer 

<!-- -->

- **Jane Miller** – App tester 

- **Contoso Electronics Support Team** – Live Agents

- **Miriam Graham –** Customer

These personas will participate in the following sequential scenarios: 

- Remy Morris designs and plans the digital architecture to meet the
  business needs. He presents this framework to Mark Brown and helps him
  select the appropriate Power Platform tools for the implementation.

- Mark Brown provides David Flores with an overview of the selected
  tools and processes. This includes enhancing the virtual agent with
  the live agent feature using Copilot, Dynamics 365, and implementing
  the bot on the Contoso Electronics webpage.

- David Flores creates the virtual assistant, ensuring it meets all the
  requirements specified by Contoso Electronics. He then submits the
  developed assistant to Jane Miller for testing.

- Jane Miller conducts thorough testing and validation of the virtual
  assistant to ensure functionality and performance.

- Upon successful testing, Mark Brown officially deploys the virtual
  assistant with live agent features on the Contoso Electronics website.

- Miriam Graham initiates interaction with the Virtual Assistant Copilot
  to inquire about the return policy for her laptop due to
  unsatisfactory battery life. If the Virtual Assistant Copilot cannot
  resolve the issue completely or if Miriam prefers to speak with a
  human, the copilot escalates the conversation to a Live Support Agent.

- The Live Support Agents handle the escalation, addressing any complex
  issues or detailed inquiries. They ensure Miriam’s refund request is
  processed smoothly and promptly.

## Pre-requisites 

For this use case, all participants will need the following: 

- Microsoft Copilot Studio Free Trial License

- Microsoft Dynamic 365 Free Trial License

- Microsoft Power Pages

- Contoso Electronics Bot Use Case 2 (Build a copilot for your
  customer’s webpage)

# **Lab Instructions**

# Exercise1: Configure Copilot with Dynamics 365

In this exercise, you will set up Dynamics 365 for customer service by
signing in, creating a new workstream, and configuring a chat channel.
This process will enable you to integrate and manage customer
interactions efficiently using Dynamics 365’s capabilities.

## Task 1: Sign in to Dynamic 365

1.  Open your preferred web browser and navigate to
    <https://www.microsoft.com/en-us/dynamics-365/products/customer-service>

2.  On the homepage, click the **Try for free** button to initiate the
    process of signing up for a free trial of Dynamics 365 Customer
    Service.

<img src="./media/image1.png"
style="width:6.26806in;height:3.32708in" />

3.  Enter your Tenant ID on the redirected page. This ID uniquely
    identifies your organization within Microsoft's ecosystem.

4.  Click **Start your free trial** to proceed.

<img src="./media/image1.png"
style="width:6.26806in;height:3.32708in" />

5.  Enter your password and click **Sign in**.

<img src="./media/image2.png"
style="width:6.26806in;height:4.05903in" />

6.  On the next screen, select **United States** as your Region.

7.  Enter your Phone Number for verification and click **Submit**.

<img src="./media/image3.png"
style="width:6.26806in;height:4.19167in" />

8.  After submission, you will be redirected to the Dynamics 365
    Customer Service workspace.

9.  Click on **Customer Service workspace** to explore the tools
    available.

<img src="./media/image4.png"
style="width:6.26806in;height:2.98125in" />

10. Locate and click on **Customer Service admin Center** within the
    workspace to configure settings, manage users, and customize your
    customer service setup.

<img src="./media/image5.png"
style="width:6.26806in;height:2.94931in" />

## Task 2: Create a new Workstream

1.  In the left navigation bar, click on **Workstream**, then click on
    **+ New Workstream** to create a new one.

<img src="./media/image6.png"
style="width:6.26806in;height:2.77569in" />

2.  Enter **Contoso Agent** in the Name field.

3.  Select **Messaging** from the Type dropdown menu.

4.  Select **Chat** from the Channel dropdown menu.

5.  Select **Push** and choose **Existing**.

6.  From the dropdown menu, select **Fallback-chat demo (1 user)**.

7.  Click **Create** to finalize the new workstream.

<img src="./media/image7.png"
style="width:6.26806in;height:2.93125in" />

## Task 3: Configure a new Channel

1.  In the **Contoso Agent** workstream, click on **Set up chat**.

<img src="./media/image8.png"
style="width:6.26806in;height:2.91389in" />

2.  Enter **Contoso Live Agent** as the name of the channel. Click
    **Next**.

<img src="./media/image9.png"
style="width:6.26806in;height:2.98819in" />

3.  Enter **Contoso Agent** in the Title field. Click **Next** again.

<img src="./media/image10.png"
style="width:6.26806in;height:2.99653in" />

<img src="./media/image11.png"
style="width:6.26806in;height:2.97708in" />

4.  On the User Features page, turn off **File attachment** and **Voice
    and Video Call** options, then click **Next**.

<img src="./media/image12.png"
style="width:6.26806in;height:2.97639in" />

5.  Click **Create Channel**.

<img src="./media/image13.png"
style="width:6.26806in;height:2.98403in" />

6.  Copy the widget code and click **Done**.

<img src="./e8b7c58ebb460968eb282d7e07fbe43a3dcd0ecd.png"
style="width:6.26806in;height:3.14514in" />

## Conclusion

After completing all exercise, you will have:

1.  Logged into Dynamics 365 Customer Service and accessed the workspace

2.  Established "Contoso Agent" with messaging and chat channel
    settings.

3.  Set up "Contoso Live Agent" with specific features and obtained the
    widget code for integration.

This setup prepares Dynamics 365 for effective customer interaction
management.

# Exercise 2: Escalate Copilot and connect Omnichannel

In this exercise, you'll enhance the functionality of your Copilot by
configuring escalation topics and establishing a connection with
Dynamics 365. You'll also activate the Copilot channel to ensure
seamless integration and communication with the customer engagement hub.

## Task 1: Configure Escalate Topic

1.  Navigate to **Copilot Studio** and select your **Contoso Electronics
    Services Copilot**.

2.  In the top navigation bar, click on **Topics** (located next to the
    knowledge base).

<img src="./media/image15.png"
style="width:6.26806in;height:2.95625in" />

3.  Scroll down to locate the **Escalate** topic and select it to open
    the configuration.

<img src="./media/image16.png"
style="width:6.26806in;height:2.96042in" />

4.  In the topic canvas, find the **message node**.

5.  Click on the three dots next to the message node and choose
    **Delete** to remove it.

<img src="./media/image17.png"
style="width:6.26806in;height:2.95208in" />

6.  Click on the **+ sign** below the trigger node to add a new node.

7.  Select **Topic Management** from the options.

8.  In the topic management options, select **Transfer Conversation** to
    create a new transfer node.

<img src="./media/image18.png"
style="width:6.26806in;height:2.97153in" />

9.  Once the **Transfer Conversation** node is added, click the **Save**
    button to save the configuration changes.

<img src="./media/image19.png"
style="width:6.26806in;height:2.93611in" />

## Task 2: Activate the Copilot Channel

1.  Navigate to **Copilot Studio** and open your **Contoso Electronics
    Services Copilot**.

2.  Click on the **Channel** next to the action button.

<img src="./media/image20.png"
style="width:6.26806in;height:2.94028in" />

3.  Scroll down and select **Customer Engagement Hub**.

<img src="./media/image21.png"
style="width:6.26806in;height:2.98056in" />

4.  Click **Connect** to create a connection with Dynamics 365.

<img src="./media/image22.png"
style="width:6.26806in;height:2.97708in" />

## Task 3: Publish your Copilot

1.  Navigate to Overview section and In Microsoft Copilot Studio, look
    for the **Publish** button on the right side of the screen.

2.  Click on the **Publish** button to start the publishing process.

<img src="./media/image23.png"
style="width:6.26806in;height:2.95764in" />

3.  A confirmation dialog may appear. Select **Publish** again to
    finalize and publish your copilot.

<img src="./b164e1810c3e71ef548071334278a3b1451512aa.png"
style="width:6.26806in;height:2.97292in" />

## Conclusion

After completing all exercise, you will have:

1.  Modified the "Escalate" topic by removing the message node and
    adding a Transfer Conversation node to facilitate escalation.

2.  Established a connection between the Copilot and Dynamics 365
    Customer Engagement Hub by selecting and connecting the channel.

3.  Completed the publishing process to make the Copilot live and
    available for use.

These steps enhance the Copilot's functionality and integration with
Dynamics 365, ensuring effective escalation handling and seamless
communication.

# Exercise 3: Add and activate Copilot Bot in Dynamic 365

In this exercise, you'll integrate your Copilot bot into Dynamics 365 by
adding it to the Customer Service workspace. This process involves
connecting the bot to the existing workstream and verifying its
activation to ensure it is functioning correctly.

## Task 1: Add Bot in Dynamic 365

1.  Click on **Customer Service workspace** to explore the apps.

<img src="./media/image25.png"
style="width:6.26806in;height:2.96181in" />

2.  Locate and click on **Customer Service admin Center** within the
    workspace.

<img src="./media/image26.png"
style="width:6.26806in;height:2.92014in" />

3.  In the left navigation bar, click on **Workstream**, then select the
    **Contoso Agent** workstream created earlier.

<img src="./media/image27.png"
style="width:6.26806in;height:2.94306in" />

4.  At the bottom, click **Add Bot**.

<img src="./media/image28.png" style="width:6.26806in;height:2.975in" />

5.  Select **Contoso Electronics Services** and click **Connect**.

<img src="./media/image29.png"
style="width:6.26806in;height:2.98403in" />

## Task 2: Check Bot Connection

1.  In the left navigation bar, click on **Bot** and check that the
    **Contoso Electronics Services** bot is active.

<img src="./media/image30.png"
style="width:6.26806in;height:2.93889in" />

<img src="./51340a7ebee049105e3ab02c58b464d406e35902.png"
style="width:6.26806in;height:2.85694in" />

## Conclusion

1.  Integrated the "Contoso Electronics Services" bot into the "Contoso
    Agent" workstream by connecting it within the Customer Service admin
    center.

2.  Verified that the bot is active and functioning correctly in the Bot
    section of the Dynamics 365 interface.

This process ensures that your Copilot bot is effectively integrated and
operational within Dynamics 365, ready to handle customer interactions
through the configured workstream.

# Exercise 4: Deploy Copilot on a Power Page Website

In this exercise, you'll deploy your Copilot bot onto a Power Page
website. This involves connecting the bot with Power Pages, adding the
necessary code to the website, and previewing it to ensure everything is
functioning as expected.

## Task 1: Connect Bot with Power Pages

1.  Visit
    <https://www.microsoft.com/en-us/power-platform/products/power-pages>
    and sign in with the same ID and password.

<img src="./media/image32.png"
style="width:6.26806in;height:2.93889in" />

2.  From the top right corner, select the same environment as your
    customer service trial.

<img src="./media/image33.png"
style="width:6.26806in;height:2.99444in" />

3.  Scroll down and select **Start a template**.

<img src="./media/image34.png"
style="width:6.26806in;height:2.9625in" />

4.  Choose a template, name the website **Contoso**, and click **Done**.

<img src="./media/image35.png"
style="width:6.26806in;height:2.99722in" />

<img src="./media/image36.png"
style="width:6.26806in;height:2.77569in" />

5.  Click **Edit Code** and then **Open Visual Studio Code**.

<img src="./media/image37.png"
style="width:6.26806in;height:2.94792in" />

6.  Sign in to Visual Studio Code when prompted.

<img src="./media/image38.png"
style="width:6.26806in;height:2.91806in" />

7.  Paste the widget code (copied earlier) at the bottom of the website
    home page code.

<img src="./media/image39.png"
style="width:6.26806in;height:2.95347in" />

8.  Save the file with **Ctrl + S**.

9.  Return to the Power Pages window and click **Sync**.

<img src="./media/image40.png"
style="width:6.26806in;height:3.01111in" />

10. Click **Preview** and then **Desktop** to preview the website. The
    **Contoso Agent** bot should appear at the bottom.

<img src="./b7dfd23654846e4a0f8f335316003a3100934bdc.png"
style="width:6.26806in;height:2.93125in" />

## Conclusion

1.  Logged into Power Pages, created a website using a template, and
    integrated the Copilot bot by adding the widget code to the
    website's home page code.

2.  Saved the code changes, synced with Power Pages, and previewed the
    site to ensure the "Contoso Agent" bot appears and functions
    correctly.

This deployment ensures your Copilot bot is live and operational on the
Power Page website, providing a seamless customer interaction
experience.

# Test Live Agent

In this exercise, you'll test the live agent functionality by
interacting with the Contoso Agent bot deployed on the Power Pages
website. This will involve initiating a live agent chat request from the
website and managing the interaction within the Dynamics 365 Customer
Service workspace.

Top of Form

Bottom of Form

1.  Go to Dynamics 365 and select **Customer Service workspace** and
    then select **Customer Service workspace** App to open and explore
    the apps.

2.  In another window, open the Power Pages app and preview the website
    created in the previous step.

3.  Open **Contoso Agent** on the Power Pages website.

4.  Type **Live agent** in the chatbot.

<img src="./media/image42.png"
style="width:6.26806in;height:2.95208in" />

<img src="./media/image43.png"
style="width:6.26806in;height:2.95208in" />

5.  The live agent chat request will be sent to the Customer Service
    workspace, where the live agent can accept or reject the request.

<img src="./media/image44.png"
style="width:6.26806in;height:2.98958in" />

6.  Live agent accepts the request and start conversation.

<img src="./media/image45.png"
style="width:6.26806in;height:2.78403in" />

7.  Customer reply to live agent.

<img src="./media/image46.png"
style="width:6.26806in;height:2.89861in" />

8.  Contoso Electronic live agent replies.

<img src="./f97cf2523eceb8e14643178fbc3dd75635277b47.png"
style="width:6.26806in;height:2.76458in" />

# Final Conclusion

1.  **Configured Dynamics 365:** Successfully signed in, created a new
    workstream, and configured a chat channel to manage customer
    interactions efficiently.

2.  **Enhanced Copilot Functionality:** Configured escalation topics,
    connected the Copilot with Dynamics 365, and activated the Copilot
    channel to streamline customer service operations.

3.  **Integrated Copilot Bot:** Added and verified the Copilot bot
    within the Dynamics 365 Customer Service workspace, ensuring it was
    properly connected and active.

4.  **Deployed Copilot on Power Pages:** Connected the bot with Power
    Pages, integrated it into the website, and previewed the deployment
    to confirm its functionality.
