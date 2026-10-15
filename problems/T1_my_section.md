# T1. 내 섹션 PR 올리기 — A·B·C 각자

세 사람이 페이지의 섹션을 하나씩 맡아, 각자 브랜치에서 만들고 PR 로 올립니다. HTML 은 `index.html` 의 내 섹션 안에, CSS 는 `style.css` 의 내 칸에만 씁니다.

| | A | B | C |
|---|---|---|---|
| 섹션 | 행사 소개 `#intro` | 일정표 `#schedule` | 참가 안내와 FAQ `#faq` |
| 브랜치 | `intro` | `schedule` | `faq` |
| 커밋 메시지 | `feat: intro section` | `feat: schedule section` | `feat: faq section` |
| 리뷰어 | B | A | A 또는 B |

세 사람이 **동시에** 진행합니다. 각자 다른 줄만 고치므로 순서가 엉켜도 충돌은 나지 않습니다.

## 지켜야 할 것: 내 칸만, 내 id 로 시작

`style.css` 는 세 사람이 같이 쓰는 파일입니다. 맨 위 **공통** 부분은 건드리지 않고, 아래의 내 칸에만 씁니다.

```css
/* ===== B: #schedule ===== */
/* 선택자는 #schedule 로 시작합니다. 예: #schedule table { ... } */
#schedule table {      ← 여기부터 B 가 씀
  ...
}
```

**모든 선택자를 내 섹션 id 로 시작합니다.** `table { ... }` 처럼 쓰면 페이지의 모든 표가 바뀝니다. 지금은 표가 B 의 것 하나뿐이라 문제가 없어 보여도, 나중에 다른 사람이 표를 넣으면 그 표까지 바뀝니다. `#schedule table` 은 "`#schedule` 안에 있는 표" 만 고릅니다.

## 브랜치 만들기 (터미널)

1. main 을 최신으로 받고, 내 브랜치를 만듭니다.
   ```
   git checkout main
   git pull
   git checkout -b <브랜치>
   ```

## 내 섹션 HTML (VS Code)

2. `index.html` 에서 내 섹션의 `<!-- X 가 이 안을 채웁니다 -->` 줄을 지우고, 그 자리에 아래 내 칸의 내용을 넣습니다. 내용은 그대로 써도 되고, 행사 정보는 바꾸지 말고 문장만 다듬어도 됩니다.

### A — `#intro`

```html
      <h1>OSS Mini Hackathon 2026</h1>
      <p>하루 동안 <strong>오픈소스 프로젝트에 첫 기여</strong>를 해 보는 <em>작은</em> 해커톤입니다.</p>
      <p>2026년 11월 21일(토) 10:00 – 18:00 · 가상 캠퍼스 홀</p>
      <a class="cta" href="#faq">참가 안내 보기</a>
```
마지막 링크의 `href="#faq"` 는 다른 페이지가 아니라 **이 페이지의 `id="faq"` 위치**로 가는 링크입니다. 머리글 메뉴의 링크도 같은 방식입니다.

### B — `#schedule`

```html
      <h2>일정</h2>
      <table>
        <tr><th>시간</th><th>프로그램</th></tr>
        <tr><td>10:00</td><td>등록과 팀 확인</td></tr>
        <tr><td>10:30</td><td>오프닝: 오늘 기여할 저장소 소개</td></tr>
        <tr><td>11:00</td><td>이슈 고르기와 첫 PR</td></tr>
        <tr><td>13:00</td><td>점심</td></tr>
        <tr><td>14:00</td><td>멘토와 코드 리뷰</td></tr>
        <tr><td>17:00</td><td>머지된 PR 공유와 마무리</td></tr>
      </table>
```

### C — `#faq`

```html
      <h2>참가 안내</h2>
      <ul class="info">
        <li>대상: Git 과 GitHub 를 써 본 학부생 누구나</li>
        <li>준비물: 노트북, GitHub 계정</li>
        <li>참가비: 없음</li>
      </ul>
      <h3>자주 묻는 질문</h3>
      <p class="question">혼자 참가해도 되나요?</p>
      <p class="answer">됩니다. 현장에서 3명씩 팀을 만듭니다.</p>
      <p class="question">오픈소스 기여가 처음인데 괜찮나요?</p>
      <p class="answer">괜찮습니다. 처음 기여하는 사람을 위한 쉬운 이슈를 미리 골라 둡니다.</p>
```

