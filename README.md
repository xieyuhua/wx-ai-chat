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


域名部署

```
server{
   server_name openai.test.cn;  # 请根据实际情况修改你的域名

   location / {
          client_max_body_size  64m;
          proxy_http_version 1.1;
          proxy_pass http://localhost:3000;  # 请根据实际情况修改你的端口
          proxy_set_header Host $host;
          proxy_set_header X-Forwarded-For $remote_addr;
          proxy_cache_bypass $http_upgrade;
          proxy_set_header Accept-Encoding gzip;
          proxy_read_timeout 300s;  # GPT-4 需要较长的超时时间，请自行调整
   }
}
```


### 运行

1. 登录微信
2. 在.env中填写指定环境变量值
3. 运行chat.py

```shell
python chat.py
```
