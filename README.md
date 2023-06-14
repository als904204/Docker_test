# SpringBoot + Gradle + Docker + AWS 배포

## 1. jar 파일 생성
(jar : 여러 개의 자바 클래스 파일과, 클래스들이 이용하는 관련 리소스(텍스트, 그림 등) 및 메타데이터를 하나의 파일로 모아서 자바 플랫폼에 응용 소프트웨어나 라이브러리를 배포하기 위한 소프트웨어 패키지 파일 포맷)
![image](https://github.com/als904204/Docker_test/assets/55350901/cb76a5d3-b5af-4275-8297-222cb2f10140)

## 2. Gradle > Tasks > build > bootJar

<img width="465" alt="image" src="https://github.com/als904204/Docker_test/assets/55350901/228e6dab-2f11-4cc2-b8f2-03e30abe1bd5">

## 3. Dockerfile 만들기
(도커 이미지파일을 생성하기위한 도커파일)

<img width="406" alt="image" src="https://github.com/als904204/Docker_test/assets/55350901/9074f540-0984-4538-b144-63f95730ee49">

## 4. 도커파일 빌드
(cd build/libs)
`docker build -t springio/gs-spring-boot-docker .`

## 5. 생성된 도커 이미지 목록 확인
`docker images`

## 6. 도커 컨테이너 실행
`docker run -d -p 5000:8080 springio/gs-spring-boot-docker`

## 7. 접속
localhost:5000
