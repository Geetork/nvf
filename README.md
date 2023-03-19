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

## Виртуализация сетевых функций
NFV (Network Function Virtualization) подразумевает виртуализацию сетевых функций, которые на данный момент выполняются на физическом оборудовании таком, как маршрутизаторы, коммутаторы. NFV позволяет использовать программное обеспечение для настройки и управления физическими устройствами.

Благодаря виртуализация сетевых функций можно добиться следующего:

- Сокращение потребностей в оборудовании - при виртуализации инфраструктуры количество оборудования сводится к минимуму. Также нивелируется проблема избыточной подготовки, которая часто встречается при работе с физическим оборудованием. 
   
- Экономия места и энергии возможна при работе с виртуальными сервисами, которыми можно полностью управлять с помощью программного обеспечения.
   
- Сокращение времени на выпуск служб, то есть развертывание сетевых служб выполняется гораздо быстрее, чем это возможно при использовании аппаратного обеспечения. Изменения вносятся достаточно быстро при изменении требований предприятий.
   
- Возможность масштабирования услуг по требованию.
   
Рассмотрим основные архитектурные компоненты NFV:

- NFV Infrastructure представляет собой совокупность физических ресурсов, их компоненты и конфигурации. Например, серверы с гипервизорами и системами виртуализации, сетевые устройства, хранилища данных;
   
- Virtualized Network Functions (VNF) – это основа архитектуры NFV, которая представляет собой виртуализированные функции сетевых элементов. VNF-элементом, как правило, является виртуальная машина или совокупность нескольких виртуальных машин.
   
- NFV Management and Orchestration (MANO) управляет жизненным циклом виртуальных элементов и инфраструктурой, то есть является системой, которая в автоматизированном режиме запускает сетевые функции, отслеживает их состояние и масштабирует при увеличении нагрузки, перезапускает при неправильном поведении, а также останавливает их работу.
- Virtual Customer Premises Equipment (vCPE) – это виртуализация конечных устройств заказчика в операторском облаке.
   
- Element Management System (EMS) отвечает за управление FCAPS (Fault, Configuration, Accounting, Performance, Security Management.
   
    NFV удобна и необходима, поскольку данная технология позволяет использовать виртуализированные функции, например, такие как маршрутизация и брандмауэр, и визуализировать их. Традиционные устройства, брандмауэры и маршрутизаторы более подвержены сбоям, чем их виртуализированные версии. С помощью виртуализации сетевых функций можно развертывать функции в виде виртуальных машин на различных аппаратных средствах, что появляется менять структуру сети. Также данные функции можно будет перемещать и автоматически перезапускать по мере необходимости. Другими словами, сетевая инфраструктура становится гораздо более гибкой после ее виртуализации.
Виртуализация сетевых функций также имеет заметные преимущества с точки зрения восстановления. Если произойдет стихийное бедствие или системный сбой, то быстрое восстановление физических устройств будет невозможно. Однако виртуальное устройство может быть перемещено в другое место или центр обработки данных, чтобы была возможность быстро восстановить нормальную работу сети.

В современных программно-определенных центрах обработки данных сетевые функции, выполняемые аппаратными устройствам, например, подсистемами балансировки нагрузки, брандмауэрами, маршрутизаторами, коммутаторами, все чаще виртуализированы как виртуальные устройства. Такая виртуализация сетевых функций является естественным этапом развития виртуализации серверов и сетей. Виртуальные устройства быстро появляются и создают совершенно новый рынок. Они продолжают создавать интересы и получать импульс как на платформах виртуализации, так и в облачных службах. Например, корпорация Майкрософт включила автономный шлюз в качестве виртуального устройства, начиная с Windows Server 2012 R2.

Таким образом, NFV показал себя как популярную и полезную концепцию даже в зародыше. Приложения виртуализации сетевых функций многочисленны, например, виртуализация мобильных базовых станций, платформа как услуга (PaaS), сети доставки контента (CDN), фиксированный доступ и домашняя среда. Ожидается, что потенциальные преимущества NFV будут значительными, а также, что виртуализация сетевых функций, развернутых на стандартизированном оборудовании общего назначения, сократит капитальные и эксплуатационные расходы и время внедрения услуг и продуктов. Многие крупные поставщики сетевого оборудования заявили о поддержке NFV. Это совпало с объявлениями NFV от основных поставщиков программного обеспечения, которые предоставляют платформы NFV, используемые поставщиками оборудования для создания своих продуктов NFV.

