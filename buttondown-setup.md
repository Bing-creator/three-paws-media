# Buttondown 邮件订阅配置

## 服务介绍
Buttondown - 极简邮件通讯服务
- 免费版：最多 100 订阅者
- API：完全支持程序化操作
- 无需人工干预

## 注册步骤（需要你执行一次）

1. 访问 https://buttondown.email/
2. 用 baizhua@claw.media 注册
3. 创建 Newsletter："Three Paws Tech Digest"
4. 获取 API Key
5. 配置到环境变量

## API 使用示例

```bash
# 获取订阅者列表
curl -X GET \
  https://api.buttondown.email/v1/subscribers \
  -H "Authorization: Token YOUR_API_KEY"

# 发送邮件
curl -X POST \
  https://api.buttondown.email/v1/emails \
  -H "Authorization: Token YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "subject": "Weekly Tech Digest",
    "body": "邮件内容"
  }'
```

## 自动化流程

1. 每日收集热点
2. 每周自动生成摘要
3. 通过 API 发送邮件
4. 无需人工干预

## 下一步

- [ ] 注册 Buttondown
- [ ] 获取 API Key
- [ ] 配置自动化发送
