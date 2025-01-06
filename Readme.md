## SingleStack

`SingleStack` 是一个基于 Docker Compose 的一站式解决方案，帮助你快速部署常见的中间件和数据库服务。通过简单的配置和一键启动，你可以在本地或服务器上轻松运行这些服务。



### 快速开始

#### 1. 克隆项目并进入目录

```bash
git clone https://github.com/FreemanKevin/SingleStack.git
cd SingleStack
```

#### 2. 准备镜像文件

- 若需要离线使用，首先将镜像文件上传到 `images/` 目录，然后执行脚本批量导入镜像：

```bash
chmod +x load-images
./load-images
```

#### 3. 解压插件文件

- 将插件压缩包上传到 `plugins/` 目录，并解压：

```bash
chmod +x ./scripts/unzip-plugins
./scripts/unzip-plugins
```

#### 4. 初始化环境

- 更新目录权限和初始化环境配置：

```bash
chmod +x ./scripts/init-env
./scripts/init-env
```

#### 5. 配置服务

- 编辑 `docker-compose.yaml`，根据需求选择需要的服务并修改相应配置。
- 更新 `.env` 文件，配置端口、密码、镜像等信息。

```bash
vim docker-compose.yaml
vim .env
```

#### 6. 启动服务

- 使用 Docker Compose 批量启动所有服务：

```bash
docker-compose up -d
```

#### 7. 查看服务状态

- 查看服务是否正常运行：

```bash
docker-compose ps -a
```

#### 8. 查看服务日志

- 查看指定服务的日志（如 `myserver`）：

```bash
docker-compose logs -f --tail 1000 myserver
```

### 支持的服务

`onepo` 支持以下服务，用户可以根据需求选择启用：

- **Nginx**：反向代理和负载均衡
- **Minio**：高性能对象存储服务
- **Nacos**：服务发现与配置管理
- **Redis**：内存数据存储
- **RabbitMQ**：消息队列服务
- **PostgreSQL**：关系型数据库
- **Elasticsearch**：分布式搜索与分析引擎
- **Geoserver**：地理信息服务

### 配置网络

`onepo` 使用自定义的 `middleware` 网络，确保各个服务之间可以相互通信。你可以根据需要调整网络设置。

```yaml
networks:
  middleware:
    driver: bridge
```

------

如果你有任何问题或建议，欢迎提交 Issues 或 Pull Requests！
