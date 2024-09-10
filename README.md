<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:FF0000,100:FFA500&height=240&text=SKN01-4th-5Team&animation=&fontColor=ffffff&fontSize=90" width="1000" />
  
  [![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-4th-1Team&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
</div>



# 1. Introduction Team (팀 소개)
### ✅ 팀명 : TCP(Text Chat Programmers)
<table align=center>
  <tbody>
    <tr>
      <td align=center><b>김용현</b></td>
      <td align=center><b>한병찬</b></td>
      <td align=center><b>김지민</b></td>
      <td align=center><b>이용우</b></td>
      <td align=center><b>정원형</b></td>
    </tr>
    <tr>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/80f0a998-61ab-4de5-a652-51575e8a4468"width="200px; alt=""/>
        </div>
      </td>
      <td align="center">
        <div>
          <img src="https://github.com/user-attachments/assets/30f29d8b-bcec-46c7-bce6-e6e4ec414e55"width="200px;" alt=""/>
        </div>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/c01c579b-7f4f-436b-984a-74a26d2cef44"width="200px;" alt=""/>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/77eff59b-1c54-4d91-a49c-5f81cf28fb35"width="200px;" alt=""/>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/49822355-b1ef-485b-a45b-dc2199d8397b"width="200px;" alt=""/>
      </td>
    </tr>
    <tr>
      <td><a href="https://github.com/younghyen7956"><div align=center>@Jh-jaehyuk</div></a></td>
      <td><a href="https://github.com/MinMessi"><div align=center>@MinMessi</div></a></td>
      <td><a href="https://github.com/Ah-ram"><div align=center>@Ah-ram</div></a></td>
      <td><a href="https://github.com/ih9511"><div align=center>@ih9511</div></a></td>
      <td><a href="https://github.com/y0ng98"><div align=center>@y0ng98</div></a></td>
    </tr>
  </tbody>
</table>
<br><br><br>


# 2. Introduction Project (프로젝트 개요)

### ✅프로젝트 명
논문 요약 및 설명 제공 서비스

### ✅프로젝트 소개
논문 요약 및 설명 제공 서비스

### ✅프로젝트 필요성(배경)
- 새로운 기술에 대한 연구가 과거 대비 매우 빠른 속도로 발표되고 있습니다.
- 이에 새로운 기술을 논문을 통해 접하고자 하는 니즈가 발생하고 있음을 발견하였고, 이러한 니즈를 충족시키기 위해 논문을 읽을 수 있는 방식을 LLM을 통해 제공하여 많은 사람들이 이용할 수 있도록 서비스화하고자 합니다.

## 비동기 통신 방식의 Deep Learning Local Server
### Syncronous Communication
- 동기(Syncronous)란 동시에 일어난다는 뜻입니다. 즉, Request와 Response가 동시에 일어나는 통신 방식입니다.
- 노드 A와 노드 B 사이의 작업 처리 단위를 동시에 맞춥니다.
- 요청한 결과가 그 자리에서 동시에 주어집니다.
### Asyncronous Communication
- 비동기(Asyncronous)란 동시에 일어나지 않는다는 뜻입니다. 즉, Request와 Response가 동시에 일어나지 않는 통신 방식입니다.
- 노드 사이의 작업 처리 단위를 동시에 맞추지 않겠다는 것으로, 요청한 결과가 그 자리에서 주어지지 않습니다.
### 각 통신 방식의 장단점
- 동기 통신의 경우 설계가 간단하며, 직관적이지만 그 작업이 끝날 때까지 아무런 작업도 할 수 없다는 단점이 있습니다.
- 비동기 통신의 경우 동기 통신보다 비교적 복잡한 구현이 필요하지만, 작업이 끝날 때 까지 기다리지 않아도 되기 때문에 그 동안 다른 작업을 수행할 수 있으므로 효율적인 자원의 사용이 가능합니다.
### 비동기 통신 방식 DLLS
- 모델이 Request에 따라 Response를 하기까지 입력에 대한 결과를 추론하는데에 시간이 필요합니다. 만약 Response를 반환하는 과정을 동기 통신 방식으로 구현한다면, 결과 반환이 완료될 때 까지 사용자는 아무것도 하지 못합니다.
- 따라서, 모델이 추론하여 Response를 반환하는 과정을 비동기 방식으로 설계하여 사용자가 추론 요청 이외의 작업을 수행할 때에도 문제가 없도록 하였습니다.
### 물리적 로컬 서버 구현 이유
- AWS 상에서 LLM 모델의 Fine Tuning 및 추론 과정을 구동시킬 경우, 예산을 넘어서는 비용이 발생할 가능성이 존재합니다.
- 이에 컴퓨팅 자원이 많이 필요한 부분을 따로 물리적 로컬 서버에서 구동하여 Response를 반환하도록 설계하였습니다.
- 결과적으로, 모델 서빙 역할의 FastAPI와 DLLS 상의 AI Client 사이의 비동기 통신을 통해 비용적인 측면에서의 최적화를 달성하고 사용자가 서비스를 사용함에 있어서 불편함이 없도록 하였습니다.
### TLS/SSL 보안 통신 환경 구축
- 커스텀 서버 특성 상, 비교적 해킹에 취약할 가능성이 존재합니다. 이에 보안 프로토콜을 적용하여 외부에서 우리의 서비스에 접근할 수 없도록 보안 통신 환경을 구축하였습니다.


### ✅프로젝트 목표
1. Front-End에서는 **TypeScript**와 **Vue.js + Vuetify3**를 이용하여 사용자 측면에서 유리한 UI-UX를 구축하였고, **Axios** 를 통해서 올바른 Request를 하는 것을 목표로 삼았습니다. 
2. Back-End에서는 **Python**과 **Django**, **MySQL** 등을 이용하여 Request에 대한 정확한 Response와 원활한 웹사이트 운영하는 것을 목표로 삼았습니다.
3. Fast API에서는 **Machine Learning** **Deep Learning** 이용하여 데이터를 분석 및 예측할 수 있도록 하였습니다.
4. Deep Learning Local Server (DLLS) 에서는 **Fast API와 AI Client의 비동기 통신 환경**을 소켓 통신으로 구축하여 일반적인 동기 Request들이 처리될 때, 정상적으로 동작하도록 구축하였습니다.
5. CI-CD는 지속적인 코드 통합과 지속적인 배포를 통해 궁극적으로 개발 속도를 높이고, 코드 품질을 유지하며, 개발과 운영의 경계를 허물며 신속하게 가치를 제공하는 것을 목표로 삼았습니다. 
<br><br><br>

## 애자일 보드를 사용하는 이유
```c
과거 정의서들을 일일히 작성하였지만 빠른 속도로 무언가를 개발하는데 한계가 있습니다.
처음부터 많은 것들을 빌드업하면서 빠른 생산성을 기반으로 움직이려면 반드시 애자일해야합니다.
고로 폭포수 설계 방식이 아닌 애자일 프로세스 방식으로 애자일 보드를 작성하면서 진행했습니다.

애자일 보드는 자체적으로 제목이 요구 사항을 내포하며 각 카드 내부에는 정의한 Domain의 세부 사항이 기록됩니다.
고로 빠르게 팀원들과 협업 할 수 있고 소통 비용을 최소화시킬 수 있습니다.
작은 것 같지만 이와 같은 것들이 쌓여서 아주 기민하고 민첩한 조직을 만들어 냅니다.
```
# 3. 시스템 구성도
![image](https://github.com/user-attachments/assets/66a78240-b41d-487a-8800-29bccbab7d41)
<br><br><br>

# 4. Backend 애자일 보드 - 요구 사항 정의서
![image](https://github.com/user-attachments/assets/89ece460-81bd-44cf-bc7d-644487b3b267)
<br><br><br>


# 5. Frontend 애자일 보드 - 화면 설계서
![image](https://github.com/user-attachments/assets/b547b885-25f8-413f-ab40-3251e8b77e95)
![image](https://github.com/user-attachments/assets/b947d9db-b2d1-4494-8842-82285289d6ff)

<br><br><br>


# 6. FastAPI 애자일 보드 - AI 서빙 설계서
![image](https://github.com/user-attachments/assets/ccd6592b-4e7c-4fab-a7fe-6f16e8515195)
<br><br><br>

# 7. AI Client 애자일 보드 - 모델 파인튜닝 및 추론 설계서
![image](https://github.com/user-attachments/assets/ee098b0b-77b0-4e53-9a47-836e61081638)
<br><br><br>




# 8. Manual Deploy (수동 배포 진행 절차)

## Frontend (UI)
### ➡️ Build
frontend 로컬 저장소에서 .env에 필요한 IP 옵션들을 설정해줍니다.

이후 아래 명령어를 입력하여 build 합니다.
```bash
npm run build
``` 
![image](https://github.com/user-attachments/assets/8fd293b2-5166-4684-9561-ca88bbffb7b0)

### ➡️ dist
build를 하고 나면 dist가 생성되는 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/cc497e6c-02fa-429e-8595-c6ce082f65f9)

### ➡️ scp 명령어
```bash
scp -i "pem키(상대경로 혹은 절대경로)" -r * ec2-user@AWS_IP:/home/ec2-user/프로젝트팀/vue-frontend/html/
```
![image](https://github.com/user-attachments/assets/2cd28b2e-2fef-4390-ae4a-643f882969fc)

### ➡️ docker-compose up
AWS에서 이전에 작성했던 docker-compose.yml을 활용해서 아래와 같이 실행합니다.
```bash
docker-compose up -d
```
![image](https://github.com/user-attachments/assets/8b7d9020-68a1-4df0-8218-71573666a2af)



## Backend (Server)
### Local
1. 먼저 프로젝트 저장소로 이동합니다.  
![image](https://github.com/user-attachments/assets/de94c3cf-82ff-4cac-8816-401efa605028)
  
2. 아래 파일들에 대해서 권한 설정을 해줍니다.
  
```bash
chmod +x wait-for-it.sh
chmod +x manage.py
```

3. GHCR에 로그인합니다.
  
```bash
echo "GHCR Token" | docker login ghcr.io -u (username) --password-stdin
```
  
4. wait-for-it.sh를 LF로 바꿔놓아야 합니다. 
![image](https://github.com/user-attachments/assets/d08ef835-df6f-4e26-9a40-441904b6205b)
  
5. 아래 명렁어를 이용하여 Docker 빌드를 진행합니다.
  
```bash
docker buildx create --use
docker buildx build --platform linux/arm64 -f Dockerfile -t ghcr.io/(username)/(teamname)-django-test-server:latest --push .
```
  
### AWS
1. pem key를 사용해 AWS에 접속하고 docker-compose.yml를 아래와 같이 구성합니다.
  
```yaml
version: '3'
services:
  django:
    container_name: django
      # image: ghcr.io/${GITHUB_ACTOR}/(teamname)-django-server:latest
    image: ghcr.io/${GITHUB_ACTOR}/django-test-server:latest
    command: /app/wait-for-it.sh db:3306 -t 15 -- sh -c "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"
    restart: always
    ports:
      - "8000:8000"
        #    volumes:
        #      - .:/app
    depends_on:
      - db
      - redis
    environment:
      - DJANGO_SETTINGS_MODULE=config.settings
      - CORS_ALLOWED_ORIGINS=${CORS_ALLOWED_ORIGINS}
      - CSRF_TRUSTED_ORIGINS=${CSRF_TRUSTED_ORIGINS}
      - DATABASE_HOST=${DATABASE_HOST}
      - DATABASE_PORT=3306
      - DATABASE_NAME=${DATABASE_NAME}
      - DATABASE_USER=${DATABASE_USER}
      - DATABASE_PASSWORD=${DATABASE_PASSWORD}
      - KAKAO_LOGIN_URL=${KAKAO_LOGIN_URL}
      - KAKAO_CLIENT_ID=${KAKAO_CLIENT_ID}
      - KAKAO_REDIRECT_URI=${KAKAO_REDIRECT_URI}
      - KAKAO_TOKEN_REQUEST_URI=${KAKAO_TOKEN_REQUEST_URI}
      - KAKAO_USERINFO_REQUEST_URI=${KAKAO_USERINFO_REQUEST_URI}
      - REDIS_HOST=redis
      - REDIS_PORT=6379
      - REDIS_PASSWORD=${REDIS_PASSWORD}
      - ALLOWED_HOSTS=${ALLOWED_HOSTS}
    networks:
      - app-network

  db:
    image: mysql:8.0
    container_name: db
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: ${DATABASE_PASSWORD}
      MYSQL_DATABASE: ${DATABASE_NAME}
      MYSQL_USER: ${DATABASE_USER}
      MYSQL_PASSWORD: ${DATABASE_PASSWORD}
    ports:
      - "3306:3306"
    volumes:
      - db_data:/var/lib/mysql
        #      - ./mysql/custom.cnf:/etc/mysql/conf.d/custom.cnf
        #      - ./mysql/logs:/var/log/mysql
      - ./init.sql:/docker-entrypoint-initdb.d/init.sql
    networks:
      - app-network

  redis:
    image: redis:latest
    container_name: redis-container
    restart: always
    ports:
      - "6379:6379"
    volumes:
      - redis_data:/data
    command: ["redis-server", "--requirepass", "${REDIS_PASSWORD}"]
    networks:
      - app-network

volumes:
  db_data:
  redis_data:
  app:

networks:
  app-network:
    driver: bridge
```  
  
2. 이후 아래 명령어를 입력하여 docker image를 pull 합니다.
  
```bash
echo "GHCR Token" | docker login ghcr.io -u (username) --password-stdin
```
  
3. 이후 아래 명령어를 입력하여 백그라운드에서 작동시킵니다.
  
```bash
docker-compose up -d
```
  
## FastAPI (AI Core Server)
### Build
프로젝트 최상단에 Dockerfile과 docker-compose.yml 파일을 구성합니다.
![image](https://github.com/user-attachments/assets/558dd449-5a52-4b51-9d33-533a89bb34b6)

이후 GHCR에 docker login을 하여 docker build 구성을 진행합니다.
```bash
export DOCKER_BUILDKIT=1
docker buildx create --use
docker buildx build --platform linux/arm64 --file ./Dockerfile --push -t ghcr.io/github계정/tcp-fastapi-server:latest .
```
build가 완료되어 아래와 같은 결과를 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/400b0701-5179-4627-becd-e95807ca1bdf)

![image](https://github.com/user-attachments/assets/673e79ee-ccc8-4b41-a64d-8d714fc605a2)

### 구동
AWS에 접속해서 마찬가지로 docker-compose.yml 파일을 구성합니다.

![image](https://github.com/user-attachments/assets/649539a5-7d58-44e7-9a74-76b458d39a13)

<br>
컨테이너를 생성하고 구동합니다.

```bash
docker-compose up
```

잘 구동된 모습입니다.
![image](https://github.com/user-attachments/assets/7ab8fd20-fda1-498e-b28b-d8dc4ece6cb1)

외부에서 API 테스트를 위해 아래와 같이 인바운드 규칙을 설정합니다.
![image](https://github.com/user-attachments/assets/0021b74a-e8d0-44c0-b8a3-146e9c7ca8b6)

아래와 같이 수동배포가 잘 된 것을 확인할 수 있습니다.  
![image](https://github.com/user-attachments/assets/b3e2ffcd-6f5c-41f0-873b-9ae29c516d32)
<br><br><br>



# 9. Autonomous Deploy (자동 배포 진행 절차)

## Frontend (UI)
![image](https://github.com/user-attachments/assets/ca3d7962-bb4a-4668-9ce8-9976ef04b924)

### ✅ CI / CD 전체 흐름
1. 개발자들이 각 Domain에 맞춰 Backlog 작업을 진행합니다.

2. 이 때 테스트가 동작하면서 CI (Continuous Integration) 관련 사항을 체크합니다.

3. 당장 큰 문제가 없다면 PR을 승인합니다.

    (2, 3번은 정책에 따라 달라질 수 있습니다)


4. CI가 통과되면 CD로 넘어가서 배포가 진행됩니다.

5. 이 때 npm build를 통해 프로젝트가 빌드됩니다.

6. 빌드 이후 빌드 결과로 html, css, javascript, 리소스(이미지 등등)이 나옵니다.

7. 이 정보가 AWS에 scp를 통해 전달됩니다.

8. 전달한 정보를 가지고 nginx를 구동합니다.

9. nginx를 구동할 때 docker-compose.yml 을 참조합니다.

10. nginx는 구동 시 어떤 javascript, html, css를 참조할지 판정합니다.

     이 내용들은 docker-compose에 명시되어 있습니다.

11. 추가적으로 nginx가 어떤 요청에 대해 어떻게 처리할지 configuration 정보는 conf 폴더 하위에 배치됩니다.

12. 즉 docker-compose up -d 명령 이후 nginx에 의해 frontend 코드가 동작합니다.


### 📍 CI 구성
 ### ➡️ ci.yml
  Github Actions -> workflows 에서 파일을 작성합니다.

``` bash
name: CI (Continuous Integration)

on:
  push:
    branches: ["main"]

jobs:
  build:
    name: Frontend CI
    runs-on: ubuntu-latest
    steps:
    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '20'

    - name: Cache dependencies
      id: cache
      uses: actions/cache@v3
      with:
        path: '**/node_modules'
        key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
        restore-keys: |
          ${{ runner.os }}-node-

    - name: Install Dependencies
      if: steps.cache.outputs.cache-hit != 'true'
      run: |
        npm ci --legacy-peer-deps

    - name: Create .env development for CI
      run: |
        pwd
        echo "${{ secrets.ENV_DEVELOPMENT }}" > .env.development
        cat .env.development

    - name: Real Test
      run: |
        npm run test:unit

    - name: send FRONTEND_TEST_FINISH_TRIGGER
      run: |
        curl -S -X POST https://api.github.com/repos/${{ github.repository }}/dispatches \
            -H 'Accept: application/vnd.github.v3+json' \
            -u ${{ secrets.GHCR_TOKEN }} \
            -d '{"event_type": "FRONTEND_TEST_FINISH_TRIGGER", "client_payload": { "repository": "'"$GITHUB_REPOSITORY"'" }}'

```
이후 Actions를 살펴보면 CI가 진행되는 것을 확인할 수 있습니다.

  ![image](https://github.com/user-attachments/assets/f5b8f8ee-edd2-4360-8484-cb87bb13cea7)


## 📍CD 구성하기
  ### ➡️cd.yml
  CI와 마찬가지로 조직 저장소에서 Actions를 눌러 workflows를 작성합니다.
  ```bash
  name: CD (Continuous Deploy)

on:
  repository_dispatch:
    types: [FRONTEND_TEST_FINISH_TRIGGER]

jobs:
  build:
    name: build-app
    runs-on: ubuntu-latest
    steps:
    - name: Get Github Actions IP
      id: ip
      uses: haythem/public-ip@v1.2

    - name: Configure AWS IAM Credentials
      uses: aws-actions/configure-aws-credentials@v1
      with:
        aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
        aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
        aws-region: ap-northeast-2

    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Setup node.js
      uses: actions/setup-node@v2
      with:
        node-version: '20'

    - name: Cache dependencies
      id: cache
      uses: actions/cache@v3
      with:
        path: '**/node_modules'
        key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
        restore-keys: |
          ${{ runner.os }}-node-

    - name: Install Dependencies
      if: steps.cache.outputs.cache-hit != 'true'
      run: |
        npm ci --legacy-peer-deps

    - name: Create .env.production for Continuous Deploy
      run: |
        echo "${{ secrets.ENV_PRODUCTION }}" > .env.production
        cat .env.production

    - name: Build
      run: |
        npm run build
        ls

    - name: Setup SSH
      uses: webfactory/ssh-agent@v0.5.0
      with:
        ssh-private-key: ${{ secrets.PRIVATE_KEY }}

    - name: Add Github Actions IP to Security Group
      run: |
        aws ec2 authorize-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32

    - name: SCP Action
      uses: appleboy/scp-action@master
      with:
        host: ${{ secrets.HOST_IP }}
        username: ec2-user
        key: ${{ secrets.PRIVATE_KEY }}
        source: "./dist/**"
        target: "/home/ec2-user/tcp/actions-frontend"

    - name: Remove Github Actions IP From Security Group
      run: |
        aws ec2 revoke-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32

    - name: SSH Agent Cleanup
      if: ${{ always() }}
      uses: webfactory/ssh-agent@v0.5.0
      with:
        ssh-private-key: ${{ secrets.PRIVATE_KEY }}

  deploy:
    name: Deploy to Production
    needs: build
    runs-on: [ self-hosted, deploy-tcp-frontend ]
    steps:
      - name: Get Github Actions IP
        id: ip
        uses: haythem/public-ip@v1.2
        
      - name: Configure AWS IAM Credentials
        uses: aws-actions/configure-aws-credentials@v1
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: ap-northeast-2

      - name: Add Github Actions IP to Security Group
        run: |
          aws ec2 authorize-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32
    
      - name: Deploy to Production
        uses: appleboy/ssh-action@v0.1.10
        with:
          host: ${{ secrets.HOST_IP }}
          username: ec2-user
          key: ${{ secrets.PRIVATE_KEY }}
          script_stop: true
          script: |
            pwd
            cd /home/ec2-user/tcp/vue-frontend
            cp -r /home/ec2-user/tcp/actions-frontend/dist/* ./html/

            docker image prune -f
            docker logout

            docker-compose up -d

      - name: Remove Github Actions IP From Security Group
        run: |
          aws ec2 revoke-security-group-ingress --group-id ${{ secrets.AWS_SG_ID }} --protocol tcp --port 22 --cidr ${{ steps.ip.outputs.ipv4 }}/32
  ```

### ➡️ frontend 에서 필요한 환경변수
- Gitub Settings -> Secrets and variables -> Actions -> Repository secrets
![image](https://github.com/user-attachments/assets/9c558df6-84c6-42c5-87ad-b56fb67fbc31)

### ➡️ Github Action Runner 연결
Github Actions Runner를 설정하기 위해 Settings에서 Actions → Runner →  New self-hosted runner를 누릅니다. 
    
  구동되는 버전이 ARM64 Linux에 해당하므로 아래와 같이 설정합니다.
    ![image](https://github.com/user-attachments/assets/b4222f15-aded-4fb6-9c42-8f79083c8a42)

AWS에 접속하면 CD 스크립트가 생성한 팀 프로젝트의 폴더에 진입하여 runner들을 모아놓을 runners 디렉토리를 생성하고 frontend 용 action runner 디렉토리를 설정합니다.
```bash
mkdir frontend-action-runner
cd frontend-action-runner
```
이후 Github Actions Runner 설정에서 하단에 있었던 Download, Configure에 해당하는 명령어들을 순서대로 넣어줍니다.
![image](https://github.com/user-attachments/assets/ce3e6e4f-0432-44a8-a589-8d57265e1797)
여기서 레이블을 설정할 때 주의할 점은 CD 스크립트의 self-hosted에 작성했던 레이블을 동일하게 입력해야 합니다. 

./run.sh 명령을 입력하면 아래와 같이 Listen 상태가 되며,
CD 스크립트의 deploy 파트와 통신하여 작업이 진행됩니다.

백그라운드 실행을 위해 아래와 같은 명령어로 구동합니다.
```bash
nohup ./run.sh > run.log 2>&1 &
```

### ➡️ docker-compose.yml
팀프로젝트 하위에 vue-frontend 디렉토리에서 작업합니다.
```bash
version: "3.7"
services:
  nginx:
    image: "nginx:latest"
    container_name: frontend-deploy-nginx
    restart: unless-stopped
    volumes:
      - /home/ec2-user/att/vue-frontend/conf:/etc/nginx/conf.d
      - /home/ec2-user/att/vue-frontend/html:/usr/share/nginx/html
    ports:
      - "80:80"
    networks:
      - app

networks:
  app:
    driver: bridge
```
### ➡️ nginx.conf
nginx를 사용하는 이유는  

리버스 프록시를 사용하여 본래 서버의 IP 주소를 노출시키지 않아 서버 보안에 유용하기 때문입니다.


```bash
server {
        listen 80;
        location / {
                root /usr/share/nginx/html;
                index index.html index.htm;
                try_files $uri $uri/ /index.html;
        }
}
```


docker 컨테이너를 구동합니다.
```bash
docker-compose up
```


## Backend (Server)
![image](https://github.com/user-attachments/assets/88077b76-db66-4169-b451-0d0cf849a637)

### Django CI
#### Basic Settings
GitHub Actions를 활용해서 CI를 구성합니다. 브랜치의 경우, develop 브랜치가 아닌, main 브랜치에서 작업을 수행합니다.  
  
![image](https://github.com/user-attachments/assets/a537bdde-8ec9-46d7-b37b-7c881087349d)  
파일 이름의 경우 ci 로 설정하고, 파일의 경우 yaml 형식으로 구성합니다. XML, JSON 등의 형식으로 구성해도 무방하나, 유지 보수의 유연성과 개발 편의성으로 위해 yaml을 선택하였습니다. 저희 프로젝트에서 Backend의 경우, Django를 기반으로 하여 MySQL과 Redis를 활용합니다. 이에 맞게 yaml 파일을 구성합니다.  

#### Django 일괄 테스트 진행
또한, 매번 integration 이전에 테스트를 하는 과정에서 모든 테스트 파일을 수동으로 돌리는 번거로움을 줄이기 위해서 Django 테스트 패키지를 찾아서 CI에 전달하게끔 구성하였습니다.  

![image](https://github.com/user-attachments/assets/9afb8a59-eaf9-47dc-ba52-de95da84b681)
  
해당 위치에 find_test.sh 를 생성하고 다음의 코드를 작성합니다.  
```bash
#!/usr/bin/env bash

TEST_DIRS=$(find . -path ./.venv -prune -o -type d -name 'tests' -print)

APP_TESTS=()

for TEST_DIR in $TEST_DIRS; do
  APP_NAME=$(basename $(dirname $TEST_DIR))
  TEST_FILES=$(find $TEST_DIR -type f -name 'test*.py')

  if [ -z "$TEST_FILES" ]; then
    continue
  fi

  APP_TESTS+=("${APP_NAME}.tests")
done

echo "${APP_TESTS[@]}"
```
다음으로 실행 권한을 부여합니다. 모든 명령어는 기본적으로 Git Bash에서 실행하기 때문에 Linux 명령어를 사용합니다. 이후, 파일을 실행시켜 루트 위치 내의 모든 tests 파일들을 잘 가져오는지 확인합니다.
```bash
chmod +x find_test.sh
./find_test.sh
```
### Django CD
#### Basic Settings
CI 구성때와 마찬가지로 GitHub Actions를 이용하여 CD를 구성합니다. 
![image](https://github.com/user-attachments/assets/89bdb835-5276-419b-b902-ccf3c6023449)

Django 환경을 여러 개 구성해야 할 경우, build 시에 서로 구분이 돼야합니다. 그렇기 때문에, jobs: build: steps: `Build and push Docker image` 쪽을 다음과 같이 구성합니다.  
```bash
- name: Build and push Docker image
  run: |
    cd <프로젝트 이름>
    docker buildx build --platform linux/arm64 -f Dockerfile -t ghcr.io/${{ github.actor }}/<빌드하고자 하는 환경 이름>:latest --push .
```
#### Github Actions Runner 구성
GitHub Actions Runner 설정을 위해 Settings로 이동합니다. Settings -> Code and automation -> Actions -> Runners 이동 후 우측 상단에 `New self-hosted runner` 버튼을 클릭합니다.

![image](https://github.com/user-attachments/assets/2bc9e67a-32c8-4985-9006-cfd4ee157bbd)
우리는 AWS에서 `Linux`를 선택했기 때문에 `Runner image`를 `Linux`로 선택합니다. 전체적인 세팅은 다음과 같습니다.  
- Runner Image: `Linux`
- Architecturre: `ARM64`  
  
이후 `Git Bash`를 통해 AWS에 접속합니다.
  
![image](https://github.com/user-attachments/assets/fec99c35-004b-4d83-8d27-f9d8e0f49630)
  
이후 `Django` 프로젝트 폴더로 이동한 다음, 생성된 `runners` 폴더로 들어갑니다. 다음의 명령을 실행하여 `backend-action-runner` 폴더를 생성합니다.
```bash
mkdir backend-action-runner
cd backend-action-runner
```
이후 아래쪽에 있는 명령어들을 입력합니다. 입력 시 CD 스크립트의 `deploy` 부분의 구성을 토대로 수정합니다.
```bash
deploy:
  needs: build
  name: Deploy
  runs-on: [ self-hosted, <runners 실행할 이름 > ]
  steps:
  - name: Login to GHCR
  ...
```
`config` 버튼을 누르면 아래와 같은 화면이 나옵니다.

![image](https://github.com/user-attachments/assets/13393ca6-4878-451f-afbd-5d3278ae2d5f)

정상적으로 구동된다면 쉘 스크립트 파일을 실행합시다.
```bash
./run.sh
```
이후 background 에서도 실행되도록 설정합니다.
```bash
nohup ./run.sh > run.log 2>&1 &
```
추가적으로 background에서 잘 작동하는지 확인하려면 다음의 명령을 입력합니다.
```bash
ps -ef | grep run.sh
```
잘 작동한다면, 다음과 같이 표시됩니다.
  
![image](https://github.com/user-attachments/assets/dcb9f5f7-6ea0-4d37-b0c5-a35abccccc1b)

### docker-compose 구성
`Git Bash`를 통해 AWS에 접속합니다. 이후 아래와 같이 명령어를 입력합니다.
```bash
cd <프로젝트명>
mkdir django-backend
cd django-backend
```
Django 프로젝트 디렉토리 하위에 .env 파일과 함께 docker-compose.yml 파일을 생성하고 다음의 내용을 기입합니다.
```bash
version: '3'
services:
  django:
    container_name: django
    image: ghcr.io/${GITHUB_ACTOR}/tf-django-server:latest
    command: /app/wait-for-it.sh db:3306 -t 15 -- sh -c "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"
    restart: always
    ports:
      - "8000:8000"
    depends_on:
      - db
      - redis
    environment:
      - DJANGO_SETTINGS_MODULE=config.settings
      - CORS_ALLOWED_ORIGINS=${CORS_ALLOWED_ORIGINS}
      - CSRF_TRUSTED_ORIGINS=${CSRF_TRUSTED_ORIGINS}
      - DATABASE_HOST=${DATABASE_HOST}
      - DATABASE_PORT=3306
      - DATABASE_NAME=${DATABASE_NAME}
      - DATABASE_USER=${DATABASE_USER}
      - DATABASE_PASSWORD=${DATABASE_PASSWORD}
      - KAKAO_LOGIN_URL=${KAKAO_LOGIN_URL}
      - KAKAO_CLIENT_ID=${KAKAO_CLIENT_ID}
      - KAKAO_REDIRECT_URI=${KAKAO_REDIRECT_URI}
      - KAKAO_TOKEN_REQUEST_URI=${KAKAO_TOKEN_REQUEST_URI}
      - KAKAO_USERINFO_REQUEST_URI=${KAKAO_USERINFO_REQUEST_URI}
      - REDIS_HOST=redis
      - REDIS_PORT=6379
      - REDIS_PASSWORD=${REDIS_PASSWORD}
      - ALLOWED_HOSTS=${ALLOWED_HOSTS}
    networks:
      - app-network

  db:
    image: mysql:8.0
    container_name: db
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: ${DATABASE_PASSWORD}
      MYSQL_DATABASE: ${DATABASE_NAME}
      MYSQL_USER: ${DATABASE_USER}
      MYSQL_PASSWORD: ${DATABASE_PASSWORD}
    ports:
      - "3306:3306"
    volumes:
      - db_data:/var/lib/mysql
      - ./mysql/custom.cnf:/etc/mysql/conf.d/custom.cnf
      - ./mysql/logs:/var/log/mysql
      - ./init.sql:/docker-entrypoint-initdb.d/init.sql
    networks:
      - app-network

  redis:
    image: redis:latest
    container_name: redis-container
    restart: always
    ports:
      - "6379:6379"
    volumes:
      - redis_data:/data
    command: ["redis-server", "--requirepass", "${REDIS_PASSWORD}"]
    networks:
      - app-network

volumes:
  db_data:
  redis_data:
  app:

networks:
  app-network:
    driver: bridge
```
이후 django-backend 하위에 `mysql`디렉토리를 만들고 `custom.cnf` 파일을 생성합니다.
```bash
mkdir mysql
cd mysql
vi custom.cnf
```
```bash
[mysqld]
character-set-server = utf8mb4
collation-server = utf8mb4_general_ci
skip-character-set-client-handshake
innodb_buffer_pool_size = 16M
```
이후 `mysql` 디렉토리 하위에 `logs` 디렉토리를 배치합니다.
```bash
mkdir logs
cd logs
touch README.md
```
그리고 django-backend 디렉토리 하위에 init.sql 파일을 아래와 같이 작성합니다.
```bash
CREATE DATABASE IF NOT EXISTS <db 이름>;
GRANT ALL PRIVILEGES ON <db 이름>.* TO 'eddi'@'%';
FLUSH PRIVILEGES;
```
`Git Bash`에서 `docker-compose up`명령어를 통해 동작하는지 확인합니다. 잘 동작한다면, docker-compose 구성이 잘 마무리 되었습니다.
<br>  

# 10. Deep Learning Local Server 구성
## 10-1 Socket Server (FastAPI) 구성 및 구동 방법
1. FastAPI 프로젝트 폴더 내에서 미리 구성해 놓은 소켓 통신 관련 submodule을 다음의 명령어를 통해 연결합니다.
```bash
git submodule add "socket server submodule Github 주소" template
```

2. 다음과 같이 `template` 라는 submodule이 프로젝트 내부에 붙은 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/fc83fd3b-3cf0-4852-a6e1-c143afb3eed3)
3. 이후에 `cd include/socket_server/`에 소켓 서버의 역할을 하도록 해놓은 모듈에 대한 내용들을 다음의 명령어로 갱신시킵니다.
![image](https://github.com/user-attachments/assets/1bf1190e-1aad-45d9-ad6b-d44090f88c0f)
```bash
cd ../..
git submodule update --init --recursive
```
4. 그러면 아래처럼 내용들이 추가된 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/bb624477-e11a-461c-a532-63389108c566)

5. 이후 미리 준비해놓은 보안 관련 파일들을 프로젝트 폴더에 배치시킵니다.
```bash
CA.pem
svr.key
svr.crt
```

6. 서버를 구동시키면 다음과 같이 ai-client의 접속을 대기하는 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/dbdf40fe-1fc0-4e15-9c05-73618d202e63)

## 10-2 Socket Client (ai-client) 구성 및 구동 방법
1. ai-client 프로젝트 폴더 내에서 소켓 서버와 마찬가지로 미리 구성해 놓은 소켓 통신 관련 submodule을 다음의 명령어를 통해 연결합니다.
```bash
git submodule add "socket client submodule Github 주소" template
```

2. 다음과 같이 `template` 라는 submodule이 프로젝트 내부에 붙은 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/7340470c-97c3-4ee4-ab18-d52bbc6a8c83)

3. 이후 미리 준비해놓은 보안 관련 파일들을 프로젝트 폴더에 배치시킵니다.
```bash
CA.pem
client.key
client.crt
```

4. 서버를 구동시킨 상태에서 ai-client를 구동하여 socket server로 접속을 시도하면 다음과 같이 잘 접속되는 것을 확인할 수 있습니다. 또한, 미리 구성한 보안 접속도 잘 작동하는 것을 확인할 수 있습니다.
![image](https://github.com/user-attachments/assets/98fdf151-ee23-41ba-a09d-fc1ac6ffd2d0)



# 11. Result (수행 결과)


# 11. Tech Stack (기술 스택)

### Co-Work(Communication)
![Github](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white)
<img src="https://img.shields.io/badge/gitkraken-179287?style=for-the-badge&logo=gitkraken&logoColor=white"/>
<img src="https://img.shields.io/badge/notion-%23000000?style=for-the-badge&logo=notion&logoColor=white"/> 
<img src="https://img.shields.io/badge/slack-%234A154B?style=for-the-badge&logo=slack&logoColor=white"/>
<img src="https://img.shields.io/badge/discord-5865F2?style=for-the-badge&logo=discord&logoColor=white"/>

### IDE
![PyCharm](https://img.shields.io/badge/pycharm-%23000000?style=for-the-badge&logo=pycharm&logoColor=white")
<img src="https://img.shields.io/badge/Jupyter_Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
<img src="https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white"/> 


### Frontend
![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
<img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/Javascript-ffb13b?style=for-the-badge&logo=javascript&logoColor=white"/>
<img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"/> 
<img src="https://img.shields.io/badge/vuetify-%231867C0?style=for-the-badge&logo=vuetify&logoColor=white"/>
<img src="https://img.shields.io/badge/typescript-3178C6?style=for-the-badge&logo=typescript&logoColor=black"/>
<img src="https://img.shields.io/badge/axios-%235A29E4?style=for-the-badge&logo=axios&logoColor=white"/>

### Backend
![Python](https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white)
<img src="https://img.shields.io/badge/pandas-%23150458?style=for-the-badge&logo=pandas&logoColor=white"/> 
<img src="https://img.shields.io/badge/numpy-%23013243?style=for-the-badge&logo=numpy&logoColor=white"/>
<img src="https://img.shields.io/badge/Openpyxl-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white"/>
<img src="https://img.shields.io/badge/SQLAlchemy-666699?style=for-the-badge&logo=sqlalchemy&logoColor=white"/>

### Fast API (AI Core)
![FastAPI](https://img.shields.io/badge/fastapi-%23009688?style=for-the-badge&logo=fastapi&logoColor=white)
<img src="https://img.shields.io/badge/Machine_Learning-FF6F00?style=for-the-badge&logo=machine-learning&logoColor=white"/>
<img src="https://img.shields.io/badge/scikitlearn-%23F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white"/>
<img src="https://img.shields.io/badge/Deep_Learning-00599C?style=for-the-badge&logo=deep-learning&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white"/>

### CI-CD Infrastructure
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
<img src="https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazon-ec2&logoColor=white"/>
<img src="https://img.shields.io/badge/AWS_S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white"/>
<img src="https://img.shields.io/badge/github%20actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white"/>
<img src="https://img.shields.io/badge/docker-%232496ED?style=for-the-badge&logo=docker&logoColor=white"/> 
<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
<img src="https://img.shields.io/badge/redis-%23FF4438?style=for-the-badge&logo=redis&logoColor=white"/>
<br><br><br>

# 12. 테스트 보고서 (CI 테스트 결과)
1. **테스트 환경**  
  * Jest

2. **유닛 테스트**  
  * Mocking test
  * 게시판에 게시글이 예상대로 등록되는지 확인

3. **커버리지 테스트**  
   * 커버리지 테스트를 통하여 코드 품질을 모니터링하고 개선할 수 있음  
   * 테스트 결과, 코드베이스에서 약 87퍼센트 실행됨을 알 수 있음  
  ![Coverage1](https://github.com/user-attachments/assets/e3d13016-8efc-4681-8264-f4cc047f0c3a)  
4. **테스트 스크린샷**  
  * 🧪 **Backend Build Test**  
    <img width="976" alt="Backend-Build-Test" src="https://github.com/user-attachments/assets/b7ad4ba0-f070-477a-b1f6-39460f94837c">  
  * 🧪 **Frontend Build Test**  
    <img width="993" alt="Frontend-Build-Test" src="https://github.com/user-attachments/assets/449cff0e-1953-4a93-aa0f-3ea8e07291d9">   
  
5. **결 론**
  * 🆗 _Backend_ 와 _Frontend_ 모두 성공적으로 **Build** 되는 것을 확인할 수 있습니다.

# 13. Deploy Issue (배포 이슈)
1. **Error: repository name must be lowercase**
![Issue1](https://github.com/user-attachments/assets/0eaa074a-c88e-469b-8ab2-e90919ad1c88)  
<br>

### _Solution_   
만약 actor가 Uppercase라면, 아래와 같이 직접 Lowercase를 명시하여 문제를 해결할 수 있습니다.

```yaml
name: Django CD (Continuous Deploy)

on:
  repository_dispatch:
    types: [BACKEND_TEST_FINISH_TRIGGER]

jobs:
  build:
    name: build-app
    runs-on: ubuntu-latest
    steps:
    - name: Checkout repository
      uses: actions/checkout@v3
```
  
위의 내용을 아래와 같이 수정합니다.  
```yaml
name: Django CD (Continuous Deploy)

on:
  repository_dispatch:
    types: [BACKEND_TEST_FINISH_TRIGGER]
    
env:
  DOCKER_IMAGE: ghcr.io/${{ secrets.REAL_ACTOR }}/tcp-backend

jobs:
  build:
    name: build-app
    runs-on: ubuntu-latest
    steps:
    - name: Checkout repository
      uses: actions/checkout@v3
```

그리고 아래 내용을 수정합니다.  
```yaml
- name: Build and Push Docker Image
  run: |
    cd tcp_backend/tcp_django
    docker buildx build --platform linux/arm64 -f Dockerfile -t ghcr.io/${{ github.actor }}/tcp-django-backend-server:latest --push .
```
  
위의 내용을 아래와 같이 수정합니다.
```yaml
- name: Build and Push Docker Image
  run: |
    cd tcp_backend/tcp_django
    docker buildx build --platform linux/arm64 -f Dockerfile -t ${{ env.DOCKER_IMAGE }}:latest --push .
```

**secrets**에 _REAL_ACTOR_ 를 설정하고 _REAL_ACTOR_ 를 **소문자 본인 계정**으로 작성하면 됩니다.  
ex) Ah-ram >> ah-ram  

마지막으로 아래 내용을 수정합니다.  
```yaml
deploy:
  needs: build
  name: Deploy
  runs-on: [ self-hosted, deploy-tcp-backend ]
  steps:
  - name: Login to GHCR
    uses: docker/login-action@v1
    with:
      registry: ghcr.io
      username: ${{ github.actor }}
      password: ${{ secrets.GHCR_TOKEN }}
```

위의 내용을 아래와 같이 수정합니다.  
```yaml
deploy:
  needs: build
  name: Deploy
  runs-on: [ self-hosted, deploy-lms-backend ]
  steps:
  - name: Login to GHCR
    uses: docker/login-action@v1
    with:
      registry: ghcr.io
      username: ${{ secrets.REAL_ACTOR }}
      password: ${{ secrets.GHCR_TOKEN }}
```

2. **Cannot connect to the Docker daemon at <workdir>**
![Issue2](https://github.com/user-attachments/assets/775cadb2-3228-425a-bf98-9ebf4aed8d43)  
<br>

### _Solution_  
local에 **docker desktop이 켜져있는지 확인**해보아야 합니다.  
Docker desktop을 실행하고 다시 시도하니 해결되었습니다.  

3. **FastAPI 배포 이후, 웹에 접속이 되지 않습니다.**
<img width="722" alt="Issue3" src="https://github.com/user-attachments/assets/89331de6-8e8b-42d8-bf7b-e15364e2260d">
<br>

### _Solution_  
FastAPI 배포 후, **인스턴스 보안 그룹에서 33333 port에 대하여 인바운드 설정**을 해주어야 합니다.  
설정하고 다시 접속하면 정상적으로 처리되는 것을 확인할 수 있습니다.  
![Issue3-1](https://github.com/user-attachments/assets/0a4d7844-692f-43e2-98fb-76680f98e5a1)  
  
# 14. 한 줄 회고
🤓<b>한재혁</b>  
_AWS와 Docker에 대해서 배우고 싶었는데, 단순히 배우는 것에서 그치지 않고 웹 애플리케이션 작성부터 배포까지 경험할 수 있어서 정말 좋은 경험이었습니다! 팀원분들도 같이 열심히 해주셔서 어렵지 않게 마무리 할 수 있었습니다. 다들 고생하셨습니다!!👏_  

👨‍💻<b>민경원</b>  
_AWS -GitHub Actions-Docker등을 이용한 CI-CD 구축을 직접 경험해볼 수 있어서 좋았습니다._  

😺<b>정아람</b>  
_CI/CD 환경 구성으로 프로젝트 배포를 자동화하고 AWS와 결합해 서비스를 할 수 있는 좋은 경험이었습니다._  

🪐<b>최인헌</b>  
_Django, MySQL과 Vue를 활용하여 웹 기반 서비스들의 작동 방식을 이해하는 기회가 되었고, AWS와 GitHub Actions를 활용하여 배포까지 해봄으로서 CI/CD가 어떻게 이루어지는지 알 수 있었던 계기가 되었습니다. 모두 고생 많으셨습니다!_  

😁<b>이용휘</b>  
_AWS와 Docker를 제대로 다루어 본 것은 처음인데, 다양한 issue들을 겪어서 힘들었지만 그만큼 많이 배운 것 같습니다._  
