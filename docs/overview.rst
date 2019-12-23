####
概要
####

One.Robo APIを使ってSotaに動かす事が出来ます。

SotaはOne.Roboアプリに設定したシナリオに従って動きます。
One.Robo APIはこのシナリオの名前や年齢などの値を設定して任意のタイミングで動かす為のAPIです。

APIを呼び出す
--------------
APIを呼び出すには、One.Roboが受付モードに遷移して、発話できるようセットアップされていなければなりません。

以下のコマンドを実行してシナリオ「reception」を呼び出します。{one.robo app address}の部分をOne.RoboをインストールしたPCのアドレスに置換してください。

::

    $ curl -X POST -H "Content-Type: application/json" -d "{\"ScenarioID\":\"reception\",\"FileInsuranceCard\":\"1\",\"Age\":40,\"Sex\":\"1\",\"LatestInfo\":\"{latestinfoN}\",\"LatestVisit\":\"2016-06-20T15:00:00Z\"}" http://{one.robo app address}/api/v1/scenario
