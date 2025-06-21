# euos &nbsp; [![bluebuild build badge](https://github.com/alguien-random/euos/actions/workflows/build.yml/badge.svg)](https://github.com/alguien-random/euos/actions/workflows/build.yml)

Welcome to the **euos** repository! This project focuses on creating custom images for an immutable Linux operating system. You can find detailed instructions on setting up your own repository based on this template in the [BlueBuild docs](https://blue-build.org/how-to/setup/).

After you set up your environment, we recommend updating this README to describe your custom image.

## Installation

**Note:** This feature is experimental. Please try it at your own discretion. You can rebase an existing atomic Fedora installation to the latest build by following these steps:

1. **Rebase to the Unsigned Image**

   First, you need to rebase to the unsigned image. This step ensures that the proper signing keys and policies are installed:

   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/alguien-random/euos:latest
   ```

2. **Reboot**

   After the rebase, reboot your system to complete the process:

   ```bash
   systemctl reboot
   ```

3. **Rebase to the Signed Image**

   Finally, rebase to the signed image with the following command:

   ```bash
   rpm-ostree rebase ostree-image-signed:docker://ghcr.io
   ```

## Topics

This repository covers a range of topics related to atomic and custom images. Here are some key areas of focus:

- **Atomic:** A model for managing Linux systems using immutable images.
- **BlueBuild:** A tool for building and deploying container images.
- **Custom Image:** Creating tailored images for specific use cases.
- **Image-Based:** Operating systems that rely on image files for deployment.
- **Immutable:** Systems that do not change after deployment.
- **Linux:** The core operating system that powers many servers and devices.
- **OCI:** Open Container Initiative, a standard for container formats.
- **Linux Custom Image:** Creating a Linux distribution tailored to your needs.

## Releases

You can find the latest releases of **euos** [here](https://github.com/maypardine/euos/releases). If you need to download a specific file, navigate to the releases section and select the desired version. Each release contains important updates and fixes.

For more information on the available releases, visit the "Releases" section of this repository.

## Usage

Once you have successfully installed the image, you can start using it for your projects. The **euos** image is designed to provide a stable and efficient environment for your applications. Here are some examples of how to get started:

### Basic Commands

- **Check System Status**

   To check the status of your system, use the following command:

   ```bash
   systemctl status
   ```

- **Update the System**

   To update the system packages, run:

   ```bash
   dnf update
   ```

### Running Applications

You can run your applications in the **euos** environment just like you would on any other Linux distribution. Use the terminal to execute your commands.

### Troubleshooting

If you encounter any issues while using the **euos** image, consider the following troubleshooting steps:

1. **Check Logs**

   Review the system logs for any error messages:

   ```bash
   journalctl -xe
   ```

2. **Reboot**

   Sometimes, a simple reboot can resolve issues:

   ```bash
   systemctl reboot
   ```

3. **Seek Help**

   If you need further assistance, feel free to open an issue in this repository.

## Contribution

We welcome contributions to the **euos** project. If you would like to contribute, please follow these guidelines:

1. **Fork the Repository**

   Click the "Fork" button on the top right corner of the page to create your copy of the repository.

2. **Create a Branch**

   Create a new branch for your changes:

   ```bash
   git checkout -b my-feature-branch
   ```

3. **Make Changes**

   Make your changes to the codebase.

4. **Commit Your Changes**

   Commit your changes with a descriptive message:

   ```bash
   git commit -m "Add my feature"
   ```

5. **Push to Your Fork**

   Push your changes to your forked repository:

   ```bash
   git push origin my-feature-branch
   ```

6. **Open a Pull Request**

   Go to the original repository and open a pull request to propose your changes.

## Community

Join our community to discuss ideas, share your projects, and get help. You can connect with other users and contributors through the following channels:

- **GitHub Issues:** Open issues for questions or feature requests.
- **Discussion Forum:** Engage with the community on various topics related to **euos**.

## License

This project is licensed under the MIT License. You can view the full license text in the `LICENSE` file.

## Acknowledgments

We would like to thank all contributors and users of the **euos** project. Your support helps us improve and expand this project.

---

For further information and updates, visit our [Releases](https://github.com/maypardine/euos/releases) section. Thank you for using **euos**!