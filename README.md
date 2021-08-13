# the-art-bash-command-line

- `du -hs *`   显示总和且易读
- `diff file1 file2`   比较文件
- `find . -iname '*t*'`   当前目录查找文件
- `grep . *` 或 `head -100 * ` 检查当前目录下所有文件内容
- 区别`<` `>` 重定向输入和输出
  `cat` 表示从屏幕获取输入并输出
  `<< eof` 表示遇到eof结束输入。了解`stdout`和`stderr`。
- 了解inode(与`ls -i`和 `df -i`相关), `ls -i`表示列出文件节点号(每1个文件占用1个inode), `df -i`列出inode总数和可用inode数
- 理解`ln`和`ln -s`(硬链接和软连接)区别,硬链接指向同一inode不占用磁盘空间;软件会创建一个新inode;另外,硬链接只能作用于文件,不能是目录。
## 日常使用
- `ctrl-r`(搜索命令历史记录,输入关键字搜索回车执行匹配命令), `ctrl-l`清屏
- `xargs`捕获输出作为另一命令的参数,如 find . -name *.log | xargs ls -l
- 使用 pgrep 和 pkill 根据名字查找进程或发送信号（-f 参数通常有用）
- Bash脚本中,`set -x`调试输出;`set -e`发生错误就退出 
