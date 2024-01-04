## Compile-python and Create VirtualEnv with It
`sudo apt-get update`

`sudo apt-get install build-essential gdb lcov libbz2-dev libffi-dev libgdbm-dev liblzam-dev libncurses5-dev libreadline6-dev libsqlite3-dev libssl-dev lzma lzma-dev tk-dev uuid-dev zliblg-dev`

터미널 창 하나 더 열어서 htop입력시 메모리사용량 실시간 관찰 可  


## get link from Ptyhon homepage of Gzipped source tarball
`wget https://www.python.org/ftp/python/3.11.7/Python-3.11.7.tgz`

`tar zxvf Python-3.11.7.tgz`

`rm Python-3.11.7.tgz`

`cd Python-3.11.7/`

`./configure --enable-optimizations`

16개 코어를 다 complie하는데 쓰고싶다는 명령어. 환경에 맞게 숫자 조정한다.
현재 htop에 8개만 뜨므로 8개로 써야함
`make -j 16`

현 위치에서 (최신버전) 파이썬 사용가능하도록 설치(Python-3.11.7 폴더)
`sudo make altinstall`

cd .. 작업 후 그냥 python 입력시 vscode 내장된 3.10버전 실행됨.
/usr/local/bin/python3.11 실행시 3.11.7버전 실행!
이제 기존 명령어 python을 3.11.7버전 실행하도록 바꾸어보자.
`vim ~/.bashrc`
`source ~/.bashrc`

기존 내장 파이썬을 특정 조건에서 실행시키도록하려면
`python -m venv ~/.venv`

`vim ~/.bashrc`
`source ~/.bashrc`