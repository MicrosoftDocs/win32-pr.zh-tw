---
description: '[感應器 \_ 類別] \_ 環境類別包含的感應器，可提供有關周圍環境或天氣的資訊。'
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: 'SENSOR_CATEGORY_ENVIRONMENTAL (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7cc2a6ca1d2832045a77f0a2ffa1902732e484700afaacd757719e99d667c55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126608"
---
# <a name="sensor_category_environmental"></a>感應器 \_ 類別 \_ 環境

[感應器 \_ 類別] \_ 環境類別包含的感應器，可提供有關周圍環境或天氣的資訊。

**平臺定義的感應器類型**

此類別包括下列平臺定義的感應器類型。



| 感應器類型                                                                                                                                                                                                                                                                                                                                                     | 描述               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**感應器 \_輸入 \_ 環境 \_ 大氣 \_ 壓力**</dt> <dt>{0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | 氣壓 計。<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**感應器 \_輸入 \_ 環境 \_ 濕度**</dt> <dt>{5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Hygrometers.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**感應器 \_輸入 \_ 環境 \_ 溫度**</dt> <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | 溫度計<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**感應器 \_輸入 \_ 環境 \_ 風 \_ 方向**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | 氣象 vanes。<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**感應器 \_輸入 \_ 環境 \_ 風 \_ 速度**</dt> <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> </dl>                               | Anemometers.<br/>   |



**平臺定義的資料欄位**

此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型的 \_ 環境 \_ GUID 為基礎：

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

此類別包括下列的平臺定義資料欄位。



| 資料欄位名稱和 PID                                                                                                                                                                                                                                                                                                                                    | 描述                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 大氣 \_ 壓力 \_ BAR**</dt> <dt> (PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Atmospheres (橫欄) 的大氣壓力。<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 溫度 \_ 攝氏**</dt> <dt> (PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> 溫度（攝氏）。<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**感應器 \_DATA \_ TYPE \_ 相對濕度 \_ \_ PERCENT**</dt> <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> 相對濕度（以百分比表示）。<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 的 \_ 方向 \_ 是 \_ 逆時針**</dt> <dt> (PID = 5)</dt> </dl> | **VT \_ R4**<br/> 相對於磁性北部的風方向（以度為單位）。 北部會以 X 軸)  (頂端0.0 表示，而值會以逆時針旋轉的方式遞增。 Z 軸會向上指向。 <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**感應器 \_\_每秒的資料類型 \_ 風 \_ 速度 \_ 計量 \_ \_**</dt> <dt> (PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> 每秒計量速度。<br/>                                                                                                                                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>感應器。h</dt> </dl> |



 

 




