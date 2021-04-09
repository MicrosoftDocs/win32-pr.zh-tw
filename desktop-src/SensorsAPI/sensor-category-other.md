---
description: '[感應器 \_ 類別] 類別 \_ 包含的感應器，可支援 HID 類別驅動程式中的自訂類別。'
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: 'SENSOR_CATEGORY_OTHER (的感應器 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026154"
---
# <a name="sensor_category_other"></a>其他的感應器 \_ 類別 \_

[感應器 \_ 類別] 類別 \_ 包含的感應器，可支援 HID 類別驅動程式中的自訂類別。

<dl> <dt>

<span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**感應器 \_ 類型 \_ 自訂**
</dt> <dd> <dl> <dt>

{E83AF229-8640-4D18-A213-E22675EBB2C3}
</dt> <dt>



支援 HID 類別驅動程式中自訂類別的自訂感應器。


</dt> </dl> </dd> </dl>

**平臺定義的資料欄位**

此類別的平臺定義屬性索引鍵是以感應器 \_ 資料 \_ 類型 \_ 自訂 \_ GUID 為基礎：

{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}

此類別包括下列的平臺定義資料欄位。



| 資料欄位名稱和 PID                                                                                                                                                                                                                                                                                    | Description                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ 使用**</dt>方式 <dt> (PID = 5)</dt> </dl>                          | **VT \_ UI4**<br/> 可以用來區別多個自訂感應器的 HID 用途。<br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ 布林 \_ 陣列**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ UI4**<br/> 指定自訂感應器的布林值陣列。<br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE1**</dt> <dt> (PID = 7)</dt> </dl>                       | **VT \_ UI4 \| \| vt \_ R4**<br/> 指定自訂感應器的六個可用值之一。<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE2**</dt> <dt> (PID = 8)</dt> </dl>                       | **VT \_ UI4 \| \| vt \_ R4**<br/> 指定自訂感應器的六個可用值之一。<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE3**</dt> <dt> (PID = 9)</dt> </dl>                       | **VT \_ UI4 \| \| vt \_ R4**<br/> 指定自訂感應器的六個可用值之一。<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE4**</dt> <dt> (PID = 10)</dt> </dl>                      | **VT \_ UI4 \| \| vt \_ R4**<br/> 指定自訂感應器的六個可用值之一。<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE5**</dt> <dt> (PID = 11)</dt> </dl>                      | **VT \_ UI4 \| \| vt \_ R4**<br/> 指定自訂感應器的六個可用值之一。<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <dt>**感應器 \_資料 \_ 類型 \_ 自訂 \_ VALUE6**</dt> <dt> (PID = 12)</dt> </dl>                      | **VT \_ UI4 \| \| vt \_ R4**<br/> 指定自訂感應器的六個可用值之一。<br/>       |



## <a name="remarks"></a>備註

在 HID 類別驅動程式中支援泛型類別的感應器，會對應至其中一個其他定義的類別， (生物識別、電氣、環境等) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>感應器。h</dt> </dl> |



 

 




