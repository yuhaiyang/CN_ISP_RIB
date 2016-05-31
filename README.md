# 简介
* 数据基于APNIC，准确有效
* 适用于StoneOS 4.0~5.5各版本
* 对APNIC数据进行路由聚合，实现最小子网
* 覆盖中国大陆地区电信、联通、移动三大运营商，长宽、电信通等二级运营商以及教育网正在准备中
* 每天自动更新，确保可以获取到最新的路由信息

# 安装
##WebUI方式导入至StoneOS（以5.0版本为例）:

	“网络”=>”路由”=>”ISP信息”=>”上传”=>“从电脑上传用户定义的ISP配置文件”=>”浏览”=>选择已下载StoneOS-User-Defined-ISP.DAT文件=>”上传”

##CLI方式导入至(需要自建FTP或者TFTP服务器，以TFTP为例)
```Bash
	import ispfile from tftp server 192.168.1.2 StoneOS-User-Defined-ISP.DAT
```
	
#已知问题
* 不支持二级运营商、教育网等
* 由于低端设备最大ISP路由条目为1000条，所以在导入值低端设备时，会提示“上传失败”，实际联通和移动已导入成功，电信只导入前1000条

#反馈
由于是脚本自动生成，难免出现误差，所以如果出现IP地址与运营商不符或其他问题，你可以通过以下方式联系我
* 本项目[提交Issue](issues/new)
* 通过[博客页面](http://www.cnblogs.com/haiyangyu/p/5545133.html "[定期自动更新]Hillstone 山石网科 StoneOS ISP路由表配置文件")留言
* 给我[发送邮件](mailto:yuhaiyang@outlook.com)