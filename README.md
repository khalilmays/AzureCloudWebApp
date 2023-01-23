<h1>Azure Cloud Webapp</h1>

<h2>Description</h2>
In this project I developed and designed a cyber-blog web application using Azure’s Cloud services and Docker.
I then created and stored SSL certificates in Azure’s Key Vault, and bound them to secure the web application. I also protected the web application by utilizing Azure’s Security features, such as Azure’s Front Door, WAF, and Security Center.

<br />


<h2>Technologies Used</h2>

- <b>Azure: {Keyvaults, App Services, Front Door, WAF}</b>
- <b>PHP</b>
- <b>HTML</b>
- <b>Docker</b>
- <b>OpenSSL</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Walk-through:</h2>

<p align="center">
Select "App Services" in the Azure search field: <br/>
<img src="https://i.imgur.com/k7h6mdZ.png" height="80%" width="80%" alt="App Services"/>
<br />
<br />
Select "Create" to create your app:  <br/>
<img src="https://i.imgur.com/PCaXvLb.png" height="80%" width="80%" alt="Create app"/>
<br />
<br />
Selected these options for the "Basics" tab: <br/>
<img src="https://i.imgur.com/EszCcBi.png" height="80%" width="80%" alt="Basics"/>
<br />
<br />
Selcted these options for the App Service Plan:  <br/>
<img src="https://i.imgur.com/WJK5EeZ.png" height="80%" width="80%" alt="App service plan"/>
<br />
<br />
Leave the default options for every other tab and select the "Review + Create" tab. Then you will select the create button at the bottom of your screen to create your web app.
<br />
<br />
Once you have created your app you can either select "Go to Resource" or you can go to the app by clicking "App Services" in the Azure search bar. Then would select your app from this page:  <br/>
<img src="https://i.imgur.com/BzsA80B.png" height="80%" width="80%" alt="select app"/>
<br />
<br />
After selecting your app, a menu of options appears on the left. You will choose the "Custom domains" option:  <br/>
<img src="https://i.imgur.com/MHx7ZTp.png" height="30%" width="30%" alt="custom domains"/>
<br />
<br />
A new page will open, and you will be able to see a unique IP address that your app was assigned:  <br/>
<img src="https://i.imgur.com/B4hKa5S.png" height="80%" width="80%" alt="IP address"/>
<br />
<br />
Your domain is now accessible on the internet and it begins with the name you chose ".azurewebsites.net"
<br />
<br />
This is the docker container that I deployed to my web app using Azure Cloud Shell:  <br/>
<img src="https://i.imgur.com/C0QSchr.png" height="80%" width="80%" alt="Docker Container"/>
<br />
<br />
To get into Azure CLoud Shell, you click the shell logo located inthe tool bar:  <br/>
<img src="https://i.imgur.com/0sHCBtm.png" height="80%" width="80%" alt="Azure Cloud Shell"/>
<br />
<br />
I configured the web app with the container mentioned above by running the following command:  <br/>
az webapp config container set --name (name of your webapp) --resource-group (name of your resource group) --docker-custom-image-name cyberxsecurity/project1-apachewebserver --enable-app-service-storage-t  <br/>
<br />
<br />
After pressing enter you should see this output: <br />
<img src="https://i.imgur.com/syypJCY.png" height="80%" width="80%" alt="Output"/>
<br />
<br />
To verify that the container has been added correctly, make sure to run the fdollowing command to show the container for your webapp: <br />
az webapp config container show --name (name of your webapp) --resource-group (name of your resourece group) <br />
<br />
<br />
Next, visit the domain that you chose to see if your container was successfully deployed. The webpage should like like this: <br />
<img src="https://i.imgur.com/uT6TQzD.png" height="80%" width="80%" alt="Blog Site"/> <br />
<br />
<br />

 
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
