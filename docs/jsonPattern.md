# ユーザー情報について
{

    "user_uploadable":{
        "id"(
            - ユーザーでかぶりなし
            - 利用者識別
            - フロントで見せない
            - 必須
            - 数列か文字列？
            - ランダム生成してかぶりがないか確認？
        ), 
        "name"(
            - 入力したら名前で呼んでもらえる
            - 入力されなくてもよい
            - 初期値はNull
            - 文字列またはnull
        ),
        "email"(
            - アカウント登録のメールアドレス
            - 文字列またはnull
            - if (env == ブラウザ): 必須
            - else: 任意
            - 初期値はNull
        ),
        "env"(
            - 使用環境
            - ブラウザか
            - Windowsか
            - MacOSか
            - Linuxか
            - AndroidOSか
            - iOSか
            - その他か（何があるか知らないが）
        )
    }

}

{

    "user_secret":{
        "folder"(
            - 端末にデータを送る際のフォルダパス
            - 必須
            - 文字列
        ),
        "export"(
            - MarkDown出力する際のデフォルトの出力パス
            - 必須
            - 文字列
        ),
    }

}

# 悩みの送信と返答の受信について
{

    "serve":{
        "mode"{
            - 問題を分割したいなら"split"
            - 肯定されたいなら"cheer"
            - 解決策が欲しいなら"solve"
            - 文字列
            - 必須
        },
        "response"{
            - 相談内容
            - 自由記述
            - 文字列
            - 必須
        }
    }

}

{

    "receive":{
        "chat"{
            - LLMによる回答
            - 文字列
        }
    }

}

# データの保存について
{

    "save":{
        serve.response,
        receive.chat,
        user.secret,
        date{
            - 最終更新日
            - 文字列または日付
        },
    }
    
}