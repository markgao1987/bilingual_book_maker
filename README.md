# bilingual_book_maker

Make bilingual epub books Using AI translate

![image](https://user-images.githubusercontent.com/15976103/222317531-a05317c5-4eee-49de-95cd-04063d9539d9.png)

## 準備

1. ChatGPT or OpenAI token
2. epub books
3. 能正常聯網的環境或 proxy
4. python3.8+

## 使用

1. pip install -r requirements.txt
2. openapi token
3. 本地放了一個 animal_farm.epub 給大家測試
4. 預設用了 ChatGPT 模型，用 `--model gpt3` 來使用 gpt3 模型
5. 加了 `--test` 命令如果大家沒付費可以加上這個先看看效果（有 limit 稍微有些慢）
6. 加了 `--lang` 參數，設為 `zh-cn` 可翻譯為簡體中文，設為 `zh-tw` 可翻譯為繁體中文

使用範例

```shell
# 如果你想快速測一下
python3 make_book.py --book_name test_books/animal_farm.epub --openai_key ${openai_key} --no_limit --test
# or do it
python3 make_book.py --book_name test_books/animal_farm.epub --openai_key ${openai_key}
# or 用 gpt3 模型
export OPENAI_API_KEY=${your_api_key}
python3 make_book.py --book_name test_books/animal_farm.epub --model gpt3 --no_limit
```

## 注意

1. 有 limit 如果想要速度可以付費
2. 現在是 demo 版本有很多工作要做 PR welcome
3. 尤其是 batch translat 做完效果會好很多
4. DeepL 模型稍後更新

# 感謝

- @[yetone](https://github.com/yetone)

# 貢獻

- 任何 issue PR 都歡迎
- Issue 中有些 TODO 沒做的都可以選
- 提交程式碼前請先 `black make_book.py`

## 讚賞

謝謝就夠了

![image](https://user-images.githubusercontent.com/15976103/222407199-1ed8930c-13a8-402b-9993-aaac8ee84744.png)
