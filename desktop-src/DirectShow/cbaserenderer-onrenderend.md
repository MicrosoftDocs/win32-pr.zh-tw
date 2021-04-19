---
description: 轉譯樣本之後，會呼叫 OnRenderEnd 方法。
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: 'CBaseRenderer. OnRenderEnd 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981409"
---
# <a name="cbaserendereronrenderend-method"></a><span data-ttu-id="640cd-103">CBaseRenderer. OnRenderEnd 方法</span><span class="sxs-lookup"><span data-stu-id="640cd-103">CBaseRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="640cd-104">轉譯 `OnRenderEnd` 樣本之後，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="640cd-104">The `OnRenderEnd` method is called after a sample is rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="640cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="640cd-105">Syntax</span></span>


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="640cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="640cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640cd-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="640cd-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="640cd-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="640cd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="640cd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="640cd-109">Return value</span></span>

<span data-ttu-id="640cd-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="640cd-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="640cd-111">備註</span><span class="sxs-lookup"><span data-stu-id="640cd-111">Remarks</span></span>

<span data-ttu-id="640cd-112">[**CBaseRenderer：： Render**](cbaserenderer-render.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="640cd-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="640cd-113">它不會在基類中執行任何動作，但衍生類別可以覆寫它。例如，收集品質控制資料。</span><span class="sxs-lookup"><span data-stu-id="640cd-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="640cd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="640cd-114">Requirements</span></span>



| <span data-ttu-id="640cd-115">需求</span><span class="sxs-lookup"><span data-stu-id="640cd-115">Requirement</span></span> | <span data-ttu-id="640cd-116">值</span><span class="sxs-lookup"><span data-stu-id="640cd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640cd-117">標頭</span><span class="sxs-lookup"><span data-stu-id="640cd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="640cd-118"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="640cd-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="640cd-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="640cd-119">Library</span></span><br/> | <dl> <span data-ttu-id="640cd-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="640cd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="640cd-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="640cd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640cd-122">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="640cd-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




