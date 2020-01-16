## Docker miniconda3 준비

### 도커 설치

### 미니콘다 설치 및 컨테이너 제작 실행

https://hub.docker.com/r/continuumio/miniconda3

`❯ docker run --name notebook_study -it -p 8888:8888 -v ~/Development/study/notebook-study:/notebooks continuumio/miniconda3`



### 컨테이너 내에서 라이브러리 설치

`(base) root@f31dcb0416d5:/# /opt/conda/bin/conda install -c conda-forge matplotlib -y --quiet`


### 쥬피터 노트북 설치

`(base) root@f31dcb0416d5:/# /opt/conda/bin/conda install jupyter -y --quiet `


### 필요하다면 이것들도 설치

`(base) root@f31dcb0416d5:/# apt install curl wget vim`



### 쥬피터 노트북 실행

`(base) root@f31dcb0416d5:/# /opt/conda/bin/jupyter notebook --notebook-dir=/notebooks --ip='*' --port=8888 --no-browser --allow-root`


### 쥬피터 노트북 실행

- http://localhost:8888/ 접속 후 jupyter notebook 사용

- `control + z` 입력으로 서버 종료

- `(base) root@f31dcb0416d5:/# exit`


### Docker 컨터이너 재접속

`❯ docker start notebook_study`

`❯ docker attach notebook_study`


### ./jpt.sh 파일 생성 후 실행

`/opt/conda/bin/jupyter notebook --notebook-dir=/notebooks --ip='*' --port=8888 --no-browser --allow-root`

`(base) root@f31dcb0416d5:/# chmod 755 jpt.sh`
