---
title: 執行 CEcho FinalConstruct
description: 執行 CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，CEcho FinalConstruct 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092257"
---
# <a name="implementing-cechofinalconstruct"></a><span data-ttu-id="c148e-109">執行 CEcho：： FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="c148e-109">Implementing CEcho::FinalConstruct</span></span>

<span data-ttu-id="c148e-110">CEcho：： FinalConstruct 方法是在 Echo 中實作為。</span><span class="sxs-lookup"><span data-stu-id="c148e-110">The CEcho::FinalConstruct method is implemented in Echo.cpp.</span></span> <span data-ttu-id="c148e-111">它包含的程式碼可在 Windows Media Player 具現化 DSP 外掛程式物件時，從登錄讀取屬性值。</span><span class="sxs-lookup"><span data-stu-id="c148e-111">It contains code to read the property values from the registry when Windows Media Player instantiates the DSP plug-in object.</span></span> <span data-ttu-id="c148e-112">這點很重要，因為它可讓使用者設定在物件的實例之間以及會話之間保存。</span><span class="sxs-lookup"><span data-stu-id="c148e-112">This is important because it allows the user settings to persist between instances of the object, as well as between sessions.</span></span> <span data-ttu-id="c148e-113">外掛程式 wizard 範例程式碼提供從登錄讀取單一屬性的執行。</span><span class="sxs-lookup"><span data-stu-id="c148e-113">The plug-in wizard sample code provides implementation to read a single property from the registry.</span></span> <span data-ttu-id="c148e-114">您可以修改此程式碼以處理 [延遲時間] 屬性，然後加入程式碼以讀取 [潮濕混合] 屬性值。</span><span class="sxs-lookup"><span data-stu-id="c148e-114">You can modify this code to handle the delay time property, and then add code to read the wet mix property value.</span></span>

<span data-ttu-id="c148e-115">下列程式碼範例會從登錄讀取每個屬性值，並將每個屬性值儲存在正確的成員變數中：</span><span class="sxs-lookup"><span data-stu-id="c148e-115">The following example code reads each property value from the registry and stores each in the correct member variable:</span></span>


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



<span data-ttu-id="c148e-116">請注意，濕混合的 DWORD 值會轉換成浮點值。</span><span class="sxs-lookup"><span data-stu-id="c148e-116">Notice that the DWORD value for the wet mix is converted to a floating-point value.</span></span> <span data-ttu-id="c148e-117">另請注意，程式碼會計算 m fDryMix 的正確值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c148e-117">Also note that the code calculates the correct value for m\_fDryMix.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c148e-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="c148e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c148e-119">**修改 Echo 範例屬性頁**</span><span class="sxs-lookup"><span data-stu-id="c148e-119">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




