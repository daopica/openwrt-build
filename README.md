**使用github的Actions来编译openwrt固件,替代使用服务器来编译**

Fork到自己的储存库内点Actions，选择"编译openwrt",点击"Run workflow"，看到SSH connection to Actions输入框输入"true"然后点击Run workflow

再次点击"编译openwrt"中间出现workflow runs，选择中间的"编译openwrt",点build,等待任务进行到"Use tmate connect ssh"

看到```Web shell: https://tmate.io/t/xxx```点击访问，然后快捷键```ctrl+c```进入ssh

然后输入命令``` make menuconfig ```即可配置openwrt，配置完成后输入命令exit退出ssh，github actions会自动运行后面的编译任务
