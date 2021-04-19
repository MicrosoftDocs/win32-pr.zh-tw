---
description: Windows 感應器和位置平台會定義驅動程式事件的常數。 感應器 manfuactureres 也可以定義自己的常數。
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: " (感應器的事件常數。 h) "
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996859"
---
# <a name="event-constants-sensorsh"></a> (感應器的事件常數。 h) 

Windows 感應器和位置平台會定義驅動程式事件的常數。 感應器 manfuactureres 也可以定義自己的常數。

**感應器事件種類**

平臺會定義下列感應器事件種類識別碼。



| 感應器事件種類                                                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**感應器 \_事件 \_ 加速計 \_ 搖動**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | 指出裝置已 shaken。<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**感應器 \_\_ \_ 已更新事件資料**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | 指出有新的資料可供使用。<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**感應器 \_事件 \_ 屬性 \_ 已變更**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | 表示屬性值已變更。 檢查 [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) 介面（透過 *pEventData* 參數傳遞至 [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent)），以判斷已變更的屬性及其新值。<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**感應器 \_事件 \_ 狀態 \_ 已變更**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | 表示作業狀態的變更，例如，從感應器 \_ 狀態 \_ 初始化至感應器 \_ 狀態 \_ 就緒。<br/>                                                                                                                                                                                            |



**感應器事件 PROPERTYKEYs**

事件的平臺定義屬性索引鍵是以下列 GUID 為基礎：

{64346E30-8728-4B34-BDF6-4F52442C5C28}

感應器平臺會定義下列可識別感應器事件參數的 **PROPERTYKEY**。



| 感應器事件 PROPERTYKEY 和 PID                                                                                                                                                                                                                                                      | Description                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**感應器 \_事件 \_ 參數 \_ 事件 \_ 識別碼**</dt> <dt> (PID = 2)</dt> </dl> | 指出 [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))中的 **GUID** 值是事件種類識別碼，例如更新的感應器 \_ 事件 \_ 資料 \_ 。<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**感應器 \_事件 \_ 參數 \_ 狀態**</dt> <dt> (PID = 3)</dt> </dl>           | 指出 **IPortableDeviceValues** 中不帶正負號的整數值為感應器狀態，例如感應器 \_ 狀態 \_ 就緒。<br/>                                                  |



**感應器錯誤 PROPERTYKEYs**

適用于錯誤的平臺定義屬性索引鍵會以下列 GUID 為基礎：

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

感應器平臺會保留此 GUID 供日後使用。

<dl></dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>感應器。h</dt> </dl> |



 

