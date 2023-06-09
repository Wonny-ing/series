# 📌 **주어진 OMDb API를 활용하여 영화 검색 사이트 만들기**

## ✨ 결과물

### 🔗 배포 링크 및 코드

- https://gleeful-cobbler-a450de.netlify.app

- https://github.com/Wonny-ing/KDT3-M2

### ⚙️ 사용 기술

<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white"> <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=Bootstrap&logoColor=white"> <img src="https://img.shields.io/badge/Javascript-E7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black"> <img src="https://img.shields.io/badge/github-white?style=for-the-badge&logo=github&logoColor=black">

### 📃설명

- 전부 vanilla js로 구현했습니다.
- 각 기능별로 모듈화를 하였습니다.
- bootstrap를 통해 전부 디자인하려 했지만 실패하여 헤더 부분과 로딩이미지만 적용해 보았습니다.
- hash event를 사용하여 검색된 영화들의 리스트들이 보이는 페이지와 영화 상세페이지를 볼 수 있도록 하였습니다.

### 구현 사항
- [x] 영화 제목으로 검색 가능하고 검색된 결과의 영화 목록이 출력돼야 합니다.
- [x] jQuery, React, Vue 등 JS 라이브러리와 프레임워크는 사용하지 않아야 합니다.
- [x] 스타일(CSS) 라이브러리나 프레임워크 사용은 자유입니다.
- [x] 실제 서비스로 배포하고 접근 가능한 링크를 추가해야 합니다.
- [x] 한 번의 검색으로 영화 목록이 20개 이상 검색되도록 만들어보세요.
- [x] 영화 개봉연도로 검색할 수 있도록 만들어보세요.
- [x] 영화 목록을 검색하는 동안 로딩 애니메이션이 보이도록 만들어보세요.
- [x] 무한 스크롤 기능을 추가해서 추가 영화 목록을 볼 수 있도록 만들어보세요.
- [x] 영화 포스터가 없을 경우 대체 이미지를 출력하도록 만들어보세요.
- [x] 단일 영화의 상세정보(제목, 개봉연도, 평점, 장르, 감독, 배우, 줄거리, 포스터 등)를 볼 수 있도록 만들어보세요.
- [x] 영화 상세정보가 출력되기 전에 로딩 애니메이션이 보이도록 만들어보세요.
- [x] 영화 상세정보 포스터를 고해상도로 출력해보세요.(실시간 이미지 리사이징)
- [x] 차별화가 가능하도록 프로젝트를 최대한 예쁘게 만들어보세요.

### ✏️ 아쉬운점 및 어려웠던점

- 영화를 검색 후, 영화 상세페이지를 클릭하고 뒤로 가기를 했을때, 그 전 페이지 그대로인 화면을 나오게 하고 싶었으나 다음페이지의 목록들을 보여주는 문제가 발생하였습니다. 페이지 값을 초기화해도 해당 문제가 계속 발생하였고 결국 해결하지 못해 뒤로 가기를 했을때 초기화면이 나오도록 구현했습니다.
- 모듈화를 하는 과정에 있어 어려움을 겪었지만 성공은 했습니다. 하지만 제대로 했는지에 대한 의문이 듭니다.

### 💡 질문 및 피드백 요청

- 뒤로가기를 했을 때, 영화 검색목록이 페이지 변화없이 그대로 보여질 수 있게 하려면 어떻게 해야할지 궁금합니다. (우선은 header영역의 search버튼을 눌렀을때 작동하는 renderSearch 함수가 작동하도록 구현하여 초기화면이 나오도록 했습니다.)
  - renderSearch 함수가 작동하지 않도록 구현될 경우 문제점 : initMovieDetails 함수를 통해 영화 상세페이지를 초기화 시켜주고 영화리스트들이 담겨있는 div가 보여지도록 설정을 하면 안에 기존에 검색된 영화들의 데이터가 나오지 않습니다.
- 무한스크롤을 `Intersection Observer`를 적용하여 구현하였습니다. **Scroll Event**에서 호출 수를 제한하는 방법인 throttle를 사용하지 않아도 된다는 점과 특정 요소만 감지할 경우 작동한다는 장점때문에 사용을 하였습니다.
  - 문제점 : 검색버튼을 눌렀을 때 무한 스크롤 기능을 하도록 구현을 했는데, 이때 화면이 초기화되면서 footer영역이 보이면서 자동으로 addBtnMovies함수가 실행되는것을 발견했습니다. 이 문제를 방지하기 위해 movies container에 footer가 안보이도록 min-height값을 주는것으로 해결했지만 더 좋은 방법이 있을지 궁금합니다.
