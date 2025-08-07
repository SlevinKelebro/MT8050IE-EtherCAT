# Интеграция MT8050IE с TwinCAT 3

## 1. Настройка EtherCAT Master
1. Откройте TwinCAT XAE Shell.
2. Добавьте устройство: `ПКМ → Add New Item → EtherCAT Master`.
3. Настройте параметры:
   - Cycle Time: `1 ms`
   - DC Synchronization: Enabled

## 2. Добавление устройств
1. **Преобразователь MS-A2-1011**:
   - ESI-файл: `ms-a2-1011.xml` (загрузите в `TwinCAT/IO/EtherCAT`).
   - Адрес: `0x1000`.

2. **Серводрайвер SZGH-E7A20LE**:
   - Используйте стандартный профиль `CiA 402`.

## 3. PDO-Маппинг
Настройте обмен данными через таблицу:
```csv
Index, Subindex, Name, Direction, Data Type
0x1600, 0x01, OutputByte0, Output, UINT8
0x1A00, 0x01, InputByte0, Input, UINT8
