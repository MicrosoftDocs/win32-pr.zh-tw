---
description: Pause 方法會暫停篩選。
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: 'CBaseRenderer： Pause 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999534"
---
# <a name="cbaserendererpause-method"></a><span data-ttu-id="83444-103">CBaseRenderer. Pause 方法</span><span class="sxs-lookup"><span data-stu-id="83444-103">CBaseRenderer.Pause method</span></span>

<span data-ttu-id="83444-104">`Pause`方法會暫停篩選。</span><span class="sxs-lookup"><span data-stu-id="83444-104">The `Pause` method pauses the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="83444-105">語法</span><span class="sxs-lookup"><span data-stu-id="83444-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="83444-106">參數</span><span class="sxs-lookup"><span data-stu-id="83444-106">Parameters</span></span>

<span data-ttu-id="83444-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="83444-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83444-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="83444-108">Return value</span></span>

<span data-ttu-id="83444-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="83444-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="83444-110">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="83444-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="83444-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="83444-111">Return code</span></span>                                                                             | <span data-ttu-id="83444-112">Description</span><span class="sxs-lookup"><span data-stu-id="83444-112">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="83444-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="83444-113"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="83444-114">轉換已完成。</span><span class="sxs-lookup"><span data-stu-id="83444-114">The transition is complete.</span></span><br/> |
| <dl> <span data-ttu-id="83444-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="83444-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="83444-116">轉換未完成。</span><span class="sxs-lookup"><span data-stu-id="83444-116">Transition is not complete.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83444-117">備註</span><span class="sxs-lookup"><span data-stu-id="83444-117">Remarks</span></span>

<span data-ttu-id="83444-118">這個方法會覆寫 [**CBaseFilter：:P ause**](cbasefilter-pause.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="83444-118">This method overrides the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="83444-119">它會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="83444-119">It performs the following steps:</span></span>

-   <span data-ttu-id="83444-120">呼叫 **CBaseFilter：:P ause** 方法。</span><span class="sxs-lookup"><span data-stu-id="83444-120">Calls the **CBaseFilter::Pause** method.</span></span>
-   <span data-ttu-id="83444-121">認可配置器。</span><span class="sxs-lookup"><span data-stu-id="83444-121">Commits the allocator.</span></span> <span data-ttu-id="83444-122"> (參閱 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)。 ) </span><span class="sxs-lookup"><span data-stu-id="83444-122">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="83444-123">如果先前的狀態為 [已停止]，則篩選會釋放它所持有的任何範例。</span><span class="sxs-lookup"><span data-stu-id="83444-123">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="83444-124"> (範例不再有效。 ) </span><span class="sxs-lookup"><span data-stu-id="83444-124">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="83444-125">呼叫 [**CBaseRenderer：： CompleteStateChange**](cbaserenderer-completestatechange.md) 方法，並傳回值。</span><span class="sxs-lookup"><span data-stu-id="83444-125">Calls the [**CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) method and returns the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="83444-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="83444-126">Requirements</span></span>



| <span data-ttu-id="83444-127">需求</span><span class="sxs-lookup"><span data-stu-id="83444-127">Requirement</span></span> | <span data-ttu-id="83444-128">值</span><span class="sxs-lookup"><span data-stu-id="83444-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83444-129">標頭</span><span class="sxs-lookup"><span data-stu-id="83444-129">Header</span></span><br/>  | <dl> <span data-ttu-id="83444-130"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="83444-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="83444-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="83444-131">Library</span></span><br/> | <dl> <span data-ttu-id="83444-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="83444-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83444-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83444-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83444-134">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="83444-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




