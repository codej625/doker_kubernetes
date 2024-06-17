# 도커 파일 만들기

<br /><br />

1. 간단하게 도커 파일을 만들어보자.
```
# 사용할 베이스 이미지를 선택. OpenJDK 11을 사용.
FROM openjdk:17-jdk-slim

# Root 디렉토리 설정
WORKDIR /app

# JAR 파일을 Docker 이미지로 복사 [복사 파일이름] [복사 파일 경로]
COPY app.jar .

# 컨테이너가 시작될 때 실행할 명령어를 설정
CMD ["java", "-jar", "app.jar"]
```

<br />

2. 도커 파일 빌드.
```
# -f 명령어를 사용해서 app.dockerfile [파일 경로]을 my-app이라는 이름으로 바꿈

docker build -t my-app -f app.dockerfile .
```

<br />

3. 도커 이미지 완성.
