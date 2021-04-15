---
description: 某些屬性和資料欄位包含資訊的陣列。
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: 正在抓取向量類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945b45e4e78b6c4f9f9e0fb4b3848f813549105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511146"
---
# <a name="retrieving-vector-types"></a><span data-ttu-id="68a8e-103">正在抓取向量類型</span><span class="sxs-lookup"><span data-stu-id="68a8e-103">Retrieving Vector Types</span></span>

<span data-ttu-id="68a8e-104">某些屬性和資料欄位包含資訊的陣列。</span><span class="sxs-lookup"><span data-stu-id="68a8e-104">Some properties and data fields contain arrays of information.</span></span> <span data-ttu-id="68a8e-105">例如，感應器 \_ 屬性 \_ LIGHT \_ 回應 \_ 曲線屬性包含4位元組不帶正負號的整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="68a8e-105">For example, the SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE property contains an array of 4-byte unsigned integers.</span></span> <span data-ttu-id="68a8e-106">不過，當您透過感應器 API 接收這類陣列時，它們一律會表示為 type VT \_ VECTOR UI1，也就是 \| 單一位元組字元的陣列，而不論陣列中的資料實際型別為何。</span><span class="sxs-lookup"><span data-stu-id="68a8e-106">However, when you receive such arrays through the Sensor API, they are always represented as type VT\_VECTOR\|UI1, an array of single-byte characters, regardless of the actual type of the data in the array.</span></span> <span data-ttu-id="68a8e-107">針對這些類型，您必須小心將陣列變數轉換成屬性或資料欄位的正確資料類型。</span><span class="sxs-lookup"><span data-stu-id="68a8e-107">For these types, you must be careful to cast array variables to the correct data type for the property or data field.</span></span>

<span data-ttu-id="68a8e-108">如需屬性、資料欄位及其類型的詳細資訊，請參閱 [常數](constants.md)。</span><span class="sxs-lookup"><span data-stu-id="68a8e-108">For information about properties, data fields, and their types, see [Constants](constants.md).</span></span>

<span data-ttu-id="68a8e-109">下列範例程式碼示範如何將感應器屬性 LIGHT 回應曲線中抓取的資料轉換 \_ \_ \_ \_ 成正確的型別。</span><span class="sxs-lookup"><span data-stu-id="68a8e-109">The following example code shows how to cast the data retrieved in SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE to the correct type.</span></span>


```C++
PROPVARIANT pvCurve;
PropVariantInit(&pvCurve);

// Retrieve the property value.
hr = pSensor->GetProperty(SENSOR_PROPERTY_LIGHT_RESPONSE_CURVE, &pvCurve);
if (SUCCEEDED(hr))
{
    if ((VT_UI1|VT_VECTOR) == V_VT(pvCurve)) // Note actual type of UI1
    {
        // Cast the array to UINT, a 4-byte unsigned integer.

        // Item count for the array.
        UINT  cElement = pvCurve.caub.cElems/sizeof(UINT);
        // Array pointer.
        UINT* pElement = (UINT*)(pvCurve.caub.pElems);

        // Use the array.
    }
}

// Remember to free the PROPVARIANT when done.
PropVariantClear(&pvCurve);
```



 

 



