**64-常用的库sys讲解**

import sys
*# 01:sys.argv返回的是一个列表 #*

#第一个用法

if sys.argv[1]=="sleep":
	print("sleep")
else:
	print("end)
'''
01:在cmd的环境中执行
02:不要在解释器的环境中执行
'''
应用
cd E:\git\GITTHUB\ed\day-06
e:
python sys.py sleep

#第二个用法

print(dir(sys))

#查看操作系统的版本号
print(sys.version)#3.7.1 (v3.7.1:260ec2c36a, Oct 20 2018, 14:57:15) [MSC v.1915 64 bit (AMD64)]
#查看操作平台
print(sys.platform) #win64

#问题:执行的时候，提示login模块不存在，或者说找不到，解决方案如下
import os
import sys

base_os=os.path.join((os.path.dirname(os.path.dirname(__file__))),"day-06")
#吧这个路径添加到path的变量中去
sys.path.append(base_os)

#重新执行代码
from ceshi import *

num()



