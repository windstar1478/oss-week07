# P0. 내 저장소 만들기

이 저장소(`oss2026-week07`)는 템플릿입니다. 그대로 복사해서 내 계정에 `oss-week07` 을 만들고, 내 노트북으로 받아 옵니다.

이 문제에서 하는 것:
- 템플릿으로 내 저장소 만들기 (브라우저)
- clone 하고 VS Code 로 열기 (터미널)
- `index.html` 을 브라우저로 열어 보기

## 저장소 만들기 (브라우저)

1. 이 저장소 페이지 오른쪽 위 초록색 **Use this template** → **Create a new repository**.
2. **Owner** 가 내 계정인지 확인하고, **Repository name** 에 `oss-week07` 을 정확히 입력합니다. 확인 스크립트가 이 이름을 찾습니다.
3. **Public** 을 고르고 **Create repository**. 템플릿의 파일이 그대로 들어 있는 내 저장소가 열립니다.

## clone 하고 열기 (터미널, VS Code)

4. 실습 폴더에서 clone 합니다. 주소는 내 저장소의 초록색 **Code** 버튼 → HTTPS 에서 복사합니다.
   ```
   git clone https://github.com/<내 ID>/oss-week07.git
   cd oss-week07
   code .
   ```
5. VS Code 왼쪽 파일 목록에 아래가 보이면 됩니다.
   ```
   images/vongole.jpg
   index.html
   p5_answers.md
   p5_quiz.html
   README.md
   style.css
   ```
   `index.html` 을 열어 보면 `<head>` 에 `<meta charset="utf-8">` 이 미리 들어 있습니다. 이 줄은 "이 파일의 글자는 UTF-8 로 저장되어 있다" 고 브라우저에 알려 줍니다. 지우면 한글이 깨질 수 있으니 그대로 둡니다.

## 브라우저로 열어 보기

6. 파일 탐색기(Mac 은 Finder)에서 `oss-week07` 폴더의 `index.html` 을 더블클릭합니다. 크롬(또는 기본 브라우저)이 열립니다.
7. **확인**: 화면은 하얗게 비어 있고, 브라우저 탭 제목에 `레시피` 가 보이면 됩니다. 주소창은 `file:///.../oss-week07/index.html` 처럼 내 컴퓨터의 파일 경로입니다. 아직 인터넷에 올라간 게 아니라 내 컴퓨터의 파일을 브라우저가 읽어서 그린 것입니다.

   이 브라우저 탭은 실습 내내 열어 둡니다. 파일을 고치고 저장한 뒤 이 탭에서 **F5** 를 누르면 바뀐 화면이 보입니다.

---

[← 문제 목록](../README.md#문제) · [다음: P1](P1_html.md) · [부록: 흔한 오류](../README.md#부록-흔한-오류)
