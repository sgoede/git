# Git Tutorials Repository

Welcome to the Git Tutorials Repository!

This repository contains various Git tutorials following the [GitHub Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf). The cheatsheet is available in PDF format at the root of this repository if you have it open in Visual Studio Code (VSCode).

## Table of Contents

1. **Introduction to Git**
   - What is Git?
   - Setting up Git
   - Basic Commands

2. **Branching and Merging**
   - Creating branches
   - Switching branches
   - Merging branches

3. **Staging and Committing**
   - Staging files
   - Committing changes
   - Viewing commit history

4. **Remote Repositories**
   - Cloning repositories
   - Fetching updates
   - Pushing changes

5. **Collaboration**
   - Pull requests
   - Forking repositories
   - Contributing to open source projects

## Getting Started

1. **Clone the Repository**
   To get started, clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-username/git-tutorials.git
   cd git-tutorials
   ```

2. **Open in VSCode**
   Open the cloned repository in Visual Studio Code:
   ```bash
   code .
   ```

3. **View the Cheatsheet**
   If you have the cheatsheet open in VSCode, you can view it directly from the Explorer pane.

## SSH Key Setup (Optional but Recommended)

If you encounter permission issues when trying to push changes, consider setting up SSH keys for secure authentication with GitHub.

1. **Generate an SSH Key**
   Open a terminal and run:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   Replace `"your_email@example.com"` with your actual email address.

2. **Add the SSH Key to the ssh-agent**
   Start the ssh-agent in the background:
   ```bash
   eval "$(ssh-agent -s)"
   ```
   Add your SSH private key to the ssh-agent:
   ```bash
   ssh-add ~/.ssh/id_rsa
   ```

3. **Add the SSH Key to Your GitHub Account**
   1. Open a web browser and log into your GitHub account.
   2. Go to `Settings` (gear icon) -> `SSH and GPG keys`.
   3. Click on the `New SSH key` button.
   4. Paste the contents of your public key file (`~/.ssh/id_rsa.pub`) by running:
      ```bash
      xclip -selection clipboard < ~/.ssh/id_rsa.pub
      ```
   5. Paste the copied text into the `Key` field on GitHub.
   6. Add a descriptive title for your key (e.g., "My Laptop") and click `Add SSH key`.

4. **Test Your SSH Connection**
   Run:
   ```bash
   ssh -T git@github.com
   ```
   If everything is configured correctly, you should see a message like:
   ```
   Hi username! You've successfully authenticated, but GitHub does not provide shell access.
   ```

5. **Update Your Remote URL**
   Update your remote URL to use SSH instead of HTTPS:
   ```bash
   git remote set-url origin git@github.com:your-username/git-tutorials.git
   ```

## Contributing

Contributions are welcome! Feel free to suggest new tutorials or improvements to existing ones. To contribute:

1. Fork this repository.
2. Create a new branch for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes and commit them:
   ```bash
   git add .
   git commit -m "Your descriptive commit message"
   ```
4. Push to the forked repository:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a Pull Request (PR) to merge your changes into the main branch.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```

Make sure to replace `your_username` and `git-tutorials.git` with your actual GitHub username and repository name in the remote URL update step. Save this updated README.md in your repository and commit it:

```bash
git add README.md
git commit -m "Update README.md with correct link to GitHub Cheatsheet PDF"
git push origin main