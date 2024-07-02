# FastAPIでTodoアプリ

参考文献: [FastAPI入門](https://zenn.dev/sh0nk/books/537bb028709ab9)

## 環境構築

### 1. イメージのビルド

```shell
docker-compose build
```

### 2. poetryによるPython環境のセットアップ

```shell
docker-compose run \
  --entrypoint "poetry init \
    --name todo-app \
    --dependency fastapi \
    --dependency uvicorn[standard]" \
  todo-app
```

### 3. FastAPIのインストール

```shell
docker-compose run --entrypoint "poetry install --no-root" todo-app
```

※新しいパッケージを追加した場合は以下のコマンドで再ビルド

```shell
docker-compose build --no-chache
```
