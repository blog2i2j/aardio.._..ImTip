# ImTip 桌面助手
 
<a href="https://imtip.aardio.com/update/ImTip.7z">点这里下载 ImTip</a> - 免费开源，仅 796 KB。独立 EXE 无任何外部依赖，兼容 XP，Vista，Win7，Win8，Win10，Win11 …… 等所有流行桌面操作系统。  

ImTip 提供超级热键、输入法状态提示、AI 助手等功能。

[超级热键开发指南](https://www.aardio.com/zh-cn/doc/?q=library-guide%2Fstd%2Fkey%2Fhotkey.html)

输入法提示通过**在输入光标处显示 2 个简洁的图标** —— 提前知道中英、中英标点、全半角、大小写、多语言键盘布局等所有状态。

![通用输入法状态跟踪提示](./screenshots/imtip.gif)

可以方便地自定义外观方案，例如[单图标方案](https://imtip.aardio.com/#dot-scheme)效果如下：

![ImTip 单图标配置方案](./screenshots/imtip-dot.gif)

**再也不怕按错了！** 保持思考与输入的连续性，避免低头看任务栏或通过其他操作检查输入状态。


- 不是只能看中英状态，而是关注更少的图标，了解更多的常用输入法与键盘状态。
- 不是只在切换输入法才显示一次状态，当切换到新的输入位置都会及时地提醒输入法状态，可以自定义显示时长、方式、外观。
<br>

![获取输入框光标位置](./screenshots/web.gif)

有了 ImTip 就可以关掉输入法自带的状态栏，屏幕更干净了，**美滋滋再也不用看右下角** ！

![输入法自带状态栏](./screenshots/ime.png)

理论上支持所有输入法，系统自带的微软拼音，微软五笔，搜狗输入法，小小输入法，百度输入法，QQ输入法，谷歌输入法，小鹤输入法，手心输入法 …… 包括我测试的日文、韩文、西班牙语输入法都可以支持 ImTip 。

ImTip 支持可视化编辑状态提示外观：

![调色](./screenshots/color.gif)

可将外观方案直接拖入 ImTip.exe 或外观设置窗口快速导入。  
支持用剪贴板直接复制粘贴配置方案代码。  

![复制配置方案](./screenshots/copy.gif)

ImTip 提供可编程扩展的「超级热键」。
例如按 Ctrl+$ 打开财务大写、日期时间大写、数学运算工具：

![超级热键](./screenshots/cn.gif)

<a href="https://mp.weixin.qq.com/s/-bdN1oypEdpHhx_SKx2p-Q">官方微信 | 超级热键大全 | 教程 </a>

ImTip 托盘菜单提供快捷启用系统输入法、切换双拼方案等功能。

![超级热键](./screenshots/menu.png)

ImTip **CPU 占用极低**，可以通过设置「跟踪检测速度」调整 CPU 占用：

![跟踪检测速度](./screenshots/cpu.png)

默认有微小延迟 —— 这是程序的主动优化( 并非被动延迟 )，您可以加快「跟踪检测速度」（更丝滑，增加的资源占用仍然是可忽略的）。

**附：输入法常用快捷键**  
「Shift」切换中/英输入；  
「Ctrl + . 」切换中/英标点；  
「Shift + 空格 」切换全/半角；  
「Alt + Shift」切换语言  

## 常见问题

一、关于英文键盘

有些第三方输入法会安装「中文美式键盘」 - 可能导致不必要的错乱。这个键盘在 Win10 其实已被废弃，建议移除或更改为「英语美式键盘」。Win7/Win10/Win11 可在 ImTip 托盘菜单中禁用启用一次「英语键盘」就可修复该问题。  

二、管理权限窗口

ImTip 默认以普通权限启动，以管理权限启动 ImTip.exe —— 才会对其他管理权限窗口生效。以管理权限启动后重新勾选 「允许开机启动」，则开机以管理权限启动（ 不会再弹出请求权限弹框 , 注意只有同样在管理权限下启动才能取消此设置 ）。

三、个别窗口无法识别状态

个别输入法在某个特定的窗口偶尔会状态错乱（或导致其他输入法错乱），切换到其他窗口（或重新打开原窗口）可恢复正常（这可能是因为安装了某些有问题的输入法导致的问题）。 

四、个别窗口无法检测到输入光标或鼠标文本指针

有少数无法获取输入光标的窗口会退化为检测并跟踪鼠标“I”型文本指针。虽然 ImTip 兼容几乎所有窗口，但仍然可能会有少数窗口无法检测输入光标或鼠标文本指针。这时候可打开 ImTip 配置窗口在「兼容类名」中尝试添加该窗口的类名（可使用窗口探测软件查看）。

五、无输入框的窗口不显示  

即使取消勾选「仅切换输入目标或状态后显示」，在检测不到输入目标的窗口仍然是不会显示的（除非设置了兼容窗口类名）。  

六、输入法兼容性  

小小输入法最新版已完美支持 ImTip，可使用小小输入法自带的自动更新功能更新到最新版。注意需要注册 TSF 内置组件（这是默认选项）。小小输入法返回的语言代码受系统设置的区域格式影响，如果区域格式不是中文，请到设置中修改为中文，并重新执行小小输入法 tsf 目录下的卸载、注册程序重新注册一次 TSF 组件即可正常识别状态。

手心输入法英文模式返回的状态不正确，但可以正确识别中文标点等状态。好在手心输入法每次切换到中文模式都会自动切换为中文标点，所以可在 ImTip 配置窗口中勾选「怪异模式」即可区分中英状态。

小鹤输入法有一个小问题，在英文模式下切换全半角后状态会错乱，按 Shift 切换一次中英模式会恢复正常，可能基于多多的输入法都有类似问题。

七、关于切换输入法

在超级热键中，已提供了切换输入法中英状态的演示。如果没有按热键，ImTip 不会影响或切换输入法。如果有这类需求，可向输入法作者反馈。

八、启动参数

`ImTip.exe *.aardio`  
加载配置方案，或者直接将配置文件拖到 ImTip.exe 上也可以。  

`ImTip.exe 无参数`  
如果 ImTip 已运行则打开配置窗口，或者直接双击 ImTip.exe 也可以。  

九、关于 /.ImTip/ 目录

ImTip 默认将运行时数据（ AppData ）保存在 AppData 目录（推荐保持这个默认设置，AppData 体积很小放在独立目录，可一键删除不用卸载）。如果在 ImTip.exe 所在目录创建 /.ImTip/ 目录，ImTip 将会优先使用该目录保存 AppData ——  将 AppData 存于 EXE 目录是过时与不安全的做法，容易出现误删操作，也不能方便地移动独立 EXE 文件（例如将 EXE 放在桌面），影响便携性。

十、提示窗口闪烁

ImTip 默认会阻止重复运行，但如果您在 aardio 开发环境中单独运行创建提示窗口的源码，并且同时创建了多个输入法提示窗口，多个窗口相互冲突当然就会闪烁了。

****

本页的动画主要使用 [开源免费，下载体积仅 820 KB 的极简录屏软件 Gif123](https://gif123.aardio.com/) 录制。
