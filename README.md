# Mabelley deploy
## [server link](https://github.com/HC-Service/mabelley-server) 

## [clinet link](https://github.com/HC-Service/mabelley-client)

## Usage
docker compose up 이전에 필요한 프로세스
+ client 폴더에 client repo pull 받고 .env.docker 작성
+ server 컴파일 후 .jar 파일 루트에 위치 (server는 application-prod.yml 작성)
+ docker-compose에 사용될 .env 파일 작성 (여기서 작성한 root_password가 server properties에도 동일해야함)

실행: `docker compose up -d`  
로그 확인: `docker compose logs -f`

저장된 서버 로깅 확인은 java container에서 copy 
  + ex) docker cp {server container}:/logging.log logging.log

db data 복사 및 이전에 대해 고려안된 상태
  + docker compose down하면 db data reset