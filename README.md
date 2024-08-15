# SSO-integration-via-Python_Kerberos

** Implementation Plan
1. Configure Django for Integrated Windows Authentication (IWA)

    Set Up Active Directory (AD) Integration:
        Ensure your Django app is integrated with the company’s Active Directory.
        Install the necessary libraries, such as django-auth-ldap or django-kerberos, which will allow your Django application to communicate with AD.

   ![image](https://github.com/user-attachments/assets/b13bd1a6-ced8-43f7-aa85-0921349eae84)

** Django Settings Configuration:

    Update the settings.py file to include LDAP or Kerberos authentication backends.

Example LDAP configuration in settings.py:

![image](https://github.com/user-attachments/assets/e54a5207-a22d-485e-8671-fcff4038a537)

Step 2: Set Up Your Local LDAP Server

Since I don't have a local LDAP server running, I can either:

    Install OpenLDAP on your local machine.
    Use a Docker container that runs an LDAP server.

So Docker it is !

Run the following command to get started :
```docker run --env LDAP_ORGANISATION="My Company" --env LDAP_DOMAIN="mycompany.com" --env LDAP_ADMIN_PASSWORD="adminpassword" -p 389:389 --name my-openldap-container --detach osixia/openldap
```

This command will start an OpenLDAP server locally on port 389.

Step 3: Configure Django to Use LDAP

Now, let's modify your settings.py file to integrate LDAP. Here’s a basic setup:

    Import the necessary modules at the top of your settings.py:
![image](https://github.com/user-attachments/assets/7ec27c4f-3a95-43b4-ba26-9b1bbbdd3327)

Add the LDAP configuration:

![image](https://github.com/user-attachments/assets/e711ba99-0694-4470-9c43-90e2a73aa540)



    
