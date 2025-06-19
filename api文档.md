API Key：sk-a7349f35a2ea4c9986b36b6396a5f45b

API对接文档：

curl --location 'https://dashscope.aliyuncs.com/compatible-mode/v1/chat/completions' \
--header "Authorization: Bearer $DASHSCOPE_API_KEY" \
--header 'Content-Type: application/json' \
--data '{
  "model": "qwen-vl-max",
  "messages": [
  {"role":"system",
  "content":[
    {"type": "text", "text": "You are a helpful assistant."}]},
  {
    "role": "user",
    "content": [
      {"type": "image_url", "image_url": {"url": "https://help-static-aliyun-doc.aliyuncs.com/file-manage-files/zh-CN/20241022/emyrja/dog_and_girl.jpeg"}},
      {"type": "text", "text": "图中描绘的是什么景象?"}
    ]
  }]
}'