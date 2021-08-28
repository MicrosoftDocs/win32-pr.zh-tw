---
description: 本主題說明如何以同步和非同步方式從感應器中取出資料。
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: 正在捕獲感應器資料值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e240b9bc14d917db0e0c4280ad957aa139369eb7762abfcd69441d25e66857d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960028"
---
# <a name="retrieving-sensor-data-values"></a>正在捕獲感應器資料值

本主題說明如何以同步和非同步方式從感應器中取出資料。

## <a name="retrieving-data-synchronously"></a>同步取出資料

您可以藉由呼叫 [**ISensor：：**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata)來同步取出感應器資料。

下列範例程式碼會取出感應器資料包表，然後抓取三個個別的資料欄值。 範例感應器會提供有關目前當地時間的自訂資料，以小時、分鐘和秒為單位的資料欄位。 名為 pSensor 的變數包含 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) 的指標，代表提供資料的感應器。


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
  
if(SUCCEEDED(hr))
{
    PROPVARIANT var = {};

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);        

    if(SUCCEEDED(hr))
    {
        // Print the local time to the console window.
        wprintf_s(L"\nCurrent local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (synchronous)\n\n", ulHour, ulMinute, ulSecond);
    }

```



## <a name="retrieving-data-asynchronously"></a>非同步地取出資料

您可以藉由註冊接收 [**ISensorEvents：： OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) 事件，以非同步方式接收感應器資料。 若要瞭解如何接收感應器事件回呼，請參閱 [使用感應器 API 事件](using-sensor-api-events.md)。

下列範例程式碼示範了 [**ISensorEvents：： OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) 的實值，可從事件所提供的資料包表中抓取資料值。 範例感應器會提供有關目前當地時間的自訂資料，以小時、分鐘和秒為單位的資料欄位。


```C++
STDMETHODIMP OnDataUpdated(
        ISensor *pSensor,
        ISensorDataReport *pNewData)
{
    HRESULT hr = S_OK;

    if(NULL == pNewData ||
       NULL == pSensor)
    {
        return E_INVALIDARG;
    }

    ULONG ulHour = 0;
    ULONG ulMinute = 0;
    ULONG ulSecond = 0;

    PROPVARIANT var = {};

    hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        // Print
        wprintf_s(L"Current local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
    }

    return hr;
}
```



 

 
