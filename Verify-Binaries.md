Verify Binaries

Bookmark Link: 
    
    https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/


Points:

1. Download the checksum for kubectl. Provide the client version number from the pervious command (including the v ):
            
        curl -LO "https://dl.k8s.io/<kubectl client version>/bin/linux/amd64/kubectl.sha256"
2. Verify the kubectl binary using the checksum:
        
        echo $(<binary.sha256>) <binarylocation> | sha256sum --check 


Result should be OK to pass. 