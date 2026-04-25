# 배포 가이드

이 프로젝트는 Tailwind CDN을 사용하는 단일 정적 `index.html` 파일입니다. 별도의 빌드 과정은 필요하지 않습니다.

## 방법 1: GitHub Pages로 배포하기

GitHub 저장소만으로 무료 정적 웹사이트를 배포하려면 이 방법을 사용하세요.

1. GitHub에서 새 저장소를 만듭니다.
2. 저장소 루트 경로에 `index.html` 파일을 업로드합니다.
3. 로컬에서 작업 중이라면 아래 명령으로 커밋하고 푸시합니다.

```sh
git add index.html
git commit -m "Add business website"
git push origin main
```

4. GitHub에서 해당 저장소 페이지를 엽니다.
5. **Settings > Pages** 메뉴로 이동합니다.
6. **Build and deployment** 항목에서 다음과 같이 설정합니다.
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
7. **Save**를 클릭합니다.

배포가 완료되면 보통 아래 주소로 접속할 수 있습니다.

```text
https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/
```

저장소 이름을 `YOUR_GITHUB_USERNAME.github.io`로 만든 경우에는 아래 주소를 사용합니다.

```text
https://YOUR_GITHUB_USERNAME.github.io/
```

## 방법 2: Vercel로 배포하기

간단한 배포 관리와 커스텀 도메인 연결이 필요하다면 Vercel을 사용할 수 있습니다.

1. 이 프로젝트를 GitHub 저장소에 푸시합니다.
2. [https://vercel.com](https://vercel.com)에 접속합니다.
3. GitHub 계정으로 로그인합니다.
4. **Add New > Project**를 클릭합니다.
5. 배포할 GitHub 저장소를 선택해 Import합니다.
6. 설정은 기본값을 유지합니다.
   - Framework Preset: `Other`
   - Build Command: 비워둠
   - Output Directory: 비워둠
7. **Deploy**를 클릭합니다.

배포가 완료되면 Vercel이 아래와 같은 접속 주소를 제공합니다.

```text
https://your-project-name.vercel.app
```

## Google Play Console 제출 전 확인사항

배포 전에 `index.html`의 플레이스홀더를 실제 정보로 바꾸세요.

- Business Name: `[혁주 님이 정할 영문 상호명 입력]` 교체
- Email: `[본인 이메일]` 교체

배포 후 실제 URL에 접속해서 아래 항목을 확인하세요.

- 하단 푸터에 사업자 정보가 표시되는지 확인
- 개인정보 처리방침이 페이지에 표시되는지 확인
- 이메일 링크가 정상적으로 열리는지 확인
- 모바일과 데스크톱에서 레이아웃이 깨지지 않는지 확인
