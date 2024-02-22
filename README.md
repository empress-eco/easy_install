<div align="center">
  <a href="https://github.com/empress-eco/easy_install">
    <img src="https://grow.empress.eco/uploads/default/original/2X/1/1f1e1044d3864269d2a613577edb9763890422ab.png" alt="Logo" width="80" height="80">
  </a>

<h2 align="center">Easy Install: Your One-Stop Empress Setup Solution</h2>

<p align="center">
  Streamline your Empress site setup with our all-in-one automated script.
  <br />
  <a href="https://empress.eco/"><strong>Explore the Documentation »</strong></a>
  <br />
  <br />
  <a href="https://github.com/empress-eco/easy_install/issues">Report Bug</a>
  ·
  <a href="https://github.com/empress-eco/easy_install/issues">Request Feature</a>
</p>
</div>

## About Easy Install

Easy Install is a comprehensive script designed to simplify the setup process of an Empress site for developers, system administrators, and others. It automates the process of installing multiple dependencies and configurations, making Empress setup a breeze.

### Key Features

- Automated installation of all prerequisites and the command line `bench`.
- Creation of a new bench and an Empress site on the bench.
- Efficient password management for Administrator and MariaDB.
- Provision of a log file for troubleshooting installation issues.

## Technical Stack and Setup Instructions

Easy Install is built on Python, leveraging the power of automation to streamline the setup of your Empress site.

### Prerequisites

A fresh server with a dedicated user for Empress equipped with sudo privileges.

### Installation

Clone the project using the following command: 
```sh
git clone https://github.com/empress-eco/easy_install.git
```

Follow the step-by-step guide below to set up your development environment:

```sh
# Setup user & Download the install script
adduser [Empress-user]
usermod -aG sudo [Empress-user]

# Switch to Empress-user and start setup
su [Empress-user]
wget https://raw.githubusercontent.com/Empress/bench/develop/install.py

# Run the install script
sudo python3 install.py

# For production or development, append the --production or --develop flag respectively.
sudo python3 install.py --production --user [Empress-user]
sudo python3 install.py --develop
sudo python3 install.py --develop --user [Empress-user]
sudo python3 install.py --production --user [Empress-user] --container
```

## Usage

After installation, navigate to your bench folder and start Empress. For development, use `bench start`. For production, `nginx` and `supervisor` will manage your process.

## Contributing

We welcome your contributions! Here's how you can contribute:

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License and Acknowledgements

### License

This project is under the MIT License. Your contributions are also licensed under the MIT License. 

### Acknowledgements

We extend our heartfelt thanks to the Empress Community, the driving force behind the essential tools that power this project. Their dedication and innovative spirit have been pivotal in developing the foundations and functionalities we rely on. We are profoundly grateful for their pioneering work and ongoing support.
