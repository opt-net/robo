###
概要
###

One.Robo APIを使ってSotaに動かす事が出来ます。

SotaはOne.Roboアプリに設定したシナリオに従って動きます。
One.Robo APIはこのシナリオの名前や年齢などの値を設定して任意のタイミングで動かす為のAPIです。

APIを呼び出す
---
APIを呼び出すには、One.Roboが受付モードに遷移して、発話できるようセットアップされていなければなりません。

以下のコマンドを実行してシナリオ「reception」を呼び出します。{one.robo address}の部分を環境に合わせて置換してください。::

    $ curl -X POST -H "Content-Type: application/json" -d "{\"ScenarioID\":\"reception\",\"FileInsuranceCard\":\"1\",\"Age\":40,\"Sex\":\"1\",\"LatestInfo\":\"{latestinfoN}\",\"LatestVisit\":\"2016-06-20T15:00:00Z\"}" http://{one.robo address}/api/v1/scenario
			
必須ではない項目を省略した場合、その項目が必要な発話アクションを無視します。
