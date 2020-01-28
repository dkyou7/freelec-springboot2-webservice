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

echo "> step1 디렉토리로 이동"
cd $REPOSITORY

echo "> Build 파일 복사"
cp $REPOSITORY/$PJ_NAME/build/libs/*.jar $REPOSITORY/

echo "> 성공"
```
