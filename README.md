# EdgeUp GitHub Pages 배포본

이 폴더의 파일을 GitHub 저장소 루트에 그대로 업로드하면 됩니다.

- `index.html`: EdgeUp 메인 페이지
- `CNAME`: `www.edgeup.kr` 커스텀 도메인 지정
- `.nojekyll`: GitHub Pages에서 Jekyll 처리를 건너뜀

## GitHub Pages 설정

1. 저장소 `Settings > Pages`로 이동
2. `Source`를 `Deploy from a branch`로 선택
3. `main` 브랜치, `/ (root)` 선택 후 Save
4. Custom domain이 자동으로 `www.edgeup.kr`로 잡히지 않으면 직접 입력
5. DNS의 `www` CNAME을 `<GitHub아이디>.github.io`로 연결

## 배포 후 확인

브라우저 Console에서 아래를 실행했을 때 FINEDEAL 링크가 여러 개 보여야 합니다.

```js
[...document.querySelectorAll('a[href*="finedeal.co.kr"]')]
```

FINEDEAL 지원 버튼은 iframe/JavaScript navigation 없이 일반 `<a>` 링크로 유지되어 있습니다.
