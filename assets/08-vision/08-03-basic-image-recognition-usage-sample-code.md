## ソースコード（コピー・アンド・ペースト用）:
```
response = client.chat.completions.create(
  model="gpt-4o",
  messages=[
    {
      "role": "user",
      "content": [
        {"type": "text", "text": "この画像には何が含まれていますか？"},
        {
          "type": "image_url",
          "image_url": {
            "url": "https://drive.usercontent.google.com/download?id=1n-ZJeqq0M6a6_kZG8oV4yK66cYs-fYXR",
          },
        },
      ],
    }
  ],
  max_tokens=300,
)

print(response.choices[0].message.content)
```