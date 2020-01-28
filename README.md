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

echo "> 현재 구동중인 애플리케이션 pid 확인"
CURRENT_PID=$(pgrep -f ${PJ_NAME}*.jar)

if [ -z "$CURRENT_PID" ]; then
  echo "> 현재 구동중인 애플리케이션이 없으므로 종료하지 않습니다."
else
  echo "> kill -15 $CURRENT_PID"
  kill -15 $CURRENT_PID
  sleep 5
fi
echo "> 성공"
```
