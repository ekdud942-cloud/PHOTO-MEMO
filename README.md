# 포토 메모장

구글 로그인 후 내 계정에만 사진이 저장되는 메모장. Firebase(Auth + Firestore) 사용.

## 구성

| 파일 | 설명 |
| --- | --- |
| `index.html` | 앱 전체 (HTML + CSS + JS, 단일 파일) |
| `firestore.rules` | Firestore 보안 규칙 (본인 `users/{uid}` 데이터만 읽기/쓰기) |

## 시작하기

1. [Firebase 콘솔](https://console.firebase.google.com)에서 프로젝트를 만들고 웹 앱을 등록합니다.
2. **Authentication** → 로그인 방법에서 **Google**을 활성화합니다.
3. **Firestore Database**를 생성합니다.
4. `firestore.rules` 내용을 Firestore 규칙에 붙여넣고 게시합니다.
5. `index.html`의 `firebaseConfig`(`YOUR_PROJECT` 부분)를 본인 프로젝트 설정값으로 바꿉니다.
6. `index.html`을 브라우저로 열거나 정적 호스팅(GitHub Pages, Firebase Hosting 등)에 올립니다.

## 사용법

1. 구글 계정으로 로그인합니다.
2. 사진과 메모를 추가합니다.
3. 데이터는 로그인한 계정별로 저장되어 다른 사람은 볼 수 없습니다.

## 기술 스택

- Firebase Authentication (Google 로그인)
- Cloud Firestore
- Vanilla JavaScript (Firebase JS SDK 10.12.2, CDN)
