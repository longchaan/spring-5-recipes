스프링5 레시피 (4판) Spring 5 Recipes: A Problem-Solution Approach
- 마틴 데니엄(Marten Deinum), 다니엘 루비오(Daniel Rubio), 조시 롱(Josh Long)
- 이일웅 역
- 한빛미디어, 2018 / Apress, 2017.10.11

STS 3.8.4 Neon.3 (4.6.3)
- Project SDK: jdk1.8.0\_92 (java version "1.8.0_92") 
- Buildship: Eclipse Plug-ins for Gradle 1.0.21.v20161010-1640
- New Gradle Project (gradle-2.14.1)

# 1 스프링 개발 툴

## 1-1 STS로 스프링 애플리케이션 빌드하기

- https://github.com/Apress/spring-5-recipes.git

### 메이븐 프로젝트 임포트, 빌드하기

- File > Import > Existing Maven Project
- spring-recipes-4th/ch01/springintro_mvn 디렉터리를 지정

### 그레이들 프로젝트 임포트, 빌드하기

> Maven project (i.e., pom.xml file) → Gradle project (i.e., build.gradle file)
- bootstrap plug-in at http://gradle.org/docs/current/userguide/bootstrap_plugin.html
- maven2gradle tool at https://github.com/jbaruch/maven2gradle.git

- File > Import > Existing Gradle Project
- spring-recipes-4th/ch01/springintro 디렉터리를 지정
- Gradle Tasks 탭: springintro 프로젝트 > build 메뉴 열기 > build 오른쪽-클릭 Run Gradle Tasks
- Gradle Tasks 뷰: springintro 프로젝트 > application (plugin)열기 > run 더블-클릭
- ▷ Run Configurations... 클릭 > Main class: com.apress.springrecipes.hello.Main 입력
