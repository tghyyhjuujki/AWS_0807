1. https://github.com/joneconsulting/simple-nodejs.git에서 본인 github 계정으로 코드 복사
2. AWS RDS 서비스 생성 
    - simple-nodejs/db/createTable.txt 참조
3. AWS EC2 인스턴스 생성
    - simple-nodejs/ver1.0 프로젝트를 포함하는 EC2 인스턴스 생성 (version 1.0)
    - Port 8000으로 실행
    - RDS와 연동
4. AWS Auto Scaling 생성 (BLUE)
    - 최소 1개, 최대 2개의 인스턴스가 유지될 수 있도록 Auto Scaling 설정
5. AWS Elastic Load Balance 생성
6. S3에 index.html 페이지를 생성
    - simple-nodejs/static/index.html 참조
    - Load Balancer로 이동할 수 있는 링크 수정
------------------------------------------------------------
7. AWS EC2 인스턴스 생성
    - simple-nodejs/ver2.0 프로젝트를 포함하는 EC2 인스턴스 생성 (version 2.0)
    - Port 9000으로 실행
    - RDS와 연동
8. AWS Auto Scaling 생성 (GREEN)
    - 최소 1개, 최대 2개의 인스턴스가 유지될 수 있도록 Auto Scaling 설정
9. AWS Elastic Load Balance에서 버전 업그레이드
    - Verion 1.0에서 Verion 2.0으로 업그레이드 배포 