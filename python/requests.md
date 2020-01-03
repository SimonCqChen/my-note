requests.post的data参数，传值类型不同，header不同

如果直接传字典对象，服务器端会无法解析，需要将字典对象转为json字符串（json.dumps(_)）,并设置headers：
```python
    headers = {
            'Content-type': 'application/json'
        }
```