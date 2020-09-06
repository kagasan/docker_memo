# docker_memo
使おうとするたびに忘れてるので、メモしておく。

# install
- [mac](https://qiita.com/kurkuru/items/127fa99ef5b2f0288b81)
- [centos](https://qiita.com/ymasaoka/items/b6c3ffea060bcd237478)

# tutorial
バージョン確認
```docker version```
run
```docker run -d -p 80:80 -v /Users/kagasan/Documents/dwww:/var/www/html --name php70-apache php:7.0-apache```
| option | 解釈                                             | 
| ------ | ------------------------------------------------ | 
| -d     | デタッチモード（バックグラウンド実行？）         | 
| -p a:b | ポートの露出（ローカルのaとコンテナのbが繋がる） | 
| -v a:b | ディレクトリの共有                               | 
| --name | コンテナ名                                       | 

```docker ps -a ```
```docker stop php70-apache```
```docker start php70-apache```
```docker rm php70-apache```

# dockerfile
イメージを作成する記述
```
FROM
RUN
WORKDIR
```
```docker build -t <Dockerイメージ名> <Dockerfileが存在するディレクトリ>```
```docker run -it -d --name <コンテナ名> -p 8081:8080 <Dockerイメージ名>```
