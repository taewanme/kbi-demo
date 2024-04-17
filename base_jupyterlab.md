## Jupyter lab 구성


```
sudo yum install python3 python3-pip -y
pip3 install jupyterlab
jupyter lab --generate-config

```

## 패스워드 설정

```
jupyter lab password
```

- 입력: Welcome1
- 확인입력: Welcome1

## Jupyter Lab 구성
```
echo "c.NotebookApp.open_browser = False" >> ~/.jupyter/jupyter_lab_config.py
echo "c.NotebookApp.ip = '0.0.0.0'" >> ~/.jupyter/jupyter_lab_config.py
echo "c.NotebookApp.port = 8888" >> ~/.jupyter/jupyter_lab_config.py
echo "c.NotebookApp.allow_origin = '*'" >> ~/.jupyter/jupyter_lab_config.py
```

## Java 설치

```
sudo yum install java-17-amazon-corretto -y
```

## 서비스 등록

````
wget https://raw.githubusercontent.com/taewanme/kbi-demo/main/jupyter.service
chmod 777 jupyter.service 
sudo chown root:root jupyter.service 
sudo mv ./jupyter.service /etc/systemd/system/
sudo systemctl daemon-reload  
sudo systemctl enable jupyter.service  # jupyter.service 등록
sudo systemctl start jupyter.service  # jupyter.service 시작
sudo systemctl status jupyter.service
```
