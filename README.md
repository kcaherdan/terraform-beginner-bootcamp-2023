# Terraform Beginner Bootcamp 2023

## Semantic Versioning :mage:

This is going to utilize semamtic versioning for its tagging.
[semver.org](https://semver.org/)

The general format:

 **MAJOR.MINOR.PATCH**, eg. `1.0.1`

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes

## Install the Terraform CLI

The Terraform CLI installation instruction have changed due to gpg keyring changes. So we need to referr to the latest install CLI instructions via Terraform Documantation and change the scriptiing for install.

[Install Terraform CLI]
(https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

### Consideration for Linuc Distribution

This project is built against linux distribution.
Please consider checking your linus distribution and change accordingly.
[How to check Os version ](https://www.cyberciti.biz/faq/how-to-check-os-version-in-linux-command-line/)

Example of command result
```
$ cat /etc/os-release
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.3 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=jammy```


### Refactoring into Bash Scripts

While fixing the Terraform CLI gpg depreciation issues we noticed that the bash scripts steps were considerable amount more code. So we decide to create a bash script to install the Terraform CLI

This bash script is located here: [./bin/install_terraform_cli](./bin/install_terraform_cli)

- This will keep Gitpos Task File ([.gitpod.yml](.gitpod.yml)) tidy.
- This will allow us an easier to debug and execute manually Terraform CLI install
- This will allow better portability for other projects that need to install Terraform CLI


### Shebang #! Considerations

https://en.wikipedia.org/wiki/Shebang_(Unix)

### Linux Considerations

https://linuxize.com/post/chmod-command-in-linux/

### Linux Permission Considerations

https://en.wikipedia.org/wiki/Chmod


### Gitpod LifecycleConsiderations

https://www.gitpod.io/docs/configure/workspaces/tasks
