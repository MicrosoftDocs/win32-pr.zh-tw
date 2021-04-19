---
description: 在篩選器呈現範例之前，會呼叫 PrepareRender 方法。
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: 'CBaseRenderer. PrepareRender 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996502"
---
# <a name="cbaserendererpreparerender-method"></a><span data-ttu-id="2c43f-103">CBaseRenderer. PrepareRender 方法</span><span class="sxs-lookup"><span data-stu-id="2c43f-103">CBaseRenderer.PrepareRender method</span></span>

<span data-ttu-id="2c43f-104">在 `PrepareRender` 篩選器呈現範例之前，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="2c43f-104">The `PrepareRender` method is called before the filter renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c43f-105">語法</span><span class="sxs-lookup"><span data-stu-id="2c43f-105">Syntax</span></span>


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a><span data-ttu-id="2c43f-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c43f-106">Parameters</span></span>

<span data-ttu-id="2c43f-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2c43f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c43f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c43f-108">Return value</span></span>

<span data-ttu-id="2c43f-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c43f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c43f-110">備註</span><span class="sxs-lookup"><span data-stu-id="2c43f-110">Remarks</span></span>

<span data-ttu-id="2c43f-111">篩選準則會在呼叫 [**CBaseRenderer：： OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) 方法或 [**CBaseRenderer：： Render**](cbaserenderer-render.md) 方法之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2c43f-111">The filter calls this method before it calls the [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) method or the [**CBaseRenderer::Render**](cbaserenderer-render.md) method.</span></span> <span data-ttu-id="2c43f-112">`PrepareRender` 不會在基類中執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="2c43f-112">`PrepareRender` does not do anything in the base class.</span></span> <span data-ttu-id="2c43f-113">衍生類別可以覆寫它，以執行轉譯之前所需的任何動作。</span><span class="sxs-lookup"><span data-stu-id="2c43f-113">The derived class can override it to perform any actions required before rendering.</span></span> <span data-ttu-id="2c43f-114">例如，影片轉譯器可以覆寫這個方法，以實現其調色板。</span><span class="sxs-lookup"><span data-stu-id="2c43f-114">For example, a video renderer can override this method to realize its palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c43f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c43f-115">Requirements</span></span>



| <span data-ttu-id="2c43f-116">需求</span><span class="sxs-lookup"><span data-stu-id="2c43f-116">Requirement</span></span> | <span data-ttu-id="2c43f-117">值</span><span class="sxs-lookup"><span data-stu-id="2c43f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c43f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="2c43f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2c43f-119"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2c43f-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2c43f-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c43f-120">Library</span></span><br/> | <dl> <span data-ttu-id="2c43f-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2c43f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c43f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c43f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c43f-123">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="2c43f-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




