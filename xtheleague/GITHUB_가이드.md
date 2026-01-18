# GitHub Pages 배포 가이드

## 📋 준비물
- GitHub 계정
- 프로젝트 파일들 (이 폴더의 모든 파일)

## 🚀 배포 단계

### 1단계: GitHub 저장소 생성
1. GitHub.com에 로그인
2. 우측 상단 "+" 클릭 → "New repository" 선택
3. Repository name: `xtheleague` (또는 원하는 이름)
4. Public으로 설정
5. "Create repository" 클릭

### 2단계: 파일 업로드
**방법 A: 웹 인터페이스 사용 (쉬움)**
1. 생성된 저장소에서 "uploading an existing file" 클릭
2. 모든 파일을 드래그 앤 드롭
   - index.html
   - README.md
   - .gitignore
   - images 폴더 전체
3. "Commit changes" 클릭

**방법 B: Git 사용 (추천)**
```bash
# 터미널에서 실행
cd xtheleague
git init
git add .
git commit -m "Initial commit: X the League website"
git branch -M main
git remote add origin https://github.com/yourusername/xtheleague.git
git push -u origin main
```

### 3단계: GitHub Pages 활성화
1. 저장소 페이지에서 "Settings" 클릭
2. 왼쪽 메뉴에서 "Pages" 클릭
3. Source 섹션에서:
   - Branch: `main` 선택
   - Folder: `/ (root)` 선택
4. "Save" 클릭

### 4단계: 배포 확인
- 몇 분 후 사이트가 활성화됩니다
- URL: `https://yourusername.github.io/xtheleague/`
- 페이지 상단에 초록색 체크 표시가 나타나면 배포 완료!

## 📝 업데이트 방법

### 파일 수정 후:
```bash
git add .
git commit -m "Update: 설명"
git push
```

### 웹에서 직접 수정:
1. GitHub 저장소에서 파일 클릭
2. 연필 아이콘 클릭 (Edit)
3. 수정 후 "Commit changes"

## ⚠️ 주의사항

1. **이미지 경로**: 모든 이미지가 `images/` 폴더에 있는지 확인
2. **파일 이름**: 파일명에 공백이나 특수문자 없는지 확인
3. **대소문자**: 파일명 대소문자가 HTML과 일치하는지 확인
4. **배포 시간**: 변경사항 반영까지 1-5분 소요

## 🔧 문제 해결

### 이미지가 안 보일 때:
- 파일명이 정확한지 확인
- 경로가 `images/파일명.png` 형식인지 확인
- GitHub 저장소에 이미지가 업로드되었는지 확인

### 페이지가 안 뜰 때:
- Settings → Pages에서 배포 상태 확인
- Actions 탭에서 배포 로그 확인
- index.html이 루트에 있는지 확인

### 수정사항이 반영 안 될 때:
- 브라우저 캐시 삭제 (Ctrl+Shift+R 또는 Cmd+Shift+R)
- 5분 정도 대기 후 재확인

## 📞 도움말

GitHub Pages 공식 문서: https://pages.github.com/
GitHub 지원: https://support.github.com/

---

성공적인 배포를 기원합니다! 🎉
