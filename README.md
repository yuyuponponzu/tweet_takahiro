# tweet_takahiro
雑です

## ツイートの取得
http://www.twimemachine.com/user/AI_junk88_takah/
ここで全ツイートを取得（全部コピーしてる）

## AI(ではないけど，マルコフ連鎖)によるツイート生成
1.tweet.txt というテキストファイルに，コピーしたツイートを全部張る
2.preproc_txt.pyでnew_tweet.txt(簡単にする為に日本語以外の文字や数字を全て除外，もっと良いのを作りたいならここを弄ればちゃんとできる)
3.make_dict.pyでマルコフ連鎖用の辞書作成
4.gene_tweet.pyで辞書に沿ってツイート生成（現状，初句(w1)はランダム選択だから不自然になることも．文終了のトリガーは理系ぶって「．」）
5.ai_tweet.txtに任意の行数分の自動生成文ができる

## bot化
https://twittbot.net
ここで複数行入力で一括登録

## 補足
ちゃんとbot化したければAPI取得の申請が必要（リプの対応まで可能）
たまに長いわけのわからない文ができるのは，preprocが激甘だから
意味的な理解まで含めたAIを作るならマルコフ連鎖じゃなくてLSTM