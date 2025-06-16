# Model Test Scripts

测试已部署ApeRAG系统中模型的可用性和功能。

## 测试脚本

### test_embedding_model.py
测试所有可用的embedding模型，验证哪些模型实际可用。

### test_rerank_model.py  
测试所有可用的rerank模型，验证重排序功能。

### test_completion_model.py
测试指定的completion模型，验证文本生成功能。可手动配置provider、model和prompts。

## 使用方法

```bash
# 测试embedding模型
python tests/model_test/test_embedding_model.py

# 测试rerank模型
python tests/model_test/test_rerank_model.py

# 测试completion模型（需手动编辑脚本配置）
python tests/model_test/test_completion_model.py
```

## 环境变量

| 变量 | 默认值 | 描述 |
|------|--------|------|
| `APERAG_API_URL` | `http://localhost:8000` | ApeRAG API地址 |
| `APERAG_USERNAME` | `user@nextmail.com` | 登录用户名 |
| `APERAG_PASSWORD` | `123456` | 登录密码 |

## 输出

每个脚本会生成：
- 控制台实时输出
- JSON格式的详细测试报告

## 依赖

```bash
pip install httpx yaml
``` 