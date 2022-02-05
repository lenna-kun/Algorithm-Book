# 平衡2分探索木
扱うデータ数を\\(N\\)とすると，平衡2分探索木の各操作と時間計算量は以下．
- 値(大小関係が定義されている必要がある)の挿入: \\(O(\log N)\\)
- 値の削除: \\(O(\log N)\\)
- 値の検索/取得: \\(O(\log N)\\)

データを2分木のノードとして持つことで上記クエリを高速に求める．値の挿入，削除を繰り返す中で，2分木に偏りが出ないように調整することで各クエリの計算量を\\(O(\log N)\\)に抑えるところから，**平衡2分探索木**という名前になっている．

平衡2分探索木の実装は多くある．有名な例を下にいくつか挙げる．

- 赤黒木 : C++の`set`クラスの内部で使われており，OSの実装におけるタスクスケジューラにも使われていたりする．おそらく最も有名な平衡2分探索木．
- AVL木 : こちらも非常に有名な平衡2分探索木．後日加筆．
- Splay木 : Splayという特殊な操作により各種操作の償却計算量を\\(O(\log N)\\)に抑える(詳しくは該当の章を参照して欲しい)．実装が上と比較すると簡単であるため，自実装する必要がある場合はこれがおすすめ．
- 2-3木 : "2分"ではないが，目的は同じ．後日加筆．
- Treap : 後日加筆．
- RBST : 後日加筆．