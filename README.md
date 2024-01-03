# 🚧 ForumChatbot 🚧
[🌐WIZnet 포럼🌐](https://forum.wiznet.io/) 은 WIZnet 제품과 관련된 다양한 토론과 질문을 포함하고 있는 온라인 커뮤니티입니다. 

이 레포지토리는 WIZnet 포럼 데이터를 추출하고 정제하는 과정을 담고 있습니다.

## 🎯 목표
이 프로젝트의 주요 목표는 다음과 같습니다.

- 📊 db로 구조화된 forum데이터에서 특정 열의 데이터만 추출한다.
- 📝 같은 페이지에 있는 QnA 작성 글들을 묶어 하나의 데이터 세트로 만든다.
- 🤖 QnA를 구분할 수 있는 chatbot을 만들고 instruction을 부여한다. (개인정보 삭제, 무응답 내용 설정 등)
- 📩 chatbot에게 가공된 QnA 데이터 세트를 제공받는다.
 
## 📌 주요 기능
- GPT 통합: 인간과 같은 반응을 생성하기 위해 고급 GPT3.5 turbo와 GPT4-turbo 모델을 사용합니다. (금액적인 측면에서 필요한 내용만 4-turbo를 사용.)
- 데이터베이스 전처리: DB로 구조화된 forum데이터에서 특정 열의 데이터만 추출하고 개인정보, 무응답, 재촉하는 글 등의 비활용적 요소들을 제거해나가는 작업을 합니다.
- 데이터 생성: QnA를 구분할 수 있는 간단한 instruction을 부여한 chatbot에게 기존 DB에 있는 내용을 재가공 시킵니다.


## 📚 파일 소개
| 파일명                                                                                              | 설명                                      |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------|
| [GPTs 설정.txt](https://github.com/WzAcorn/ForumChatBot/tree/main/GPTs%20설정.txt)| GPTs 모델에 부여한 role 확인 파일    |
| [dbConnect.ipynb](https://github.com/WzAcorn/ForumChatBot/tree/main/dbConnect.ipynb)   | forumdb를 가져와 필요한 정보만 남기고 제거하는 코드  |
| [forum_makedata_by_Chatbase.ipynb](https://github.com/WzAcorn/ForumChatBot/tree/main/forum_makedata_by_Chatbase.ipynb)    | Chatbase로 QnA데이터를 정제시킨 코드          |
| [forum_makedata_by_OpenAi.ipynb](https://github.com/WzAcorn/ForumChatBot/tree/main/forum_makedata_by_OpenAi.ipynb)     | OpenAi로 QnA데이터를 정제시킨 코드  |
| [forum_dataset_reduced1~N.ipynb](https://github.com/WzAcorn/ForumChatBot/tree/main/forum_dataset_reduced1~4698.csv)     | 챗봇을 통해 정제된 data.csv파일  |
