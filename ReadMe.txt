

STEPS:

    Install Hyperledger Fabric pre-requisites including Unbuntu Virtual Machine where the Hyperledger Fabric needs to run.

    Open the Virtual machine then, download and install Go language from https://golang.org/dl/ link that matches up to your operating system.

    Go to the directory where the file located, right click to open the terminal.

    Type in "tar -C /usr/local -xzf go1.11.5.linux-amd64.tar.gz"

    To add Go environment variable, type in • export PATH=$PATH:/usr/local/go/bin • export GOPATH=$HOME/go • export PATH=$PATH:$GOPATH/bin

    After that, we need to clone the fabric-sample project that IBM provided. Clone it by typing “git clone https://github.com/hyperledger/fabric-samples.git” to your terminal. Open the file using “cd fabric-sample”

    Afterwards, download the image and binaries by typing in “curl -sSL http://bit.ly/2ysbOFE | bash -s -- 1.4.0" in the terminal.

    Go back to the default path using “cd ..” then clone the repository "git clone https://github.com/khrandm/blockchain-training-labs" then go to the fabric-sample folder usibg “cd fablic-sample”

    Copy the chaincode and supply from the last cloned project and paste it inside fabric-sample, then merge the file if it lready exists. Open the supply folder, type “cd supply” in the terminal.

    Download the required library for chaincode. Type the following in the terminal. • go get github.com/golang/protobuf/proto • go get github.com/hyperledger/fabric/common/attrmgr • go get github.com/pkg/errors • go get github.com/hyperledger/fabric/core/chaincode/lib/cid

    now open file manager go to Home/go/src/github.com

    copy three folders: hyperledger, pkg, golang then paste it inside fabric-sample/chaincode

    Go to fabric-sample/supply and type the following: • Type ./startFabric.sh • Type npm install • Type node enrollAdmin.sh • Type node registerSupplier.sh • Type node registerOem.sh • Type node registerBank.sh • Type node app

    To check if its running, open the postman application, change the method from GET to POST then add url “localhost:3000/invoice”

    below url you should see Params Authroization Headers Body then click Headers

    Add another key below Content-Type

    type user

    and the value would be "supplier"

    next open the body tab

    click the x-www-form-url-encoded

    You should see a form there then type the following below then hit send. You should see result: Success KEY VALUE

invoicenumber INVOICE001 billedto OEM invoicedate 02/08/19 invoiceamount 10000 itemdescription KEYBOARD goodreceived False ispaid False paidamount 0 repaid False repaymentamount 0

