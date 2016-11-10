# How to create a web application to bottle!!!
Webアプリをつくってみおうfor Python
今回は軽量ウェブフレームワークのBottleを使うよ[Official](http://bottlepy.org/docs/dev/)

## 参考
* [Pythonの軽量WebフレームワークBottleを試してみた（その１） - ルーティング編 （Advent Calendar 23日目） | アライドアーキテクツ エンジニアブログ](http://tech.aainc.co.jp/archives/9826)

## 環境構築
venvで環境つくてpipで入れるよ

```bash
python3 -m venv env
. env/bin/activate
pip install bottle
```

Hello worldサンプルだよお
インタープリターで試してみおう

```python
from bottle import route, run, templete

@route('/hello/<name>')
def hello(name):
  return template('<h1>Hello {{name}}</h1>', name=name)

run(host='localhost', port=8080)
```
