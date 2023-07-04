Click on Settings > Actions > Runner > New Self Hosted Runner

Select OS type - Linux

Follow the steps:

# Create a folder
$ mkdir actions-runner && cd actions-runner

# Download the latest runner package
$ curl -o actions-runner-linux-x64-2.305.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.305.0/actions-runner-linux-x64-2.305.0.tar.gz

# Optional: Validate the hash
$ echo "737bdcef6287a11672d6a5a752d70a7c96b4934de512b7eb283be6f51a563f2f  actions-runner-linux-x64-2.305.0.tar.gz" | shasum -a 256 -c

# Extract the installer
$ tar xzf ./actions-runner-linux-x64-2.305.0.tar.gz

# Create the runner and start the configuration experience
$ ./config.sh --url https://github.com/joyienjoy/react-shopcart --token AV6RLKA6YOEYTUVE75WN2JLEUQGGG# 

#Last step, run it

$ sudo ./svc.sh install
$ sudo ./svc.sh stop
$ sudo ./svc.sh start
