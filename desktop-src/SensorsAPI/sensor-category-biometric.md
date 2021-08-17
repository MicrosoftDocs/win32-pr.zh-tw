---
description: 感應器 \_ 類別 \_ 生物特徵辨識類別包含的感應器，可提供客廳的相關資訊。
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: 'SENSOR_CATEGORY_BIOMETRIC (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1551a82e359d2277c8b46f227d7a72660b1419b3ba3ddfcf58bdd4ac1de5425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889574"
---
# <a name="sensor_category_biometric"></a>感應器 \_ 類別 \_ 生物特徵辨識

感應器 \_ 類別 \_ 生物特徵辨識類別包含的感應器，可提供客廳的相關資訊。

**平臺定義的感應器類型**

此類別包括下列平臺定義的感應器類型。



| 感應器類型                                                                                                                                                                                                                                                                                           | Description                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**感應器 \_輸入 \_ 人類 \_ 狀態**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | 偵測人為存在的感應器。<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**感應器 \_輸入 \_ 人類 \_ 鄰近**</dt>性 <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | 偵測人類附近的感應器。<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**感應器 \_輸入 \_ TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | 觸控感應器。<br/>                       |



**平臺定義的資料欄位**

此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 生物特徵辨識 GUID \_ 為基礎：

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

此類別包括下列的平臺定義資料欄位。



| 資料欄位名稱和 PID                                                                                                                                                                                                                                                                                         | Description                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**感應器 \_資料 \_ 類型的 \_ 人為 \_ 存在**</dt> <dt> (PID = 2)</dt> </dl>                          | **VT \_ BOOL**<br/> 當人類使用電腦時 **為 TRUE** 。<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**感應器 \_資料 \_ 類型的 \_ 人類 \_ 近距離 \_ 計量**</dt> <dt> (PID = 3)</dt> </dl> | **VT \_ R4**<br/> 人類和電腦之間的距離（以計量為單位）。<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 觸控 \_ 狀態**</dt> <dt> (PID = 4)</dt> </dl>                                   | **VT \_ BOOL**<br/> 觸碰觸控感應器時為 **TRUE** ;否則 **為 FALSE**。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>感應器。h</dt> </dl> |



 

 