3. 저장하고 브라우저에서 F5. 내 칸에 내용이 들어오면 됩니다. 아직 꾸미지 않아 기본 모양입니다.

## 내 섹션 CSS (VS Code)

4. `style.css` 의 내 칸, 안내 주석 바로 아래에 씁니다. 아래 **해야 할 것** 을 채우는 규칙을 직접 씁니다. 값(색, 크기)은 마음대로 정합니다.

### A — `#intro`
- 섹션 안의 글자를 가운데 정렬
- `.cta` 링크를 버튼처럼: 안쪽 여백(`padding`), 배경색, 흰 글자, 밑줄 없애기(`text-decoration: none`), 둥근 모서리(`border-radius`)
- 힌트: `a` 는 글자처럼 줄 안에 놓이는 요소라 위아래 `padding` 이 제대로 자리를 차지하지 않습니다. `display: inline-block;` 을 같이 쓰면 상자처럼 자리를 잡습니다.

### B — `#schedule`
- 표를 섹션 폭 전체로(`width: 100%`), 두 겹 선을 하나로(`border-collapse: collapse`)
- 칸(`th`, `td`)에 안쪽 여백과 아래쪽 선(`border-bottom`), 글자 왼쪽 정렬
- 머리줄(`th`)에 배경색
- 힌트: `th` 와 `td` 에 같은 규칙을 줄 때는 `#schedule th, #schedule td { ... }` 처럼 쉼표로 묶습니다. 쉼표 뒤도 `#schedule` 로 시작합니다.

### C — `#faq`
- 질문(`.question`)은 굵게, 아래 여백 0
- 답(`.answer`)은 회색, 위 여백 작게 — 질문과 답이 한 덩어리로 붙어 보이게

5. 저장하고 F5. 내 섹션만 바뀌고 **다른 칸과 머리글·바닥글은 그대로**인지 봅니다.
6. F12 → **Elements** 에서 내 섹션 안의 요소를 하나 누르고 **Styles** 를 봅니다. 내가 쓴 규칙이 적용되어 있고, 선택자가 `#내섹션 …` 으로 시작하면 됩니다.

## 커밋, push, PR (터미널 → 브라우저)

7. ```
   git add index.html style.css
   git commit -m "<커밋 메시지>"
   git push -u origin <브랜치>
   ```
8. 저장소 페이지의 노란 띠 **Compare & pull request** → **base: main ← compare: `<브랜치>`** 확인.
9. 설명에 씁니다. `<ID>` 는 리뷰어의 아이디입니다.
   ```
   ## What
   <섹션 이름> 섹션을 채웠습니다.

   ## Checklist
   - [x] index.html 의 내 섹션 안만 고침
   - [x] style.css 의 내 칸에만, 선택자는 #<내 섹션 id> 로 시작
   - [ ] 리뷰어가 브라우저로 열어 봄

   @<ID> 리뷰 부탁합니다.
   ```
10. 오른쪽 **Reviewers** 에서 위 표의 리뷰어를 고르고 **Create pull request**.
11. **Files changed** 탭을 열어 봅니다. 바뀐 파일이 `index.html`, `style.css` 두 개이고, 초록 줄이 내 섹션과 내 칸에만 있으면 됩니다. 다른 곳에 빨간 줄(지운 줄)이 있으면 실수로 지운 것입니다. VS Code 에서 되살려 저장하고 커밋, push 하면 PR 에 자동으로 더해집니다.

리뷰와 머지는 [T2](T2_review.md) 에서 합니다.

---

[← 문제 목록](../README.md#문제) · [이전: T0](T0_team_repo.md) · [다음: T2](T2_review.md) · [부록: 흔한 오류](../README.md#부록-흔한-오류)
