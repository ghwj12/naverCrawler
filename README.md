# 네이버 쇼핑 순위 자동 크롤러

이 프로젝트는 구글 스프레드시트에서 상품 정보를 가져와
네이버 쇼핑 사이트에서 해당 상품을 검색하여 순위를 크롤링 한 후  
다시 시트에 자동 기록해주는 Node.js 백엔드 서버입니다.

---

## 1. 주요 기능

- 구글 시트에서 상품 정보 가져오기
- 네이버 검색 API를 통해 네이버 쇼핑에서 크롤링 + 순위 조회
- 시트에 새 열 추가하여 날짜와 순위 자동 기록
- Apps Script에서 POST로 자동 실행 연동

---

## 2. 준비 사항

- Node.js 18+ 설치
- 구글 서비스 계정 키 파일 (`package-google-key.json`), 네이버 오픈 API 인증 키 파일(`package-naver-key.json`) 별도 준비
- 구글 시트 공유: 서비스 계정 이메일에 "편집자" 권한 부여
- 필요한 NPM 패키지 설치(터미널): npm install

---

## 3. js파일별 기능

- **naver_final_app.js** : Apps Script에서 호출되어 서버와 연동해서 전체 과정 자동 실행(main)
