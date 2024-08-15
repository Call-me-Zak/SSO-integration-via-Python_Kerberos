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


