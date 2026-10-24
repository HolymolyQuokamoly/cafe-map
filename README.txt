서울·경기 실제 카페 분석 지도 — GitHub Pages 배포용

1. 이 압축파일을 먼저 윈도우에서 '모두 압축 풀기' 하세요.
2. 안에는 index.html 과 data 폴더가 있습니다.
3. GitHub 저장소 https://github.com/holymolyquokamoly/cafe-map 에 로그인하세요.
4. 저장소 최상단에서 Add file > Upload files를 선택하세요.
5. index.html 및 data 폴더 속 파일 4개를 올려 다음 구조로 만들어 주세요.
   /index.html
   /data/areas.csv
   /data/points_seoul.json
   /data/points_gyeonggi.json
   /data/seoul_commercial.geojson
   ※ ZIP 파일 자체를 GitHub에 올려서는 사이트에 반영되지 않습니다.
   ※ 폴더째 업로드가 되지 않는 경우, GitHub의 Create new file에서
      data/.gitkeep 파일을 먼저 생성해 data 폴더를 만들고,
      data 폴더 화면에서 4개 파일을 Upload files 하세요.
6. index.html 파일을 GitHub에서 열고 연필 아이콘(Edit)을 클릭하세요.
7. const VWORLD_API_KEY = ''; 줄에 이전에 발급받은 V-World 키를
   따옴표 안에 입력하세요. 이 채팅으로 키를 보내지 마세요.
   기존 공개 사이트에 키가 들어 있다면 그 값을 개인적으로 보관한 다음에 새 버전으로 교체하세요.
8. Commit changes 버튼으로 저장하세요.
9. 기존 주소 https://holymolyquokamoly.github.io/cafe-map/ 접속 후
   Ctrl+Shift+R 또는 시크릿 창으로 최신 파일을 확인하세요.
10. 브이월드에서 GitHub Pages 서비스 URL 제한, 공개 사용 정책,
    인증키 사용량/만료일을 꼭 확인하세요.

구성: HTML, CSS, JavaScript, OpenLayers, 브이월드 지도 API + 정적 CSV/JSON/GeoJSON.
별도 Python 서버나 유료 웹서버는 필요 없습니다.

실제 데이터 출처 및 범위:
- 소상공인시장진흥공단 상가(상권)정보 2026년 6월 말, I21201 카페.
- 서울 22,739개/경기 27,048개/총 49,787개, 56개 시군구.
- 서울 실제 상업지역 안의 카페: 4,944개, 면적: 25.910017㎢
  (점포: 2026.6, 상업지역 경계: 2026.9, 면적: 2025.12).
- 공간도형의 union 면적 26.498249㎢와 면적 통계 25.910017㎢는 시점 및 산출 방식이 다릅니다.
- 경기도 상업지역 내 카페 실제 개수는 아직 확인되지 않았습니다.
- 인구 1만 명당 카페 수는 검증된 인구 자료가 없어 표시하지 않았습니다.
- 식별 48개 브랜드는 상호명 기준으로 분류했으며 공식 전체 가맹점 수가 아닙니다.
- 49,787개 개별 점포 좌표는 실제 데이터이며 최대 3,000개씩 화면에 표시합니다.
  단일 지역 지도 확대(12레벨 이상)에서 점포 표시 옵션을 선택하세요.
