# 継続学習に関する論文をまとめたリスト
2024年（修士1年）5月から読んだ継続学習に関する論文をまとめたリスト
## Survey論文
  - A Comprehensive Survey of Continual Learning: Theory, Method and Application [[paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10444954&tag=1)]
    - 2024年

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
 - Learning without Forgetting [[paper](https://ieeexplore.ieee.org/ielaam/34/8520726/8107520-aam.pdf?tag=1)]
   - リプレイバッファを使用せず，過去タスクの分類層の出力が変化しないように学習することで知識の忘却を抑制
 - Dark Experience for General Continual Learning: a Strong, Simple Baseline [[paper](https://proceedings.neurips.cc/paper/2020/file/b704ea2c39778f07c617f6b7ce480e9e-Paper.pdf)]
   - 現在モデルと過去モデルのバッファ内の過去タスクのデータに対するlogitsのユークリッド距離を損失として追加
 - Continual Learning with Deep Generative Replay [[paper](https://proceedings.neurips.cc/paper_files/paper/2017/file/0efbe98067c6c73dba1250d2beaa81f9-Paper.pdf)]
   - 生成モデルを使用した継続学習の初期手法
 - Meta-Learning Representations for Continual Learning [[paper](https://papers.nips.cc/paper_files/paper/2019/file/f4dd765c12f2ef67f98f3558c282a9cd-Paper.pdf)]
   - メタ学習法MAMLをベースにした損失MAML-RepとOnline aware Meta-Learningによって学習
 - Rainbow Memory: Continual Learning with a Memory of Diverse Samples [[paper](https://openaccess.thecvf.com/content/CVPR2021/papers/Bang_Rainbow_Memory_Continual_Learning_With_a_Memory_of_Diverse_Samples_CVPR_2021_paper.pdf)]
   - 摂動に対する不確実性を基準に多様なデータをリプレイバッファに保持
 - Incremental Learning of Object Detectors without Catastrophic Forgetting [[paper](https://openaccess.thecvf.com/content_ICCV_2017/papers/Shmelkov_Incremental_Learning_of_ICCV_2017_paper.pdf)]
   - 背景スコアの低いROIに対して知識蒸留を行うことで物体検出における破滅的忘却を阻止

### 教師なし学習・自己教師あり学習
  - Self-Supervised Models are Continual Learners [[paper](https://openaccess.thecvf.com/content/CVPR2022/papers/Fini_Self-Supervised_Models_Are_Continual_Learners_CVPR_2022_paper.pdf)]
    - 多くの自己教師あり学習に適用可能な自己教師あり継続学習のフレームワークを提案
    
## オンライン継続学習
### 教師あり学習
 - Repeated Augmented Rehearsal: A Simple but Strong Baseline for Online Continual Learning [[paper](https://proceedings.neurips.cc/paper_files/paper/2022/file/5ebbbac62b968254093023f1c95015d3-Paper-Conference.pdf)]
   - 強化学習によってリアルタイムでハイパーパラメータを調整することで動的環境に対応
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
  - DisCo: Remedy Self-supervised Learning on Lightweight Models with Distilled Contrastive Learning [[paper](https://arxiv.org/pdf/2104.09124)]
    - 自己教師あり学習の対照学習を対象とした知識蒸留法
