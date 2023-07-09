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
<html>
<img src="https://user-images.githubusercontent.com/16732195/252139532-03915f70-0927-4e94-844f-7773b986db34.JPG">
<br/>
</html>
2. Assign role roles/storage.admin to service account from cloud storage
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139678-1db4419d-572e-4800-bc68-758be2b3596d.JPG">
<br/>
</html>


3. Create a key and download the key locally
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139724-a7b0f55e-a0ef-43c0-9dbd-137515b14957.JPG">
<br/>
</html>

> **GitHub**
1.Create a repo in your own GitHub account with private

2. Create  a providers.tf on the folder and past provider from this url https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/getting_started
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139763-0d9b6853-dcb4-4009-bdae-bde5a21b85d5.JPG">
<br/>
</html>
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139774-1ec77540-29a6-43c8-aa95-b1ce4962c697.JPG">
<br/>
</html>

3. Create main.tf and past below
https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/storage_bucket#example-usage---life-cycle-settings-for-storage-bucket-objects
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139808-96f1286a-6271-436d-883b-cdca7c1eaf01.JPG">
<br/>
</html>

4. change name to name          = "terraform-hack-bucket"

5. commit and push
 
> **Terraform Cloud**
1. Create a free account in (https://app.terraform.io/)
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139814-0d63e80a-ec27-4f99-bed5-ca7c5bbc35ca.JPG">
<br/>
</html>
2. Create a new Organization and Workspace
3. Choose a Version control workflow with the GitHub repository
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139833-1a9c441c-aaab-4294-a57f-790248b05e4f.JPG">
<br/>
</html>

4. Create a configure variable with name GOOGLE_CREDENTIALS
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139825-0a57439c-94f8-4e17-b422-341c9f319ec2.JPG">
<br/>
</html>
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139833-1a9c441c-aaab-4294-a57f-790248b05e4f.JPG">
<br/>
</html>
<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139818-03e09251-af57-4743-bd34-0d0c7540a12d.JPG">
<br/>
</html>
Create an environment variable called GOOGLE_CREDENTIALS in your Terraform Cloud workspace.
Remove the newline characters from your JSON key file and then paste the credentials into the environment variable value field.
Mark the variable as Sensitive and click Save variable.
 https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/getting_started#using-terraform-cloud-as-the-backend) with the Service Account JSON file 

5. Now run the pipeline

<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139836-4fbc9151-c637-4235-9ebc-a2e16cb43979.JPG">
<br/>
</html>


> **API token on Terraform and Hithub action**


<html>
<br/>
<img src="https://user-images.githubusercontent.com/16732195/252139841-e34df147-ee3e-4066-93b7-1b06bee5e3ed.JPG">
<br/>
</html>