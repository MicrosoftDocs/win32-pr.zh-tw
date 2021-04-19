---
description: 使用 Light 感應器資料
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: 使用 Light 感應器資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988352"
---
# <a name="using-light-sensor-data"></a><span data-ttu-id="0d22b-103">使用 Light 感應器資料</span><span class="sxs-lookup"><span data-stu-id="0d22b-103">Using Light Sensor Data</span></span>

<span data-ttu-id="0d22b-104">有兩種建議的方式可解讀和使用來自環境光線感應器的 lux 資料。</span><span class="sxs-lookup"><span data-stu-id="0d22b-104">There are two recommended ways of interpreting and using lux data that comes from ambient light sensors.</span></span>

-   <span data-ttu-id="0d22b-105">將轉換套用至資料，讓正規化的光源可以直接在程式列為或互動的比例中使用。</span><span class="sxs-lookup"><span data-stu-id="0d22b-105">Apply a transform to the data so that the normalized light level can be used in direct proportion to program behaviors or interactions.</span></span> <span data-ttu-id="0d22b-106">例如，將程式中的按鈕大小變更為標準化資料 (或一範圍的正規化資料（例如) ），就是如此。</span><span class="sxs-lookup"><span data-stu-id="0d22b-106">An example would be to vary the size of a button in your program in direct proportion to the normalized data (or a range of the normalized data, corresponding to outdoors, for example).</span></span> <span data-ttu-id="0d22b-107">這種方法可提供最佳的執行方式。</span><span class="sxs-lookup"><span data-stu-id="0d22b-107">This approach gives the optimal implementation.</span></span>
-   <span data-ttu-id="0d22b-108">處理 lux 資料的範圍，並將程式列為和反應對應到這些 lux 資料範圍的上限和下限閾值。</span><span class="sxs-lookup"><span data-stu-id="0d22b-108">Deal with ranges of lux data, and map program behaviors and reactions to the upper and lower thresholds of these ranges of lux data.</span></span> <span data-ttu-id="0d22b-109">這是回應照明狀況的簡單方式，而且可能無法產生最佳的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="0d22b-109">This is a simple way to respond to lighting conditions and may not yield the optimal user experience.</span></span> <span data-ttu-id="0d22b-110">不過，如果無法順利進行轉換，此方法就會正常運作。</span><span class="sxs-lookup"><span data-stu-id="0d22b-110">However, this approach works fine if smooth transitions are not feasible.</span></span>

## <a name="handling-data-from-multiple-light-sensors"></a><span data-ttu-id="0d22b-111">處理多個光線感應器的資料</span><span class="sxs-lookup"><span data-stu-id="0d22b-111">Handling Data from Multiple Light Sensors</span></span>

<span data-ttu-id="0d22b-112">若要產生目前光源的最精確近似值，您可以使用多個環境光線感應器的資料。</span><span class="sxs-lookup"><span data-stu-id="0d22b-112">To produce the most accurate approximation of the current lighting conditions, you can use data from multiple ambient light sensors.</span></span> <span data-ttu-id="0d22b-113">由於環境光線感應器可以部分或完全遮蔽，或涵蓋感應器的物件，因此，多個感應器之間的距離，可提供比單一感應器更好的目前照明條件近似值。</span><span class="sxs-lookup"><span data-stu-id="0d22b-113">Because ambient light sensors can be partly or fully obscured by shadows or objects that cover the sensor, multiple sensors placed some distance apart can provide a much better approximation of the current lighting conditions than a single sensor.</span></span>

<span data-ttu-id="0d22b-114">若要追蹤來自多個感應器的資料，您可以使用下列兩種技術：</span><span class="sxs-lookup"><span data-stu-id="0d22b-114">To keep track of the data coming from multiple sensors, you can use the following two techniques:</span></span>

-   <span data-ttu-id="0d22b-115">您可以保留每個環境光源感應器的最新資料值，以及每個讀數的感應器資料包表中的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="0d22b-115">The most recent data value for each ambient light sensor can be retained, along with the time stamp from the sensor data report for each of these readings.</span></span> <span data-ttu-id="0d22b-116">針對每個感應器讀取所收到的最後一個 [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) 可以保留，並可提供這兩個值供日後參考。</span><span class="sxs-lookup"><span data-stu-id="0d22b-116">The last [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) received for each sensor reading could be retained and could provide both values for later reference.</span></span> <span data-ttu-id="0d22b-117">藉由參考每個感應器資料包表的時間戳記，即可根據資料的存留期來管理資料。</span><span class="sxs-lookup"><span data-stu-id="0d22b-117">By referring to the time stamp for each sensor data report, the data can be managed based on its age.</span></span> <span data-ttu-id="0d22b-118">例如，如果資料超過2秒，則可以省略。</span><span class="sxs-lookup"><span data-stu-id="0d22b-118">For example, if the data is more than 2 seconds old, it could be omitted.</span></span> <span data-ttu-id="0d22b-119">根據較新的感應器資料值，可以使用最高的讀取，因為對應的感應器會假設不會遮蔽。</span><span class="sxs-lookup"><span data-stu-id="0d22b-119">Based on the newer sensor data values, the highest reading could be used because the corresponding sensor would be presumed not to be obscured.</span></span>
-   <span data-ttu-id="0d22b-120">您可以使用所報告的最後一個環境光源感應器值。</span><span class="sxs-lookup"><span data-stu-id="0d22b-120">You can use the last ambient light sensor value reported.</span></span> <span data-ttu-id="0d22b-121">由於多個感應器的值不會彼此比較，以取得最精確的結果，因此這項實行不是最佳做法。</span><span class="sxs-lookup"><span data-stu-id="0d22b-121">This implementation would not be optimal because the values from multiple sensors are not compared to one another to obtain the most accurate result.</span></span> <span data-ttu-id="0d22b-122">我們不建議採用此方法。</span><span class="sxs-lookup"><span data-stu-id="0d22b-122">We do not recommend this method.</span></span>

## <a name="example-code"></a><span data-ttu-id="0d22b-123">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="0d22b-123">Example Code</span></span>

<span data-ttu-id="0d22b-124">下列範例程式碼顯示 [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) 事件的執行。</span><span class="sxs-lookup"><span data-stu-id="0d22b-124">The following example code shows an implementation for the [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="0d22b-125">事件處理常式會呼叫名為 **UpdateUI** 的 helper 函式，以根據 lux 值變更使用者介面。</span><span class="sxs-lookup"><span data-stu-id="0d22b-125">The event handler calls a helper function, named **UpdateUI**, that changes the user interface based on the lux value.</span></span> <span data-ttu-id="0d22b-126">撰寫 UpdateUI 的執行是由您負責。</span><span class="sxs-lookup"><span data-stu-id="0d22b-126">Writing the implementation of UpdateUI is up to you.</span></span>


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
