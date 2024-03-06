# 도커의 기본 개념을 알아보자!

<br />

```
Container vs VM

VM은 가상의 머신을 만드는 것인데,
운영체제를 포함하기 때문에 매우 무겁다.

반면, 도커는 Container Engine(Doker Engine)이 설치된
호스트 운영체제를 공유하며 Container 단위로 실행이 된다.
운영체제가 포함되지 않기 때문에 VM단위 작동보다
Container 단위 작동이 훨씬 적은 리소스로 가볍게 작동한다.
```

```
1) 도커 파일(Dockerfile)
도커 이미지를 빌드하기 위한 설정 파일이다.
컨테이너가 어떻게 구성되어야 하는지에 대한 명령어와 설정이 포함된다.

ex) copy files, install dependencies, assets ..등
```

```
2) 이미지(Image)
도커 컨테이너를 실행하기 위한 파일과 설정 등을 포함한 가볍고 독립적인 패키지이다.
이미지는 빌드할 수 있으며, 도커 허브와 같은 저장소에서 공유할 수 있다.

ex) Dokerfile을 build하여 자바로 치면 class와 같은 상태로 만든다.
    한번 만들어진 image는 불변 상태로 존재한다.
```

```
3) 컨테이너(Container)
이미지를 기반으로 실행된 가상 환경이다.
컨테이너는 격리된 환경에서 동작하며, 호스트 시스템과는 독립적으로 실행된다.
```

```
4) 도커 허브(Docker Hub)
도커 이미지를 저장하고 공유하는 온라인 저장소이다.
다양한 공개 이미지를 찾고, 자신의 이미지를 업로드하거나 다운로드할 수 있다.
```

<br />

```
도커는 git과 github의 개념과 매우 유사하다.
(사용 순서는 아래와 같다.)

1) Local에서 Doker를 설치한다.
2) Dokerfile을 Build하여 Image를 만든다.
3) 만들어진 Image를 Container Registry(Doker hub)에 Push 한다.
4) 사용하려는 서버에 Doker를 설치 후 Image를 Pull 받는다.
```
