# Bombardier with proxy
Adopted from [bombardier@78-add-proxy-support](https://github.com/mariotrucco/bombardier@78-add-proxy-support)

## Installation
```shell script
mkdir bombardier_tmp
cd bombardier_tmp
go mod init bombardier_tmp
go mod edit -replace github.com/codesenberg/bombardier=github.com/PXEiYyMH8F/bombardier@78-add-proxy-support
go get github.com/codesenberg/bombardier
cd ..
rm -r bombardier_tmp
```
