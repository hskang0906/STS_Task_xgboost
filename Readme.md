# Used by XGBoost's NLP
- Semantic Similarity Task에서 XGBoost 사용 테스트
- Semantic Similarity Benchmark(stsb) dataset을 사용한 STS Task를 Pytorch lightning으로 구현. 2개의 BERT Model의 CLS Token을 Decoder layer의 입력으로 사용하여, Score를 출력하는 구조. Cosine-similarity를 사용하는 Decoder layer를  XGboostRegressor로 변경
## run_xgb
    - Pretrained Tokenizer만 사용한 구조
    - Tokenized dataset을 XGboostRegressor에 입력으로 사용
## run_bert_xgb
    - Pretrained BERT model의 last_hidden_state를 XGBoostRegressor input으로 사용
    - BERT Model의 Layer는 Freeze.

## STSBoost, YNATboost
    - xgboost와 catboost 차이점 확인을 위한 테스트 코드 @