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
# <a name="using-light-sensor-data"></a>使用 Light 感應器資料

有兩種建議的方式可解讀和使用來自環境光線感應器的 lux 資料。

-   將轉換套用至資料，讓正規化的光源可以直接在程式列為或互動的比例中使用。 例如，將程式中的按鈕大小變更為標準化資料 (或一範圍的正規化資料（例如) ），就是如此。 這種方法可提供最佳的執行方式。
-   處理 lux 資料的範圍，並將程式列為和反應對應到這些 lux 資料範圍的上限和下限閾值。 這是回應照明狀況的簡單方式，而且可能無法產生最佳的使用者體驗。 不過，如果無法順利進行轉換，此方法就會正常運作。

## <a name="handling-data-from-multiple-light-sensors"></a>處理多個光線感應器的資料

若要產生目前光源的最精確近似值，您可以使用多個環境光線感應器的資料。 由於環境光線感應器可以部分或完全遮蔽，或涵蓋感應器的物件，因此，多個感應器之間的距離，可提供比單一感應器更好的目前照明條件近似值。

若要追蹤來自多個感應器的資料，您可以使用下列兩種技術：

-   您可以保留每個環境光源感應器的最新資料值，以及每個讀數的感應器資料包表中的時間戳記。 針對每個感應器讀取所收到的最後一個 [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) 可以保留，並可提供這兩個值供日後參考。 藉由參考每個感應器資料包表的時間戳記，即可根據資料的存留期來管理資料。 例如，如果資料超過2秒，則可以省略。 根據較新的感應器資料值，可以使用最高的讀取，因為對應的感應器會假設不會遮蔽。
-   您可以使用所報告的最後一個環境光源感應器值。 由於多個感應器的值不會彼此比較，以取得最精確的結果，因此這項實行不是最佳做法。 我們不建議採用此方法。

## <a name="example-code"></a>範例程式碼

下列範例程式碼顯示 [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) 事件的執行。 事件處理常式會呼叫名為 **UpdateUI** 的 helper 函式，以根據 lux 值變更使用者介面。 撰寫 UpdateUI 的執行是由您負責。


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



 

 
