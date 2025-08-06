# MT8050IE EtherCAT Integration

Проект интеграции панели управления Wientek MT8050IE через преобразователь интерфейсов RS485-EtherCAT MS-A2-1011 к серводрайверу SZGH-E7A20LE.

## Схема подключения
![Connection Diagram](docs/connection_diagram.png)

## Особенности:
- Используется кроссовый EtherCAT кабель (1-3, 2-6)
- Преобразователь интерфейсов MS-A2-1011
- Интеграция с TwinCAT 3

## Документация
1. [Инструкция по TwinCAT 3](twincat3/integration_guide.md)
2. [Распиновка EtherCAT](docs/ethercat_pinout.png)
3. [Спецификации оборудования](hardware/)

## Пример кода TwinCAT
```plc
PROGRAM MAIN
VAR
    bEnable : BOOL;
END_VAR
