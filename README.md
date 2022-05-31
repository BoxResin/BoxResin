![header](https://capsule-render.vercel.app/api?type=waving&color=0:2C70CE,100:006AFB&fontColor=FFFFFF&height=200&section=header&text=Profile)

<div>
<a href="https://solved.ac/profile/boxresin">
    <img src="http://mazassumnida.wtf/api/v2/generate_badge?boj=boxresin" align="right"/>
</a>

<p>
    <img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=Android&logoColor=white"/>
    <img src="https://img.shields.io/badge/Windows-0078D6?style=flat-square&logo=Windows&logoColor=white"/>
</p>

<p>
    <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=C&logoColor=black"/>
    <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=C%2B%2B&logoColor=white"/>
    <img src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=Java&logoColor=white"/>
    <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=Kotlin&logoColor=white"/>
    <img src="https://img.shields.io/badge/ReactiveX-B7178C?style=flat-square&logo=ReactiveX&logoColor=white"/>
    <img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=Jenkins&logoColor=white"/>
    <img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=Firebase&logoColor=black"/>
</p>

<p>
    <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=GitHub&logoColor=white"/>
    <img src="https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=GitLab&logoColor=white"/>
    <img src="https://img.shields.io/badge/Bitbucket-0052CC?style=flat-square&logo=Bitbucket&logoColor=white"/>
    <img src="https://img.shields.io/badge/Slack-4A154B?style=flat-square&logo=Slack&logoColor=white"/>
    <img src="https://img.shields.io/badge/Trello-0052CC?style=flat-square&logo=Trello&logoColor=white"/>
    <img src="https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=Jira&logoColor=white"/>
    <img src="https://img.shields.io/badge/Confluence-172B4D?style=flat-square&logo=Confluence&logoColor=white"/>
</p>
</div>

# 소개
- 2010년 C언어로 프로그래밍 입문 및 Win32 API를 통한 윈도우즈 프로그램 개발
- 2011년 `Java`와 `C++` 입문
- 2012년 Android 입문
- 2013년 ~ 현재 구글 Play 스토어에 [급식 앱](https://play.google.com/store/search?q=%EA%B8%89%EC%8B%9D&utm_source=github) 운영 중
- 前 [㈜버즈니](https://buzzni.com/) Android 클라이언트 엔지니어

<div align="center">
    <img src="https://github-readme-stats.vercel.app/api?username=boxresin&count_private=true&show_icons=true&bg_color=2A2B37&title_color=2C70CE&icon_color=2C70CE&text_color=CCCCCC&locale=kr&line_height=40"/>
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=boxresin&bg_color=2A2B37&title_color=2C70CE&icon_color=2C70CE&text_color=CCCCCC&locale=kr&&hide=javascript,html,nsis"/>
</div>

# JCenter에 배포했던 라이브러리
오픈소스를 진행 중인 프로젝트에 맞게 수정하거나, 직접 작성한 코드 중 유용한 부분을 추출하여 배포했던 라이브러리입니다. 현재 JCenter 서비스가 종료된 관계로 더 이상 새로운 업데이트는 게시하지 않고 있습니다.

<div align="center">

[<img src="https://github-readme-stats.vercel.app/api/pin/?username=boxresin&repo=AndroidThreadSwitcher"/>](https://github.com/BoxResin/AndroidThreadSwitcher)
[<img src="https://github-readme-stats.vercel.app/api/pin/?username=boxresin&repo=JavaHTTP"/>](https://github.com/BoxResin/JavaHTTP)
[<img src="https://github-readme-stats.vercel.app/api/pin/?username=boxresin&repo=MarkdownViewSupport"/>](https://github.com/BoxResin/MarkdownViewSupport)
[<img src="https://github-readme-stats.vercel.app/api/pin/?username=boxresin&repo=AndroidCameraHelper"/>](https://github.com/BoxResin/AndroidCameraHelper)

</div>

# 오픈소스 기여
## kotlinx.coroutines
- [`Flow<T>.collectLatest()` 함수 제안](https://github.com/Kotlin/kotlinx.coroutines/issues/1269)
    - `Flow<T>.collect()`와 달리 `Flow<T>`에 새로운 값이 emit 되면 기존의 collect 작업을 취소하고 새로 collect 하는 함수.
    - [급식 앱](https://play.google.com/store/apps/details?id=winapi251.app.schoolmeal)에서, 설정된 학교(`Flow<School>`)가 변경될 때(emit), 이전 학교의 급식 정보를 불러오는 작업을 '즉시' 중단하고 새 학교의 급식 정보를 불러와야 했으나 `collect()` 함수로는 불가능했기에 `collectLatest()`를 제안함.
    - 코루틴 `v1.3.0`에 실제 반영됨. [릴리즈 노트](https://github.com/Kotlin/kotlinx.coroutines/releases/tag/1.3.0-rc2) 참조.

## detekt
- [패키지 네이밍 규칙 수정 기여](https://github.com/detekt/detekt/pull/1434)
    - [Kotlin 공식 코딩 컨벤션](https://kotlinlang.org/docs/coding-conventions.html#naming-rules)에 따라, 패키지 이름에 대문자가 오더라도 문제삼지 않도록 정규표현식 수정
    > Names of packages are always lowercase and do not use underscores (`org.example.project`). Using multi-word names is generally discouraged, but if you do need to use multiple words, you can either just concatenate them together or use camel case (`org.example.myProject`).

## butterknife
- [`annotationProcessor` 관련 문제 해결방법 공유](https://github.com/JakeWharton/butterknife/issues/908#issuecomment-298167584)
    
    ![image](https://user-images.githubusercontent.com/13031505/171043844-fff83f6d-0e24-4741-8e6b-ae7d7b88b8ed.png)
    - 지금까지 게시했던 댓글 중 👍를 제일 많이 획득

## Material-Calendar-View
- [`values-ko/strings.xml` 한국어 번역 기여](https://github.com/Applandeo/Material-Calendar-View/pull/133)

## mockk
- [의존 라이브러리 버전 업데이트 기여](https://github.com/mockk/mockk/pull/162)

## koin
- [`README.md`의 사소한 오타 수정 기여](https://github.com/InsertKoinIO/koin/pull/478)
