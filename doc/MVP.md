# Minimal Viable Product
### Нижче представлена демонстрація роботи програми в середовищі Kubernetes:
![Image](./654184.gif)
#### 1) Перевіряємо наявні сервіси:
```bash
$ k get svc
```
#### 2) Нас цікавить сервіс із назвою ambassador. Активуємо для нього порт 8088:
```bash
$ k port-forward svc/ambassador 8088:80&
```
#### 3) Перевіряємо відповідь порту
```bash
$ curl http://localhost:8088
```
#### 4) Підставляємо додатку наш малюнок і отримуємо бажаний результат в ascii graphics:
```bash
$ curl -F "image=@trident.png" localhost:8088/img/
```

### Демонстрація роботи інтерфейса ArgoCD і його реакції на зміни вихідного коду

[![Video](.img/MVP.PNG)](https://youtu.be/jwjv506laSo)

### Скріншоти налаштування застосунку на синхронізацію з репозиторієм https://github.com/den-vasyliev/go-demo-app та налаштованої автоматичної синхронізації
![Image2](.img/den_vas1.png)
![Image3](.img/den_vas2.png)
![Image4](.img/den_vas3.png)
![Image5](.img/den_vas4.png)
