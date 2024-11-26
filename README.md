# KoBERT
Developed an automated industry name matching algorithm using KoBERT

KoBERT 모델을 통한 업종 추천 정확도 테스트

1. **train_data.xlsx**: 국세청 11차 표준산업분류 업종명에 대한 학습 키워드
*************************
2. **test_data.xlsx**: 소상공인시장진흥공단_상가(상권)정보 데이터에서 확보한 테스트 키워드
* 다른 테스트 데이터가 있을 경우, 해당 데이터로 코드 상에서 적용 가능
*************************
3. **KoBERT_model.bin**: 'kykim/bert-kor-base' 사전 학습(pre-trained) 모델을 사용해 train_data.xlsx을 학습시킨 모델 (bin 형식의 파일)


## KoBERT Model

Hugging Face의 kykim/bert-kor-base KoBERT 사전 학습 모델을 사용 (https://huggingface.co/kykim/bert-kor-base)

- tokenizer = BertTokenizer.from_pretrained('kykim/bert-kor-base')
- bert_model = BertModel.from_pretrained('kykim/bert-kor-base')
