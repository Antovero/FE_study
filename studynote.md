# FE_study

1. ES6
- ECMA Script 6 버전 이다. 차세대 자바스크립트 문법. 현재는 ES5를 대부분 표준으로 쓰며 프로젝트를 제작하고 있다. 

2. GIT
- 분산 버전 관리 시스템
- 현재 대표적인 형상 관리 툴이자, 프로젝트 제작시에 필수적으로 사용해야 하는 시스템.
- GITHUB 를 이용하여 실제로 로컬 작업물을 웹상에 REMOTE 할 수 있다.

Node.js는 확장성 있는 네트워크 어플리케이션 개발에 사용되는 소프트웨어 플랫폼입니다. 특시 서버사이드에서 많이 사용되곤 합니다. 사용되는 언어로는 자바스크립트(Javascript)를 활용하며, Non-blocking I/O 와 단일 스레드 이벤트 루프를 통한 높은 처리 성능을 가지고 있는 특징을 가지고 있습니다.

내장 HTTP 서버 라이브러리르 포함하고 있어 웹 서버에서 아파치 등의 별도 소프트웨어 없이 동작하는 것이 가능하며, 이를 통한 웹 서버의 동작에 있어 더 많은 통제에서 벗어나 여러가지 기능을 가능하게 합니다.

즉 Node.js 를 통해 웹어플리케이션이 더욱 발전하게 되었으며, 정적인 홈페이지 뿐만 아니라 쇼핑몰, 티켓 예메사이트, 블로그 등 data가 변하는 사이트를 만들 수 있으며, 여러 개발자들이 만든 프로그램과 게임을 웹상에서 구동시켜 안드로이드폰, 아이폰, 윈도우PC, 맥 등 플랫폼의 제약에 벗어나 어디든 상관없이 실행이 가능하게 해줍니다.

2. Node.Js
- Chrome v8 Javascript 엔진으로 빌드된 Javascript 런타임. (여기서 중요한 포인트는 '런타임')
    1) 런타임이란
    - 런타임은 프로그램이 실행되고 있을 때, 존재하는 그곳을 의미한다.
    - 즉, 프로그래밍 언어가 구동되고 있는 환경
        ex) JS는 web browser 와 Node.js 환경에서 구동되는 두 측면이 있고, Browser 와 Node.js 를 런타임이라고 볼 수 있다.
- 예전에는 JS 런타임은 Web Browser 밖에 존재하지 않았음.
- Node.Js 가 그 한계를 극복


3. NPM
- npm은 nodeJS 기반의 모듈을 모아둔 저장소이자, Node package Manager 이다.


4. GULP 
- 프로젝트 제작 시, 반복적인 작업을 일괄적으로 처리해주는 툴. (하단의 BABEL과 콜라보레이션 예시 주목)


5. BABEL (+GULP)
- ES6 에서 ES5 로 변환해주는 트랜스컴파일러.

ex)
// GULP를 이용한 BABEL 사용  (ES6 to ES5)

const gulp = require('gulp');
const babel = require('gulp-babel');

gulp.task('babel', function() {
    gulp.src("es6/**/*.js")
    .pipe(babel())
    .pipe(gulp.dest("dist"));

    gulp.src("public/es6/**/*.js")
    .pipe(babel())
    .pipe(gulp.dest("public/dist"));
});

6. LINT