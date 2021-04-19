---
description: Render 方法會呈現範例。
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: 'CBaseRenderer：轉譯方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987969"
---
# <a name="cbaserendererrender-method"></a><span data-ttu-id="5d1b4-103">CBaseRenderer 轉譯方法</span><span class="sxs-lookup"><span data-stu-id="5d1b4-103">CBaseRenderer.Render method</span></span>

<span data-ttu-id="5d1b4-104">`Render`方法會呈現範例。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-104">The `Render` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d1b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="5d1b4-105">Syntax</span></span>


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="5d1b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="5d1b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d1b4-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="5d1b4-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5d1b4-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d1b4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d1b4-109">Return value</span></span>

<span data-ttu-id="5d1b4-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5d1b4-111">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="5d1b4-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5d1b4-112">Return code</span></span>                                                                             | <span data-ttu-id="5d1b4-113">Description</span><span class="sxs-lookup"><span data-stu-id="5d1b4-113">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d1b4-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5d1b4-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5d1b4-115">篩選已停止，或 *pMediaSample* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-115">The filter is stopped, or *pMediaSample* is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="5d1b4-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5d1b4-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5d1b4-117">成功。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-117">Success.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="5d1b4-118">備註</span><span class="sxs-lookup"><span data-stu-id="5d1b4-118">Remarks</span></span>

<span data-ttu-id="5d1b4-119">這個方法會呼叫純虛擬方法 [**CBaseRenderer：:D orendersample**](cbaserenderer-dorendersample.md)，這會執行實際的工作。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-119">This method calls the pure virtual method [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md), which does the real work.</span></span> <span data-ttu-id="5d1b4-120">衍生的類別必須執行 **DoRenderSample**。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-120">The derived class must implement **DoRenderSample**.</span></span>

<span data-ttu-id="5d1b4-121">在呼叫 **DoRenderSample** 之前，這個方法會呼叫 [**CBaseRenderer：： OnRenderStart**](cbaserenderer-onrenderstart.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-121">Immediately before calling **DoRenderSample**, this method calls the [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md) method.</span></span> <span data-ttu-id="5d1b4-122">緊接在之後，它會呼叫 [**CBaseRenderer：： OnRenderEnd**](cbaserenderer-onrenderend.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-122">Immediately after, it calls the [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md) method.</span></span> <span data-ttu-id="5d1b4-123">衍生類別可以視需要覆寫這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="5d1b4-123">The derived class can override those two methods as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d1b4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d1b4-124">Requirements</span></span>



| <span data-ttu-id="5d1b4-125">需求</span><span class="sxs-lookup"><span data-stu-id="5d1b4-125">Requirement</span></span> | <span data-ttu-id="5d1b4-126">值</span><span class="sxs-lookup"><span data-stu-id="5d1b4-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d1b4-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5d1b4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5d1b4-128"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5d1b4-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d1b4-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="5d1b4-129">Library</span></span><br/> | <dl> <span data-ttu-id="5d1b4-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5d1b4-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d1b4-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d1b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d1b4-132">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="5d1b4-132">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




