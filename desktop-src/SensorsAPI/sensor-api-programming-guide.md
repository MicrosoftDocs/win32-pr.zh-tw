---
description: 本節提供有關如何使用感應器 API 功能的資訊，包括範例程式碼。 如需各種程式設計介面的背景資訊，請參閱關於感應器 API。
ms.assetid: 4c2ffd22-49ee-4318-bfa0-e0ce4d8c67bb
title: 感應器 API 程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078cc99e88a1a4fd6a232220e08c53a99dfbdfb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970391"
---
# <a name="sensor-api-programming-guide"></a>感應器 API 程式設計指南

本節提供有關如何使用感應器 API 功能的資訊，包括範例程式碼。 如需各種程式設計介面的背景資訊，請參閱 [關於感應器 API](about-the-sensor-api.md)。

本節中的範例程式碼會使用下列其他包含的標頭。


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





您也必須連結至這些其他相關聯的程式庫檔案： Propsys .lib 和 PortableDeviceGuids .lib。

本節中的範例程式碼會針對感應器類別、類型和資料欄位使用下列常數。 這些常數是自訂值，這些值是由 Windows 驅動程式套件中的 TimeSensor 驅動程式範例所定義。 請注意，雖然感應器平臺可以定義和使用自訂類型（例如這些類型），但您應該盡可能使用平臺定義類型。


```C++
// Define an object ID.
// {0D77BEE3-7169-42bf-8379-28F9A9B59A57}
DEFINE_GUID(SAMPLE_SENSOR_TIME_ID, 
0xd77bee3, 0x7169, 0x42bf, 0x83, 0x79, 0x28, 0xf9, 0xa9, 0xb5, 0x9a, 0x57);

// Define a custom category.
// {062A5C3B-44C1-4ad1-8EFC-0F65B2E4AD48}
DEFINE_GUID(SAMPLE_SENSOR_CATEGORY_DATE_TIME, 
0x62a5c3b, 0x44c1, 0x4ad1, 0x8e, 0xfc, 0xf, 0x65, 0xb2, 0xe4, 0xad, 0x48);

// Define a custom type.
// {5F199A84-409F-4e35-B2DD-F9C79F5318A0}
DEFINE_GUID(SAMPLE_SENSOR_TYPE_TIME, 
0x5f199a84, 0x409f, 0x4e35, 0xb2, 0xdd, 0xf9, 0xc7, 0x9f, 0x53, 0x18, 0xa0);

// Time sensor fields.
// Because these are related, each field uses the same GUID, but changes the PID.
// {340946F2-9A77-42b0-8176-57D4DF00E5CA}
DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_HOUR, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE); // PID = 2

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_MINUTE, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 1); // PID = 3

DEFINE_PROPERTYKEY(SAMPLE_SENSOR_DATA_TYPE_SECOND, 
0x340946f2, 0x9a77, 0x42b0, 0x81, 0x76, 0x57, 0xd4, 0xdf, 0x0, 0xe5, 0xca, PID_FIRST_USABLE + 2); // PID = 4
```



本節中的範例程式碼會使用下列變數。


```C++
HRESULT hr = S_OK;

// Sensor interface pointers
ISensorManager* pSensorManager = NULL;    
ISensorCollection* pSensorColl = NULL;
ISensor* pSensor = NULL; 
ISensorDataReport* pReport = NULL;

// Time sensor data field variables
ULONG ulHour, ulMinute, ulSecond = 0;

```



本節中的範例程式碼會使用下列函式來釋放 COM 介面指標。


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="in-this-section"></a>本節內容

-   [取出感應器物件](retrieving-a-sensor.md)
-   [要求使用者權限](requesting-user-permissions.md)
-   [正在抓取和設定感應器屬性](setting-and-retrieving-sensor-properties.md)
-   [檢查支援的感應器資料欄位](checking-for-supported-sensor-data-fields.md)
-   [使用感應器 API 事件](using-sensor-api-events.md)
-   [正在捕獲感應器資料值](retrieving-sensor-data-fields.md)
-   [正在抓取向量類型](retrieving-vector-types.md)
-   [使用邏輯感應器](using-logical-sensors.md)
-   [建立 Light-Aware 使用者介面](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於感應器 API](about-the-sensor-api.md)
</dt> </dl>

 

 



