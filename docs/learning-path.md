# local-kb-rag 学习路线（基于本仓库模块）

## 阶段一：工程骨架
1. `libs/chatchat-server` —— 先看 pyproject / cli / 配置入口，理解如何启动服务
2. `libs/python-sdk` —— 了解客户端如何调用服务（chat / kb / server）

## 阶段二：知识库（RAG 核心）
3. `file_rag` —— 文件解析与切分，文档如何变成向量
4. `knowledge_base` —— 知识库管理、向量检索与入库

## 阶段三：对话与接口
5. `chat` —— 一次问答的链路与消息处理
6. `api_server` —— FastAPI 接口层，外部如何访问

## 阶段四：进阶
7. `agent` / `agents_registry` —— Agent 编排与工具注册（联网搜索、计算等）
8. `reranker` —— 检索结果重排序，提升答案质量
9. `db` —— 元信息与用户数据的持久化

## 建议
- 先读 `docs/` 与 `markdown_docs/` 的安装与启动说明，把服务跑起来；
- 用最小文档走通 `file_rag → knowledge_base → chat` 一条链路；
- 画一张"文档上传到返回答案"的流程图，比直接读代码收获更大。
