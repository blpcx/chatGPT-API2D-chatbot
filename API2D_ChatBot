# %% 提问
import requests
import json

url = "https://oa.api2d.net/v1/chat/completions"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer YOUR-KEY' 
}

data = {
  "model": "gpt-3.5-turbo-16k",
  "messages": [{"role": "user", "content": """
  你好！
  """}],
  "temperature": 0.2,
  # "top_p":1, # 二选一
  # "n":1,
  # #  "stream":True,
  # "max_tokens":2000,
  # "presence_penalty":0,
  # "frequency_penalty":0,
}

response = requests.post(url, headers=headers, json=data)

print("Status Code", response.status_code)
print("JSON Response ", response.json())
response_str = json.dumps(response.json())
response_obj = json.loads(response_str)
content = response_obj['choices'][0]['message']['content'].strip()
print(content)

# %% 查询余额
import requests
import json

url = "https://openai.api2d.net/dashboard/billing/credit_grants"
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer YOUR-KEY' 
}
response = requests.post(url, headers=headers)
print("JSON Response ", response.json())
# %%
