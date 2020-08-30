**  64-json字典的序列化和反序列化**

也就是JSON库的学习
'''
序列化:吧python的数据类型转化为str的类型
反序列化:str的类型转化为python的数据结构

#导入json和第三方库requests
import json

#定义一个字典
dict1={"name":"唐飞","age":"25","tel":"18292016624"}

#字典的序列化dict1-str json.dumps()
dict_str=json.dumps()
print(dict_str,type(dict_str))  #{"name": "\u5510\u98de", "age": "25", "tel": "18292016624"} <class 'str'>

#字典的反序列化str-dict json.loads()
str_dict=json.loads(dict_str)
print(str_dict,type(str_dict))  #{'name': '唐飞', 'age': '25', 'tel': '18292016624'} <class 'dict'>





