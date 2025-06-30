# mattermost-docker

```bash
https://github.com/KREONET/mattermost-docker.git
cd /opt/mattermost
vi .env
vi docker-compose.yml
docker-compose up -d
```

# 유의사항

### 암호변경

`.env`의 `POSTGRES_USER`, `POSTGRES_PASSWORD`, `POSTGRES_DB`의 환경변수를 적절한 것으로 변경하고 사용한다.
[Random Password Generator](https://www.google.com/search?q=Random+Password+Generator) 등을 활용하여 적절한 것으로 변경한다.

### 추가 환경변수 변경
`.env`의 `DOMAIN`, `CERT_PATH`, `KEY_PATH`의 환경변수를 적절한 것으로 변경한다.
`docker-compose.yml`의 `volumes`와 `networks`의 이름도 적절한 것으로 지정해준다.

### 최신 버전 확인
Mattermost의 [공식 compose.yml](https://github.com/mattermost/docker)과 같은 버전을 사용한다.

본 Repo가 업데이트된 지 오래된 경우, 공식 [Github](https://github.com/mattermost)]와 [Docker Hub](https://github.com/mattermost/docker)]에서 버전을 확인하고 패치를 업데이트 해서 사용해야 한다.

```yaml
  db:
    image: 13-alpine
 
  mattermost:
    image: mattermost/mattermost-enterprise-edition:10.5.2

  nginx:
    image: nginx:alpine

  cerbot:
    image: certbot/certbot
```

## 참고
* Mattermost
  - https://github.com/mattermost
  - https://github.com/mattermost/docker


