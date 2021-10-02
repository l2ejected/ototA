# ototA
This repo consists of 2 example websites and 1 proxy server:
  - example1 (nginx)
  - example2 (nginx)
  - proxy

To run docker containers:
  1) Download all 3 folders and their files and put them in the same folder
  2) Run terminal
  3) Ensure system has Docker and Docker-compose installed
  4) Navigate to example1 from terminal by running command: "`cd example1`" 
  5) Run command: "`docker-compose build -d`", your terminal should show: "Creating network "example1_default" with the default driver
Creating example1_app_1 ... done"
  6) Navigate out of example1 using command: "`cd ..`"
  7) Navigate to example2 from terminal by running command: "`cd example2`"
  8) Run command: "`docker-compose build -d`", your terminal should show: "Creating network "example2_default" with the default driver
Creating example1_app_2 ... done"
  9) Navigate out of example2 using command: "`cd ..`"
  10) Navigate to proxy by running command: "`cd proxy`"
  11) Run command: "`docker-compose build -d`"
  12) When complete, run command: "curl example1.test". Output should be example1's index.html
  13) Next, run command: "`curl example2.test`". Output should be example2's index.html
