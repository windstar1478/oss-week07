# T3. 팀 페이지 공개하기 — A (Pages), B (README PR), C (리뷰)

[P4](P4_pages.md) 에서 내 저장소로 한 것을 팀 저장소에서 한 번 더 합니다. 팀 저장소의 Pages 는 저장소 주인 A 만 켤 수 있습니다. 주소는 B 가 README 에 PR 로 넣고, C 가 리뷰합니다.

팀 페이지 주소는 이렇게 됩니다.
```
https://<A의 ID>.github.io/oss2026-week07-teamNN/
```

## A: Pages 켜기 (브라우저)

1. 팀 저장소 **Settings** → **Pages** → **Source** 가 **Deploy from a branch** → **Branch** 를 **main**, 폴더 **/ (root)** → **Save**. Branch 목록에 `intro`, `schedule` 같은 브랜치가 같이 보일 수 있습니다(머지 뒤 Delete branch 를 안 누른 경우). 반드시 **main** 을 고릅니다.
2. **Actions** 탭의 `pages build and deployment` 가 초록 체크가 되면 **Settings → Pages** 에서 F5 → **Visit site**.
3. **확인**: T2 의 11번과 같은 페이지가 `https://<A의 ID>.github.io/oss2026-week07-teamNN/` 에서 보이면 됩니다. 주소를 팀원에게 알려 줍니다.
4. 저장소 첫 화면 **About** 의 톱니바퀴 → **Use your GitHub Pages website** 체크 → **Save changes**.

## B: README 에 주소 넣기 (터미널, VS Code → 브라우저)

5. ```
   git checkout main
   git pull
   git checkout -b readme-url
   ```
6. `README.md` 의 `페이지 주소:` 줄 뒤에 A 가 알려 준 주소를 씁니다.
7. ```
   git add README.md
   git commit -m "docs: add page url"
   git push -u origin readme-url
   ```
8. PR 을 만들고 **Reviewers** 에 **C** 를 지정합니다. (두 명뿐인 팀은 A.)

## C: 리뷰하고 머지 (브라우저)

9. PR 의 **Files changed** 에서 주소를 확인하고, 그 주소를 브라우저에서 열어 팀 페이지가 뜨는지 봅니다.
10. 줄 댓글 하나 → **Approve**. 승인 뒤 C 가 **Merge pull request** → **Confirm merge** → **Delete branch**.

C 가 오늘 오지 못했으면 이 PR 은 열어 둔 채로 둡니다. C 가 나중에 9 ~ 10번을 합니다.

## 모두: 확인

11. 팀 저장소 첫 화면의 README 에 페이지 주소가 보이고, 그 링크를 누르면 팀 페이지가 열리면 됩니다.

---

[← 문제 목록](../README.md#문제) · [이전: T2](T2_review.md) · [부록: 흔한 오류](../README.md#부록-흔한-오류)
