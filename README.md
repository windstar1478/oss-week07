# 7주차 실습 — HTML & CSS

오늘은 두 부분입니다.

- **Part 1 (혼자)**: 내 저장소에 **레시피 페이지**를 만듭니다. HTML 로 내용을 쓰고, CSS 로 꾸미고, GitHub Pages 로 인터넷에 공개합니다.
- **Part 2 (팀)**: 팀 저장소를 새로 하나 만들어 가상 행사 **OSS Mini Hackathon 2026** 의 소개 페이지를 세 사람이 나눠 만듭니다. 한 사람이 한 섹션씩 PR 로 올리고, 서로 리뷰하고, Pages 로 공개합니다.

막히면 맨 아래 **부록: 흔한 오류**를 먼저 보고, 그래도 안 되면 손을 드세요.

## 규칙

- **Part 1 저장소**: 이 저장소를 템플릿으로 내 계정에 `oss-week07` 을 만듭니다(정확히 이 이름, Public). 문제마다 지정된 **커밋 메시지**를 그대로 씁니다.
- **Part 2 저장소**: 팀원 한 명(A)의 계정에 `oss2026-week07-teamNN` 하나. `NN` 은 두 자리 조 번호입니다(3조 → `oss2026-week07-team03`). 팀 프로젝트 저장소 `oss2026-teamNN` 과는 **다른 저장소**입니다.
- **확인 방법**: 두 저장소의 파일·커밋·PR·리뷰와 Pages 주소를 봅니다. 따로 제출하는 파일은 없습니다.
- 저장소와 페이지 어디에도 **이름·학번을 적지 않습니다.** 팀원은 GitHub 아이디로만 적습니다.
- 파일을 고친 뒤에는 **브라우저에서 새로 고침(F5)해서 눈으로 확인**합니다. 확인이 안 되면 그 문제는 끝난 게 아닙니다.

파일 이름의 `p5_` 처럼 번호가 붙은 파일은 그 문제에서 처음 쓰는 파일입니다. `index.html`, `style.css` 는 여러 문제에서 이어서 고칩니다.

---

## 문제

### Part 1. 혼자 — 레시피 페이지 (`<내 ID>/oss-week07`)

| # | 문제 | 남는 것 |
|---|---|---|
| [P0](problems/P0_setup.md) | [내 저장소 만들기](problems/P0_setup.md) | 저장소 `oss-week07` |
| [P1](problems/P1_html.md) | [HTML 로 레시피 쓰기](problems/P1_html.md) | 커밋 `p1: recipe html` |
| [P2](problems/P2_selectors.md) | [CSS 연결하고 선택자 세 가지 쓰기](problems/P2_selectors.md) | 커밋 `p2: selectors` |
| [P3](problems/P3_box.md) | [박스 모델과 가운데 정렬, DevTools](problems/P3_box.md) | 커밋 `p3: box model` |
| [P4](problems/P4_pages.md) | [GitHub Pages 로 공개하기](problems/P4_pages.md) | Pages 주소, 커밋 `p4: published` |
| [P5](problems/P5_specificity.md) | [우선순위 예측하기](problems/P5_specificity.md) | 커밋 `p5: predictions`, `p5: specificity` |

### Part 2. 팀 — OSS Mini Hackathon 2026 (`<A의 ID>/oss2026-week07-teamNN`)

| # | 누가 | 문제 | 남는 것 |
|---|---|---|---|
| [T0](problems/T0_team_repo.md) | A (B·C 는 수락) | [팀 저장소 만들고 보호하기](problems/T0_team_repo.md) | 저장소, ruleset `protect-main` |
| [T1](problems/T1_my_section.md) | A·B·C 각자 | [내 섹션 PR 올리기](problems/T1_my_section.md) | PR 3개 (`#intro`, `#schedule`, `#faq`) |
| [T2](problems/T2_review.md) | 리뷰어 | [브라우저로 열어 보고 리뷰하기](problems/T2_review.md) | 리뷰(승인), 머지 |
| [T3](problems/T3_pages.md) | A, B (리뷰 C) | [팀 페이지 공개하기](problems/T3_pages.md) | Pages 켜짐, README 에 주소 (PR) |

**역할**: 저장소를 만드는 사람이 A 입니다. B·C 는 팀에서 정합니다. 섹션은 A 가 행사 소개(`#intro`), B 가 일정표(`#schedule`), C 가 참가 안내와 FAQ(`#faq`) 입니다.

**리뷰를 누가 하나**

| PR | 리뷰어 |
|---|---|
| A 의 `#intro` | B |
| B 의 `#schedule` | A |
| C 의 `#faq` | A 또는 B |
| T3 의 README 주소 PR (B 가 올림) | C |

- **C 가 오늘 오지 못했으면**: A·B 는 T0 에서 C 를 초대만 해 두고 T1 ~ T3 를 진행합니다. T3 의 README PR 은 C 를 리뷰어로 지정해 **열어 둔 채로** 둡니다. C 는 나중에 혼자 초대 수락 → clone → T1(내 섹션 PR) → T3 의 PR 리뷰·머지를 합니다. C 의 PR 은 A 나 B 가 알림을 보고 리뷰합니다.
- **두 명뿐인 팀**: C 칸이 없습니다. `#faq` 섹션은 비워 두고, T3 의 README PR 은 A 가 리뷰합니다.

