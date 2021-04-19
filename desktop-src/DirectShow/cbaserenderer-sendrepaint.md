---
description: SendRepaint 方法會將重新繪製事件傳送至篩選圖形管理員。
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: 'CBaseRenderer. SendRepaint 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3a88f0c1dae54cb5d9be1e4e9ad3e9677bdd958
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983091"
---
# <a name="cbaserenderersendrepaint-method"></a><span data-ttu-id="40550-103">CBaseRenderer. SendRepaint 方法</span><span class="sxs-lookup"><span data-stu-id="40550-103">CBaseRenderer.SendRepaint method</span></span>

<span data-ttu-id="40550-104">`SendRepaint`方法會將重新繪製事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="40550-104">The `SendRepaint` method sends a repaint event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="40550-105">語法</span><span class="sxs-lookup"><span data-stu-id="40550-105">Syntax</span></span>


```C++
void SendRepaint();
```



## <a name="parameters"></a><span data-ttu-id="40550-106">參數</span><span class="sxs-lookup"><span data-stu-id="40550-106">Parameters</span></span>

<span data-ttu-id="40550-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="40550-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40550-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="40550-108">Return value</span></span>

<span data-ttu-id="40550-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="40550-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40550-110">備註</span><span class="sxs-lookup"><span data-stu-id="40550-110">Remarks</span></span>

<span data-ttu-id="40550-111">如果下列條件成立，則這個方法會將 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件傳送至篩選圖形管理員：</span><span class="sxs-lookup"><span data-stu-id="40550-111">This method sends an [**EC\_REPAINT**](ec-repaint.md) event to the filter graph manager if the following conditions are true:</span></span>

-   <span data-ttu-id="40550-112">輸入 pin 已連線。</span><span class="sxs-lookup"><span data-stu-id="40550-112">The input pin is connected.</span></span>
-   <span data-ttu-id="40550-113">篩選不會排清資料。</span><span class="sxs-lookup"><span data-stu-id="40550-113">The filter is not flushing data.</span></span>
-   <span data-ttu-id="40550-114">未到達資料流程結尾。</span><span class="sxs-lookup"><span data-stu-id="40550-114">The end-of-stream was not reached.</span></span>
-   <span data-ttu-id="40550-115">[**CBaseRenderer：： m \_ bAbort**](cbaserenderer-m-babort.md)旗標為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="40550-115">The [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag is **FALSE**.</span></span>
-   <span data-ttu-id="40550-116">[**CBaseRenderer：： m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)旗標為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="40550-116">The [**CBaseRenderer::m\_bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) flag is **TRUE**.</span></span>

<span data-ttu-id="40550-117">根據圖形的狀態而定，EC \_ 重新繪製事件可能會導致上游篩選器重新傳送範例、篩選圖形來搜尋其目前位置，或篩選圖形管理員以暫時暫停。</span><span class="sxs-lookup"><span data-stu-id="40550-117">Depending on the state of the graph, the EC\_REPAINT event can cause the upstream filter to re-send a sample; the filter graph to seek to its current location; or the filter graph manager to pause momentarily.</span></span> <span data-ttu-id="40550-118"> (看到 [**EC 重新 \_ 繪製**](ec-repaint.md)。 ) 此事件可能沒有效率，因此應謹慎使用。</span><span class="sxs-lookup"><span data-stu-id="40550-118">(See [**EC\_REPAINT**](ec-repaint.md).) This event is potentially inefficient, so it should be used sparingly.</span></span> <span data-ttu-id="40550-119">不過，影片轉譯器有時需要重新整理顯示畫面。</span><span class="sxs-lookup"><span data-stu-id="40550-119">However, video renderers sometimes need to refresh the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="40550-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="40550-120">Requirements</span></span>



| <span data-ttu-id="40550-121">需求</span><span class="sxs-lookup"><span data-stu-id="40550-121">Requirement</span></span> | <span data-ttu-id="40550-122">值</span><span class="sxs-lookup"><span data-stu-id="40550-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40550-123">標頭</span><span class="sxs-lookup"><span data-stu-id="40550-123">Header</span></span><br/>  | <dl> <span data-ttu-id="40550-124"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="40550-124"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40550-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="40550-125">Library</span></span><br/> | <dl> <span data-ttu-id="40550-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="40550-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40550-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40550-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40550-128">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="40550-128">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




