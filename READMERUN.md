# Инструкция по запуску инференса
* Создать папку **ckpt**.
  ```powershell
  mkdir ckpt
* Скачать веса моделей https://vicserver.crs4.it/atlantanet/, переместить их в папку ckpt.
* Создать виртуальное окружение 
  ```powershell
  python -m venv venv
* Активировать виртуальное окружение
  ```powershell
  .\venv\Scripts\Activate.ps1
* Установить необходимые зависимости
  ```powershell
  pip install -r .\requirements.txt
* Запустить инференс
  ```powershell
  python inference_atlanta_net.py --pth ckpt/resnet101_atlantalayout.pth --img data/atlantalayout/test/img/2t7WUuJeko7_c2e11b94c07a4d6c85cc60286f586a02_equi.png
* Предобработка панорамного изображения
  ```powershell
  python inference_atlanta_net.py --pth ckpt/resnet101_atlantalayout.pth --img .\preprocesspanoram.jpg