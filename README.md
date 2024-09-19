# Linux-Crontab
Basic of Linux, do some automation settings for my Linux with Crontab

## 1. 현재시간 로그 남기기
![image](https://github.com/user-attachments/assets/db3107ba-0ad6-4bf9-b402-4f722e9098ac)
현재 디렉터리 위치 확인

![image](https://github.com/user-attachments/assets/ff973957-a8c5-44b3-affc-f1db2da5a54c)
Cron파일 설정

![image](https://github.com/user-attachments/assets/2e0f03a8-c778-4d8a-8aa5-4b0f4bfaaecd)
* * * * * date > /home/username/aaa.log -> aaa/log에 매분마다 로그 작성
          
![image](https://github.com/user-attachments/assets/1a79437f-bde9-4e03-9c65-d8094d0616f5)
Cron 서비스 재시작 및 상태확인
          
![image](https://github.com/user-attachments/assets/148efdf4-80fc-4663-a42e-bde59ba1d449)


## 2. 파이썬 이용하여 현재 시간 로그 남기기
![image](https://github.com/user-attachments/assets/e7acadb4-6fae-4891-82f5-78cd76daa935)
파이썬 코드 작성해서 현재시각 출력 설정

![image](https://github.com/user-attachments/assets/b639e016-26de-4b32-aabe-e7a01a6c2ecb)
파이썬 파일 확인

![image](https://github.com/user-attachments/assets/984e5f54-14fd-4b8b-ad9b-11d774d487ab)
파이썬 파일 실행 후, 정상확인

![image](https://github.com/user-attachments/assets/dcc6383f-1902-4602-abc5-11c566c6b2e4)
Cron 파일 설정
python3 /home/username/test.py >> /home/username/test.log 
파이썬에서 실행한 파일들의 로그가 test.log에 저장

![image](https://github.com/user-attachments/assets/17f64f55-b12d-4cde-98ee-44319e2dbcbb)
Cron 서비스 재시작 및 상태확인

![image](https://github.com/user-attachments/assets/aaaf21f6-7f99-495a-91ce-1e3bf2a89341)



## 3. 현재 디스크 용량 파이썬 이용하여 로그 남기기

![image](https://github.com/user-attachments/assets/bb57bae9-215a-4298-a826-69771a237c6c)
파이썬 코드활용하여 전체 디스크 용량, 사용 중인 디스크 용량, 남은 디스크 용량 출력 설정

![image](https://github.com/user-attachments/assets/65b46a80-c06a-4a82-83c9-9566736f9597)
파이썬 파일 확인

![image](https://github.com/user-attachments/assets/11bd7fd4-6205-4e37-944c-5c25e05776bc)
파이썬 파일 실행 후, 정상확인

![image](https://github.com/user-attachments/assets/45b02773-9f46-4382-a83c-d5a20285a428)
Cron 파일 설정
python3 /home/username/disk.py >> /home/username/aaa.log 
파이썬에서 실행한 파일들의 로그가 aaa.log에 저장

![image](https://github.com/user-attachments/assets/8ebd6339-de54-471f-bcea-135ce67d70d5)
Cron 서비스 재시작 및 상태확인

![image](https://github.com/user-attachments/assets/e33c79fb-7ebc-4aa9-90e7-469293f3e851)
