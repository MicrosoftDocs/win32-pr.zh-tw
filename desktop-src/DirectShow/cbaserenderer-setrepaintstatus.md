---
description: SetRepaintStatus 方法會啟用或停用重新繪製事件。
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: 'CBaseRenderer. SetRepaintStatus 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994883"
---
# <a name="cbaserenderersetrepaintstatus-method"></a><span data-ttu-id="fc5df-103">CBaseRenderer. SetRepaintStatus 方法</span><span class="sxs-lookup"><span data-stu-id="fc5df-103">CBaseRenderer.SetRepaintStatus method</span></span>

<span data-ttu-id="fc5df-104">`SetRepaintStatus`方法會啟用或停用重新繪製事件。</span><span class="sxs-lookup"><span data-stu-id="fc5df-104">The `SetRepaintStatus` method enables or disables repaint events.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc5df-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc5df-105">Syntax</span></span>


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a><span data-ttu-id="fc5df-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc5df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc5df-107">*bRepaint*</span><span class="sxs-lookup"><span data-stu-id="fc5df-107">*bRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="fc5df-108">指出是否已啟用重新繪製事件的布林值。</span><span class="sxs-lookup"><span data-stu-id="fc5df-108">Boolean value indicating whether repaint events are enabled.</span></span> <span data-ttu-id="fc5df-109">若 **為 TRUE**，則篩選會將 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="fc5df-109">If **TRUE**, the filter will sent [**EC\_REPAINT**](ec-repaint.md) events to the filter graph manager.</span></span> <span data-ttu-id="fc5df-110">否則，它不會傳送 EC 重新 \_ 繪製事件。</span><span class="sxs-lookup"><span data-stu-id="fc5df-110">Otherwise, it will not send EC\_REPAINT events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc5df-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc5df-111">Return value</span></span>

<span data-ttu-id="fc5df-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fc5df-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc5df-113">備註</span><span class="sxs-lookup"><span data-stu-id="fc5df-113">Remarks</span></span>

<span data-ttu-id="fc5df-114">這個方法可確保篩選圖形管理員不會溢滿重複的 EC 重新 \_ 繪製事件。</span><span class="sxs-lookup"><span data-stu-id="fc5df-114">This method ensures that the filter graph manager is not flooded with redundant EC\_REPAINT events.</span></span> <span data-ttu-id="fc5df-115">在篩選傳送 EC 重新 [**\_ 繪製**](ec-repaint.md) 事件之後，它會呼叫此方法並傳回 **TRUE** 值。</span><span class="sxs-lookup"><span data-stu-id="fc5df-115">After the filter sends an [**EC\_REPAINT**](ec-repaint.md) event, it calls this method with the value **TRUE**.</span></span> <span data-ttu-id="fc5df-116">篩選不會傳送更多的 EC 重新 \_ 繪製事件，直到接收到更多資料為止。</span><span class="sxs-lookup"><span data-stu-id="fc5df-116">The filter does not send more EC\_REPAINT events until it receives more data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5df-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc5df-117">Requirements</span></span>



| <span data-ttu-id="fc5df-118">需求</span><span class="sxs-lookup"><span data-stu-id="fc5df-118">Requirement</span></span> | <span data-ttu-id="fc5df-119">值</span><span class="sxs-lookup"><span data-stu-id="fc5df-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5df-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fc5df-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fc5df-121"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fc5df-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc5df-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc5df-122">Library</span></span><br/> | <dl> <span data-ttu-id="fc5df-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fc5df-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc5df-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc5df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5df-125">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="fc5df-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




