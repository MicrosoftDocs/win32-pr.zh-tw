---
description: Ready 方法表示狀態轉換已完成。
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: 'CBaseRenderer： Ready 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976264"
---
# <a name="cbaserendererready-method"></a><span data-ttu-id="5b545-103">CBaseRenderer Ready 方法</span><span class="sxs-lookup"><span data-stu-id="5b545-103">CBaseRenderer.Ready method</span></span>

<span data-ttu-id="5b545-104">`Ready`方法會指示狀態轉換已完成。</span><span class="sxs-lookup"><span data-stu-id="5b545-104">The `Ready` method signals that a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b545-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b545-105">Syntax</span></span>


```C++
void Ready();
```



## <a name="parameters"></a><span data-ttu-id="5b545-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b545-106">Parameters</span></span>

<span data-ttu-id="5b545-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5b545-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b545-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b545-108">Return value</span></span>

<span data-ttu-id="5b545-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5b545-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b545-110">備註</span><span class="sxs-lookup"><span data-stu-id="5b545-110">Remarks</span></span>

<span data-ttu-id="5b545-111">這個方法會使 [**CBaseRenderer：： >getstate**](cbaserenderer-getstate.md) 方法傳回 S \_ OK，表示篩選已完成轉換為目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="5b545-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return S\_OK, which indicates that the filter has completed the transition to its current state.</span></span> <span data-ttu-id="5b545-112">篩選準則會在每次完成狀態轉換時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5b545-112">The filter calls this method whenever it completes a state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b545-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b545-113">Requirements</span></span>



| <span data-ttu-id="5b545-114">需求</span><span class="sxs-lookup"><span data-stu-id="5b545-114">Requirement</span></span> | <span data-ttu-id="5b545-115">值</span><span class="sxs-lookup"><span data-stu-id="5b545-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b545-116">標頭</span><span class="sxs-lookup"><span data-stu-id="5b545-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5b545-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5b545-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b545-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b545-118">Library</span></span><br/> | <dl> <span data-ttu-id="5b545-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5b545-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b545-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b545-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b545-121">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="5b545-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="5b545-122">**CBaseRenderer::CheckReady**</span><span class="sxs-lookup"><span data-stu-id="5b545-122">**CBaseRenderer::CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="5b545-123">**CBaseRenderer：： NotReady**</span><span class="sxs-lookup"><span data-stu-id="5b545-123">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> </dl>

 

 




