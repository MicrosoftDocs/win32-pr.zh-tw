---
description: WaitForRenderTime 方法會等候目前樣本的呈現時間。
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: 'CBaseRenderer. WaitForRenderTime 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985938"
---
# <a name="cbaserendererwaitforrendertime-method"></a><span data-ttu-id="83a2d-103">CBaseRenderer. WaitForRenderTime 方法</span><span class="sxs-lookup"><span data-stu-id="83a2d-103">CBaseRenderer.WaitForRenderTime method</span></span>

<span data-ttu-id="83a2d-104">`WaitForRenderTime`方法會等候目前樣本的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="83a2d-104">The `WaitForRenderTime` method waits for the current sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="83a2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="83a2d-105">Syntax</span></span>


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a><span data-ttu-id="83a2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="83a2d-106">Parameters</span></span>

<span data-ttu-id="83a2d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="83a2d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83a2d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="83a2d-108">Return value</span></span>

<span data-ttu-id="83a2d-109">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="83a2d-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="83a2d-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="83a2d-110">Return code</span></span>                                                                                           | <span data-ttu-id="83a2d-111">Description</span><span class="sxs-lookup"><span data-stu-id="83a2d-111">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83a2d-112"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="83a2d-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="83a2d-113">成功。</span><span class="sxs-lookup"><span data-stu-id="83a2d-113">Success.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="83a2d-114"><dt>**VFW \_ E \_ 狀態 \_ 已變更**</dt></span><span class="sxs-lookup"><span data-stu-id="83a2d-114"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="83a2d-115">篩選準則狀態會在呈現時間到達之前變更。</span><span class="sxs-lookup"><span data-stu-id="83a2d-115">The filter state changed before the presentation time arrived.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83a2d-116">備註</span><span class="sxs-lookup"><span data-stu-id="83a2d-116">Remarks</span></span>

<span data-ttu-id="83a2d-117">這個方法會等候，直到發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="83a2d-117">This method waits until one of the following occurs:</span></span>

-   <span data-ttu-id="83a2d-118">範例的呈現時間抵達，此時可以轉譯範例。</span><span class="sxs-lookup"><span data-stu-id="83a2d-118">The sample's presentation time arrives, at which point the sample can be rendered.</span></span>
-   <span data-ttu-id="83a2d-119">篩選會停止或開始排清資料。</span><span class="sxs-lookup"><span data-stu-id="83a2d-119">The filter stops or begins flushing data.</span></span>

<span data-ttu-id="83a2d-120">如果呈現時間抵達， [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 事件就會收到信號。</span><span class="sxs-lookup"><span data-stu-id="83a2d-120">If the presentation time arrives, the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event is signaled.</span></span> <span data-ttu-id="83a2d-121">如果狀態變更，則會發出 [**CBaseRenderer：： m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) 事件的信號。</span><span class="sxs-lookup"><span data-stu-id="83a2d-121">If the state changes, the [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md) event is signaled.</span></span> <span data-ttu-id="83a2d-122">這個方法會等候兩個事件。</span><span class="sxs-lookup"><span data-stu-id="83a2d-122">This method waits on both events.</span></span> <span data-ttu-id="83a2d-123">必要時，衍生類別可以覆寫這個方法以等候其他事件。</span><span class="sxs-lookup"><span data-stu-id="83a2d-123">The derived class can override this method to wait on additional events, if necessary.</span></span>

<span data-ttu-id="83a2d-124">當等候開始時，這個方法會呼叫 [**CBaseRenderer：： OnWaitStart**](cbaserenderer-onwaitstart.md) 方法，而當等候完成時，則會呼叫 [**CBaseRenderer：： OnWaitEnd**](cbaserenderer-onwaitend.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="83a2d-124">This method calls the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method when the wait begins, and the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method when the wait is done.</span></span> <span data-ttu-id="83a2d-125">這兩種方法都不會在基類中執行任何作業，但衍生類別可以覆寫它們。</span><span class="sxs-lookup"><span data-stu-id="83a2d-125">Neither method does anything in the base class, but the derived class can override them.</span></span>

## <a name="requirements"></a><span data-ttu-id="83a2d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="83a2d-126">Requirements</span></span>



| <span data-ttu-id="83a2d-127">需求</span><span class="sxs-lookup"><span data-stu-id="83a2d-127">Requirement</span></span> | <span data-ttu-id="83a2d-128">值</span><span class="sxs-lookup"><span data-stu-id="83a2d-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83a2d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="83a2d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="83a2d-130"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="83a2d-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="83a2d-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="83a2d-131">Library</span></span><br/> | <dl> <span data-ttu-id="83a2d-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="83a2d-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83a2d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83a2d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a2d-134">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="83a2d-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




