---
title: 變更預設值
description: 變更預設值
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- 視覺效果、光暈範例
- 自訂視覺效果，發光範例
- 程式設計指南，視覺效果
- 範例，發光視覺效果
- 發光視覺效果範例
- 視覺效果，預設
- 自訂視覺效果，預設
- 視覺效果中的預設值，發光範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106983287"
---
# <a name="changing-presets"></a><span data-ttu-id="9d0b6-111">變更預設值</span><span class="sxs-lookup"><span data-stu-id="9d0b6-111">Changing Presets</span></span>

<span data-ttu-id="9d0b6-112">下列預設的程式碼區段已變更為允許三個預設值：</span><span class="sxs-lookup"><span data-stu-id="9d0b6-112">The following preset code sections were changed to allow three presets:</span></span>

## <a name="getpresettitle"></a><span data-ttu-id="9d0b6-113">GetPresetTitle</span><span class="sxs-lookup"><span data-stu-id="9d0b6-113">GetPresetTitle</span></span>

<span data-ttu-id="9d0b6-114">插入此程式碼以取代產生的預設程式碼：</span><span class="sxs-lookup"><span data-stu-id="9d0b6-114">This code was inserted in place of the generated preset code:</span></span>


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a><span data-ttu-id="9d0b6-115">列舉</span><span class="sxs-lookup"><span data-stu-id="9d0b6-115">Enumerations</span></span>

<span data-ttu-id="9d0b6-116">下列在 h.264 中的列舉已變更為允許三個預設：</span><span class="sxs-lookup"><span data-stu-id="9d0b6-116">The following enumeration in Glow.h was changed to allow three presets:</span></span>


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a><span data-ttu-id="9d0b6-117">資源標頭</span><span class="sxs-lookup"><span data-stu-id="9d0b6-117">Resource Header</span></span>

<span data-ttu-id="9d0b6-118">下列資源定義于 resources 中，以允許三個預設：</span><span class="sxs-lookup"><span data-stu-id="9d0b6-118">The following resources were defined in Resource.h to allow three presets:</span></span>


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



<span data-ttu-id="9d0b6-119">請注意，您也必須將 [ **\_ ap \_ ] 下一個 \_ SYMED \_ 值** 的資源數目變更為106。</span><span class="sxs-lookup"><span data-stu-id="9d0b6-119">Note that you must also change the resource number of **\_APS\_NEXT\_SYMED\_VALUE** to 106.</span></span>

## <a name="resource-file"></a><span data-ttu-id="9d0b6-120">資源檔案</span><span class="sxs-lookup"><span data-stu-id="9d0b6-120">Resource File</span></span>

<span data-ttu-id="9d0b6-121">您必須在 Glowdll .rc 檔中變更下列字串，以允許三個預設值，並為其指定名稱：</span><span class="sxs-lookup"><span data-stu-id="9d0b6-121">The following strings must be changed in the Glowdll.rc file to allow three presets and give them names:</span></span>


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a><span data-ttu-id="9d0b6-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d0b6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d0b6-123">**發光範例**</span><span class="sxs-lookup"><span data-stu-id="9d0b6-123">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




