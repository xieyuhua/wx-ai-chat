## 说明

### 按照模型和one-api

```
set OLLAMA_HOST="0.0.0.0:11434"
set OLLAMA_MODELS=E:\ollama
ollama run qwen:7b

one-api.exe
默认 localhost:3000 root 123456
创建渠道和令牌

OPENAI_API_KEY  = sk-zXVpryKtINryKHug077d52228d524562B714F800712b5fC5
OPENAI_BASE_URL = http://localhost:3000/v1/
```


### 安装依赖

```shell
pip install openai wxauto python-dotenv
```

### 运行

1. 登录微信
2. 在.env中填写指定环境变量值
3. 运行chat.py

```shell
python chat.py
```
