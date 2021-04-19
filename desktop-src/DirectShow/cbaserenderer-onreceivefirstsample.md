---
description: 當篩選準則在暫停時收到範例時，會呼叫 OnReceiveFirstSample 方法。
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: 'CBaseRenderer. OnReceiveFirstSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991027"
---
# <a name="cbaserendereronreceivefirstsample-method"></a><span data-ttu-id="2e867-103">CBaseRenderer. OnReceiveFirstSample 方法</span><span class="sxs-lookup"><span data-stu-id="2e867-103">CBaseRenderer.OnReceiveFirstSample method</span></span>

<span data-ttu-id="2e867-104">`OnReceiveFirstSample`當篩選準則在暫停時收到範例時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="2e867-104">The `OnReceiveFirstSample` method is called when the filter receives a sample while paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e867-105">語法</span><span class="sxs-lookup"><span data-stu-id="2e867-105">Syntax</span></span>


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="2e867-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e867-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e867-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="2e867-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2e867-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2e867-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e867-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e867-109">Return value</span></span>

<span data-ttu-id="2e867-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2e867-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e867-111">備註</span><span class="sxs-lookup"><span data-stu-id="2e867-111">Remarks</span></span>

<span data-ttu-id="2e867-112">[**CBaseRenderer：： Receive 方法會**](cbaserenderer-receive.md)呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2e867-112">The [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method calls this method.</span></span> <span data-ttu-id="2e867-113">它不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="2e867-113">It does nothing in the base class, but the derived class can override it.</span></span> <span data-ttu-id="2e867-114">此方法主要用於影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2e867-114">This method is intended primarily for video renderers.</span></span> <span data-ttu-id="2e867-115">當影片轉譯器暫停時，通常會將第一個範例顯示為靜止影像。</span><span class="sxs-lookup"><span data-stu-id="2e867-115">When a video renderer is paused, it typically displays the first sample as a still image.</span></span>

<span data-ttu-id="2e867-116">在暫停時搜尋圖形也會導致呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2e867-116">Seeking the graph while paused also causes this method to be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e867-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e867-117">Requirements</span></span>



| <span data-ttu-id="2e867-118">需求</span><span class="sxs-lookup"><span data-stu-id="2e867-118">Requirement</span></span> | <span data-ttu-id="2e867-119">值</span><span class="sxs-lookup"><span data-stu-id="2e867-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e867-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2e867-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2e867-121"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2e867-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e867-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e867-122">Library</span></span><br/> | <dl> <span data-ttu-id="2e867-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2e867-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e867-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e867-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e867-125">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="2e867-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




