# Statistics Visualization Hosting

이 프로젝트는 GitHub Pages를 통해 호스팅되도록 구성되었습니다.
`index.html` 파일이 메인 진입점 역할을 하며, `iframe`을 사용하여 왼쪽에 메뉴를 두고 오른쪽에 각 HTML 파일의 내용을 보여줍니다.

## GitHub Pages 배포 방법

1. 이 저장소(Repository)를 GitHub에 Push합니다.
2. GitHub 저장소 페이지에서 **Settings(설정)** 탭으로 이동합니다.
3. 왼쪽 사이드바에서 **Pages** 메뉴를 클릭합니다.
4. **Build and deployment** 섹션의 **Source**에서 **Deploy from a branch**를 선택합니다.
5. **Branch** 항목에서 **main** (또는 master) 브랜치를 선택하고 폴더는 `/(root)`를 선택한 후 **Save**를 클릭합니다.
6. 잠시 후 상단에 생성된 웹사이트 주소(URL)가 표시됩니다. (예: `https://username.github.io/repo-name/`)

## 파일 구조

- `index.html`: 좌측 메뉴와 콘텐츠 영역을 포함한 메인 레이아웃 파일입니다.
- `*.html`: 통계 시각화 자료들이 담긴 개별 HTML 파일들입니다.

## 새로운 파일 추가 시

새로운 HTML 파일을 폴더에 추가한 경우, `index.html` 파일을 열어 `<ul class="menu-list">` 부분에 아래와 같이 `<li>` 항목을 추가해주어야 합니다.

```html
<li class="menu-item">
    <a href="새로운파일이름.html" target="content-frame" class="menu-link">메뉴에표시될이름</a>
</li>
```

