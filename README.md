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
> - bootstrap plug-in at http://gradle.org/docs/current/userguide/bootstrap_plugin.html
> - maven2gradle tool at https://github.com/jbaruch/maven2gradle.git

- File > Import > Existing Gradle Project
- spring-recipes-4th/ch01/springintro 디렉터리를 지정
- Gradle Tasks 탭: springintro 프로젝트 > build 메뉴 열기 > build 오른쪽-클릭 Run Gradle Tasks
- Gradle Tasks 뷰: springintro 프로젝트 > application (plugin)열기 > run 더블-클릭
- ▷ Run Configurations... 클릭 > Main class: com.apress.springrecipes.hello.Main 입력

## 1-3 메이븐 CLI로 스프링 애플리케이션 빌드하기

- http://maven.apache.org/download.cgi 에서 메이븐을 내려받기
- https://downloads.apache.org/maven
- https://archive.apache.org/dist/maven

```
$ tar -xzvf apache-maven-3.5.0-bin.tar.gz
```

```
$ export JAVA_HOME=/usr/lib/jvm/java-8-openjdk/
```

```
$ export PATH=$PATH:/home/www/apache-maven-3.5.0/bin
```

- 예제 소스를 내려받아 압축 해제 후 ch01/springintro_mvn 디렉터리로 이동
- mvn 명령으로 springintro_mvn 애플리케이션을 빌드

## 1-4 메이븐 래퍼로 스프링 애플리케이션 빌드하기

- ./mvnw package 명령을 실행하면 메이블을 자동으로 내려받고 빌드까지 수행
- 예제 소스 ch01/springintro_mvn에서 ./mvnw로 메이븐 래퍼를 실행하면 자동 빌드

## 1-5 그레이들 래퍼로 스프링 애플리케이션 빌드하기
 
- http://www.gradle.org/downloads 에서 그레이들을 내려받기
- https://gradle.org/releases

```
$ unzip gradle-3.5-bin.zip
```

```
$ export JAVA_HOME=/usr/lib/jvm/java-8-openjdk/
```

```
$ export PATH=$PATH:/home/www/gradle-3.5/bin/
```

- 예제 소스를 내려받아 압축 해제 후 ch01/springintro 디렉터리로 이동
- gradle 명령으로 springintro 애플리케이션을 빌드
