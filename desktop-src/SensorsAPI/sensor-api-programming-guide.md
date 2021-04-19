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
# <a name="sensor-api-programming-guide"></a><span data-ttu-id="10ac7-104">感應器 API 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="10ac7-104">Sensor API Programming Guide</span></span>

<span data-ttu-id="10ac7-105">本節提供有關如何使用感應器 API 功能的資訊，包括範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="10ac7-105">This section provides information, including example code, about how to use the Sensor API features.</span></span> <span data-ttu-id="10ac7-106">如需各種程式設計介面的背景資訊，請參閱 [關於感應器 API](about-the-sensor-api.md)。</span><span class="sxs-lookup"><span data-stu-id="10ac7-106">For background information about the various programming interfaces, see [About the Sensor API](about-the-sensor-api.md).</span></span>

<span data-ttu-id="10ac7-107">本節中的範例程式碼會使用下列其他包含的標頭。</span><span class="sxs-lookup"><span data-stu-id="10ac7-107">The example code in this section makes use of the following additional included headers.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <propkeydef.h>


#include <iostream>
#include <propvarutil.h>
#include <functiondiscoverykeys.h>
#include <assert.h>
```





<span data-ttu-id="10ac7-108">您也必須連結至這些其他相關聯的程式庫檔案： Propsys .lib 和 PortableDeviceGuids .lib。</span><span class="sxs-lookup"><span data-stu-id="10ac7-108">You must also link to these additional associated library files: Propsys.lib and PortableDeviceGuids.lib.</span></span>

<span data-ttu-id="10ac7-109">本節中的範例程式碼會針對感應器類別、類型和資料欄位使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="10ac7-109">The example code in this section uses the following constants for sensor categories, types, and data fields.</span></span> <span data-ttu-id="10ac7-110">這些常數是自訂值，這些值是由 Windows 驅動程式套件中的 TimeSensor 驅動程式範例所定義。</span><span class="sxs-lookup"><span data-stu-id="10ac7-110">These constants are custom values that are defined by the TimeSensor driver sample in the Windows Driver Kit.</span></span> <span data-ttu-id="10ac7-111">請注意，雖然感應器平臺可以定義和使用自訂類型（例如這些類型），但您應該盡可能使用平臺定義類型。</span><span class="sxs-lookup"><span data-stu-id="10ac7-111">Note that, though the Sensor platform enables defining and using custom types such as these, you should use platform-defined types whenever possible.</span></span>


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



<span data-ttu-id="10ac7-112">本節中的範例程式碼會使用下列變數。</span><span class="sxs-lookup"><span data-stu-id="10ac7-112">The example code in this section uses the following variables.</span></span>


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



<span data-ttu-id="10ac7-113">本節中的範例程式碼會使用下列函式來釋放 COM 介面指標。</span><span class="sxs-lookup"><span data-stu-id="10ac7-113">The example code in this section uses the following function to release COM interface pointers.</span></span>


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



## <a name="in-this-section"></a><span data-ttu-id="10ac7-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="10ac7-114">In This Section</span></span>

-   [<span data-ttu-id="10ac7-115">取出感應器物件</span><span class="sxs-lookup"><span data-stu-id="10ac7-115">Retrieving a Sensor Object</span></span>](retrieving-a-sensor.md)
-   [<span data-ttu-id="10ac7-116">要求使用者權限</span><span class="sxs-lookup"><span data-stu-id="10ac7-116">Requesting User Permissions</span></span>](requesting-user-permissions.md)
-   [<span data-ttu-id="10ac7-117">正在抓取和設定感應器屬性</span><span class="sxs-lookup"><span data-stu-id="10ac7-117">Retrieving and Setting Sensor Properties</span></span>](setting-and-retrieving-sensor-properties.md)
-   [<span data-ttu-id="10ac7-118">檢查支援的感應器資料欄位</span><span class="sxs-lookup"><span data-stu-id="10ac7-118">Checking for Supported Sensor Data Fields</span></span>](checking-for-supported-sensor-data-fields.md)
-   [<span data-ttu-id="10ac7-119">使用感應器 API 事件</span><span class="sxs-lookup"><span data-stu-id="10ac7-119">Using Sensor API Events</span></span>](using-sensor-api-events.md)
-   [<span data-ttu-id="10ac7-120">正在捕獲感應器資料值</span><span class="sxs-lookup"><span data-stu-id="10ac7-120">Retrieving Sensor Data Values</span></span>](retrieving-sensor-data-fields.md)
-   [<span data-ttu-id="10ac7-121">正在抓取向量類型</span><span class="sxs-lookup"><span data-stu-id="10ac7-121">Retrieving Vector Types</span></span>](retrieving-vector-types.md)
-   [<span data-ttu-id="10ac7-122">使用邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="10ac7-122">Using Logical Sensors</span></span>](using-logical-sensors.md)
-   [<span data-ttu-id="10ac7-123">建立 Light-Aware 使用者介面</span><span class="sxs-lookup"><span data-stu-id="10ac7-123">Creating Light-Aware User Interfaces</span></span>](creating-light-aware-user-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="10ac7-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="10ac7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10ac7-125">關於感應器 API</span><span class="sxs-lookup"><span data-stu-id="10ac7-125">About the Sensor API</span></span>](about-the-sensor-api.md)
</dt> </dl>

 

 



