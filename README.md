# muta
Pi private cloud projekt

Plan:
- Objective: Private cloud storage with access from the internet
- Why important: Security, Scalability, Costs, cross-platform
- Milestones: storage solution for multiple devices via
  1. terminal
  2. GUI
  3. Website
- Biggest obstacles: static IP-Address only with paid providers
- Personal interest: Aquire knowledge in: networking, file-system
- How much time: 2 hours per week.

Steps:

1. Install rasp. OS on SD-Card. (SD card adapter required)
2. Enable SSH connection via shell
3. (from here localhost-network has access to PI, mouse, keyboard & screen not required anymore)
  - Check ip address: ifconfig
  - Connect from other device: `$ ssh <username>@<ip-address>` (password and user from OS installation)

### Access from internet (outside localhost)

only temporary solution: ngrok generate new address every time it is restarted.

Install ngrok (to expose PI port to internet)
  - Upgrade apt (package manager): `$ sudo apt upgrade`
  - Install snap-store (other package manager): `$ sudo apt install snapd`
  - Install ngrok: `$ sudo snap install ngrok` (follow ngrok website installation)
  - Expose port port to internet: `$ ngrok tcp <PORT>` (e.g. port 22)
  - Copy address from blue box shown in picture below:
    ![image](https://user-images.githubusercontent.com/50245942/164467902-21f77ce8-7265-4d1d-9384-e1f633a045e9.png)

  - Connect from outside localhost: `$ ssh <username>@0.tcp.ngrok.io -p <PORT>` (<Use

                                                                                      
