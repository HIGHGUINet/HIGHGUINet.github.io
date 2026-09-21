# HIGHGUINet.github.io

Guisik Kim 개인 홈페이지. Jekyll + GitHub Actions로 만들어져서, `main` 브랜치에 push하면
자동으로 빌드되어 `https://highguinet.github.io`에 배포됩니다.

## 논문/수상 추가하는 법 (자동 반영)

1. PDF(또는 이미지) 파일을 `paper/<연도>/` 폴더에 넣는다.
2. `_data/publications.yml`(`type: journal` 또는 `conference`), `_data/awards.yml`(수상),
   `_data/patents.yml`(특허), `_data/news.yml`(뉴스) 중 해당하는 파일에 항목 하나를 추가한다.
3. `git add -A`, `git commit`, `git push` 하면 GitHub Actions가 자동으로 빌드 · 배포한다. (1~2분 소요)

## 최초 1회 설정

1. GitHub에서 `HIGHGUINet/HIGHGUINet.github.io` 이름으로 새 저장소 생성 (Public).
2. 로컬에서:
   ```
   git remote add origin https://github.com/HIGHGUINet/HIGHGUINet.github.io.git
   git branch -M main
   git push -u origin main
   ```
3. 저장소 Settings → Pages → Build and deployment → Source를 **GitHub Actions**로 설정.
4. 잠시 후 `https://highguinet.github.io`에서 확인.

## 로컬 미리보기 (선택, Ruby 필요)

```
bundle install
bundle exec jekyll serve
```

## TODO

- ICIP 2026 Grand Challenge 논문(`ICIP_2026_Grand_Challenge_Paper_GUISIK_KIM_camera_ready.pdf`)
  정식 출판되면 `_data/publications.yml`에 제목 채우고 pdf 필드 추가, `.gitignore`에서도 제거
- ACCV 2026 논문(`418_Interference_Gated_Continu.pdf`)도 정식 출판되면 `_data/publications.yml`에
  정식 항목 추가 (현재는 `_data/news.yml`에 "ACCV 2026 논문 채택"으로만 반영됨)
- 프로필 사진(`figures/나.png`)을 원하는 사진으로 교체 가능
- 특허(`_data/patents.yml`)의 특허번호(US/EP/JP, KOR 미기재분) 채우기

## PDF 게시 정책

다음 PDF는 공개 저장소에 올리지 않습니다 (`.gitignore`에 등록, 로컬 `paper/`에는 남아있음):
- 구독이 필요한 저널(IEEE TIP, T-ITS, GRSL, MTAP, IET Computer Vision 등) 논문
- 아직 정식 출판 전인 논문 (ICIP 2026 Grand Challenge, ACCV 2026)

오픈액세스 저널(IEEE Access, Sensors/MDPI 등)과 이미 출판된 학회/워크숍 논문은 그대로 PDF를
게시합니다.
