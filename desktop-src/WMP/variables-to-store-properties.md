---
title: 用來儲存屬性的變數
description: 用來儲存屬性的變數
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，屬性
- Echo DSP 外掛程式範例，用於儲存屬性的變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183670"
---
# <a name="variables-to-store-properties"></a><span data-ttu-id="fa79a-109">用來儲存屬性的變數</span><span class="sxs-lookup"><span data-stu-id="fa79a-109">Variables to Store Properties</span></span>

<span data-ttu-id="fa79a-110">首先，您將需要一個變數來儲存延遲時間。</span><span class="sxs-lookup"><span data-stu-id="fa79a-110">First, you will need a variable to store the delay time.</span></span> <span data-ttu-id="fa79a-111">Windows Media Player 外掛程式 Wizard 建立的預設範例會提供名為 m fScaleFactor 的變數 \_ ，以儲存它用來處理的縮放乘數。</span><span class="sxs-lookup"><span data-stu-id="fa79a-111">The default sample created by the Windows Media Player Plug-in Wizard provides a variable named m\_fScaleFactor to store the scaling multiplier it uses for processing.</span></span> <span data-ttu-id="fa79a-112">此範例不再需要這個變數，因此您可以變更其名稱和類型來儲存延遲時間值。</span><span class="sxs-lookup"><span data-stu-id="fa79a-112">This sample no longer needs this variable, so you can change its name and type to store the delay time value.</span></span>

1.  <span data-ttu-id="fa79a-113">以 m dwDelayTime 取代 Echo 中的每個 m \_ fScaleFactor 實例和回應。 \_</span><span class="sxs-lookup"><span data-stu-id="fa79a-113">Replace each instance of m\_fScaleFactor in Echo.h and Echo.cpp with m\_dwDelayTime.</span></span>
2.  <span data-ttu-id="fa79a-114">變更 m fScaleFactor 的資料類型 \_ (現在 m \_ dwDelayTime) 從 DOUBLE 到 DWORD 的 Echo. h。</span><span class="sxs-lookup"><span data-stu-id="fa79a-114">Change the data type for m\_fScaleFactor (now m\_dwDelayTime) from double to DWORD in Echo.h.</span></span>
3.  <span data-ttu-id="fa79a-115">在 CEcho 的函式中，將預設的延遲時間值變更為1000。</span><span class="sxs-lookup"><span data-stu-id="fa79a-115">In the constructor for CEcho, change the default delay time value to 1000.</span></span>
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

<span data-ttu-id="fa79a-116">接下來，宣告兩個新的成員變數，以儲存效果信號的百分比，以及要在最終輸出緩衝區中混合的來源信號百分比。</span><span class="sxs-lookup"><span data-stu-id="fa79a-116">Next, declare two new member variables to store the percentage of effect signal and the percentage of source signal to be mixed in the final output buffer.</span></span> <span data-ttu-id="fa79a-117">「濕」一詞是指效果，而「幹」一詞是指來源信號。</span><span class="sxs-lookup"><span data-stu-id="fa79a-117">The term "wet" refers to the effect, and the term "dry" refers to the source signal.</span></span> <span data-ttu-id="fa79a-118">將下列宣告新增至 Echo：</span><span class="sxs-lookup"><span data-stu-id="fa79a-118">Add the following declarations to Echo.h:</span></span>


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



<span data-ttu-id="fa79a-119">這些值會儲存為百分比的十進位標記法，因此可以輕鬆地當做比例因數使用。</span><span class="sxs-lookup"><span data-stu-id="fa79a-119">These values are stored as decimal representations of percentages so they can easily be used as scale factors.</span></span> <span data-ttu-id="fa79a-120">例如，50% 效果和50% 來源信號的組合會以每個變數的0.50 值表示。</span><span class="sxs-lookup"><span data-stu-id="fa79a-120">For instance, a mixture of 50 percent effect and 50 percent source signal would be represented as a value of 0.50 for each variable.</span></span> <span data-ttu-id="fa79a-121">M \_ fWetMix 和 m fDryMix 值的總和不得超過 \_ 1.0 (100%) 。</span><span class="sxs-lookup"><span data-stu-id="fa79a-121">The sum of the values for m\_fWetMix and m\_fDryMix must not be more than 1.0 (100 percent).</span></span> <span data-ttu-id="fa79a-122">最後，這些值將可作為屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="fa79a-122">Eventually, these values will be accessible as properties.</span></span>

<span data-ttu-id="fa79a-123">將下列程式碼新增至 CEcho 的函式，以將預設值設定為50%：</span><span class="sxs-lookup"><span data-stu-id="fa79a-123">Add the following code to the CEcho constructor to set the default values to 50 percent each:</span></span>


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a><span data-ttu-id="fa79a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa79a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa79a-125">**Echo 範例屬性**</span><span class="sxs-lookup"><span data-stu-id="fa79a-125">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




