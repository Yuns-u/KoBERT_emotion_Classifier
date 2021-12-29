# KoBERT_emotion_Classifier
2021.12.29 -
KoBERT을 사용해서 한국어 대화의 감정 분류 모델 만들기

# 프로젝트 시작하게 된 계기
자연어처리를 할 때 감정이 라벨링되어 있지 않아 애를 먹었기 때문이다.
이를 보다 효율적으로 처리해보고자 한국어  BERT 모델을 사용하여 한국어로 이루어진 대화 문장에 대한 감정 분석을 해보고자 한다.
한국어로 이루어진 짧은 대화 텍스트가 어떠한 감정(긍정,부정)인지 예측하는 다중분류(특히 이중분류) 모델을 만들어볼 수 있다.

# KoBERT 소개
KoBERTsms SKTBrain에서 공개한 기계번역모델로 BERT모델을 기반으로 하는 모델이다. 
한국어 위키의 5백만개의 문장과 5천 4백만개의 단어를 학습시킨 모델로 대화엔진개발을 위해 만들어졌다고 한다.
BERT모델은 2018년 구글에서 발표된 기계번역모델로 약 33억개의 방대한 양의 데이터로 사전학습되어 있으며 자신의 사용 목적에 따라 finetuning이 가능하다.

# 선정 데이터
AI HUB에서 제공하는 '한국어 감정 정보가 포함된 단발성 대화 데이터셋'[https://aihub.or.kr/keti_data_board/language_intelligence] 사용.
AI HUB는 Bleu 30점 이상으로 품질이 일반적인 데이터보다 우수하며 해당 데이터는 단발성 대화이라는 점에서 1:다 대화의 감정을 분석하는 데에 적절하다 판단됨.

# 해야할 일
- 긍정, 부정, 중립으로 다중분류를 하도록 위의 데이터의 7가지 감정을 단순화하기
