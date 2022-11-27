# my-first-blog

**本プロジェクトで解決したい課題**

現在、ホールスタッフの人数を各店舗の店長が経験から決定しているため、時間帯によって人数の過不足が発生している可能性がある。
そこで、ホールスタッフの配置を最適化することを目的とした機械学習モデルを構築、運用していく。
今回は1日の1時間あたりの客数を予測して、ホールスタッフの人数最適化を行っていく。
これにより、人的コストの削減だけでなく、客数に対する最適な接客人数の推定も可能となるため、ホールスタッフの働きやすさにも繋がる。


**課題が解決できている状態の定義**

まず、以下の項目を設定する。（表内の数字は全て例を表している）
| 日時             | 店内にいるスタッフの人数 | 労働時間 | 入店者数 | 客単位での接客時間（5分に設定） | 接客に必要な人時（入店者数×5分） | 接客に必要な人数（接客に必要な人時÷60） | 接客できたであろう時間 | 稼働率（接客に必要な人時÷スタッフ全員の労働時間） | カバー率（スタッフ全員の労働時間÷接客に必要な人時 | 
| ---------------- | ------------------------ | -------- | -------- | ------------------------------- | -------------------------------- | --------------------------------------- | ---------------------- | ------------------------------------------------- | ------------------------------------------------- | 
| 2022/11/25 10:00  | 2                        | 120      | 10       | 5                               | 50                               | 1                                       | 50                     | 41.66%                                            | 100%                                              | 
| 2022/11/25 11:00 | 3                        | 180      | 25       | 5                               | 125                              | 3                                       | 125                    | 69.44%                                            | 100%                                              | 
| 2022/11/25 12:00 | 3                        | 180      | 40       | 5                               | 200                              | 4                                       | 180                    | 100%                                              | 90%                                               | 

上記の表にある、稼働率とカバー率の両方を高め、その結果起こる人的コストの削減による店舗の利益が増加すれば今回の課題が解決している状態だと定義する。
各店舗は関東地方および東北地方の地域別に存在することに加えて、大規模店と中規模店の種類に分けられるため、それぞれの条件内で本プロジェクトを適用する店舗と適用しない店舗を設定した上で、結果から各条件内で比較を行い効果検証を行う。

**システム構成**
データベース

課題を解決するためのワークフロー。2点
ワークフローを実現するためのシステム。2点
メンバー構成。1点


機械学習のプログラム、モデル、推論結果の管理方法

チーム開発で機械学習のプログラムを管理、レビューする。1点
モデルを管理し、過去のモデルを再利用したり、比較評価する方法が書かている。2点
推論結果を管理し、施策の評価に活用する仕組みが書かれている。2点


機械学習の学習と推論を実行するタイミング

学習および推論時に利用可能なデータの管理方法。2点
ワークフローの中で適切に学習と推論を実行する。2点
機械学習モデルを評価し、修正し、本番で利用する手順を言及している。1点


店舗への連絡方法

推論結果を店舗へ適切なタイミングで連絡する方法。2点
障害等、異常事態の発生時に店舗へ連絡し、適切な処理を取る方法。2点
施策を改善するための店舗ヒアリングやインタビュー。1点


ホールスタッフの人員配置が適切に実施されていることを確認する方法

人員配置が実施されていることを店舗から情報収集する方法。2点
適切に実施されいていない場合にその原因を調査し、改善する方法。2点
施策を評価するためにデータを自動で収集する方法。1点


本プロジェクトの成否を判断するための数値的な評価基準

コスト削減効果（人的コスト、システムコスト、運用コスト、教育コスト、その他）。2点
店舗ホールスタッフおよび店長の満足度評価。3点


本プロジェクトの品質を維持し、改善する方法

施策を維持する方法。1点
評価を改善施策（またはプロジェクトを終了する指標）にする方法。2点
運用を自動化する方法。2点




