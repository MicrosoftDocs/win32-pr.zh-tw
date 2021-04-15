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
# <a name="requesting-user-permissions"></a>要求使用者權限

本主題說明如何向使用者要求許可權以使用感應器。 如需有關感應器 API 中之許可權的背景資訊，請參閱 [管理使用者](managing-user-permissions.md)權力。

下列範例說明一些常見的 scenarious，您可以在其中選擇要求使用者的許可權。

下列範例程式碼只會使用非同步方法呼叫，針對從感應器管理員取得的所有感應器要求許可權。 平臺會開啟對話方塊，提示使用者只啟用尚未啟用的感應器。 若要判斷使用者在此案例中是否已啟用任何感應器，您必須處理 [**ISensorEvents：： OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) 事件。


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



您可以選擇在嘗試取出資料之前，同步測試感應器狀態。 下列範例程式碼示範這項技術。


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



下列範例程式碼會在嘗試從特定感應器取得資料包表失敗時，提示使用者提供感應器許可權。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[管理使用者權限](managing-user-permissions.md)
</dt> </dl>

 

 
