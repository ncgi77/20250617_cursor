## 개인 이력서/포트폴리오 웹사이트

이 프로젝트는 개인 이력서 및 포트폴리오를 효과적으로 보여주기 위해 제작된 정적 웹사이트입니다. 반응형 디자인으로 다양한 기기에서 최적화된 경험을 제공하며, 한국어와 영어 두 가지 언어를 지원합니다.

### 주요 기능

- **반응형 디자인**: 데스크톱, 태블릿, 모바일 등 모든 기기에서 보기 좋게 조정됩니다.
- **다국어 지원**: 한국어와 영어로 이력서 내용을 볼 수 있습니다.
- **동적 콘텐츠 로딩**: 모든 이력서 데이터는 `js/data.js` 파일에서 관리되며, `js/script.js`를 통해 동적으로 페이지에 렌더링됩니다.
- **섹션별 탐색**: 소개, 학력, 경력, 프로젝트, 기술, 연구, 수상 섹션을 통해 쉽게 이동할 수 있습니다.
- **대화형 모달**: "CONTACT ME" 버튼과 프로젝트 카드 클릭 시 상세 정보를 보여주는 모달 창이 제공됩니다.

### 사용된 기술

- **HTML5**: 웹 페이지 구조를 정의합니다.
- **CSS3**: `css/style.css`를 사용하여 웹사이트의 시각적 디자인과 레이아웃을 담당합니다. 변수(`:root`)를 활용하여 테마 관리가 용이합니다.
- **JavaScript (ES6+)**: `js/data.js`에 정의된 데이터를 불러와 `js/script.js`에서 동적으로 콘텐츠를 렌더링하고, 언어 전환, 모달 제어 등 모든 동적 기능을 처리합니다.
- **Google Fonts**: `Noto Sans KR` 폰트를 사용하여 가독성을 높였습니다.
- **인라인 SVG**: 다양한 섹션 아이콘 및 연락처 아이콘을 제공합니다.

### 프로젝트 구조

```
.
├── index.html
├── README.md
├── assets/
│   └── images/
│       ├── profile.png
│       └── projects/
│           ├── project1.png
│           ├── project2.png
│           └── project3.png
├── css/
│   └── style.css
└── js/
    ├── data.js
    └── script.js
```

- `index.html`: 웹사이트의 메인 HTML 파일입니다.
- `README.md`: 이 프로젝트에 대한 설명 파일입니다.
- `assets/`: 이미지와 같은 정적 자산이 저장됩니다.
  - `images/`: 프로필 사진 및 프로젝트 썸네일 이미지가 포함됩니다.
- `css/`: 웹사이트의 스타일시트 파일이 저장됩니다.
  - `style.css`: 모든 CSS 규칙이 정의된 메인 스타일 파일입니다.
- `js/`: JavaScript 파일이 저장됩니다.
  - `data.js`: 이력서/포트폴리오에 표시될 모든 구조화된 데이터(개인 정보, 학력, 경력, 프로젝트, 기술 등)를 한국어와 영어로 포함하고 있습니다.
  - `script.js`: `data.js`의 데이터를 사용하여 HTML 요소를 동적으로 생성하고, 언어 전환, 모달 기능 등 사용자 상호작용을 처리합니다.

### 설치 및 실행 방법

이 프로젝트는 정적 웹사이트이므로 별도의 빌드 과정이나 서버 설정이 필요하지 않습니다.

1.  이 저장소를 클론(clone)하거나 다운로드합니다:
    ```bash
    git clone <저장소-URL>
    cd <프로젝트-디렉토리>
    ```
2.  `index.html` 파일을 웹 브라우저에서 엽니다.
    (예: 파일을 더블 클릭하거나, 브라우저의 '파일 열기' 기능을 사용합니다.)

### 콘텐츠 맞춤 설정

자신의 이력서 내용으로 웹사이트를 맞춤 설정하려면 `js/data.js` 파일을 편집하면 됩니다. 이 파일은 JSON과 유사한 JavaScript 객체 형식으로 구조화되어 있어, 각 섹션의 내용을 쉽게 수정할 수 있습니다. 한국어(`kor`)와 영어(`eng`) 필드를 적절히 채워 넣으세요.

```javascript
// js/data.js 예시
const cvData = {
  personalInfo: {
    name: {
      kor: "홍길동",
      eng: "Gildong Hong",
    },
    tagline: {
      kor: "혁신을 추구하는 소프트웨어 엔지니어",
      eng: "Innovative Software Engineer",
    },
    // ...
  },
  // ...
};
```

### 사용 방법

- **언어 전환**: 상단 내비게이션 바의 "KOR" 또는 "ENG" 버튼을 클릭하여 언어를 전환할 수 있습니다.
- **섹션 이동**: 내비게이션 메뉴를 클릭하여 해당 섹션으로 부드럽게 스크롤됩니다.
- **프로젝트 상세 보기**: 프로젝트 섹션에서 각 프로젝트 카드에 있는 "프로젝트 보기" 버튼을 클릭하여 프로젝트의 상세 설명을 모달로 확인할 수 있습니다.
- **연락하기**: 사이드바 하단의 "CONTACT ME" 버튼을 클릭하여 연락처 모달을 열 수 있습니다.

### 기여

이 프로젝트는 개인 포트폴리오 목적으로 제작되었습니다. 기능 추가나 버그 수정에 대한 기여는 환영합니다. 풀 리퀘스트를 보내주세요.

### 라이선스

이 프로젝트는 MIT 라이선스에 따라 배포됩니다. 자세한 내용은 `LICENSE` 파일을 참조하세요 (현재 프로젝트에 포함되어 있지 않지만, 필요한 경우 추가할 수 있습니다).

### 문의

추가 질문이 있으시면 [gildong.hong@example.com](mailto:gildong.hong@example.com)으로 연락주세요.
