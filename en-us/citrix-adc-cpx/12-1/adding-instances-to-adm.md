---
layout: doc
---
# Adding Citrix ADC CPX Instances to Citrix ADM

You must add the Citrix ADC CPX instances installed on a Docker host to Citrix Application Delivery Management (ADM) software if you want to manage and monitor these instances.

You can add instances either while setting up ADM for the first time or at a later time.

To add instances, you must create an instance profile and specify either the host name or IP address of each instance, or a range of IP addresses. This instance profile contains the user name and password of the instance(s) that you want to add to Citrix ADM. For each instance type, a default profile is available. For example, the ns-root-profile is the default profile for Citrix ADC instances. This profile is defined by the default ADC administrator credentials. If you have changed the default admin credentials of your instances, you can define custom instance profiles for those instances.  If you change the credentials of an instance after the instance is discovered, you must edit the instance profile or create a new profile, and then rediscover the instance.

## Prerequisites

Make sure that you have:

-  Installed the Citrix ADM software on Citrix XenServer. For more information, see [Citrix ADM Documentation](https://docs.citrix.com/en-us/netscaler-mas/12-1.html).
-  Installed the Citrix ADC CPX instances on a Docker host.

**To add Citrix ADC CPX instances to ADM:**

1.  In a web browser, type the IP address of the **Citrix Application Delivery Management** (for example, `http://192.168.100.1).`

1.  In the **User Name** and **Password** fields, enter the administrator credentials. The default administrator credentials are **nsroot** and **nsroot**.

1.  Navigate to **Networks \> Instances** > **Citrix ADC** and click **CPX** tab.

1.  Click **Add** to add new CPX instances in Citrix ADM.

1.  The **Add Citrix ADC CPX** page opens. Enter the values for the following parameters:

    1.  You can add CPX instances by providing either the reachable IP address of the CPX instance or the IP address of the Docker container where the CPX instance is hosted.
    1.  Select the profile of the CPX instance.
    1.  Select the site where the instances is to be deployed.
    1.  Select the agent.
    1.  As an option, you can enter the key-value pair to the instance. Adding key-value pair makes it easy for you to search for the instance later.

        ![localized image](/en-us/citrix-adc-cpx/12-1/media/add-cpx-instances.PNG)

1.  Click **OK**.

> **Note**
>
> If you want to rediscover an instance, navigate to **Networks \> Instances \> Citrix ADC > CPX**, select the instance you want to rediscover, and then from the **Select Action** drop-down list, click **Rediscover**.