---
description: GetSampleTimes 方法會從範例中取出時間戳記。
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: 'CBaseRenderer. GetSampleTimes 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983991"
---
# <a name="cbaserenderergetsampletimes-method"></a><span data-ttu-id="e24e0-103">CBaseRenderer. GetSampleTimes 方法</span><span class="sxs-lookup"><span data-stu-id="e24e0-103">CBaseRenderer.GetSampleTimes method</span></span>

<span data-ttu-id="e24e0-104">`GetSampleTimes`方法會從範例抓取時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e24e0-104">The `GetSampleTimes` method retrieves the time stamps from a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="e24e0-105">Syntax</span></span>


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="e24e0-106">參數</span><span class="sxs-lookup"><span data-stu-id="e24e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24e0-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="e24e0-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e24e0-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e24e0-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e24e0-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="e24e0-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e24e0-110">接收開始時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="e24e0-110">Pointer to a variable that receives the start time.</span></span>

</dd> <dt>

<span data-ttu-id="e24e0-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="e24e0-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e24e0-112">接收結束時間之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="e24e0-112">Pointer to a variable that receives the end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24e0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e24e0-113">Return value</span></span>

<span data-ttu-id="e24e0-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e24e0-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e24e0-115">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="e24e0-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e24e0-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e24e0-116">Return code</span></span>                                                                                                    | <span data-ttu-id="e24e0-117">Description</span><span class="sxs-lookup"><span data-stu-id="e24e0-117">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e24e0-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e24e0-118"><dt>**S\_OK**</dt></span></span> </dl>                           | <span data-ttu-id="e24e0-119">範例應立即轉譯。</span><span class="sxs-lookup"><span data-stu-id="e24e0-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="e24e0-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="e24e0-120"><dt>**S\_FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="e24e0-121">此範例應根據時間戳記來排程轉譯。</span><span class="sxs-lookup"><span data-stu-id="e24e0-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="e24e0-122"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e24e0-122"><dt>**E\_FAIL**</dt></span></span> </dl>                         | <span data-ttu-id="e24e0-123">請勿呈現此範例。</span><span class="sxs-lookup"><span data-stu-id="e24e0-123">Do not render this sample.</span></span><br/>                                              |
| <dl> <span data-ttu-id="e24e0-124"><dt>**VFW \_ E \_ 開始 \_ 時間 \_ \_ 結束**</dt></span><span class="sxs-lookup"><span data-stu-id="e24e0-124"><dt>**VFW\_E\_START\_TIME\_AFTER\_END**</dt></span></span> </dl> | <span data-ttu-id="e24e0-125">錯誤的時間戳記：結束時間早于開始時間。</span><span class="sxs-lookup"><span data-stu-id="e24e0-125">Bad time stamp: The end time is earlier than the start time.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="e24e0-126">備註</span><span class="sxs-lookup"><span data-stu-id="e24e0-126">Remarks</span></span>

<span data-ttu-id="e24e0-127">篩選準則會呼叫這個方法來判斷它應該如何處理範例。</span><span class="sxs-lookup"><span data-stu-id="e24e0-127">The filter calls this method to determine how it should handle a sample.</span></span> <span data-ttu-id="e24e0-128">如果傳回值為 S \_ OK，則篩選會立即呈現範例。</span><span class="sxs-lookup"><span data-stu-id="e24e0-128">If the return value is S\_OK, the filter renders the sample immediately.</span></span> <span data-ttu-id="e24e0-129">如果傳回值為 \_ FALSE，則篩選會根據時間戳記來排程轉譯的範例。</span><span class="sxs-lookup"><span data-stu-id="e24e0-129">If the return value is S\_FALSE, the filter schedules the sample for rendering, based on the time stamps.</span></span> <span data-ttu-id="e24e0-130">如果傳回值是錯誤碼，則篩選會拒絕範例。</span><span class="sxs-lookup"><span data-stu-id="e24e0-130">If the return value is an error code, the filter rejects the sample.</span></span>

<span data-ttu-id="e24e0-131">如果此範例沒有 \_ 時間戳記，或篩選沒有參考時鐘，則這個方法會傳回 [確定]。</span><span class="sxs-lookup"><span data-stu-id="e24e0-131">This method returns S\_OK if the sample has no time stamps, or if the filter does not have a reference clock.</span></span> <span data-ttu-id="e24e0-132">否則，它會傳回 [**CBaseRenderer：： ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) 方法的值。</span><span class="sxs-lookup"><span data-stu-id="e24e0-132">Otherwise, it returns the value of the [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) method.</span></span> <span data-ttu-id="e24e0-133">在基類中， **ShouldDrawSampleNow** 一律會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="e24e0-133">In the base class, **ShouldDrawSampleNow** always returns S\_FALSE.</span></span> <span data-ttu-id="e24e0-134">衍生的類別可以覆寫這個行為。</span><span class="sxs-lookup"><span data-stu-id="e24e0-134">The derived class can override this behavior.</span></span> <span data-ttu-id="e24e0-135">例如，如果衍生類別會執行品質控制管理，它可能會傳回 E \_ 無法卸載範例。</span><span class="sxs-lookup"><span data-stu-id="e24e0-135">For example, if the derived class implements quality control management, it might return E\_FAIL to drop a sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24e0-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="e24e0-136">Requirements</span></span>



| <span data-ttu-id="e24e0-137">需求</span><span class="sxs-lookup"><span data-stu-id="e24e0-137">Requirement</span></span> | <span data-ttu-id="e24e0-138">值</span><span class="sxs-lookup"><span data-stu-id="e24e0-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e24e0-139">標頭</span><span class="sxs-lookup"><span data-stu-id="e24e0-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e24e0-140"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e24e0-140"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e24e0-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="e24e0-141">Library</span></span><br/> | <dl> <span data-ttu-id="e24e0-142"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e24e0-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e24e0-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e24e0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24e0-144">**CBaseRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="e24e0-144">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




