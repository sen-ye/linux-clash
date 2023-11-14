# 在linux服务器配置clash代理

```bash
#下载Linux版Clash.zip
unzip clash.zip
cd clash
#在这一步需要新建一个proxy.yaml文件在当前文件夹下，并将代理的终端配置文件复制到proxy.yaml中。如果你曾使用过windows的clash，可以点击Profiles，右键edit配置文件，然后就可以复制内容了。
chmod +x ./clash-linux-amd64-v1.10.0
./clash-linux-amd64-v1.10.0 -f proxy.yaml -d . #使用proxy.yaml启动代理
```

# 在Python中使用代理

```python
import os
os.environ["HTTP_PROXY"] = "http://127.0.0.1:7890" #端口需要与配置文件中的端口保持一致
os.environ["HTTPS_PROXY"] = "http://127.0.0.1:7890"
```
