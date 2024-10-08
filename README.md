# Step-Wise Guide for Git

## Step 1: Install Git

1. **Download Git**: Visit the [official Git website](https://git-scm.com/) and download the installer for your operating system (Windows, macOS, or Linux).
2. **Run the Installer**: Follow the prompts to install Git with default settings.

## Step 2: Configure Git

1. **Set Your Username**: Open your terminal or command prompt and run:
   ```bash
   git config --global user.name "Your Name"
   ```

2. **Set Your Email**: This email will be associated with your commits:
   ```bash
   git config --global user.email "you@example.com"
   ```

3. **Generate SSH Key**:
   ```bash
   ssh-keygen -t ed25519 -C "you@example.com"
   ```

4. **Link Your SSH Key with GitHub**:
   - Log into GitHub and click on your profile picture in the top right corner.
   - Click on **Settings** in the drop-down menu.
   - Click on **SSH and GPG keys** on the left-hand side.
   - Click the **New SSH Key** button.
   - Name your key (e.g., "linux-ubuntu").
   - Copy the public SSH key using:
     ```bash
     cat ~/.ssh/id_ed25519.pub
     ```
   - Paste the key into the GitHub key field and click **Add SSH key**.

5. **Test Your SSH Connection**: Follow GitHub's directions for testing your SSH connection. Verify the fingerprint output matches one of GitHub's public fingerprints.

## Step 3: Create a New Repository

1. **Create a Directory**: Navigate to the folder where you want to create your project and run:
   ```bash
   mkdir my_project
   cd my_project
   ```

2. **Initialize Git**: Turn this directory into a Git repository:
   ```bash
   git init
   ```

## Step 4: Add Files

1. **Create a File**: Create a new file in your project directory, for example:
   ```bash
   echo "Hello" > README.md
   ```

2. **Stage the File**: Add the file to the staging area:
   ```bash
   git add README.md
   ```

## Step 5: Commit Changes

**Commit the Staged Files**: Save your changes with a message:
   ```bash
   git commit -m "commit1"
   ```

## Step 6: Make Changes and Commit

1. **Edit Your File**: Modify `README.md` or create new files as needed.

2. **Stage and Commit**: After making changes, repeat the staging and committing process:
   ```bash
   git add README.md
   git commit -m "commit2"
   ```

## Step 7: Push Changes to Remote Repository

**Push Your Changes**:
   ```bash
   git push -u origin main
   ```

## Step 8: View Your Commit History

**Check Commit History**: Check the history of your commits by using:
   ```bash
   git log
   ```

## You are Set!

You've successfully set up Git.
