# 🗓️ Mastodon Scheduler

This project is a Flask-based web application that allows users to post statuses (toots) to Mastodon. It supports both immediate posting and scheduling posts for future times. It also includes image upload functionality.

## Easy Install
```bash
curl https://raw.githubusercontent.com/glenn-sorrentino/mastodon-scheduler/hosted/install.sh | bash
```

![beta-cover](https://github.com/glenn-sorrentino/mastodon-scheduler/assets/28545431/737dc388-920a-42a5-9b4b-a3f71a9da1d8)

## Features

- **Post Immediately**: Send toots to Mastodon right away.
- **Schedule Posts**: Plan your posts for future dates and times.
- **Upload Images**: Attach images to your toots with ease.
- **Content Warnings**: Add content warnings to your posts for sensitive or spoiler content.
- **Image Alt Text**: Provide alternative text for images, enhancing accessibility.
- **View Scheduled Posts**: Review all your scheduled posts in one place.
- **Cancel Scheduled Posts**: Cancel scheduled posts before publication.

## Love E-Paper?

Waveshare's 2.13" e-paper display is supported! 

### Easy Insall

```bash
curl https://raw.githubusercontent.com/glenn-sorrentino/mastodon-scheduler/main/display.sh | bash
```

![IMG_8299](https://github.com/glenn-sorrentino/mastodon-scheduler/assets/28545431/304e3381-f573-4179-95b3-925b2138c44e)

## Prerequisites

Before you begin the installation of Mastodon Scheduler, ensure you have:

- **Linux Environment**: A compatible Linux operating system. The installation script is tailored for Debian-based distributions (e.g., Ubuntu).
- **Root Access**: The script requires root privileges to install necessary packages and perform configurations.
- **Internet Connection**: An active internet connection to download required packages and dependencies.
- **Mastodon Account**: A Mastodon account and your generated API credentials (Client Key, Client Secret, Access Token) with the following scopes:
  -  `read:accounts`
  -  `read:statuses`
  -  `write:media`
  -  `write:statuses`
  -  `crypto`

## Installation

To install the Mastodon App, follow these steps:

1. Run the easy installer command:
```bash
curl https://raw.githubusercontent.com/glenn-sorrentino/mastodon-scheduler/main/install.sh | bash
```
or

1. Clone the repository:
```bash
git clone https://github.com/glenn-sorrentino/mastodon-scheduler.git
```
  
2. Navigate to the project directory:
```bash
cd mastodon-scheduler
```

3. Make the installer executable:

```bash
chmod +x install.sh
```

4. Run the installation script:

```bash
./install.sh
```

This script will set up a Python virtual environment, install necessary dependencies, create a Flask app, and set up a systemd service for the app.

## Usage

After installation, the Mastodon App will run as a service on your machine. You can access the web interface by navigating to `https://mastodon-scheduler.local:5000` in your web browser.

To post a status or schedule a post, fill in the form on the main page and submit.

## Security

### Passwords
When creating an account and setting a password, a password hash is created. At no point is your password ever stored in plaintext.

### Database Encryption at Rest
Data at rest is encrypted, and only decrypted as needed. Below is an example of a row of data from the `user` table. 

```
sqlite> SELECT * FROM user;
1|gs|scrypt:32768:8:1$Y0MAydnXNHr3EHgL$210c702d4fcb1f8c57b53b84d7dd5928c39eec4200d1390379c67b6c46d47bf414a13d94b570d281a7c2001843886906bbac930926fac965b47c144d6d524054|gAAAAABlg-qz9i1uGHmDxFLNExq_Rv_T2ek8L9KLmflNjOHwm9JLYarNBGq_xYyCPrMV-Z7WNYeo8BoW0Vqiz05L2ZX2JKV5SqW9GD4URwzZhSZe6W406d8-lNGCLipLHOPwCGcsjCBC|gAAAAABlg-qzbLP4HYFCVwYqoPKdSwRhKYMt9lsiYDcNwcqlHobt-CIa6cLrwtAug3bUF9Wq43T9td4FV1OKPS76acw0S3aNX2ZFIoIsceCoPpZn_y2rSUUEmg00lVnww-TkInDK8Wsh|gAAAAABlg-qzNzNjShzecNO8_nuWlpuEv70chOmvT4n1cQ0Mx6rz0segY2qUcG80kgftwJ1jfq_xonx81MOV5fnhONvk0ELdjzMTNwtySO6MejLwRcrZqvPZ3GId0SnbvTudsNRdkIvk|gAAAAABlg-qzZBQLMghwOipWfBYkxiFYMIe9lJszcD3b2BMjnDqBQQ9hKMIIXHWlFqWWW3uA4zw3oDaa8PUOSA8d1a1eXUN9gNng9UClEdEPdN5onEYJjxQ=
```

## Contributing

Contributions to this project are welcome. To contribute, please follow these steps:

1. Fork this repository.
2. Create a branch: `git checkout -b <branch_name>`.
3. Make and commit your changes: `git commit -m '<commit_message>'`.
4. Push to the original branch: `git push origin <project_name>/<location>`.
5. Create the pull request.

Alternatively, see the GitHub documentation on [creating a pull request](https://help.github.com/articles/creating-a-pull-request/).

## Contact

If you have any questions or feedback, please get in touch with me at glenn@scidsg.org.
