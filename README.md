## Setup
https://github.com/settings/apps
echo "# hack" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/SrinathShil/hack.git
git push -u origin main

> **Google Cloud**
1.In Terraform to manage and create resources we  Create a Service Account in [Google Cloud Console] (https://console.cloud.google.com/) 
Name:- terraform-hack
![ScreenShot](img/img1.jpg)

2. Assign role roles/storage.admin to service account from cloud storage
<html>
<br/>
<img src="img/img2.jpg">
<br/>
</html>


3. Create a key and download the key locally
<html>
<br/>
<img src="img/img3.jpg">
<br/>
</html>

> **GitHub**
1.Create a repo in your own GitHub account with private

2. Create  a providers.tf on the folder and past provider from this url https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/getting_started
<html>
<br/>
<img src="img/img3.1.jpg">
<br/>
</html>
<html>
<br/>
<img src="img/img4.jpg">
<br/>
</html>

3. Create main.tf and past below
https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/storage_bucket#example-usage---life-cycle-settings-for-storage-bucket-objects
<html>
<br/>
<img src="img/img5.jpg">
<br/>
</html>

4. change name to name          = "terraform-hack-bucket"

5. commit and push
 
> **Terraform Cloud**
1. Create a free account in (https://app.terraform.io/)
<html>
<br/>
<img src="img/img6.jpg">
<br/>
</html>
2. Create a new Organization and Workspace
3. Choose a Version control workflow with the GitHub repository
<html>
<br/>
<img src="img/img6.jpg">
<br/>
</html>

4. Create a configure variable with name GOOGLE_CREDENTIALS
<html>
<br/>
<img src="img/img7.jpg">
<br/>
</html>
<html>
<br/>
<img src="img/img8.jpg">
<br/>
</html>
<html>
<br/>
<img src="img/img9.jpg">
<br/>
</html>
Create an environment variable called GOOGLE_CREDENTIALS in your Terraform Cloud workspace.
Remove the newline characters from your JSON key file and then paste the credentials into the environment variable value field.
Mark the variable as Sensitive and click Save variable.
 https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/getting_started#using-terraform-cloud-as-the-backend) with the Service Account JSON file 

5. Now run the pipeline

<html>
<br/>
<img src="img/img10.jpg">
<br/>
</html>


> **API token on Terraform and Hithub action**


<html>
<br/>
<img src="img/image11.jpg">
<br/>
</html>