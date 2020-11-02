# merakiguestwifi
Leveraging Meraki's guest WiFi captive Wi-Fi portal to improve customer engagement and provide instant contextual feedback to property mgmt duty manager. To improve guest feedback which is often shared in social media after the guest has left the premise with vivid negative experience, telling the world via social media their negative experiecnce with damaged reputation difficult to remediate.  This simple guest survey (splash page) is to collect user feedback upon successful guest Wi-Fi login. We leverage the built-in feature of Meraki Access Point. https://documentation.meraki.com/MR/MR_Splash_Page/Splash_Page_Details_for_Meraki_MR

A google form is created to collect feedback with rating between 1 (very bad) to 5 (very good)

If the feedback score is 1, the google script on the google form will triger an email (via Google SMTP) to duty manager's email address.

A language match of the feedback's text will be used to select the appropriate MV to take a snapshot whereby the image will be included in the email to be sent to the duty manager to give more context. For example, if the feedback says "broken glass near the exit A", then script will send API call to Meraki MV camera near exit A to take a screenshot and the image is pasted onto the email to Duty Manager to give a visual on the area for impact to customer flow near Exist A.
