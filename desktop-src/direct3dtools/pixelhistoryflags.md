---
description: 列舉，其中包含用來描述圖元歷程記錄結果的旗標。 請參閱 PixelHistoryOperation。
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PIXELHISTORYFLAGS 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108940"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span data-ttu-id="46951-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS 列舉</span><span class="sxs-lookup"><span data-stu-id="46951-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS enumeration</span></span>

<span data-ttu-id="46951-105">列舉，其中包含用來描述圖元歷程記錄結果的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-105">An enum containing flags used to describe a pixel history result.</span></span> <span data-ttu-id="46951-106">請參閱 PixelHistoryOperation。</span><span class="sxs-lookup"><span data-stu-id="46951-106">See PixelHistoryOperation.</span></span>

## <a name="syntax"></a><span data-ttu-id="46951-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="46951-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="46951-108">常數</span><span class="sxs-lookup"><span data-stu-id="46951-108">Constants</span></span>

<span data-ttu-id="46951-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ INITIALVALUE**</span><span class="sxs-lookup"><span data-stu-id="46951-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF\_INITIALVALUE**</span></span>  
<span data-ttu-id="46951-110">對應至框架) 之前 (初始色彩值的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-110">A flag that corresponds to the initial color value (prior to frame).</span></span>

<span data-ttu-id="46951-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ CLEAR**</span><span class="sxs-lookup"><span data-stu-id="46951-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF\_CLEAR**</span></span>  
<span data-ttu-id="46951-112">對應至清除色彩結果的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-112">A flag that corresponds to the clear color result.</span></span>

<span data-ttu-id="46951-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ DRAW**</span><span class="sxs-lookup"><span data-stu-id="46951-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF\_DRAW**</span></span>  
<span data-ttu-id="46951-114">對應至繪製色彩結果的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-114">A flag that corresponds to the draw color result.</span></span>

<span data-ttu-id="46951-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ FINALVALUE**</span><span class="sxs-lookup"><span data-stu-id="46951-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF\_FINALVALUE**</span></span>  
<span data-ttu-id="46951-116">對應至最終色彩結果的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-116">A flag that corresponds to the final color result.</span></span>

<span data-ttu-id="46951-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**</span><span class="sxs-lookup"><span data-stu-id="46951-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF\_HASCOLOR**</span></span>  
<span data-ttu-id="46951-118">對應至 PixelHistoryOperation 結構中是否有色彩結果的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-118">A flag that corresponds to whether the color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="46951-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**</span><span class="sxs-lookup"><span data-stu-id="46951-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF\_HASFBCOLOR**</span></span>  
<span data-ttu-id="46951-120">對應至 PixelHistoryOperation 結構中是否存在最終緩衝區色彩結果的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-120">A flag that corresponds to whether the final buffer color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="46951-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="46951-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF\_ERROR**</span></span>  

<span data-ttu-id="46951-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**</span><span class="sxs-lookup"><span data-stu-id="46951-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF\_VERTEXPROCESSINGSKIPPED**</span></span>  
<span data-ttu-id="46951-123">未使用。</span><span class="sxs-lookup"><span data-stu-id="46951-123">Not used.</span></span>

<span data-ttu-id="46951-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="46951-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF\_MODIFYRESOURCE**</span></span>  

<span data-ttu-id="46951-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="46951-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF\_CANNOTRUNFULLDEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="46951-126">對應于無法執行深度或樣板測試的旗標。</span><span class="sxs-lookup"><span data-stu-id="46951-126">A flag that corresponds to not being able to run the depth or stencil test.</span></span>

## <a name="requirements"></a><span data-ttu-id="46951-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="46951-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="46951-128">標頭</span><span class="sxs-lookup"><span data-stu-id="46951-128">Header</span></span></p></td><td><span data-ttu-id="46951-129">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="46951-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



