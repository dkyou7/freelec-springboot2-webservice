# freelec-springboot2-webservice

```bash
#!/bin/bash

REPOSITORY=/home/ec2-user/app/step1
PJ_NAME=freelec-springboot2-webservice

cd $REPOSITORY/$PJ_NAME/

echo "> Git pull"
git pull

echo "> 프로젝트 빌드 시작"
./gradlew build

echo "> 성공"
```
