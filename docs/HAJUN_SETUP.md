# Junhyun Ha의 al-folio 홈페이지

공식 [al-folio](https://github.com/alshedivat/al-folio) 원본을 사용했습니다. 기본 색상, 글꼴, 레이아웃, 다크 모드는 변경하지 않았습니다.

- 원본 커밋: `40c06007dab344970b681ba63b2241b1a8209ec1`
- 목표 저장소: `HaJunHyun/HaJunHyun.github.io`
- 목표 주소: `https://hajunhyun.github.io/`
- SIML에서 확인한 영문 이름, KAIST AI 석사과정 소속과 공개 이메일을 반영했습니다.
- 프로필에는 Gravatar의 기본 사람 실루엣 아바타를 사용합니다. 파일은 `assets/img/avatar-default.jpg`입니다.
- PReFlow 논문을 Publications와 홈페이지에 추가하고, 영어 연구 해설을 `/blog/preflow/`에 작성했습니다.
- 프로필과 논문 그림의 출처는 [CONTENT_SOURCES.md](CONTENT_SOURCES.md)에 기록했습니다.
- Projects에는 공개 저장소 `diffusion_rl`, `cvsg`, `KAIRI_MCD`를 연결했습니다.

## GitHub에 게시하기

### 처음 게시할 때

`HaJunHyun/HaJunHyun.github.io` 공개 저장소는 생성되어 있습니다. 소스를 `main` 브랜치에 반영하면 공식 `Deploy site` 워크플로가 사이트를 빌드하고 `gh-pages` 브랜치를 만듭니다.

1. 저장소의 **Actions → Deploy site**가 성공할 때까지 기다리세요.
2. **Settings → Pages → Build and deployment**에서 **Deploy from a branch**, 브랜치 **gh-pages**, 폴더 **/ (root)**를 선택하고 **Save**를 누르세요.
3. Pages 배포가 끝나면 `https://hajunhyun.github.io/`를 확인하세요.

배포 워크플로에 필요한 `contents: write`, `pages: write` 권한은 `.github/workflows/deploy.yml`에 선언되어 있습니다. 이 사이트를 위해 계정 전체의 권한을 바꿀 필요는 없습니다.

원본 al-folio 빌드 과정에 두 가지 게시 처리를 추가했습니다. 완성된 파일에 `.nojekyll`을 넣어 GitHub가 다시 Jekyll을 실행하지 않게 하고, `gh-pages` 갱신 후 Pages 게시를 명시적으로 요청합니다. GitHub Actions의 기본 토큰으로 만든 커밋은 Pages 빌드를 자동으로 시작하지 않기 때문에 필요한 처리입니다. 최초 한 번은 위의 Pages 설정을 저장해야 합니다.

`gh-pages`가 아직 없다면 먼저 `Deploy site`를 실행하거나 실패 로그를 확인하세요. `main` 브랜치를 Pages의 게시 소스로 고르면 원본 Markdown이 제대로 빌드되지 않습니다.

### 소스 반영 방법

이 패키지는 전체 소스입니다. **새로 만든 빈 저장소**에는 압축을 푼 내용물을 그대로 올릴 수 있습니다. 템플릿으로 만든 저장소에는 원본의 데모 파일도 삭제해야 하므로, 단순히 변경 파일 몇 개만 업로드하는 것보다 Git으로 소스 전체를 반영하는 방법이 정확합니다. `.github/workflows/deploy.yml`도 포함해야 합니다.

직접 Git 작업이 익숙하지 않으면 GitHub 앱을 연결해 이 대화에서 이어가는 편이 간단합니다.

공식 설치 안내: [al-folio Quick Start](https://github.com/alshedivat/al-folio/blob/main/docs/QUICKSTART.md)

## 본인 정보 수정하기

| 내용                             | 수정할 파일                   |
| -------------------------------- | ----------------------------- |
| 표시 이름, 사이트 설명, 주소     | `_config.yml`                 |
| 자기소개, 소속, 관심 분야        | `_pages/about.md`             |
| GitHub, 이메일, Scholar, CV 링크 | `_data/socials.yml`           |
| 프로필 사진                      | `_pages/about.md`의 `profile` |
| 실제 논문 목록                   | `_bibliography/papers.bib`    |
| 연구 글                          | `_posts/`                     |

이름을 바꿀 때 `url`과 `repository`의 GitHub 사용자명은 그대로 유지하세요. 개인 홈페이지이므로 `baseurl: ""`도 그대로 둡니다.

홈페이지의 논문 표시는 이미 활성화되어 있습니다. 새 논문을 추가할 때도 홈페이지에 표시하려면 해당 BibTeX 항목에 `selected={true}`를 넣으세요.

CV는 실제 정보가 준비되면 추가할 수 있습니다. 상단 메뉴는 about, blog, publications 구성입니다.

## 연구 글 쓰기

### GitHub에서 현재 글 수정하기

1. [PReFlow 글 파일](https://github.com/HaJunHyun/HaJunHyun.github.io/blob/main/_posts/2026-10-01-preflow.md)을 엽니다.
2. GitHub에 로그인한 상태에서 파일 위의 **연필 아이콘(Edit this file)**을 누릅니다.
3. 아래 안내에 따라 원하는 내용을 고칩니다.
4. **Commit changes…**를 누르고 수정 내용을 짧게 적은 뒤, **Commit directly to the main branch**로 저장합니다.
5. **Actions → Deploy site**와 이어지는 **pages build and deployment**가 성공하면 홈페이지에 자동 반영됩니다.

| 바꾸려는 내용        | 수정할 곳                 |
| -------------------- | ------------------------- |
| 글 제목              | 맨 위의 `title:`          |
| 제목 아래 한 줄 소개 | `description:`            |
| 본문                 | 두 번째 `---` 아래의 글   |
| 소제목               | `## Overview` 같은 줄     |
| 왼쪽 목차            | 맨 위 `toc:`의 `name:` 값 |

소제목을 바꾸면 `toc`의 이름도 똑같이 바꿔야 목차 링크가 맞습니다.
일반 문장만 고칠 때는 `layout`, `date`, `bibliography`, `authors`와 파일명을 그대로 두면 됩니다.

본문은 Markdown입니다. `**중요한 내용**`은 굵게, `[링크 이름](https://example.com)`은 링크가 됩니다.
수식은 기존 글처럼 `$$ ... $$` 안에 씁니다.
그림 설명은 해당 그림의 `<figcaption>`과 `</figcaption>` 사이를 수정하세요.
GitHub의 **Preview**는 기본 Markdown 확인용이고, 수식·그림·목차의 최종 모양은 배포된 홈페이지에서 확인하면 됩니다.

### 본문 가로 폭과 좌우 여백 조절하기

현재 글 맨 위 `_styles:` 안에 있는 `--post-content-width: 880px;`가 본문의 최대 가로 폭입니다.
숫자를 늘리면 글과 표가 더 넓게 펼쳐지고 좌우 여백은 줄어듭니다. 예를 들어 `960px`로 바꾸면 더 넓어지고,
`760px`로 바꾸면 더 좁아집니다. 좁은 화면에서는 화면 폭에 맞춰 자동으로 줄어듭니다.

`--post-side-gap: 24px;`는 작은 화면에서 확보할 최소 좌우 여백입니다.
본문을 넓히려는 경우에는 먼저 `--post-content-width`를 조절하세요.
그림의 개별 `max-width`는 별도 설정이므로 본문 폭을 바꿔도 training time 그림의 480px 제한은 유지됩니다.

### 새 연구 글 추가하기

`_drafts/research-note.md`에 al-folio의 **Distill 글 양식**을 넣었습니다. 이 초안은 기본 배포에 포함되지 않습니다.

현재 게시된 글은 `_posts/2026-10-01-preflow.md`입니다. 이 파일을 GitHub에서 수정하면 논문 해설을 바로 고칠 수 있습니다.
그림은 `assets/img/preflow/`와 `assets/img/publication_preview/preflow.png`에,
글의 참고문헌은 `assets/bibliography/preflow.bib`에 있습니다.

1. 제목, 요약과 본문을 실제 연구 내용으로 바꾸세요.
2. `_posts/YYYY-MM-DD-your-title.md`로 옮기세요. 날짜를 실제 게시 날짜로 바꾸세요.
3. 변경사항을 커밋하면 `/blog/your-title/`에 게시됩니다.

수식은 `$$ ... $$` 안에 LaTeX 문법으로 작성할 수 있습니다. 목차는 글의 `toc` 항목에 맞춰 수정하세요. 이미지 파일은 `assets/img/`에 추가하세요.

## 로컬 빌드

공식 배포와 동일한 Ruby 3.3.5와 Node.js 20 환경에서 실행하세요.

```sh
bundle install
npm ci
bundle exec jekyll build
bundle exec jekyll serve
```

`_site/`가 생성되고 로컬 서버는 보통 `http://localhost:4000/`에서 열립니다.

이 개인 사이트의 `baseurl`은 비어 있습니다. 원본 데모용 문서의 `/al-folio` 옵션을 이 사이트의 빌드에 넣지 마세요.

## 원본에서 정리한 항목

- 예시 인물의 논문, CV, 연락처, 사진과 데모 글을 제거했습니다.
- 외부 블로그 가져오기를 비활성화했습니다.
- 소스 프로젝트의 정기 유지보수 워크플로를 제거하고 공식 `Deploy site`의 빌드 과정을 유지했습니다. 이 사이트의 자동 게시를 위해 `.nojekyll` 생성과 Pages 게시 요청만 추가했습니다.
- 개인 사이트에 쓰이지 않는 원본의 README 미리보기 이미지와 Lighthouse 성능 보고서는 제외했습니다.
- 레이아웃, CSS, 테마 플러그인과 고정된 의존성 버전은 유지했습니다.
- 사용한 원본의 MIT 라이선스는 `LICENSE`에 포함되어 있습니다.

## 이 패키지의 검증 상태

초기 사이트의 설정·콘텐츠 문법, Prettier, 기본 테마 구조 검사, al-folio upgrade audit를 통과했습니다. 초기 8개 HTML 페이지의 내부 링크와 로컬 에셋을 확인했습니다.

이 실행 환경에서는 기본 Sass 네이티브 바이너리가 스레드 정보를 읽지 못했습니다. 사이트 소스와 의존성 버전을 유지한 채, 검증 과정에서만 동일 버전인 Sass 1.100.0의 JavaScript 컴파일러를 사용해 사이트 생성을 확인했습니다. 이 검증용 어댑터는 패키지에 포함하지 않았고, GitHub에서는 원본 배포 워크플로를 사용합니다.

실제 빌드 결과는 저장소의 **Actions → Deploy site**, 게시 여부는 **Settings → Pages**에서 확인할 수 있습니다.

2026-10-01에 GitHub Actions에서도 기본 Sass 컴파일러로 al-folio 빌드가 성공했고, `gh-pages`에 8개 HTML 페이지가 생성된 것을 확인했습니다.
