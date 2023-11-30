# CSE416-redistricting-server
選挙区を人為的に決定する際に生じる不公平の解消できるアメリカの選挙区分けシステムです。

選挙区を人為的に決定する際には、政治的な影響力が低い集団（貧困層、黒人、アジア人など）を一つの区域に集中させることで、これらの集団の意思決定における発言力が弱くなる可能性があります。具体的には、13の区域がある状況で、政治的影響力が低い集団が一つの区域に集中し、政治的権利を持つ人々が残りの12の区域に分散している場合、投票結果は1対12となり、その州全体が政治的権利を持つ人々が望む政策を採用することになります。

このシステムでは、最小生成木というグラフアルゴリズムに基づいて各イテレーションで区域を結ぶすべての辺の中から「最適な」辺を選び、その辺を取り除くことで全体的に選挙区の最適化や再構築を図ります。
ユーザーが期待する選挙区分けの条件（人口の差、境界線の長さなど）のリクエストを処理します。次に、区域再構築アルゴリズムは各イテレーションで二つの選挙区を組み合わせて一つにすることで最適な辺を発見して取り除きます。また、二つの新しい区域を再分割することで、地図の全体構造を最適化し、ユーザーの期待に沿った区分けプランを作成することができます。最終的には、地理情報データを含む区分けプランをユーザーに返し、期待される区分けプランを可視化した地図で表示します。

# Preview
ユーザー入力
<img width="1363" alt="Screenshot 2023-11-30 at 15 54 57" src="https://github.com/hoyyul/CSE416-redistricting-server/assets/135314622/08126303-9d29-4ce9-8f75-76a84fce9641">
zoom in
![7681701326327_ pic_hd](https://github.com/hoyyul/CSE416-redistricting-server/assets/135314622/6aa85857-3870-4349-a3f8-5890a78fb546)
生成された区分けプラン
![7721701326330_ pic_hd](https://github.com/hoyyul/CSE416-redistricting-server/assets/135314622/9d83268b-a6ea-4542-9a8f-2378dfcd0bc9)
![7711701326330_ pic_hd](https://github.com/hoyyul/CSE416-redistricting-server/assets/135314622/dc3fc79e-5fab-48b9-ac7f-83d3427e5651)
生成された区分けプランへの評価
![7731701326330_ pic_hd](https://github.com/hoyyul/CSE416-redistricting-server/assets/135314622/1908ab20-9c1e-4427-a55b-4c2ca9d5e74e)

# Technology
Java Spring(backend)

Python (for Algorithm)

Mysql

React(frontend)

