# Setup Apex for HTTPS access

<ol>
  <li>Create a directory accessible to oracle
    <code>/home/oracle/wallet</code>
  </li>
  <li>
   Move wallet file to this directory
  </li>
  <li>Update Apex Administratioon Instance Settings, set wallet path to <code>file://home/oracle/wallet/</code>
</ol>
  

# AWS Key and Secret

https://www.msp360.com/resources/blog/how-to-find-your-aws-access-key-id-and-secret-access-key/


# AWS  PLSQL PACKAGE

https://github.com/cmoore-sp/plsql-aws-s3

Since the wallet information is already configured in APEX, you don't need to set it in the package.

In the put object procedure, adjust the timezone so that your request can be made in UTC time. Unless you're on RDS with the Time Zone modifier

<code>l_date := systimestamp + interval '4' hour;</code>
