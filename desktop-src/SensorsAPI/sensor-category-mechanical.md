---
description: 感應器 \_ 類別 \_ 機械類別包含的感應器，可提供機械裝置和測量的相關資訊。
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: 'SENSOR_CATEGORY_MECHANICAL (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbac9a00895b08bd99106af7f0b6986118b4645dac690fd190f734e1499940dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666708"
---
# <a name="sensor_category_mechanical"></a>感應器 \_ 類別 \_ 機械

感應器 \_ 類別 \_ 機械類別包含的感應器，可提供機械裝置和測量的相關資訊。

**平臺定義的感應器類型**

此類別包括下列平臺定義的感應器類型。



| 感應器類型                                                                                                                                                                                                                                                                                                           | 描述                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**感應器 \_類型 \_ 布林值 \_ 參數**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt> </dl>                    | 雙狀態參數 (關閉或) 。<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**感應器 \_類型 \_ 布林值 \_ 參數 \_ 陣列**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt> </dl> | 雙狀態參數的陣列 (關閉或) 。<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**感應器 \_輸入 \_ FORCE**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt> </dl>                                                | 強制感應器。<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**感應器 \_類型多重值 \_ \_ 參數**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | 多重位置切換。<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**感應器 \_類型 \_ 壓力**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | 壓力感應器。<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**感應器 \_類型 \_ SCALE**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | 加權感應器。<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**感應器 \_輸入 \_ 壓力**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | 減輕感應器。<br/>                          |



**平臺定義的資料欄位**

此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ guid \_ 機械 \_ guid 為基礎：

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

此類別包括下列的平臺定義資料欄位。



| 資料欄位名稱和 PID                                                                                                                                                                                                                                                                                                         | 描述                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 絕對 \_ 壓力 \_ PASCAL**</dt> <dt> (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> 帕斯卡中的絕對壓力。<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 布林值 \_ SWITCH \_ 陣列 \_ 狀態**</dt> <dt> (PID = 10)</dt> </dl> | **VT \_ UI4**<br/> 布林值參數陣列的狀態欄位。<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 布林值 \_ 切換 \_ 狀態**</dt> <dt> (PID = 2)</dt> </dl>                       | **VT \_ BOOL**<br/> 感應器 \_ 類型 \_ 布林值參數的狀態欄位 \_ 。<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ FORCE \_ NEWTONS**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> 在 newtons 中強制執行。<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**感應器 \_資料類型量測計 \_ \_ \_ 壓力 \_ PASCAL**</dt> <dt> (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> 相對量測計壓力，以帕斯卡。<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**感應器 \_資料 \_ 類型多值 \_ \_ 切換 \_ 狀態**</dt> <dt> (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> 感應器類型多重值參數的狀態欄位 \_ \_ \_ 。<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 負擔**</dt> <dt> (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> 應變。<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 權數 \_ 公斤**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> 權數，以公斤為限。<br/>                             |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>感應器。h</dt> </dl> |



 

 




