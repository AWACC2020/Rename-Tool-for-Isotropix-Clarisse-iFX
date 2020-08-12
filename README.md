# Rename tool for Isotropix Clarisse IFX
# 此为适用于isotropix Clarisse iFX的重命名工具

作者:AWACS
时间:2019.11.16

### 软件版本：
- 目前在isotropix Clarisse iFX 4.0 上使用过,更老的版本多半也可以用(因为应该没什么特别的命令)，虽然我还没试过

### 免责说明:
- 此为业余的CG爱好者(同为业余的python新手)写的脚本,
- 难免会出虫,请注意保护好自己的工程文件,多做备份,
- 丢人作者并没有能力承担可能造成的损失(x
- (虽然这种事情我也不怎么懂啊大概就这样吧。。。)

### 如何安装：
- 1.在shelf上右键空白位置,点击"add item",
- 2.可选操作：
	在Title后可添加自定义名称,
	Description后可添加工具描述,
	Category后可指定你要放shelf的哪个tab里

- 3.在Script Path后面找到添加到你要添加的脚本的路径

- 4.点Add添加,完成(还可以自定义图标之类的)

### 文件说明：
- 4个文件分别为：
- RENAMER_beta_0.76.py	（英文版）
- RENAMER_beta_0.76_CH.py	（中文版）
- RENAMER_OCD_beta_0.76.py	（英文版+强迫症）
- RENAMER_OCD_beta_0.76_CH.py	（中文版+强迫症）

--------------------------------------------------------------------------------------


### 使用说明(英文版的)：

- 在BROWSER窗口里选中物体后即可进行重命名,基本类似maya的自带重命名工具的操作,很简单的,介绍可以爱看不看(

- "Including Selected Hierarchy" 勾选后,即可对所选的对象中文件夹里面的东西也进行重命名

- 1.搜索和替换

- 先在"Search for"填入搜索的内容,再在"Replace With"填入替换的内容,点击"Search & Replace"即可进行搜索和替换的操作

- 2.添加前缀,添加后缀

- 在"Prefix"填入要添加的前缀,点击"Add Prefix"即可进行添加前缀的操作
- 在"Suffix"填入要添加的后缀,点击"Add Suffix"即可进行添加后缀的操作

- 接下来是个人用的强迫症版里面加的两个功能：

- 3.重命名文件读取类物体

- 就是重命名那几个读取模型,贴图等东西的节点,自动将其命名为读取了的文件的文件名称,
- 目前只对这4个节点有效：
- GeometryPolyfile（常用的模型读取的节点）
- TextureMapFile（常用的贴图读取的节点）
- GeometryVolumeFile（常用的VDB读取的节点）
- GeometryBundleAlembic（常用的读取单独ABC文件的节点）

- 两个勾选框：
- "File Suffix"： 可选择是否加上读取了的文件的后缀名
- "Object Type Suffix": 可选择是否加上读取了的文件的节点的类型名称,此名称可在源码的最前面那地方改

点击"Rename Filereader Object"可进行自动重新命名

### 4.重命名Combiner和Group

- 就是Combiner和Group这两个节点重命名,将其名称自动改为其参考的对象中的第一个物体的名称
- 勾选框"Object Type Suffix" : 可选择是否加上"Combiner"或"Group"的后缀名

- 点击"Rename Combiner/Group"可进行自动重新命名

--------------------------------------------------------------------------------------

### 使用说明(中文版的)：

- 在BROWSER窗口里选中物体后即可进行重命名,基本类似maya的自带重命名工具的操作,很简单的,介绍可以爱看不看(

- "包括所选的子级对象" 勾选后,即可对所选的对象中文件夹里面的东西也进行重命名

- 1.搜索和替换

- 先在"搜索文字"填入搜索的内容,再在"替换为"填入替换的内容,点击"搜索并替换"即可进行搜索和替换的操作

- 2.添加前缀,添加后缀

- 在"前缀"填入要添加的前缀,点击"添加前缀"即可进行添加前缀的操作
- 在"后缀"填入要添加的后缀,点击"添加后缀"即可进行添加后缀的操作

- 接下来是个人用的强迫症版里面加的两个功能：

- 3.重命名文件读取类物体

- 就是重命名那几个读取模型,贴图等东西的节点,自动将其命名为读取了的文件的文件名称,
- 目前只对这4个节点有效：
- GeometryPolyfile（常用的模型读取的节点）
- TextureMapFile（常用的贴图读取的节点）
- GeometryVolumeFile（常用的VDB读取的节点）
- GeometryBundleAlembic（常用的读取单独ABC文件的节点）

- 两个勾选框：
- "文件后缀名"： 可选择是否加上读取了的文件的后缀名
- "物体类型后缀": 可选择是否加上读取了的文件的节点的类型名称,此名称可在源码的最前面那地方改

- 点击"重命名文件读取类物体"可进行自动重新命名

- 4.重命名Combiner和Group

- 就是Combiner和Group这两个节点重命名,将其名称自动改为其参考的对象中的第一个物体的名称
- 勾选框"物体类型后缀" : 可选择是否加上"Combiner"或"Group"的后缀名

- 点击"重命名Combiner/Group"可进行自动重新命名

--------------------------------------------------------------------------------------

### 已知可能出现的问题：

- 1.你python可能没装好?一般clarisse安装程序会自动提示装python的,一般人安装都不会漏掉安装这个的吧,没装容易影响正常的软件使用的说(

- 2.选择的时候要注意窗口左上角的锁(Lock Selection),可能会影响正常使用注意一下

- 3.软件设定了的本来就不能重命名的东西,就是重命名不了的,比如reference了的abc文件（alembic）下面的子对象之类的

- 4.作者自己遇到的情况也不多,可以反馈问题

- 如有问题有bug反馈可联系QQ:1369437619
- ("▔□▔)/
