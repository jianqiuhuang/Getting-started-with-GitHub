## Getting-started-with-GitHub


# To create a personal access token, follow these steps:

On any GitHub page, click your profile icon and then click Settings.

On the sidebar, click Personal access tokens.

Click Generate new token.

Add a token description and click Generate token.

Copy the token to a secure location or password management app.

Note: For security reasons, after you leave the page, you can no longer see the token again.

Use your personal access token instead of a password for command line access over HTTPS.

# To create an SSH key, follow these steps:

Open Git Bash (Windows) or a new Terminal window (Linux and Mac).

Paste the following text, substituting the email address that you added to your GitHub Enterprise account:

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

Creates a new ssh key, using the provided email as a label

Generating public/private rsa key pair.

When you are prompted to specify a file to save the key in, press Enter to accept the default location.


At the prompt, type a secure passphrase. For more information, see Working with SSH key passphrases External link icon.

Add your SSH key to the ssh-agent:


Make sure that ssh-agent is enabled. By using Git Bash, enter this command to enable the ssh-agent:


start the ssh-agent in the background

`$ eval "$(ssh-agent -s)"
Agent pid 59566`

Add your SSH key to the ssh-agent by entering this command:


`$ ssh-add ~/.ssh/id_rsa`

Add the SSH key to your GitHub account. For more information, see Adding a new SSH key to your GitHub account External link icon.
