---
description: 感應器 \_ 類別的 \_ 電氣類別包含可提供電力系統相關資訊的感應器。
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: 'SENSOR_CATEGORY_ELECTRICAL (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3487b779cfefc78a541fcc72d1f2c5c5e7c0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991992"
---
# <a name="sensor_category_electrical"></a>感應器 \_ 類別 \_ 電氣

感應器 \_ 類別的 \_ 電氣類別包含可提供電力系統相關資訊的感應器。

**平臺定義的感應器類型**

此類別包括下列平臺定義的感應器類型。



| 感應器類型                                                                                                                                                                                                                                                                                              | Description                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**感應器 \_類型 \_ 電容**</dt> <dt>{CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | 電容感應器。<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**感應器 \_輸入 \_ CURRENT**</dt> <dt>{5ADC9FCE-15A0-4BBE-A1AD-2D38A9AE831C}</dt> </dl>                             | 目前的感應器。<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**感應器 \_輸入 \_ 電 \_ 電源**</dt> <dt>{212F10F5-14AB-4376-9A43-A7794098C2FE}</dt> </dl> | 電感應器。<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**感應器 \_類型 \_ 頻率**</dt> <dt>{8CD2CBB6-73E6-4640-A709-72AE8FB60D7F}</dt> </dl>                       | 電力頻率感應器。<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**感應器 \_輸入 \_ 電感**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> </dl>                    | 電感感應器。<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**感應器 \_輸入 \_ POTENTIOMETER**</dt> <dt>{2B3681A9-CADC-45AA-A6FF-54957C8BB440}</dt> </dl>           | 電位器。<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**感應器 \_類型 \_ 電阻**</dt> <dt>{9993D2C8-C157-4A52-A7B5-195C76037231}</dt> </dl>                    | 阻力感應器。<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**感應器 \_類型 \_ 電壓**</dt> <dt>{C5484637-4FB7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | 電壓感應器。<br/>             |



**平臺定義的資料欄位**

此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型的 \_ 電力 \_ GUID 為基礎：

{BBB246D1-E242-4780-A2D3-CDED84F35842}

此類別包括下列的平臺定義資料欄位。



| 資料欄位名稱和 PID                                                                                                                                                                                                                                                                                                         | Description                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 電容 \_ FARAD**</dt> <dt> (PID = 4)</dt> </dl>                                | **VT \_ R8**<br/> Farads 中的電容。<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 目前的 \_ 安培**</dt> <dt> (PID = 3)</dt> </dl>                                                | **VT \_ R8**<br/> 目前的安培。<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**感應器 \_資料 \_ 類型的 \_ 電力 \_ 頻率 \_ 赫茲**</dt> <dt> (PID = 9)</dt> </dl>     | **VT \_ R8**<br/> 以赫茲為單位的電氣頻率。<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ \_ 的百分比 \_ ， \_ 範圍**</dt> <dt> (PID = 8)</dt> </dl> | **VT \_ R8**<br/> Potentiometer 讀取以可能範圍的百分比表示。<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 電 \_ 功率 \_ 瓦**</dt> <dt> (PID = 7)</dt> </dl>                | **VT \_ R8**<br/> 耗電量瓦。<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 電感 \_ HENRY**</dt> <dt> (PID = 6)</dt> </dl>                                    | **VT \_ R8**<br/> Henries 中的電感。<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 電阻 \_ OHMS**</dt> <dt> (PID = 5)</dt> </dl>                                       | **VT \_ R8**<br/> Ohms 的阻力。<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 電壓 \_ 伏**</dt> <dt> (PID = 2)</dt> </dl>                                             | **VT \_ R8**<br/> 伏特的電力潛力。<br/>                               |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>感應器。h</dt> </dl> |



 

 




