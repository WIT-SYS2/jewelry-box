# Ruby 開発用の Docker container 定義
#
# devuser を開発実行時ユーザとします。
# devuser の uid はビルド時の引数として渡します。
# 引数の指定がないとエラーになります。
FROM ruby:2.4.1
LABEL maintainer "tetsuhisa-makino@wacom-it.co.jp"

# 開発用ユーザの UID
ARG uid

# コンソール上での日本語入力に必要
ENV LANG C.UTF-8
# 開発用のユーザを追加する(問題はUIDをどう指定するか。。。)
RUN useradd -m -s /bin/bash -u $uid devuser

CMD ["tail", "-f", "/dev/null"]
