# 1. node 설치
# 최적화 하기 타인이 만들어논 이미지 불러와 사용
FROM	node:12
FROM	node:12-alpine # 용량 경량화 가능, 필요없는 기능들은 안불러옴

# FROM    ubuntu:20.04
# RUN     apt-get update
# RUN     DEBIAN_FRONTEND=noninteractive apt-get install -y nodejs npm



# 2. 패키지 우선 복사
COPY    ./package* /usr/src/app/
WORKDIR /usr/src/app
RUN     npm install


# 2. 소스 복사
COPY    . /usr/src/app

# 3. Nodejs 패키지 설치
# WORKDIR /usr/src/app
# RUN     npm install

# 4. WEB 서버 실행 (Listen 포트 정의)
EXPOSE 3000
CMD    node app.js