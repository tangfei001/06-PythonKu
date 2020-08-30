**67-JSON对于文件的序列化和反序列化**

import json

import requests


#首先我们需要发送一个请求
r=requests.get(url='http://www.weather.com.cn/data/sk/101190408.html')

#对这个数据进行处理
print(r.content.decode('utf-8'))

#对文件的序列化就是-把服务端的响应数据写到文件中 josn.dump()   r.content.decode('utf-8')  open()

json.dump(r.content.decode('utf-8'),open('weather.jdon','w'))

#对文件的反序列化就是读取文件中的内容 
'''
1:文件反序列化以后.内容是unicode
2:进行编码,吧Unicode类型转为str类型
3:然后使用反序列化,吧strl类型转为字典类型
'''
dict1=json.loads((josn.load(open('weather.jdon','r'))).encode('utf-8'))

print(dict1['weatherinfo']['city'])