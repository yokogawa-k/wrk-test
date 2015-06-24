# wrk の実験

wrk で終了時に nginx で 499 がでるというお話

## 必要なもの

- [docker](https://github.com/docker/docker)
- [docker-compose](https://github.com/docker/compose)

## 構成

- アタッカー: wrk
- ロードバランサ: nginx
- アプリサーバ: php x 2

## 結果

htdocs-php の index.php に usleep を追加すると発生を確認。 
wrk が終了時に切断してるから？

