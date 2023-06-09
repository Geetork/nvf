# Виртуализация сетевых функций
## Lab1-2. Создание топологии
Для того чтобы начать работу с эмулятором компьютерной сети Mininet, необходимо было скачать виртуальную машину [mininet VM](http://mininet.org/download).
На виртуальной машине был создан файл LinearTopo.py, в котором описана кастомная топология сети, состоящая из четырех коммутаторов и четырех хостов.

<img src="https://user-images.githubusercontent.com/58363643/224634051-691da8a7-802e-4e79-89c9-d37e7d2d6f05.png" width="600px">
<img src="https://user-images.githubusercontent.com/58363643/224634194-a586d687-a701-429b-80f1-d0ccff2b9a3f.png" width="600px">

Была проверена работа скрипта с помощью команды: 

    sudo mn --custom LinearTopo.py --topo custom
    
В консоли получен вывод, который показывает, что собрана топология, содержащая 4 коммутатора и 4 хоста.

<img src="https://user-images.githubusercontent.com/58363643/224634287-ea148b0b-efd6-4b19-82e0-61e71f1b9182.png" width="400px">

Для проверки связности пропингован каждый хост с каждого хоста:

    pingall
    
<img src="https://user-images.githubusercontent.com/58363643/224634443-9d16b67b-bb4e-4d99-bca5-ad9e122f1e5e.png" width="200px">

## Lab3.

## Выводы
Таким образом, познакомились с основами программно-конфигурируемых сетей с помощью изучения работы эмулятора компьютерной сети Mininet, ознакомились с тем, как с помощью питоновского скрипта собрать сеть. Также ознакомилимь с базовыми командами для работы с Mininet.

## Экзаменационное задание

[экзаменационое задание.pdf](https://github.com/Geetork/nvf/files/11010635/default.pdf)
