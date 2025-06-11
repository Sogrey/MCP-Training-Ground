# Demo1

mcp 的第一个 demo，用于展示如何使用 mcp 进行开发。

功能仅包含一个查询和一个计算两数加法的工具。

## 配置虚拟环境

We recommend using [uv](https://docs.astral.sh/uv/) to manage your Python projects.

Then add MCP to your project dependencies:

```bash
uv add "mcp[cli]"
```

Alternatively, for projects using pip for dependencies:

```bash
pip install "mcp[cli]"
```

## 使用

> CherryStudio 中的 uv 和 bun 需要单独安装。如果窗口右上角有红色三角符号时。

### stdio 本地标准输入输出流调用

```python
# Run the server
if __name__ == "__main__":
    mcp.run(transport="stdio")
```

CherryStudio 中mcp 的类型选择 `标准输入/输出(stdio}`。

命令填写 `uv`
参数填写 :
```
--deirectory
I:\AIWork\mcp-server\MCP-Training-Ground\01.demo1 # 这里填写项目根目录
run 
main.py # 这里填写项目入口文件
```


### sse 远程调用

```python
# Run the server
if __name__ == "__main__":
    mcp.run(transport="sse")
```

CherryStudio 中mcp 的类型选择 `服务器发送事件(sse}`。
url 填写 `http://127.0.0.1:8000/sse`。 这里ip根据自己情况修改。

### streamable-http 调用

```python
# Run the server
if __name__ == "__main__":
    mcp.run(transport="streamable-http")
```

CherryStudio 中mcp 的类型选择 `可流式传输的HTTP(streamableHttp}`。
url 填写 `http://127.0.0.1:8000/mcp`。 这里ip根据自己情况修改。