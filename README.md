# HIT ME! — 친구 전용 샌드백 클리커

## 실행하기
1. `index.html`을 더블클릭해서 브라우저에서 열기
2. 기본 비밀번호 `hitme2026` 입력
3. 친구에게 배포하기 전 `index.html` 맨 아래쪽의 `SITE_PASSWORD` 값을 바꾸기

## GitHub Pages 배포
1. GitHub에서 새 저장소(repository)를 만들고 이름을 `hit-me-clicker` 등으로 지정
2. `index.html`과 `README.md`를 저장소 최상위(root)에 업로드
3. 저장소의 **Settings → Pages**로 이동
4. **Deploy from a branch** 선택
5. Branch는 `main`, 폴더는 `/ (root)` 선택 후 Save
6. 잠시 기다리면 `https://깃허브아이디.github.io/저장소이름/` 형태의 주소가 생성됨

## 비밀번호 관련 중요 안내
현재 비밀번호 확인은 브라우저 안의 JavaScript에서 이루어지는 간단한 입장 잠금입니다.
따라서 소스 코드를 볼 수 있는 사람은 비밀번호를 알아낼 수 있으며, 사이트 주소 자체도 공개 URL입니다.
민감한 정보나 진짜 비공개 공간을 보호하는 보안 기능은 아닙니다. 실제 접근 제어가 필요하면 Firebase Authentication 등 서버 측 인증을 붙여야 합니다.

## 현재 기능
- SD 캐릭터의 얼굴/몸통/팔/다리 클릭
- 주먹/손바닥/빠따/채찍 도구 선택
- 타격 효과 애니메이션과 간단한 효과음
- 총 타격/콤보/최고 콤보
- 기기별 브라우저 저장(localStorage)
- 모바일 반응형 화면

기록은 현재 기기에만 저장됩니다. 여러 친구의 기록을 합산하는 실시간 랭킹은 Firebase 연결이 필요한 다음 단계 기능입니다.
