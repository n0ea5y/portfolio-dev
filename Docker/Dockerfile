# Node.jsの軽量版を使用
FROM node:20-slim

# コンテナ内の作業ディレクトリ
WORKDIR /app

# パッケージ管理ファイルをコピー
COPY package*.json ./

# 依存関係をインストール
RUN npm install

# アプリケーションコードをコピー
COPY . .

# Viteのデフォルトポート
EXPOSE 5173

# 開発サーバーを起動（ホストからのアクセスを許可するため --host を指定）
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]