---
description: ShouldDrawSampleNow 方法會決定如何排程範例以進行轉譯。
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: 'CBaseRenderer. ShouldDrawSampleNow 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995497"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a><span data-ttu-id="d3262-103">CBaseRenderer. ShouldDrawSampleNow 方法</span><span class="sxs-lookup"><span data-stu-id="d3262-103">CBaseRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="d3262-104">`ShouldDrawSampleNow`方法會決定如何排程範例以進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="d3262-104">The `ShouldDrawSampleNow` method determines how a sample is scheduled for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3262-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3262-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="d3262-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3262-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3262-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="d3262-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d3262-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d3262-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d3262-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="d3262-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d3262-110">變數的指標，其中包含範例的開始時間。</span><span class="sxs-lookup"><span data-stu-id="d3262-110">Pointer to a variable that contains the sample's start time.</span></span>

</dd> <dt>

<span data-ttu-id="d3262-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="d3262-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d3262-112">變數的指標，其中包含範例的結束時間。</span><span class="sxs-lookup"><span data-stu-id="d3262-112">Pointer to a variable that contains the sample's end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3262-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3262-113">Return value</span></span>

<span data-ttu-id="d3262-114">傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="d3262-114">Returns S\_FALSE.</span></span> <span data-ttu-id="d3262-115">如果衍生類別覆寫這個方法，則傳回下表所示的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d3262-115">If the derived class overrides this method, return one of the values shown in the following table.</span></span>



| <span data-ttu-id="d3262-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d3262-116">Return code</span></span>                                                                               | <span data-ttu-id="d3262-117">Description</span><span class="sxs-lookup"><span data-stu-id="d3262-117">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3262-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d3262-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d3262-119">範例應立即轉譯。</span><span class="sxs-lookup"><span data-stu-id="d3262-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="d3262-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d3262-120"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="d3262-121">此範例應根據時間戳記來排程轉譯。</span><span class="sxs-lookup"><span data-stu-id="d3262-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="d3262-122"><dt>**錯誤碼**</dt></span><span class="sxs-lookup"><span data-stu-id="d3262-122"><dt>**Error code**</dt></span></span> </dl> | <span data-ttu-id="d3262-123">請勿呈現此範例。</span><span class="sxs-lookup"><span data-stu-id="d3262-123">Do not render this sample.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="d3262-124">備註</span><span class="sxs-lookup"><span data-stu-id="d3262-124">Remarks</span></span>

<span data-ttu-id="d3262-125">[**CBaseRenderer：： GetSampleTimes**](cbaserenderer-getsampletimes.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d3262-125">The [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method calls this method.</span></span> <span data-ttu-id="d3262-126">根據預設，範例一律會根據其時間戳記排程進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="d3262-126">By default, samples are always scheduled for rendering based on their time stamps.</span></span> <span data-ttu-id="d3262-127">衍生的類別可以覆寫這個方法。例如，執行品質控制。</span><span class="sxs-lookup"><span data-stu-id="d3262-127">The derived class can override this method; for example, to implement quality control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3262-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3262-128">Requirements</span></span>



| <span data-ttu-id="d3262-129">需求</span><span class="sxs-lookup"><span data-stu-id="d3262-129">Requirement</span></span> | <span data-ttu-id="d3262-130">值</span><span class="sxs-lookup"><span data-stu-id="d3262-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3262-131">標頭</span><span class="sxs-lookup"><span data-stu-id="d3262-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d3262-132"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d3262-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3262-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3262-133">Library</span></span><br/> | <dl> <span data-ttu-id="d3262-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d3262-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3262-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3262-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3262-136">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="d3262-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




