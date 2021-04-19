---
description: 當轉譯即將開始時，會呼叫 OnRenderStart 方法。
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: 'CBaseRenderer. OnRenderStart 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994283"
---
# <a name="cbaserendereronrenderstart-method"></a><span data-ttu-id="7f0ac-103">CBaseRenderer. OnRenderStart 方法</span><span class="sxs-lookup"><span data-stu-id="7f0ac-103">CBaseRenderer.OnRenderStart method</span></span>

<span data-ttu-id="7f0ac-104">當轉譯即將 `OnRenderStart` 開始時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="7f0ac-104">The `OnRenderStart` method is called when rendering is about to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f0ac-105">Syntax</span></span>


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="7f0ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f0ac-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="7f0ac-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7f0ac-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7f0ac-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f0ac-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f0ac-109">Return value</span></span>

<span data-ttu-id="7f0ac-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7f0ac-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f0ac-111">備註</span><span class="sxs-lookup"><span data-stu-id="7f0ac-111">Remarks</span></span>

<span data-ttu-id="7f0ac-112">[**CBaseRenderer：： Render**](cbaserenderer-render.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7f0ac-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="7f0ac-113">它不會在基類中執行任何動作，但衍生類別可以覆寫它。例如，收集品質控制資料。</span><span class="sxs-lookup"><span data-stu-id="7f0ac-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0ac-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f0ac-114">Requirements</span></span>



| <span data-ttu-id="7f0ac-115">需求</span><span class="sxs-lookup"><span data-stu-id="7f0ac-115">Requirement</span></span> | <span data-ttu-id="7f0ac-116">值</span><span class="sxs-lookup"><span data-stu-id="7f0ac-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f0ac-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7f0ac-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7f0ac-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f0ac-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f0ac-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f0ac-119">Library</span></span><br/> | <dl> <span data-ttu-id="7f0ac-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7f0ac-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f0ac-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f0ac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f0ac-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="7f0ac-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




