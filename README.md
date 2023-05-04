## 概要

![](docs/img/development.jpg)

### 具体的なサービスの紹介は[こちら](https://qiita.com/rabbit0624/items/959ab309802e1a8e5115)


## 環境設定
## .envファイルの作成
- .env.exampleを複製して.envという名前に変える
- POSTGRESという名前がついた環境変数はすべてpostgresという名前に設定する
- SECRET_KEYを設定する
- API_KEYを入力する

## SECRET_KEYを生成する方法
```
>>> from django.core.management.utils import get_random_secret_key
>>> get_random_secret_key()
```

生成した文字列を.envの
DJANGO_SECRET_KEY="django-insecure-"
の -django-insecure- の後ろにくっつける

## API_KEYを生成する方法
- Replicate
    - https://replicate.com/
    - Githubのアカウントを登録するとAPIキーが発行される
    - REPLICATE_API_TOKEN=APIキー（""なし）
- OPEN_API_KEY
    - https://openai.com/blog/openai-api
    - Sign up↗からgoogleログイン
    - 右上のPersonalからView API
    - 一度見たら二度と見れなくなるのでどこか(localの.envとか)に保存しておくこと
    - OPENAI_API_KEY=APIキー
- DeepL
    - https://www.deepl.com/ja/pro/change-plan?cta=header-pro-button/#developer
    - 無料版に登録して認証キーを発行
    - 月500,000文字
    - DEEPL_API_KEY=APIキー（""はどっちでもよかったはず，僕はつけてない）
- Hugging Face
    - https://huggingface.co/
    - アカウント作成する
    - 右上のアイコンからsettings
    - Access Tokensタブから取得可能
    - HUGGINGFACE_API_KEY=API_KEY
 

## 参考
- ChatGPT PlayGround, 
https://platform.openai.com/playground

- ChatGPT role
https://blog.since2020.jp/ai/chatgpt_api_role/

- ChatGPT APIアクセス
https://dev.classmethod.jp/articles/openai-api-chat-python-first-step/
