# Fullhouse Local Play

六人德州扑克本地与局域网版本，基于 [advitrocks9/fullhouse-bot](https://github.com/advitrocks9/fullhouse-bot)。支持 AI 对战、局域网房间、账号、本场盈亏、牌局历史、可视化回放和风格统计。

## 下载与运行

本仓库目前以源码压缩包发布：[下载完整源码及模型](./fullhouse-bot-source.zip)。下载后先解压并进入 `fullhouse-bot` 目录。推荐 Python 3.10。

```bash
python -m pip install setuptools wheel "Cython<3"
python -m pip install --no-build-isolation "eval7==0.1.10"
python -m pip install -r requirements.txt
```

单机模式：

```bash
python local_play/server.py --port 5050
```

浏览器打开 http://localhost:5050 。

局域网模式：

```bash
python local_play/lan_server.py --port 5051
```

房主打开 http://localhost:5051 。同一局域网的其他设备使用 `http://房主电脑的局域网IP:5051`，创建或加入房间即可。详细说明见压缩包中的 `local_play/README.md`。

## 数据与许可

压缩包不包含私人账号数据库、牌谱和缓存。运行后产生的数据保存在本机。当前服务用于本地与可信局域网，GitHub 仓库本身不是在线游戏服务器。

保留原作者署名和原项目 LICENSE。`engine_vendored/` 适用其上游条款，不属于根目录 MIT 许可范围；参见压缩包中的 LICENSE 与相关说明。