## 끝날 때 갖춰져 있어야 하는 상태

Part 1 (사람마다)
- `<ID>/oss-week07` 이 Public, 커밋 `p1: recipe html` · `p2: selectors` · `p3: box model` · `p4: published` · `p5: predictions` · `p5: specificity` 가 push 됨
- `index.html` 에 `h1`, `h2`, `p`, `strong`, `em`, `ul`, `ol`, `table`, `img`, `a` 가 다 있음
- `style.css` 에 tag · class · id 선택자가 각각 하나 이상, `#wrapper` 에 `margin` 의 좌우 `auto`
- `p5_answers.md` 에 예측과 확인 결과가 적혀 있음
- `https://<ID>.github.io/oss-week07/` 이 열리고 스타일과 그림이 보임

Part 2 (팀 저장소)
- `oss2026-week07-teamNN` 이 A 계정에 Public, B·C 가 collaborator, main 에 ruleset(PR 필수, 승인 1, Merge 만, bypass 비어 있음)
- 세 섹션이 각자의 PR 로 들어감. 머지된 PR 은 전부 작성자가 아닌 팀원의 승인을 받은 뒤 머지됨
- 각 PR 이 `style.css` 에 넣은 선택자는 전부 자기 섹션 id 로 시작함
- `https://<A의 ID>.github.io/oss2026-week07-teamNN/` 이 열리고, README 에 그 주소가 있음

사람마다 (Part 2)
- 내 섹션 PR 이 머지됨 (C 는 결석했으면 나중에)
- 다른 팀원의 PR 하나 이상에 내 승인이 있음

---

## 부록: 흔한 오류

| 증상 | 원인 → 해결 |
|---|---|
| 파일을 고쳤는데 브라우저 화면이 그대로 | 저장 안 함(VS Code 탭 제목 옆 ●) → `Ctrl+S` 뒤 F5. 그래도 그대로면 `Ctrl+F5`(캐시 무시 새로 고침) |
| 한글이 `ê¹€ì¹˜` 처럼 깨짐 | `<head>` 의 `<meta charset="utf-8">` 을 지웠거나 그 아래로 옮김 → `<head>` 맨 위에 다시 |
| CSS 를 썼는데 아무 변화가 없음 | `<link rel="stylesheet" href="style.css">` 가 없거나 파일 이름 오타 → F12 → **Console** 에 빨간 `404` 가 있으면 경로 문제 (P2 2번) |
| CSS 규칙 하나만 안 먹음 | 선택자 오타(`.sumary`), HTML 에 class 를 안 붙임, 중괄호·세미콜론 빠짐, 또는 다른 규칙에 짐 → F12 → **Elements** 에서 그 요소를 고르고 **Styles** 를 봄. 줄이 그어진 선언이 진 쪽 |
| 그림이 깨진 아이콘으로 보임 | `src` 경로 오타 또는 폴더 이름 틀림(`image/` vs `images/`) |
| 로컬에선 되는데 Pages 에서만 CSS·그림이 안 나옴 | **대소문자**가 다름(`Style.css`, `Dish.svg`). Windows 는 대소문자를 가리지 않지만 Pages 는 가립니다 → 파일 이름과 HTML 의 경로를 똑같이 맞춤 |
| Pages 주소가 `404 There isn't a GitHub Pages site here` | 배포가 아직 안 끝남(1 ~ 2분, **Actions** 탭 확인) / Branch 를 `None` 그대로 둠 / 폴더를 잘못 고름 / `index.html` 이 저장소 맨 위에 없음 |
| Pages 에 고친 내용이 안 나옴 | push(Part 1) 또는 머지(Part 2)를 안 함 / 배포 중 / 캐시 → `Ctrl+F5` |
| Settings 에 **Pages** 메뉴가 안 보임 | 저장소 주인이 아님. 팀 저장소의 Pages 는 A 만 켤 수 있음 |
| push 가 `GH013: Repository rule violations found for refs/heads/main` 으로 거부됨 | 팀 저장소 main 에 직접 push 함 → 커밋을 브랜치로 옮기기: `git branch <새 브랜치>` → `git reset --hard origin/main` → `git checkout <새 브랜치>` → `git push -u origin <새 브랜치>` 로 PR |
| 리뷰할 PR 브랜치가 `git checkout` 으로 안 받아짐 (`did not match any file(s) known to git`) | `git fetch` 를 안 함 → `git fetch` 후 다시 (T2 2번) |
| 리뷰하다가 내 섹션 파일을 고쳐 버림 | 리뷰 브랜치에서는 고치지 않습니다 → `git restore .` 로 되돌리고 `git checkout main` |
| 내 PR 에 `This branch has conflicts` | 정해진 칸 밖을 고침(공통 부분, 다른 사람 칸) → 내 칸만 고치도록 브랜치를 정리. 모르겠으면 손을 드세요 |
| 머지 상자가 계속 `Checking for the ability to merge automatically…` | GitHub 이 아직 계산 중 → 1 ~ 2분 뒤 F5 |
| `Pull request authors can't approve their own pull request` | 내 PR 은 내가 승인할 수 없음 → 리뷰어 표대로 팀원에게 |
| 커밋했더니 편집기가 열림 | `-m` 없는 commit. VS Code 면 `Ctrl+S` 뒤 탭 닫기. Vim 이면 `Esc` → `:wq` Enter |
