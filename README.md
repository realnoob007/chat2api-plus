# chat2api-plus
**chat2api-plus** 用于将 Web 端的 ChatGPT 对话接口转换为标准的 OpenAI API 格式。本程序支持官网所有模型(会持续更新)，包括 GPT-3.5、GPT-4、GPT-4-all、GPTS， GPT-4o, GPT-4o-mini 和 dalle画图模型。本项目配备了易于使用的管理仪表板，包括渠道管理、可视化数据显示以及批量添加或修改账户的功能。

**重要提示**：运行此项目需要授权。目前可联系项目组进行试用。

**注意**：此项目需与 xyhelper 的接入点配合使用。更多详情，请点击此处：[xyhelper 接入点详情](https://xyhelper.cn/access/)。

## 特性
- **无门槛**：无需手动登录获取 access token，直接填入账号密码即可使用。
- **批量导入导出**：支持轻松导入导出各种格式的账号列表并且批量添加标签，易于管理。
- **渠道管理**：一键启用/禁用渠道。
- **均衡负载**：通过权重和优先级的双重控制，灵活分配账号使用次数。
- **人性化设计**：支持筛选和搜索账号，可查看每个账号在每个模型上的调用次数和官网订阅到期时间。
- **高度可靠**：内置自动重试机制和账号冷却功能，最小化错误率。
- **自动化操作**：定时自动更新账号状态，每日自动清理过期/异常账号。
- **数据可视化**：清晰展示所有 API 调用数据及账号池的实时状态。
- **自动继续对话**：一次性输出超长的响应回复，突破逆向的限制


## 支持的模型列表(持续更新)

本项目当前支持以下AI模型：

- `gpt-3.5-turbo`: 普号调用的官网3.5。
- `gpt-3.5o`: 普号调用的4o模型，因为不能画图，所以与plus和team的4o隔离。
- `gpt-4`: 正常的gpt-4，模拟api，不支持联网等功能。
- `gpt-4-all`: GPT-4的全功能版本，支持图像、文件输入，支持调用联网插件，代码解释器，画图等全部官网功能。
- `gpt-4o`: 最新发布的GPT-4o模型，由plus或者team号调用。
- `gpt-4o-mini`: 最新发布的GPT-4o-mini模型，最有性价比的模型，由普号调用。
- `gpt-4-gizmo-*`: 匹配传入的gpts的gizmo id，调用所有gpts。
- `dall-e-3`: 官网画图模型，可定制尺寸，生成高质量画面。



## 界面截图
<img width="1280" alt="893e84c37f8b211e65a5a0c78ea4e1a" src="https://github.com/user-attachments/assets/970ec612-a2fb-4012-b032-88d1a7166bce">
<img width="1280" alt="828be1ed65ffd9642f6494878683bd9" src="https://github.com/user-attachments/assets/d98fb3be-1994-4229-b14e-4d11e7e59a5d">
<img width="1280" alt="2738c275edc33000fae4273dc17dc2b" src="https://github.com/user-attachments/assets/2faf0b1a-c599-449e-9228-d218563a9c11">

---

## 部署

为了部署本项目，你需要跟随以下步骤操作：

### 步骤 1: 克隆仓库

首先，使用 Git 克隆仓库到你的本地或服务器上：

```bash
git clone https://github.com/realnoob007/chat2api-plus.git
```

### 步骤 2: 进入项目目录

克隆完成后，切换到项目目录中：

```bash
cd chat2api-plus
```

### 步骤 3: 配置文件

使用文本编辑器打开配置文件并按照指引填写相关配置。这里以 `vi` 编辑器为例：

```bash
vi config.yaml
```

确保根据实际情况修改配置文件中的设置，数据库连接、请求所需的验证秘钥、网关地址等。

### 步骤 4: 启动服务

使用 Docker Compose 启动服务。确保你的机器上已安装了 Docker 和 Docker Compose。

```bash
docker compose up -d
```

此命令将在后台启动所有必要的容器。

### 步骤 5: 访问后台

在浏览器中访问 `ip地址:端口/admin` 或者你配置的反向代理域名。

默认的用户名和密码为：

- 用户名: admin
- 密码: 123456

请在首次登陆后尽快更改默认密码以保证系统安全。



## 联系方式 & 购买授权

<img src="https://github.com/realnoob007/chat2api-plus/assets/87698941/c8db4e6e-4d2d-47a4-8ba5-73026a0eb402" width="250" height="auto" alt="联系方式及购买授权信息">
