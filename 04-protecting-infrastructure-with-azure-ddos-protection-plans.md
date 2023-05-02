# Exercise 4- Protecting Infrastructure with Azure DDoS Protection Plans

 ### What is DDoS protection?

Distributed denial of service (DDoS) attacks is some of the largest availability and security concerns facing customers that are moving their applations to the cloud. A DDoS attack attempts to exhaust an application's resources, making the application unavailable to legitimate users. DDoS attacks can be targeted at any endpoint that is publicly reachable through the internet.

Azure DDoS Protection, combined with application design best practices, provides enhanced DDoS mitigation features to defend against DDoS attacks. It's automatically tuned to help protect your specific Azure resources in a virtual network. Protection is simple to enable on any new or existing virtual network, and it requires no application or resource changes.

  ![](images/ddos.png)


### Types of attacks Azure DDoS Protection mitigates

- **Volumetric attacks**: These attacks flood the network layer with a substantial amount of seemingly legitimate traffic. They include UDP floods, amplification floods, and other spoofed-packet floods. DDoS Protection mitigates these potential multi-gigabyte attacks by absorbing and scrubbing them, with Azure's global network scale, automatically.
- **Protocol attacks**: These attacks render a target inaccessible, by exploiting a weakness in the layer 3 and layer 4 protocol stack. They include SYN flood attacks, reflection attacks, and other protocol attacks. DDoS Protection mitigates these attacks, differentiating between malicious and legitimate traffic, by interacting with the client, and blocking malicious traffic.
- **Resource (application) layer attacks**: These attacks target web application packets, to disrupt the transmission of data between hosts. They include HTTP protocol violations, SQL injection, cross-site scripting, and other layers 7 attacks. Use a Web Application Firewall, such as the Azure Application Gateway web application firewall, as well as DDoS Protection to provide defence against these attacks. There are also third-party web application firewall offerings available in the Azure Marketplace.

1. In the Azure portal, search **DDoS protection plans (1)** and then select **DDoS protection plans (2)**.
 
   ![](images/ddos1.png)
 
1. Click on create.
 
    ![](images/ddos2.png)
 
1. On the **DDoS protection** page, provide the information as mentioned below,
   - Subscription: **Leave it as default (1)**.
   - Resource Group: **JumpVM-rg (2)**.
   - Name: Enter **DDoSprotection (3)**.
   - Region: **<inject key="Region" />**
   - Click on **Next-Tags**.
 
     ![](images/ddos3.png)
 
1. On the **Tags** tab, leave everything to default and then  click on **Review + create**.
 
     ![](images/ddos4.png)
  
1. If the validation is passed then  click on **Create**.

    >**NOTE**: It may take a couple of minutes for the workspace to be created.

      ![](images/ddos5.png)
 
1. Once the DDoS protection is added you will see a notification that says **Deployment succeeded**, as shown below.

      ![](images/ddos6.png)
 
1. On the DDoS protection page, under setting click on **Protected resources (1)** and then select the **vnet (2)** and click on **Add (3)**.
 
      ![](images/ddos10.png)

1. On the **Add virtual network  to DDoS plan** blade, provide the information as mentioned below,
    - Subscription: **Leave it as default (1)**.
    - Resource Group: **JumpVM-rg (2)**.
    - Virtual network: Select **vnet (3)**.
    - Click on **Add (4)**
   
      ![](images/ddos8.png)
 
1. Once the Protected resources are added you will see a notification that says **Successfully updated the virtual network vnet**, as shown below.
 
      ![](images/ddos9.png)
 
1. Now, In the Azure portal, search **Firewall Manager (1)** and then select **Firewall Manager (2)**.
 
      ![](images/ddos11.png)

1. Under Deployments, click on **Virtual Networks**, and you will see that you are protected.
 
      ![](images/ddos12.png)
