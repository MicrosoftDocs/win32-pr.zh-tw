---
description: 本主題說明如何向使用者要求許可權以使用感應器。 如需有關感應器 API 中之許可權的背景資訊，請參閱管理使用者權限。
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: 要求使用者權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511147"
---
# <a name="requesting-user-permissions"></a><span data-ttu-id="aaaee-104">要求使用者權限</span><span class="sxs-lookup"><span data-stu-id="aaaee-104">Requesting User Permissions</span></span>

<span data-ttu-id="aaaee-105">本主題說明如何向使用者要求許可權以使用感應器。</span><span class="sxs-lookup"><span data-stu-id="aaaee-105">This topic describes how to request permissions from the user to use sensors.</span></span> <span data-ttu-id="aaaee-106">如需有關感應器 API 中之許可權的背景資訊，請參閱 [管理使用者](managing-user-permissions.md)權力。</span><span class="sxs-lookup"><span data-stu-id="aaaee-106">For background information about permissions in the Sensor API, see [Managing User Permissions](managing-user-permissions.md).</span></span>

<span data-ttu-id="aaaee-107">下列範例說明一些常見的 scenarious，您可以在其中選擇要求使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="aaaee-107">The following examples illustrate some of the common scenarious where you can choose to request user permissions.</span></span>

<span data-ttu-id="aaaee-108">下列範例程式碼只會使用非同步方法呼叫，針對從感應器管理員取得的所有感應器要求許可權。</span><span class="sxs-lookup"><span data-stu-id="aaaee-108">The following example code simply requests permissions for all sensors retrieved from the sensor manager, by type, using an asynchronous method call.</span></span> <span data-ttu-id="aaaee-109">平臺會開啟對話方塊，提示使用者只啟用尚未啟用的感應器。</span><span class="sxs-lookup"><span data-stu-id="aaaee-109">The platform will open a dialog box to prompt the user only to enable sensors that are not already enabled.</span></span> <span data-ttu-id="aaaee-110">若要判斷使用者在此案例中是否已啟用任何感應器，您必須處理 [**ISensorEvents：： OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) 事件。</span><span class="sxs-lookup"><span data-stu-id="aaaee-110">To determine whether the user enabled any sensors in this case, you must handle the [**ISensorEvents::OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) event.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}

```



<span data-ttu-id="aaaee-111">您可以選擇在嘗試取出資料之前，同步測試感應器狀態。</span><span class="sxs-lookup"><span data-stu-id="aaaee-111">You can choose to test the sensor state synchronously before attempting to retrieve data.</span></span> <span data-ttu-id="aaaee-112">下列範例程式碼示範這項技術。</span><span class="sxs-lookup"><span data-stu-id="aaaee-112">The following example code demonstrates this technique.</span></span>


```C++
if(SUCCEEDED(hr))
{
   // Check the current sensor state.
   SensorState state = SENSOR_STATE_NOT_AVAILABLE;

   hr = pSensor->GetState(&state);

   if(SUCCEEDED(hr))
   {
       if(state == SENSOR_STATE_ACCESS_DENIED)
       {
           wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
           hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

           if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
              hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
           {
               wprintf_s(L"\nYou have previously denied access to this sensor.\n");
               wprintf_s(L"Please use the Location and Other Sensors control panel\n");
               wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
           }
       }
   }
}

if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
```



<span data-ttu-id="aaaee-113">下列範例程式碼會在嘗試從特定感應器取得資料包表失敗時，提示使用者提供感應器許可權。</span><span class="sxs-lookup"><span data-stu-id="aaaee-113">The following example code prompts the user for sensor permissions if an attempt to retrieve a data report from a particular sensor fails.</span></span>


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);

    if(E_ACCESSDENIED == hr)
    {
       wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
       hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

       if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
          hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
       {
           wprintf_s(L"\nYou have previously denied access to this sensor.\n");
           wprintf_s(L"Please use the Location and Other Sensors control panel\n");
           wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
       }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="aaaee-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="aaaee-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaaee-115">**ISensorManager**</span><span class="sxs-lookup"><span data-stu-id="aaaee-115">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[<span data-ttu-id="aaaee-116">管理使用者權限</span><span class="sxs-lookup"><span data-stu-id="aaaee-116">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> </dl>

 

 
