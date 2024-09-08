### Step-Guide to Using Git

This guide provides a simple and unique approach to getting started with Git, a version control system widely used for managing code changes.

### Step 1: Install Git

1. **Download Git**: Visit the official Git website and download the installer for your operating system (Windows, macOS, or Linux).
2. **Run the Installer**: Follow the prompts to install Git with default settings.

### Step 2: Configure Git

1. **Set Your Username**: Open your terminal or command prompt and run:
   ```bash
   git config --global user.name "Your Name"
   ```

2. **Set Your Email**: This email will be associated with your commits:
   ```bash
   git config --global user.email "you@example.com"
   ```

3. **Set Default Branch Name**: To configure the default branch name for new repositories:
   ```bash
   git config --global init.defaultBranch main
   ```

4. **Create a New SSH Key**: Run the following command inside your terminal:
   ```bash
   ssh-keygen -t ed25519
   ```
   When prompted for a location to save the generated key, just press Enter. You can enter a password if desired, but it's not required.

5. **Link Your SSH Key with GitHub**: 

   - Log into GitHub and click on your profile picture in the top right corner, then click on **Settings**.
   - On the left-hand side, click **SSH and GPG keys**. Click the green button that says **New SSH Key**.
   - Name your key descriptively (e.g., linux-ubuntu) and leave this window open while you do the next steps.
   - Copy your public SSH key using the following command:
     ```bash
     cat ~/.ssh/id_ed25519.pub
     ```
   - Highlight and copy the entire output. Go back to GitHub, paste the key into the key field, keep the key type as **Authentication Key**, and then click **Add SSH key**.

### Step 3: Create a New Repository

1. **Create a Directory**: Navigate to the folder where you want to create your project and run:
   ```bash
   mkdir git_test
   cd git_test
   ```

2. **Initialize Git**: Turn this directory into a Git repository:
   ```bash
   git init
   ```

### Step 4: Add Files

1. **Create a File**: Create a new file in your project directory, for example:
   ```bash
   echo "Hi" > README.md
   ```
   Alternatively, you can manually create this file using a code editor such as Visual Studio Code.

2. **Stage the File**: Add the file to the staging area:
   ```bash
   git add README.md
   ```

### Step 5: Commit Changes

1. **Commit the Staged Files**: Save your changes with a descriptive message:
   ```bash
   git commit -m "commit1"
   ```

### Step 6: Push Changes to Remote Repository

1. **Add Remote Repository**: If you have a remote repository (like on GitHub), link it:
   ```bash
   git remote add origin https://github.com/yourusername/git_test.git
   ```

2. **Push Your Changes**:
   ```bash
   git push -u origin main
   ```

### Step 7: View Your Commit History

1. **Check Commit History**: To see the history of your commits, use:
   ```bash
   git log
   ```

### Step 8: Celebrate Your Progress

You've successfully set up Git, created a repository, made changes, and pushed them to a remote server!
