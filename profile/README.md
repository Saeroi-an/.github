![프로젝트 미리보기](./main.png)


# 새로이 안(安)

당신의 편안한 진료를 위해, <br>
사용자 맞춤 AI 의료 서비스 

---

## 🌐 소개 (Overview)

새로이 + 편안할 안(安)

한국에 체류하고 있는 외국인을 위한 의료서비스입니다. <br>
더 이상 어렵게 한국어로 이야기하지 않아도 돼요. <br>
새로이 안으로 간편하게 본인의 증상을 전달해보세요!<br>
사용자 정보를 기반으로 처방전 인식, 셀프 진단 체크, 주변 정보를 제공받습니다. <br>

---

## 🌐 공모전 (Contest)

![공모전](./AI.png)

'인공지능(AI), 충북의 미래를 디자인하다'<br>
전국 ICT 융합 공모전을 함께 준비하고있습니다. 

---

## 🌐 기능 (Features)

![기능1](./service1.png)
![기능2](./service2.png)
![기능3](./service3.png)



## 🌐 주요 기능 (Features)
- 사용자 정보 입력 및 관리
- AI 기반 처방전 인식 및 채팅
- 셀프 진단 체크
- 다국어 지원 (한국어 / 중국어 / 영어)
- React Native + FastAPI 연동 구조

## 🌐 AI 모델 (AI)
- base model: [Qwen/Qwen2.5-VL-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-VL-7B-Instruct)
- LoRA 파인튜닝: [참고 url]([https://github.com/2U1/Qwen-VL-Series-Finetune](https://github.com/QwenLM/Qwen-VL))
- 🤗 hugging face: [Rfy23/qwenvl-7B-medical-ko-zh](https://huggingface.co/Rfy23/qwenvl-7B-medical-ko-zh)

---
## 🌐 프로젝트 실행 가이드 (Set up)
프론트엔드와 백엔드로 구성된 프로젝트입니다. 아래 실행 가이드를 순서대로 지켜주세요.

### 1단계: 백엔드 서버 활성화(EC2)
⚠️ 앱 실행 전, API 서버가 정상적으로 동작하고 있어야 합니다. 
EC2 인스턴스는 비용 절감을 위해 사용하지 않을 때 중지할 수 있습니다. AWS Console에서 인스턴스를 시작/중지하고싶으시면 문의부탁드립니다.

**EC2 인스턴스 접속**
   ```bash
   ssh -i your-key.pem ubuntu@your-ec2-ip
```

**서비스 상태 확인 및 시작**
 ```bash
   # 서버 상태 확인
sudo systemctl status saeroi-an-backend

# 서버가 중지되어 있다면 시작
sudo systemctl start saeroi-an-backend
```

**코드 업데이트 및 배포**
 ```bash
cd /path/to/backend
git pull origin main
source venv/bin/activate
pip install -r requirements.txt
sudo systemctl restart saeroi-an-backend
```

### 2단계: 프론트엔드 설정 및 앱 실행
프론트엔드 코드는 [여기](https://github.com/Saeroi-an/FrontEnd)에서 확인할 수 있습니다.

우리 프로젝트 프론트엔드 링크를 눌러 git clone을 하거나 아래 git clone bash를 copy 해주세요. 
 ```bash
git clone https://github.com/Saeroi-an/FrontEnd.git
```
**의존성 패키지 설치**
 ```bash
npm install
# 또는
yarn install
```

⚠️ 프로젝트 루트에 .env.example 파일을 복사하여 .env을 생성해야합니다. 원하시면 문의부탁드립니다. 

**Expo 개발 서버 실행**
 ```bash
npx expo start
```

### 3단계: 모바일 기기 실행
**'Expo Go'앱 설치**
- iOS: [App Store 다운로드 링크](https://apps.apple.com/us/app/expo-go/id982107779)
- Android의: [Play Store 다운로드 링크](https://play.google.com/store/apps/details?id=host.exp.exponent&hl=ko)

---

## 🌐 기술 스택 (Tech Stack)
| 분류 | 사용 기술 |
|------|------------|
| Frontend | React Native (Expo), JavaScript |
| Backend | FastAPI, Python, PostgreSQL |
| Database | Supabase |
| AI | Hugging Face, Qwen2.5-VL-7B-Instruct |
| Deployment | AWS S3, Ngrok |

---
## 🌐 함께한 팀원(Members)
| 팀원 | 역할 |
|------|------------|
| [신우림(팀장)](https://github.com/Rainwoorimforest) | AI, LangChain |
| [정혜주](https://github.com/f020202) | Front-End, Design |
| [이희재](https://github.com/huioid2) | Back-end |
