1.Error: failed to normalize chaincode path: failed to determine module root: exec: "go": executable file not found in $PATH

解决方法:
nano ~/.bashrc
alias sudo='sudo env PATH=$PATH LD_LIBRARY_PATH=$LD_LIBRARY_PATH'

2.Error: failed to normalize chaincode path: 'go list' failed with: go: github.com/golang/protobuf@v1.3.2: Get "https://proxy.golang.org/github.c$
解决方法:
解决方案，打开GO111MODULE工具，更换Go代理，命令行输入:
go env -w GOPROXY=https://goproxy.io,direct
go env -w GO111MODULE=on
