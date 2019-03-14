# Quarkusについてガイドに沿って触ってみた

- https://quarkus.io/guides/getting-started-guide

- ビルド＆起動コマンド
    -   mvn compile quarkus:dev

- ネィティブビルドコマンド
    - 初回のみ
    - mvn package -Pnative -Dnative-image.docker-build=true
    
    - ２回目以降
    - docker build -f src/main/docker/Dockerfile -t quarkus-quickstart/quickstart .
    - 実行
    - docker run -i --rm -p 8080:8080 quarkus-quickstart/quickstart
    
- アクセスURL
    - curl http://localhost:8080/hello
    - curl http://localhost:8080/hello/greeting/taka
    - curl http://localhost:8080/hello/greeting/async