# 배당금 캘린더 V_0.97 - 안드로이드 APK 만들기

어제와 완전히 동일한 방식입니다. 안드로이드 아이콘은 초록 원 안에 흰색 달러($) 기호로 만들어 두었습니다.

## 1단계 — 새 GitHub 저장소 만들기
1. https://github.com 에서 우측 상단 `+` → `New repository`
2. 이름 예: `dividend-app-v097` → `Create repository`

## 2단계 — 파일 업로드
1. 빈 저장소 화면에서 **"uploading an existing file"** 클릭
2. 이 압축을 컴퓨터에서 먼저 풀고, 안의 파일/폴더 전체(`android`, `www`, `package.json` 등)를 통째로 끌어다 놓기
3. **주의**: `.github` 폴더는 이름이 점(.)으로 시작해서 컴퓨터에서 끌어다 놓을 때 숨김 폴더로 취급되어 자동으로 빠질 수 있습니다.
   업로드 후 저장소에 `.github/workflows/build-apk.yml` 파일이 보이는지 꼭 확인하세요.
   안 보이면 저장소 화면에서 **Add file → Create new file** → 파일명에 `.github/workflows/build-apk.yml` 입력 →
   이 압축 안의 같은 파일 내용을 그대로 붙여넣고 Commit.
4. **"Commit changes"** 클릭

## 3단계 — 자동 빌드 확인
1. 저장소 상단 **Actions** 탭 클릭
2. "Build Android APK" 워크플로우가 3~5분 내로 완료(초록 체크)됩니다
3. 완료된 항목 클릭 → 맨 아래 **Artifacts**에서 `dividend-calendar-v097-debug-apk` 다운로드 → 압축 풀면 `app-debug.apk`

## 4단계 — 휴대폰 설치
1. `app-debug.apk`를 휴대폰으로 전송 후 설치
2. "출처를 알 수 없는 앱" 경고가 뜨면 설정에서 허용 후 재설치
3. 바탕화면에 초록 원 + 흰색 $ 아이콘의 "배당금캘린더" 앱이 생깁니다

## 참고
- 어제 만든 이전 버전 앱과 패키지 이름(ID)을 다르게 설정해서(`com.dividend.calendar.v097`), 휴대폰에 **둘 다 따로 설치**됩니다. 기존 앱을 덮어쓰지 않습니다.
- 혹시 빌드가 실패(빨간 X)하면, 어제처럼 실패한 단계를 클릭해서 나오는 에러 로그를 캡처해서 보내주세요.
