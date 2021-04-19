---
description: 本主題說明如何以同步和非同步方式從感應器中取出資料。
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: 正在捕獲感應器資料值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4642f120e549cd77b1b37610037092facf2ead1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973437"
---
# <a name="retrieving-sensor-data-values"></a><span data-ttu-id="4a61f-103">正在捕獲感應器資料值</span><span class="sxs-lookup"><span data-stu-id="4a61f-103">Retrieving Sensor Data Values</span></span>

<span data-ttu-id="4a61f-104">本主題說明如何以同步和非同步方式從感應器中取出資料。</span><span class="sxs-lookup"><span data-stu-id="4a61f-104">This topic describes how to retrieve data from a sensor, synchronously and asynchronously.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="4a61f-105">同步取出資料</span><span class="sxs-lookup"><span data-stu-id="4a61f-105">Retrieving Data Synchronously</span></span>

<span data-ttu-id="4a61f-106">您可以藉由呼叫 [**ISensor：：**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata)來同步取出感應器資料。</span><span class="sxs-lookup"><span data-stu-id="4a61f-106">You can retrieve sensor data synchronously by calling [**ISensor::GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span></span>

<span data-ttu-id="4a61f-107">下列範例程式碼會取出感應器資料包表，然後抓取三個個別的資料欄值。</span><span class="sxs-lookup"><span data-stu-id="4a61f-107">The following example code retrieves a sensor data report, and then retrieves three individual data field values.</span></span> <span data-ttu-id="4a61f-108">範例感應器會提供有關目前當地時間的自訂資料，以小時、分鐘和秒為單位的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="4a61f-108">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span> <span data-ttu-id="4a61f-109">名為 pSensor 的變數包含 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) 的指標，代表提供資料的感應器。</span><span class="sxs-lookup"><span data-stu-id="4a61f-109">The variable named pSensor contains a pointer to [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) that represents the sensor that supplies the data.</span></span>


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



## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="4a61f-110">非同步地取出資料</span><span class="sxs-lookup"><span data-stu-id="4a61f-110">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="4a61f-111">您可以藉由註冊接收 [**ISensorEvents：： OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) 事件，以非同步方式接收感應器資料。</span><span class="sxs-lookup"><span data-stu-id="4a61f-111">You can receive sensor data asynchronously by registering to receive the [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="4a61f-112">若要瞭解如何接收感應器事件回呼，請參閱 [使用感應器 API 事件](using-sensor-api-events.md)。</span><span class="sxs-lookup"><span data-stu-id="4a61f-112">To understand how to receive sensor event callbacks, see [Using Sensor API Events](using-sensor-api-events.md).</span></span>

<span data-ttu-id="4a61f-113">下列範例程式碼示範了 [**ISensorEvents：： OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) 的實值，可從事件所提供的資料包表中抓取資料值。</span><span class="sxs-lookup"><span data-stu-id="4a61f-113">The following example code shows an implementation of [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) that retrieves data values from the data report provided by the event.</span></span> <span data-ttu-id="4a61f-114">範例感應器會提供有關目前當地時間的自訂資料，以小時、分鐘和秒為單位的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="4a61f-114">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span>


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



 

 
