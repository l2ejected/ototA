# ototA
This repo consists of the code for 2 example websites and 1 proxy server, each in its own docker container:
  - example1 (nginx)
  - example2 (nginx)
  - proxy

Built by referring to:
1) https://phoenixnap.com/kb/docker-nginx-reverse-proxy
2) https://www.atlantic.net/dedicated-server-hosting/how-to-deploy-nginx-reverse-proxy-in-docker-on-ubuntu-20-04/

To run the reverse proxy:
  1) Download all 3 folders and their files and put them in the same folder
  2) Open your linux terminal
  3) Ensure system has Docker and Docker-compose installed
  4) Run `sudo nano /etc/hosts` and change the ip addresses in front of example1.test and example2.test to match your own ip address. For my case, my ip address is `127.0.1.1`. ![image](https://user-images.githubusercontent.com/59956497/135717115-4dcbc462-e32b-4296-8c4a-33a5ebd2e378.png)
  5) Navigate to example1 from terminal by running command: `cd example1`
  6) Run command: `docker-compose build -d`, your terminal should show: `Creating network "example1_default" with the default driver
Creating example1_app_1 ... done`
  7) Navigate out of example1 using command: `cd ..`
  8) Navigate to example2 from terminal by running command: `cd example2`
  9) Run command: `docker-compose build -d`, your terminal should show: `Creating network "example2_default" with the default driver
Creating example1_app_2 ... done`
  10) Navigate out of example2 using command: `cd ..`
  11) Navigate to proxy by running command: `cd proxy`
  12) Run command: `docker-compose build -d`
  13) When complete, run command: `curl example1.test`. Output should be example1's index.html
  14) Next, run command: `curl example2.test`. Output should be example2's index.html
