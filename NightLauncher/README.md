### **Step 1: Installing Visual Studio 2022 and Updating the Launcher**

1. **Installing Visual Studio 2022**  
   - Download and install Visual Studio 2022 with the `.NET Desktop Development` workload.

2. **Opening the Project**  
   - Extract the source code from the zip file.  
   - Open the **NightFamilyLauncherCore.sln** file located in the extracted folder with Visual Studio.

3. **Updating the Version Number**  
   - Locate the **App.xaml.cs** file in Visual Studio.  
   - Update the `Version` value inside the file (e.g., change `1.0` to `1.1`).

4. **Building and Running the Project**  
   - After making the changes, press **F5** to build and run the project.

5. **Packaging the Compiled Files**  
   - Navigate to the **NightFamilyLauncherCore** folder.  
   - Go to `/bin/Debug/net8.0-windows/` and select all the files inside.  
   - Create a `.zip` file containing all the selected files.  
   - **Important:** Ensure that all necessary files are included in the zip file.

6. **Updating the Launcher on GitHub**  
   - Provide your GitHub username, and after permissions are granted, follow these steps:  
     1. Go to **https://github.com/Hamzaless/Fiverr/tree/main/NightLauncher**.  
     2. Delete the existing `launcher.zip` file.  
     3. Use **Add file > Upload file** to upload your updated `launcher.zip`.  
     4. Edit the `properties.json` file and update the `launcher_version` field to the new version (e.g., change `1.0` to `1.1`).  

---

### **Step 2: Updating the Modpack**

1. **Downloading and Installing Git**  
   - Download and install Git using this link:  
     [Download Git (v2.47.1)](https://github.com/git-for-windows/git/releases/download/v2.47.1.windows.2/Git-2.47.1.2-64-bit.exe)

2. **Creating the Working Folder**  
   - Create a new folder named **Fiverr** on your desktop.  
   - Open the **Command Prompt (CMD)** and navigate to this folder:  
     ```cmd
     cd "C:\Users\<your_username>\Desktop\Fiverr"
     ```

3. **Setting Up the Git Repository**  

   **Step 1: Initialize the Repository and Add Remote**  
   ```cmd
   git init
   git remote add origin https://github.com/Hamzaless/Fiverr.git
   git lfs install
   ```

   **Step 2: Track the Required Files**  
   ```cmd
   git lfs track "packed_minecraft.zip"
   git add .gitattributes packed_minecraft.zip
   ```
   packet_minecraft.zip should contain the following folders: config, libraries, mods, versions

   **Step 3: Commit the Changes**  
   ```cmd
   git commit -m "Modpack update"
   ```

   **Step 4: Push the Changes to the Remote Repository**  
   ```cmd
   git branch -M main
   git push --set-upstream origin main
   ```

4. **Handling Errors**  
   If you encounter the error:  
   - **"Updates were rejected because the remote contains work that you do not have locally"**  
     - Pull the changes from the remote repository first:  
       ```cmd
       git pull origin main --rebase
       ```

   - If there are conflicts, resolve them manually and follow these steps:  
     ```cmd
     git add <conflicted_file>
     git rebase --continue
     ```

   - Once resolved, push the changes again:  
     ```cmd
     git push origin main
     ```

5. **Uploading the Updated Modpack**  
   - Upload the updated `.zip` file for the modpack to the remote repository using the above steps.  
   - The new modpack will then be available for all users.

---

### **Important Notes**
- Always update the launcher when you update the modpack.  
- Follow each step carefully to ensure the process completes successfully.  
- If any issues arise, double-check the steps or contact me for assistance.
