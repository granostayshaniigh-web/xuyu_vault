- rpm = Red Hat Package Manager（红帽包管理器，现统称 RPM Package Manager），是 Red Hat 系发行版（RHEL / CentOS / Fedora 等）用来安装、卸载、查询、校验 .rpm 软件包（ 二进制软件包（已编译好，可直接装）。与之相对的是源码包.tar.gz，需自己 `./configure && make && make install 编译`）的底层工具。
	最常用的安装组合：`rpm -ivh xxx.rpm`
		-i install：安装。-v verbose：显示详细信息。-h hash：用 # 号打印进度条（看着舒服，确认没卡死）。
	最常用的升级组合：`rpm -Fvh newpkg-2.0.rpm`
		-F（freshen）	有旧版→升级；没装过→什么都不做
	最常用的卸载组合：`rpm -e 包名   # 注意：这里写"包名"，不是 xxx.rpm 文件名！`
		安装时给的是文件：`rpm -ivh httpd-2.4.6.rpm`
		卸载时给的是包名：`rpm -e httpd（不带版本号、不带 .rpm）`
	最常用的卸载组合：`rpm -qa包名`列出所有已安装包
	               `rpm -ql 包名`列出该包**安装了哪些文件**（l=list）
	               经典组合：`rpm -qa | grep 关键字`

| 选项           | 含义             |
| ------------ | -------------- |
| `rpm -i`     | install，**安装** |
| **`rpm -e`** | **erase，卸载**   |
| `rpm -q`     | query，**查询**   |
| `rpm -V`     | verify，**校验**  |

**记忆口诀**：**"i 装、e 卸、q 查、V 验"**——考试反复考 `-e` 是卸载，务必条件反射。

| 命令                   | 含义                        |
| -------------------- | ------------------------- |
| ==**`rpm -ql 包名`**== | 列出该包**安装的所有文件**（l = list） |
| ==**`rpm -qa`**==    | 列出**所有**已安装的包（a = all）    |
| `rpm -qi 包名`         | 查看包的**详细信息**（i = info）    |
| `rpm -qf 文件`         | 查看某文件**属于哪个包**（f = file）  |
| `rpm -qc 包名`         | 只列该包的**配置文件**（c = config） |

**辨析要点（◆ 易错）**：
- **`-ql`（list）**：文件夹→ 文件（"这个文件夹装了哪些文件？"）
- **`-qf`（file）**：文件 → 文件夹（"这个文件属于哪个文件夹？"）
- 二者**方向相反**，考试爱用 `-qf` 做干扰项。
