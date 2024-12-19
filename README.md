# azure-website-deployment
Deploying a static website in Azure Virtual Machine

STEP 1: Create a Virtual Machine:
- Go to Virtual Machines and click Create > Virtual Machine.
- Choose an appropriate Resource Group and Region.
- Select a Linux OS (e.g., Ubuntu).
- Configure other settings like VM, Disk size, SSH pub key and click Review + Create.

STEP 2: Connect to your VM
- Use an SSH client (e.g., Terminal or PuTTY or Termius(for Mac)) and log in with the public IP address and your SSH key.

STEP 3: Set up a web server
- Update and install Nginx (sudo apt update
sudo apt install nginx -y)
- Start the server (sudo systemctl start nginx)

STEP 4: Upload your static website files
- Replace the default index.html with your static website’s index.html.

STEP 5: Open port for web traffic
- Allow HTTP/HTTPS Traffic:
In the Azure Portal, navigate to your VM.
Go to Networking > Inbound Port Rules > Add Rule. (Allow port 80 (HTTP))

STEP 6: Access the website
- Find your VM public IP in the Azure Portal under it's Overview tab.
- Open a browser and go to http://your-public-ip