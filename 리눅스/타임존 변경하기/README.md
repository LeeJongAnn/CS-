# 리눅스 타임존 변경하기 

1. /etc/localtime 삭제 
2. /usr/share/zoneinfo/Asia/Seoul를 localtime에 심볼릭 링크 걸어줌
3. localtime 생성되면 date 갈기면 됨