Jupyter Notebook samples for book of "データ分析ライブラリーを用いた最適化モデルの作り方".
======

セキュリティ上の理由により、requirements.txt は、2020/03/25 時点での最新にしています。この requirements.txt では、下記の修正が必要です。

正誤表
----

p18 脚注追加：`pip3 install requests`が必要である。

p15 2行目「本書で使用するライブラリー」の表内

- PuLP 2.0
- pandas 1.0.3
- NumPy 1.18.2
- NetworkX 2.4
- matplotlib 3.2.1
- more-itertools 8.2.0
- Pillow 7.0.0
- ortoolpy 0.2.29
- japanmap 0.0.21

p72 下図参考

- 「g.node[0]」 → 「g.nodes[0]」
- 「g.node[0]の出力の『’demand': …』」 → 「{'id': 0, 'x': 5, 'y': 5, 'demand': -4, 'weight': 4}」
- 「g.edges[0]の出力の『’capacity': …』」 → 「{'node1': 0, 'node2': 1, 'capacity': 2, 'weight': 1}」

p15
「pulpTestAll」の脚注に「PuLP 2.0 では、pulpTestAllは使用不可となっている。」を追加。

p59
df.pivot('時限', '曜日')
↓
df.pivot(index='時限', columns='曜日')

p124 6行目
「g.node[nwl+i]['demand'] = dem-1」 → 「g.nodes[nwl + i]['demand'] = dem - 1」

p127 下から5行目
「for nd in list(g.node())[2:]:」 → 「for nd in list(g.nodes())[2:]:」

p160

    import pandas as pd
    start = pd.datetime(2020, 1, 1)
    end = pd.datetime(2020, 1, 14)

↓

    import pandas as pd
    import datetime
    start = datetime.datetime(2020, 1, 1)
    end = datetime.datetime(2020, 1, 14)

