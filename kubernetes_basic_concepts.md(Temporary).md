# 쿠버네티스에 대해 알아보자

<br /><br />

* Kubernetes?
---

```
쿠버네티스는(k8s) 컨테이너 오케스트레이션 시스템으로,
클러스터 내에서 컨테이너화된 애플리케이션을 배포, 관리, 스케일링하기 위한 도구이다.

컨테이너 오케스트레이션 시스템을 사용하는 대표적인 프로그램으로는
Docker swarm, Kubernetes(k8s), Mesos 등이 있지만,
DocKer가 컨테이너 표준이듯이 오케스트레이션 시스템은 Kubernetes가 표준이라 할 수 있다.
```

<br /><br /><br />

* 발전 배경
---

```

Traditional Deployment -> Virtualized Deployment -> Container Deployment 순서로 발전

```

| Traditional Deployment | Virtualized Deployment | Container Deployment |
|------------------------|------------------------|----------------------|
| X                      | ┌ App                  | ┌ App                |
| X                      | ├ Bin / Lib            | ├ Bin / Lib          |
| X                      | ├ Operating System     | ├ X                  |
| App                    | └ Virtual Machine      | └ Container          |
| Bin / Lib              | Hypervisor             | Container Runtime    |
| Operating System       | Operating System       | Operating System     |
| Hardware               | Hardware               | Hardware             |

<br />

1. Traditional Deployment
```
Hardware에 Operating system(OS)이 올라가 있고,
그 위로 App가 설치되어있다.
서버의 자원이 남아도 효율적으로 활용하기 힘든 구조이다.
```

<br />

2. Virtualized Deployment
```
Operating system(OS)에 가상화 기술을 사용한다.
VM(Virtual Machine) 단위로 가상의 서버를 구현하는 구조이다.
VM으로 완벽히 영역을 나눌 수 있지만,
VM마다 Operating system이 필요하다.
```

<br />

3. Container Deployment
```
Container 단위로 서버를 관리하고,
Operating system을 공유한다.
Docker와 같은 Container runtime을 사용한다.

마지막으로 가장 큰 차이점은 위에 표에는 존재하지 않지만,
컨테이너화된 애플리케이션의 배포, 확장 및 관리를 자동화하는
Orchestration engine(Kubernetes)이 존재한다는 것이다.
```
