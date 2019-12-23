########
Scenario
########

http://{one.robo address}
Encoding: UTF-8
Data Format: JSON

api/v1/scenario
---------------
POST
シナリオを実行します。

例::
    $ curl -X POST -H "Content-Type: application/json" -d '{"ScenarioID":"reception","FileInsuranceCard":"1","LastName":"タロウ","FirstName":"ニホン","Age":40,"Sex":"1","RoomName":"診察室","LatestInfo":"{latestinfoN}","LatestVisit":"2016-06-20T15:00:00Z"}' http://192.168.100.59/api/v1/scenario

.. csv-table::
    :header: "変数名", "型", "必須", "意味"
    :widths: 30, 10, 5, 30

    "ScenarioID", "string", "〇", "すべてのシナリオIDはOne.Roboの設定を確認してください。"
    "LastName", "string", "", "姓（カナ）"
    "FirstName", "string", "", "名（カナ）"
    "Age", "number", "", "年齢"
    "Sex", "string", "", "コード一覧。性別参照"
    "FileInsuranceCard", "string", "", "コード一覧。保険証提示参照"
    "LatestInfo", "string", "", "前回治療情報。コード一覧。発話タグ参照"
    "LatestVisit", "string", "", "前回来院日。日付フォーマット参照"
    "NextVisit", "string", "", "次回来院日。日付フォーマット参照"
    "RoomName", "string", "", "案内する部屋の名前"

性別
----

保険証提示
----------

日付フォーマット
----------------
ISO8601(UTC)です。

2019-10-11の例::

    2019-10-10T15:00:00Z

発話タグ
--------
設定>シナリオ>アクション>発話の置換文字列を確認してください。初期値は以下の通りです。::

    latestinfo1
    latestinfo2
    latestinfo3
    latestinfo4
    latestinfoN
