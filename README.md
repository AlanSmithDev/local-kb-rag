# 本地知识库 RAG 应用实验室 (local-kb-rag)

> 整理自 chatchat-space/Langchain-Chatchat（Apache-2.0）的学习型仓库。
> 保留原始 LICENSE 与署名（见 NOTICE）；本仓库仅做中文梳理、模块化拆分与本地化说明，便于系统学习基于 LangChain 的本地知识库问答（RAG）系统。

## 项目定位

Langchain-Chatchat 是一套基于 LangChain 的本地知识库问答系统，支持文档上传、向量检索、Agent 工具调用与多种大模型接入。本仓库聚焦其两大核心代码库：

- `libs/chatchat-server`：后端服务（FastAPI），包含 RAG 检索、Agent、知识库管理、API 服务；
- `libs/python-sdk`：Python 客户端 SDK（`open_chatcaht`）。

## 模块划分

- `libs/chatchat-server/chatchat/server`：核心服务
  - `api_server`：FastAPI 接口层
  - `chat`：对话链路与消息处理
  - `file_rag` / `knowledge_base`：文件切分与向量知识库
  - `agent` / `agents_registry`：Agent 编排与工具注册
  - `db`：数据库模型（SQLAlchemy）
  - `reranker`：结果重排序
- `libs/python-sdk/open_chatcaht`：对外客户端（chat / kb / server / tools）
- `docs` / `markdown_docs`：官方与使用文档
- `tools` / `docker`：部署与运维脚本

## 推荐学习顺序

1. `libs/chatchat-server` 骨架与配置，理解启动方式；
2. `knowledge_base` + `file_rag`：文档如何变成可检索知识；
3. `chat` + `api_server`：一次问答请求的全链路；
4. `agent` + `reranker`：进阶的 Agent 与结果重排；
5. `libs/python-sdk`：如何用客户端对接服务。

## 许可与署名

- 原始项目：chatchat-space/Langchain-Chatchat，Apache-2.0。
- 本仓库保留原始 LICENSE；修改与整理说明见 NOTICE。
- 本仓库为学习整理用途，不声称原创代码，所有示例源码著作权归 chatchat-space 所有。
