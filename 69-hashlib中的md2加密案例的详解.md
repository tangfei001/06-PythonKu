**69-hashlib中的md2加密案例的详解**

对请求参数做ascill码的排序
做URL encode编码
做md5的加密

dict1={'name':'唐飞','age':'18','tel':'18292016624'}

#第一步进行排序

dict1=dict(sorted(dict1.items(),key=lambda item:item[0]))

#第二步对dict1进行编码

from urllib import parse
datas=parse.urlencode(dict1)

#加密
import hashlib

md5=hashlib.md5()

md5.update(datas.encode('utf-8'))
print(md5.hexdigest())
---------------------------------------------

from urllib import parse
import hashlib

写一个函数
def getMd5(**kwargs):
	#对字典进行排序
	dict1=dict(sorted(kwargs.items(),key=lambda item:item[0]))
	#进行编码  parse.urlencode()
	datas = parse.urlencode(dict1)
	#进行加密 md5.update()     md5.hexdigest()
	md5 = hashlib.md5()
	md5.update(datas.encode('utf-8'))
	#打印数据
	return md5.hexidigest()
print(getMd5(name="wuya",gae="1889"))  #728f1bcbd88fa0431d130550fdef6224
