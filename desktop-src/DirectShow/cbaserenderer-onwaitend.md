---
description: 當篩選完成等候樣本的呈現時間時，就會呼叫 OnWaitEnd 方法。
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: 'CBaseRenderer. OnWaitEnd 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996308"
---
# <a name="cbaserendereronwaitend-method"></a><span data-ttu-id="5f506-103">CBaseRenderer. OnWaitEnd 方法</span><span class="sxs-lookup"><span data-stu-id="5f506-103">CBaseRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="5f506-104">`OnWaitEnd`當篩選完成等候樣本的呈現時間時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="5f506-104">The `OnWaitEnd` method is called when the filter is done waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f506-105">語法</span><span class="sxs-lookup"><span data-stu-id="5f506-105">Syntax</span></span>


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="5f506-106">參數</span><span class="sxs-lookup"><span data-stu-id="5f506-106">Parameters</span></span>

<span data-ttu-id="5f506-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5f506-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f506-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f506-108">Return value</span></span>

<span data-ttu-id="5f506-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5f506-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f506-110">備註</span><span class="sxs-lookup"><span data-stu-id="5f506-110">Remarks</span></span>

<span data-ttu-id="5f506-111">[**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md)方法會在完成等候樣本的呈現時間時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5f506-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it has finished waiting for a sample's presentation time.</span></span> <span data-ttu-id="5f506-112">這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="5f506-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="5f506-113">如果您正在執行品質控制，您可能會覆寫此方法以及 [**CBaseRenderer：： OnWaitStart**](cbaserenderer-onwaitstart.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5f506-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method.</span></span> <span data-ttu-id="5f506-114">您可以使用這些方法來追蹤篩選器的效能。</span><span class="sxs-lookup"><span data-stu-id="5f506-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f506-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f506-115">Requirements</span></span>



| <span data-ttu-id="5f506-116">需求</span><span class="sxs-lookup"><span data-stu-id="5f506-116">Requirement</span></span> | <span data-ttu-id="5f506-117">值</span><span class="sxs-lookup"><span data-stu-id="5f506-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f506-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5f506-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5f506-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5f506-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5f506-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f506-120">Library</span></span><br/> | <dl> <span data-ttu-id="5f506-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5f506-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f506-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f506-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f506-123">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="5f506-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




