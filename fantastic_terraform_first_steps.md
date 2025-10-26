"Fantastic" Terraform First Steps

-	Before you start any Terraform project, you must set up and initialize the application.

-	Please perform the following workflow to accomplish this task:

-	If this is your very first project in Terraform, please do the following:

		Launch a command line interface of your choice as administrator.  This can be within VS Code, Terminal, Git Bash, or PowerShell.
		
		Path to the location of the directory you want to create a project in.  For Class 7, this will be the Terraform directory located here: "C:\Users\<Your username here>\Documents\TheoWAF\class7\AWS\Terraform".
		
		Once there, run Aaron's Terraform verification script: "curl https://raw.githubusercontent.com/aaron-dm-mcdonald/Class7-notes/refs/heads/main/101825/check.sh | bash".
		
		Once the script is complete, the results will tell you if Terraform is configured correctly and a new file will be created in the Terraform directory called .gitignore.
	
-	In the command line, create a new directory for your new Terraform project using the following command: mkdir <Your directory name>.  I typically name the project after the date it was created (mkdir mm.dd.yy). You can name the directory whatever you want.

-	Copy the created .gitignore file to the project directory using the following command: "cp ./.gitignore ./<Your directory name>". 

-	Once the .gitignore file is copied to your project directory, you can now begin to create your Terraform project files. 

-	Launch VS Code and select File -> Open Folder.  Choose your project directory and click Open Folder.  

-	Launch your terminal by clicking Terminal -> New Terminal at the top of the VS Code window.  Ensure that the terminal has opened into your project directory.

-	Next, create the Terraform authentication file using the following command: "touch 0-auth.tf"

-	Launch your web browser and visit the Terraform Registry (https://registry.terraform.io/) and select Browse Providers.  Choose AWS.

-	In the AWS provider screen, click the Use Provider button in the upper right corner.

-	A smaller window should open below the Use Provider button.  Copy the code within this window.

-	Open your 0-auth.tf file in VS code and paste the AWS Provider code copied from the Terraform Registry.  Save the 0-auth.tf file.  

-	Once done, go back to your terminal and run the "terraform init" command.  This will initialize Terraform and copy the necessary files for use with the application.  If successful, this should generate a Terraform lock file within your project directory.

-	VERY IMPORTANT: Do not modify or delete the Terraform lock file.  It is vital for Terraform to function.  
-	Next, run the "terraform validate" command.  If no error message presents itself, then the command ran successfully.  

-	You will now run the "terraform plan" command.  You should see message stating how Terraform will update its files and what resources it will create once the plan is applied.  If no error message presents itself, then the command ran successfully.  

-	Finally, run the "terraform apply" command.  This will initiate the Terraform plan and create any resources you have requested.  If successful, this should generate a Terraform state file within your project directory.  

-	VERY IMPORTANT: Do not modify or delete the Terraform state file.  It is vital for Terraform to function.

-	If you have done the above steps correctly, Terraform is set up for use within this project folder.  You may now create additional Terraform files to create resources and perform various tasks within the AWS API.  

-	Also, the Terraform workflow of terraform validate -> terraform plan -> terraform apply -> terraform destroy should now function normally.  


