# 식물 관찰 학습 웹앱

## 준비물

- Windows
- Node.js 18 이상
- Docker에서 실행 중인 AnythingLLM
- AnythingLLM Developer API 키

## 실행 방법

1. `.env` 파일을 메모장으로 엽니다.
2. 다음 두 항목을 입력하고 저장합니다.

   ```env
   ANYTHINGLLM_API_KEY=발급받은_Developer_API_키
   ANYTHINGLLM_WORKSPACE_SLUG=워크스페이스_slug
   ```

   `workspace slug`는 AnythingLLM 워크스페이스 주소의 `/workspace/` 뒤에
   표시되는 값입니다.

3. Docker AnythingLLM이 `http://localhost:3001`에서 실행 중인지 확인합니다.
4. `start.bat`을 더블 클릭합니다.
5. 브라우저에서 `http://127.0.0.1:8765`를 엽니다.

`.env`를 수정했다면 실행 중인 서버 창에서 `Ctrl+C`를 누른 후
`start.bat`을 다시 실행해야 합니다.

## 보안 및 기능 안내

- API 키는 브라우저로 전달되지 않고 로컬 Node.js 서버에서만 사용됩니다.
- `.env`는 Git에 포함되지 않습니다.
- 왼쪽에서 선택한 사진은 로컬 미리보기용이며 AnythingLLM에는 전송되지 않습니다.
- 사진에 관해 질문하려면 사진에서 관찰한 특징을 채팅에 글로 입력해 주세요.

## 문제 해결

- `설정 필요`: `.env`의 API 키와 workspace slug를 확인합니다.
- `API 키가 올바르지 않습니다`: AnythingLLM의 Developer API에서 발급한 키인지 확인합니다.
- `연결할 수 없습니다`: Docker와 AnythingLLM이 실행 중인지 확인합니다.
- `포트 8765가 이미 사용 중`: 기존에 실행한 `start.bat` 창을 종료합니다.
