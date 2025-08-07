# MT8050IE EtherCAT Integration Project
Проект интеграции панели управления Wientek MT8050IE через преобразователь RS485-EtherCAT MS-A2-1011 с серводрайвером SZGH-E7A20LE и TwinCAT 3.

![Схема подключения](docs/connection_diagram.png)

## 🔌 Блок-схема подключения
```plaintext
[MT8050IE (RS485)] 
       │
       ▼
[MS-A2-1011 (RS485→EtherCAT)]
       │
       ▼ 
[EtherCAT Network (кроссовый кабель: 1-3, 2-6)]
       │
       ▼
[SZGH-E7A20LE (EtherCAT Slave)]
       │ 
       ▼
[TwinCAT 3 (EtherCAT Master)]
