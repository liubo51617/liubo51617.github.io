mac本机最早是brew install的go 1.12版本,由于开发需求，需要升级到1.14版本，但是brew的官方更新实在太慢了，等不及，手动升级到1.14版本。

1.从官网下载


2.下载完成后，直接安装，默认的安装路径在 /usr/local/go 目录下

3.修改硬链接文件

which go

/usr/local/bin/go

cd /usr/local/bin

ll go*

rm go

sudo ln -s /usr/local/go/bin/go go

rm gofmt

sudo ln -s /usr/local/go/bin/gofmt gofmt

如果有其他文件，参照上面的方式修改

go version

go version go1.14.1 darwin/amd64

4.转到用户主目录 cd ~ ，修改环境变量 .bash_profile

exportGOROOT=“/usr/local/go”

source.bash_profile  重新加载环境变量使修改生效

5.删除旧版本编译生成的文件

rm -rf $GOPATH/pkg
