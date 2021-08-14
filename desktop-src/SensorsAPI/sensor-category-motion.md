---
description: '[感應器 \_ 類別] \_ 動作類別包含的感應器，會提供與實體移動相關的資訊。'
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: 'SENSOR_CATEGORY_MOTION (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d57c8406ad1344d696f63e574484943ea68a6654f63c3d7d38e904aaa44e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889486"
---
# <a name="sensor_category_motion"></a>感應器 \_ 類別 \_ 移動

[感應器 \_ 類別] \_ 動作類別包含的感應器，會提供與實體移動相關的資訊。 加速計量值加速的感應器，包括 gravitational 加速。 運動偵測器，例如安全性系統中的人工移動偵測，以及移動物件的意義。 角度速度的 Gyrometers 意義變化。 Speedometers 測量速度。

**平臺定義的感應器類型**

此類別包括下列平臺定義的感應器類型。



| 感應器類型                                                                                                                                                                                                                                                                                              | 描述                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**感應器 \_類型 \_ 加速計 \_ 1d**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | 一軸加速計。<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**感應器 \_類型 \_ 加速計 \_ 2d**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | 兩軸加速計。<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**感應器 \_類型 \_ 加速計 \_ 3d**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | 三軸加速計。<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**感應器 \_輸入 \_ 陀螺儀 \_ 1d**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | 一軸 gyrometers。<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**感應器 \_輸入 \_ 陀螺儀 \_ 2d**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | 兩軸 gyrometers。<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**感應器 \_輸入 \_ 陀螺儀 \_ 3d**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | 三軸 gyrometers。<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**感應器 \_類型 \_ 動作 \_**</dt>偵測器 <dt>{5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | 動作偵測器，例如安全性系統中使用的動作。<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**感應器 \_輸入 \_ SPEEDOMETER**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | 動作感應器的速率。<br/>                                   |



**平臺定義的資料欄位**

此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 動作 \_ GUID 為基礎：

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

此類別包括下列的平臺定義資料欄位。



| 資料欄位名稱和 PID                                                                                                                                                                                                                                                                                                                                                                               | 描述                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 加速 \_ X \_ G**</dt> <dt> (PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> X 軸加速（ *g*）。<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 加速 \_ Y \_ G**</dt> <dt> (PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Y 軸加速（ *g*）。<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 加速 \_ Z \_ G**</dt> <dt> (PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Z 軸加速（ *g*）。<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 的 \_ 角度 \_ 加速 \_ X \_ 每 \_ 秒 \_ 平方度**</dt> <dt> (PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Gyrometric X 軸加速，以每秒的平方為單位。<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 的 \_ 角度 \_ 加速 \_ \_ 每秒 Y 度 \_ \_ 平方**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Gyrometric y 軸加速，以每秒的平方為單位。<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**感應器 \_資料 \_ 類型的 \_ 角度 \_ 加速 \_ Z \_ 度 \_ / \_ 秒 \_ 平方**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Gyrometric Z 軸加速（以每秒的平方為單位）。<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**感應器 \_\_每秒資料類型的 \_ 角度 \_ 速度 \_ X \_ 度 \_ \_**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric X 軸速度（單位為每秒）。<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 的 \_ 角度 \_ Y \_ \_ 每 \_ 秒速度 Y 度**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric y 軸速度，以度為單位。<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**感應器 \_\_每秒資料類型的 \_ 角度 \_ 速度 \_ Z \_ 度 \_ \_**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric Z 軸速度（單位為每秒）。<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 動作 \_ 狀態**</dt> <dt> (PID = 9)</dt> </dl>                                                                                                                      | **VT \_ BOOL**<br/> 如果偵測到動作則 **為 TRUE** ;否則 **為 FALSE**。<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**感應器 \_\_ \_ \_ \_ 每 \_ 秒資料類型速度計量**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> 每秒的計量速度。<br/>                                    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>感應器。h</dt> </dl> |



 

 




