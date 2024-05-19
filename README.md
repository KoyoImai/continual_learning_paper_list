# 継続学習に関する論文をまとめたリスト
これまでに読んだ継続学習に関する論文をまとめたリスト（未完成）
## Survey論文

## （オフライン）継続学習
### 教師あり学習
 - Learning without Memorizing [[paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Dhar_Learning_Without_Memorizing_CVPR_2019_paper.pdf)]
   - Attention mapの変化にペナルティを加える蒸留損失を導入することで破滅的忘却に対処
 - iCaRL: Incremental Classifier and Representation Learning [[paper](https://openaccess.thecvf.com/content_cvpr_2017/papers/Rebuffi_iCaRL_Incremental_Classifier_CVPR_2017_paper.pdf)]
   - 分類器の旧クラスに対応する出力のラベルを過去モデルの出力で代用することで知識の蒸留を行う
   - クラス増加型，リプレイ＋正則化ベースのアプローチ
 - Learning a Unified Classifier Incrementally via Rebalancing [[paper](https://openaccess.thecvf.com/content_CVPR_2019/papers/Hou_Learning_a_Unified_Classifier_Incrementally_via_Rebalancing_CVPR_2019_paper.pdf)]
   - クラス不均衡問題に対して，コサイン正規化，忘却抑制制約，Margine Ranking lossによるクラス間分離の3つの主要な機能を用いて対処
 - iTAML : An Incremental Task-Agnostic Meta-learning Approach [[paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Rajasegaran_iTAML_An_Incremental_Task-Agnostic_Meta-learning_Approach_CVPR_2020_paper.pdf)]
   - Inner loopによるタスクに特化した分類器の学習とOuter loopによる汎用的な分類器の学習を行うことでタスクに依存しないクラスインクリメンタル学習手法

## オンライン継続学習
### 教師あり学習
### 教師なし・自己教師あり学習 
 - The Challenges of Continuous Self-Supervised Learning [[paper](https://arxiv.org/abs/2203.12710)]
   - コサイン類似度を使用した冗長性を削減したデータ選択 (MinRed)
 - SCALE: Online Self-Supervised Lifelong Learning without Prior Knowledge [[paper](https://openaccess.thecvf.com/content/CVPR2023W/CLVision/html/Yu_SCALE_Online_Self-Supervised_Lifelong_Learning_Without_Prior_Knowledge_CVPRW_2023_paper.html)]
   - 疑似教師あり対照損失（Pseudo-Supervised Contrastive Loss）
   - 自己教師あり忘却損失（Self-Supervised Forgetting Loss）
   - Online Memory Update (PSA）
  
## 継続学習？？


## その他の関連論文（知識蒸留，自己教師あり学習など）
### 自己教師あり学習
  - EMP-SSL: Towards Self-Supervised Learning in One Training Epoch [[paper](https://arxiv.org/abs/2304.03977)]
    - 1エポックで学習可能な自己教師あり学習法
  - Fast-MoCo: Boost Momentum-based Contrastive Learning with Combinatorial Patches [[paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136860283.pdf)]
    - 自己教師あり学習法MoCov3の収束を早めた手法
### 知識蒸留
