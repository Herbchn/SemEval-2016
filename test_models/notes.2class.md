Baseline (majority class):
==========================
awk 'NF {print $0 "\tpositive"}' data/dev/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.2
Micro-averaged MAE: 0.261157
Accuracy:           0.738843

awk 'NF {print $0 "\tpositive"}' data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.2
Micro-averaged MAE: 0.171875
Accuracy:           0.828125

sentiment_2_class_3_iters_1685_cost.model
=========================================

Description:
------------
Classification: 2 class
Cost: 1,685
# of iterations: 3
Vector dimension: 31
# of convolution filters width 2: 2
# of convolution filters width 3: 2
# of convolution filters width 4: 2

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_3_iters_1685_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1853425
Micro-averaged MAE: 0.3793388

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_3_iters_1685_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1787528
Micro-averaged MAE: 0.3215726

sentiment_2_class_300_iters_1293_cost.model
===========================================

Description:
------------
Classification: 2 class
Cost: 1293
# of iterations: 300
Vector dimension: 31
# of convolution filters width 2: 2
# of convolution filters width 3: 2
# of convolution filters width 4: 2

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_3_iters_1685_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.182682
Micro-averaged MAE: 0.4677686

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_3_iters_1685_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1389531
Micro-averaged MAE: 0.3848286

sentiment_2_class_150_iters_1457_cost.model
===========================================
Description:
------------
Classification: 2 class
Cost: 1457
# of iterations: 150
Vector dimension: 31
# of convolution filters width 2: 2
# of convolution filters width 3: 4
# of convolution filters width 4: 8

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_150_iters_1457_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.2090165
Micro-averaged MAE: 0.4033058

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_150_iters_1457_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1751286
Micro-averaged MAE: 0.3036794

sentiment_2_class_300_iters_1633_cost.model
===========================================
Description:
------------
# Classification: 2 class
# Cost: 1633
# of iterations: 300
# Vector dimension: 31
# of convolution filters width 2: 2
# of convolution filters width 3: 4
# of convolution filters width 4: 8
# +dropout +He initialization
# Classification: 2 class

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_150_iters_1457_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.2
Micro-averaged MAE: 0.261157

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_150_iters_1457_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.2
Micro-averaged MAE: 0.171875

sentiment_2_class_100_iters_1194_cost.model
===========================================
Description:
------------
# Classification: 2 class
# Cost: 1194
# of iterations: 100
# Vector dimension: 31
# of convolution filters width 2: 2
# of convolution filters width 3: 4
# of convolution filters width 4: 8
# -dropout +He initialization +mean LSTM
# Classification: 2 class

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_100_iters_1194_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1789907
Micro-averaged MAE: 0.3347107

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_100_iters_1194_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1345986
Micro-averaged MAE: 0.2368952

Time:
-----
# no CUDNN (could not configure), no minibatches
Iteration #0: cost = 1487.7169513507 (110.00000 sec)
Iteration #1: cost = 1372.2523398520 (110.00000 sec)
Iteration #2: cost = 1330.8701465991 (113.00000 sec)

# no CUDNN, with minibatches
Iteration #0: cost = 7144.4065179974 (119.00000 sec)
Iteration #1: cost = 6429.2302158028 (113.00000 sec)
Iteration #2: cost = 5689.7521182895 (120.00000 sec)

sentiment_2_class_100_iters_1825_cost.model
===========================================
the same as the prvious one, but with mini-batches

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_100_iters_1194_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.2
Micro-averaged MAE: 0.261157

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_100_iters_1194_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.2
Micro-averaged MAE: 0.171875

sentiment_2_class_100_iters_1194_cost.model
===========================================
Description:
------------
# Classification: 2 class
# Cost: 1194
# of iterations: 100
# Vector dimension: 64
# of convolution filters width 2: 2
# of convolution filters width 3: 4
# of convolution filters width 4: 8
# -dropout +He initialization +sum LSTM
# Classification: 2 class

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_300_iters_1201_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1882593
Micro-averaged MAE: 0.5231405

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_300_iters_1201_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1380789
Micro-averaged MAE: 0.4322077

sentiment_2_class_100_iters_1148_cost.model
===========================================
Description:
------------
# Classification: 2 class
# Cost: 1194
# of iterations: 100
# Vector dimension: 64
# of convolution filters width 2: 2
# of convolution filters width 3: 4
# of convolution filters width 4: 8
# -dropout +He initialization +mean LSTM +Highway (wrong)
# Classification: 2 class

Results:
--------
Dev:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_100_iters_1148_cost.model data/dev/topic-two-point.BD.msg.dev.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.167226
Micro-averaged MAE: 0.4983471
Accuracy:           0.5016529

Train:
./scripts/twitter_sentiment test -m test_models/sentiment_2_class_100_iters_1148_cost.model data/train/topic-two-point.BD.train.txt | ./scripts/evaluate.py
Macro-averaged MAE: 0.1519615
Micro-averaged MAE: 0.5272177
Accuracy:           0.4727823