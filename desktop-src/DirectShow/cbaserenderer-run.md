---
description: Run 方法會執行篩選。
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: 'CBaseRenderer： Run 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987849"
---
# <a name="cbaserendererrun-method"></a><span data-ttu-id="819ba-103">CBaseRenderer 方法</span><span class="sxs-lookup"><span data-stu-id="819ba-103">CBaseRenderer.Run method</span></span>

<span data-ttu-id="819ba-104">`Run`方法會執行篩選。</span><span class="sxs-lookup"><span data-stu-id="819ba-104">The `Run` method runs the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="819ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="819ba-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="819ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="819ba-106">Parameters</span></span>

<span data-ttu-id="819ba-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="819ba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="819ba-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="819ba-108">Return value</span></span>

<span data-ttu-id="819ba-109">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="819ba-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="819ba-110">備註</span><span class="sxs-lookup"><span data-stu-id="819ba-110">Remarks</span></span>

<span data-ttu-id="819ba-111">這個方法會覆寫 [**CBaseFilter：： Run**](cbasefilter-run.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="819ba-111">This method overrides the [**CBaseFilter::Run**](cbasefilter-run.md) method.</span></span> <span data-ttu-id="819ba-112">其會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="819ba-112">It performs the following actions:</span></span>

-   <span data-ttu-id="819ba-113">呼叫 **CBaseFilter：： Run** 方法。</span><span class="sxs-lookup"><span data-stu-id="819ba-113">Calls the **CBaseFilter::Run** method.</span></span>
-   <span data-ttu-id="819ba-114">認可配置器。</span><span class="sxs-lookup"><span data-stu-id="819ba-114">Commits the allocator.</span></span> <span data-ttu-id="819ba-115"> (參閱 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)。 ) </span><span class="sxs-lookup"><span data-stu-id="819ba-115">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="819ba-116">如果先前的狀態為 [已停止]，則篩選會釋放它所持有的任何範例。</span><span class="sxs-lookup"><span data-stu-id="819ba-116">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="819ba-117"> (範例不再有效。 ) </span><span class="sxs-lookup"><span data-stu-id="819ba-117">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="819ba-118">呼叫 [**CBaseRenderer：： StartStreaming**](cbaserenderer-startstreaming.md) 方法，並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="819ba-118">Calls the [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method and returns the result.</span></span> <span data-ttu-id="819ba-119">如果範例暫止， **StartStreaming** 方法會排程它以進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="819ba-119">If a sample is pending, the **StartStreaming** method schedules it for rendering.</span></span>

<span data-ttu-id="819ba-120">如果篩選未連接，則會立即張貼 [**EC \_ 完成**](ec-complete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="819ba-120">If the filter is not connected, it posts an [**EC\_COMPLETE**](ec-complete.md) event immediately.</span></span>

## <a name="requirements"></a><span data-ttu-id="819ba-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="819ba-121">Requirements</span></span>



| <span data-ttu-id="819ba-122">需求</span><span class="sxs-lookup"><span data-stu-id="819ba-122">Requirement</span></span> | <span data-ttu-id="819ba-123">值</span><span class="sxs-lookup"><span data-stu-id="819ba-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="819ba-124">標頭</span><span class="sxs-lookup"><span data-stu-id="819ba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="819ba-125"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="819ba-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="819ba-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="819ba-126">Library</span></span><br/> | <dl> <span data-ttu-id="819ba-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="819ba-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="819ba-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="819ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819ba-129">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="819ba-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




